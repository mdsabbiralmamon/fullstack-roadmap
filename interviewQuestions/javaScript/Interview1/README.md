## Question 1 : What will be the outputs of the given code:

```javascript
function abc() {
    console.log(abc.xyz);
}

abc()
abc.xyz = 400;
abc.xyz = 200;
abc()
```

Let's break down the code step by step to understand what happens:

```javascript
function abc() {
    console.log(abc.xyz);
}

abc() // First call to abc()
abc.xyz = 400; // Assign 400 to abc.xyz
abc.xyz = 200; // Assign 200 to abc.xyz
abc() // Second call to abc()
```

### Step 1: `abc()` is called for the first time
- When you call `abc()`, the function tries to log `abc.xyz` to the console.
- At this point, `abc.xyz` is **undefined** because the property `xyz` has not been set yet. In JavaScript, properties can be added to functions (which are objects), but initially, `xyz` does not exist.
- The output is: `undefined`.

### Step 2: `abc.xyz = 400`
- Here, you assign the value `400` to the property `xyz` of the `abc` function.
- Now, `abc.xyz` holds the value `400`.

### Step 3: `abc.xyz = 200`
- Next, you change the value of `abc.xyz` to `200`. This overwrites the previous value of `400`.
- Now, `abc.xyz` holds the value `200`.

### Step 4: `abc()` is called again
- When you call `abc()` again, it tries to log `abc.xyz` to the console.
- This time, `abc.xyz` is **200** because you previously assigned `200` to it.
- The output is: `200`.

### Final Explanation:
- The function `abc()` is called twice.
- On the first call, `abc.xyz` is undefined, so `undefined` is logged to the console.
- On the second call, `abc.xyz` is `200`, so `200` is logged to the console.


## Question 2: What is event propagation?

### What is Event Propagation in JavaScript?

Event propagation is a mechanism in JavaScript that defines the way events flow through the Document Object Model (DOM). When an event is triggered on an element (e.g., a `click` on a button), it doesn't just affect that element—it propagates through the DOM tree in a specific way.

Understanding event propagation is essential for effectively handling events in JavaScript and controlling how they behave. Event propagation occurs in three phases:

---

### **1. Capturing Phase (Event Capture)**
- The event starts at the root of the DOM (`document`) and travels down through its ancestors toward the target element.
- During this phase, listeners registered for the **capturing phase** can intercept the event before it reaches the target.

---

### **2. Target Phase**
- The event reaches the actual target element where it was triggered.
- At this point, listeners attached directly to the target are executed.

---

### **3. Bubbling Phase (Event Bubble)**
- After reaching the target, the event travels back up through the DOM tree toward the root (`document`).
- Listeners registered for the **bubbling phase** handle the event as it moves upward.

---

### Visual Representation of Event Propagation

```plaintext
Capturing Phase: Document -> HTML -> Body -> Div -> Button
Target Phase: Button
Bubbling Phase: Button -> Div -> Body -> HTML -> Document
```

---

### Example of Event Propagation

Here’s an example to demonstrate event propagation:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Event Propagation</title>
</head>
<body>
    <div id="parent">
        <button id="child">Click Me</button>
    </div>

    <script>
        const parent = document.getElementById('parent');
        const child = document.getElementById('child');

        // Listener on the parent element (bubbling phase by default)
        parent.addEventListener('click', () => {
            console.log('Parent element clicked (bubbling phase)');
        });

        // Listener on the child element
        child.addEventListener('click', () => {
            console.log('Child element clicked');
        });

        // Listener on the parent element during the capturing phase
        parent.addEventListener(
            'click',
            () => {
                console.log('Parent element clicked (capturing phase)');
            },
            true // true indicates the capturing phase
        );
    </script>
</body>
</html>
```

#### Output When the Button is Clicked:
1. **Parent element clicked (capturing phase)** → From the capturing phase.
2. **Child element clicked** → From the target phase.
3. **Parent element clicked (bubbling phase)** → From the bubbling phase.

---

### Controlling Event Propagation

JavaScript provides methods to control how events propagate through the DOM:

1. **`stopPropagation()`**
   - Prevents the event from continuing to propagate through the DOM (stops both capturing and bubbling phases).
   - Example:
     ```javascript
     child.addEventListener('click', (event) => {
         event.stopPropagation(); // Stops propagation
         console.log('Event propagation stopped');
     });
     ```

2. **`stopImmediatePropagation()`**
   - Prevents propagation and also stops other listeners of the same event on the same element from executing.
   - Example:
     ```javascript
     child.addEventListener('click', (event) => {
         event.stopImmediatePropagation();
         console.log('This will be the only listener executed for this event');
     });

     child.addEventListener('click', () => {
         console.log('This will not run due to stopImmediatePropagation');
     });
     ```

3. **`preventDefault()`**
   - Prevents the browser’s default behavior for an event (e.g., preventing form submission or a link from navigating).
   - Example:
     ```javascript
     child.addEventListener('click', (event) => {
         event.preventDefault();
         console.log('Default action prevented');
     });
     ```

---

### Bubbling vs. Capturing in Practice

- **Bubbling Phase** is the default in most cases. When you attach an event listener using `addEventListener` without the third parameter (or with `false`), it runs during the bubbling phase.
- **Capturing Phase** is used less frequently but can be enabled by passing `true` as the third parameter in `addEventListener`.

---

### Use Cases of Event Propagation

1. **Event Delegation**
   - Use the bubbling phase to attach a single event listener to a parent element and handle child element events dynamically.
   - Example:
     ```javascript
     document.getElementById('parent').addEventListener('click', (event) => {
         if (event.target.tagName === 'BUTTON') {
             console.log('Button clicked:', event.target);
         }
     });
     ```

2. **Preventing Unwanted Propagation**
   - Use `stopPropagation()` to prevent parent elements from reacting to an event meant for a specific child element.

3. **Capturing Phase for Early Handling**
   - Use the capturing phase to intercept and handle events early before they reach the target element.

---

### Summary

Event propagation defines the journey of an event through the DOM, consisting of three phases: **capturing**, **target**, and **bubbling**. By understanding these phases and how to control them using JavaScript, you can handle events more effectively in your web applications. Whether you're delegating events, intercepting them, or preventing unwanted behavior, mastering event propagation is a fundamental skill for any JavaScript developer.