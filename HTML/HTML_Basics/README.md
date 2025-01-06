
# HTML Basics

## 1. Introduction to HTML
HTML (HyperText Markup Language) is the standard language used to create and design web pages. It defines the structure of a webpage and its content using markup tags.

### Key Components:
- **Tags**: Elements enclosed in angle brackets (e.g., `<html>`, `<body>`, `<p>`, etc.).
- **Attributes**: Additional information about elements (e.g., `class`, `id`, `href`, etc.).

## 2. Basic HTML Structure
An HTML document is structured with a set of basic elements:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document Title</title>
</head>
<body>
    <h1>Welcome to HTML</h1>
    <p>This is a basic HTML page.</p>
</body>
</html>
```

### Explanation:
- `<!DOCTYPE html>`: Declares the document type and version of HTML.
- `<html>`: Root element of the HTML document.
- `<head>`: Contains meta information (e.g., charset, title).
- `<body>`: Contains the content of the webpage that users see.

## 3. HTML Tags and Elements

### a) Headings
Headings define the structure and hierarchy of the content.

```html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Sub Sub Heading</h3>
```

### b) Paragraphs
Use `<p>` to define paragraphs.

```html
<p>This is a paragraph of text.</p>
```

### c) Links
Links are created using the `<a>` tag. Use the `href` attribute to specify the destination URL.

```html
<a href="https://www.example.com">Visit Example</a>
```

### d) Images
To embed images, use the `<img>` tag. The `src` attribute defines the image source.

```html
<img src="image.jpg" alt="Description of Image">
```

### e) Lists
There are two types of lists in HTML: ordered and unordered.

#### Unordered List
```html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>
```

#### Ordered List
```html
<ol>
    <li>First Item</li>
    <li>Second Item</li>
</ol>
```

## 4. HTML Forms

Forms are used to gather user input.

### a) Form Tag
The `<form>` tag is used to define an HTML form.

```html
<form action="/submit" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
    <input type="submit" value="Submit">
</form>
```

### b) Input Elements
- `<input type="text">`: Text input field.
- `<input type="password">`: Password input field.
- `<input type="radio">`: Radio button.
- `<input type="checkbox">`: Checkbox.

## 5. HTML Tables

Tables are used to display data in rows and columns.

```html
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Data 1</td>
        <td>Data 2</td>
    </tr>
</table>
```

### Explanation:
- `<table>`: Defines the table.
- `<tr>`: Table row.
- `<th>`: Table header.
- `<td>`: Table data (cell).

## 6. HTML Attributes

HTML elements can have attributes that provide additional information about the element.

### Common Attributes:
- `id`: Unique identifier for an element.
- `class`: Specifies a class for an element.
- `src`: Specifies the source (used in `<img>`, `<script>`, etc.).
- `href`: Defines the link target (used in `<a>`).
- `alt`: Alternative text for images.

Example:
```html
<img src="image.jpg" alt="Description">
<a href="https://example.com" target="_blank">Link</a>
```

## 7. Semantic HTML

Semantic HTML tags provide meaning and structure to the web content, making it accessible and SEO-friendly.

### Common Semantic Tags:
- `<header>`: Represents the header section of a page or section.
- `<footer>`: Represents the footer section.
- `<article>`: Defines independent content.
- `<section>`: Defines sections of content.
- `<nav>`: Defines navigation links.

Example:
```html
<header>
    <h1>Welcome to My Website</h1>
</header>
<article>
    <p>This is an article.</p>
</article>
<footer>
    <p>Contact us at info@example.com</p>
</footer>
```

## 8. HTML Forms & Input Validation

Forms often require validation before submission. Some basic input validation can be achieved using attributes like `required`, `pattern`, etc.

```html
<form>
    <input type="email" required>
    <input type="submit">
</form>
```

## 9. HTML Best Practices

- Always close your tags (e.g., `<p></p>`).
- Use semantic tags for better accessibility and SEO.
- Use lowercase for tags and attributes.

## 10. Interview Preparation Tips

- **Understand the structure of an HTML page**: Know the role of elements like `<html>`, `<head>`, and `<body>`.
- **Practice writing forms**: Familiarize yourself with input types and form handling.
- **Learn about HTML5 features**: Features like local storage, audio/video tags, and canvas are common in modern web development.
- **Responsive design**: Understand how HTML can be used with CSS to create responsive layouts.
- **Accessibility**: Learn about accessibility attributes like `aria-*` and proper use of semantic HTML.

---

