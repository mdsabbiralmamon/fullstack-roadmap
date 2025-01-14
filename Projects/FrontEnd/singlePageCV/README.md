# Single-Page HTML CV

This project is designed to teach you how to create a clean and structured single-page CV using only HTML. The focus is on creating a semantically correct and SEO-optimized CV that is ready for styling in future projects.

---

## **Project Overview**

### Project URL : https://roadmap.sh/projects/single-page-cv

Your task is to create a single-page CV that includes:
- **Education Section**: Display your academic background.
- **Skills Section**: Highlight your key skills.
- **Career History Section**: Summarize your work experience.

Additionally, you will:
- Use semantic HTML to ensure accessibility and clarity.
- Include meta tags for SEO optimization and Open Graph (OG) sharing.
- Add a favicon for better presentation.

---

## **Project Goals**

1. Build a semantically correct single-page CV using only HTML.
2. Understand and apply basic SEO principles with meta tags.
3. Prepare the HTML structure for future CSS styling.

---

## **Key Requirements**

### **1. Semantic HTML**
- Use appropriate HTML tags for each section (e.g., `<header>`, `<section>`, `<footer>`).
- Ensure your structure is logical and easy to read.

### **2. SEO Meta Tags**
Add these tags inside the `<head>` section:
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="A professional CV showcasing education, skills, and career history.">
<meta name="author" content="Your Name">
<meta name="keywords" content="CV, Resume, HTML, Web Development, Career">
<title>My CV</title>
```

### **3. Open Graph Tags**
Enhance social media sharing with OG tags:
```html
<meta property="og:title" content="My CV">
<meta property="og:description" content="A professional CV showcasing education, skills, and career history.">
<meta property="og:image" content="link-to-thumbnail-image.jpg">
<meta property="og:url" content="your-website-url">
<meta property="og:type" content="website">
```

### **4. Favicon**
Include a favicon for your webpage:
```html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

### **5. Page Structure**
Here’s the basic structure of your CV:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Meta Tags -->
</head>
<body>
    <header>
        <h1>Your Name</h1>
    </header>

    <main>
        <section id="education">
            <h2>Education</h2>
            <ul>
                <li><strong>Degree Name</strong> - University Name (Year)</li>
            </ul>
        </section>

        <section id="skills">
            <h2>Skills</h2>
            <ul>
                <li>Skill 1</li>
                <li>Skill 2</li>
            </ul>
        </section>

        <section id="career-history">
            <h2>Career History</h2>
            <ul>
                <li><strong>Job Title</strong> - Company Name (Year-Year)</li>
            </ul>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Your Name</p>
    </footer>
</body>
</html>
```

---

## **How to Complete This Project**

1. **Set Up the HTML File**: Create a new file named `index.html`.
2. **Add Meta Tags**: Include all required meta tags in the `<head>` section.
3. **Create the Header**: Add your name, job title, and contact information.
4. **Build the Sections**:
   - Education: List your academic qualifications.
   - Skills: Highlight your relevant skills.
   - Career History: Summarize your work experience.
5. **Include a Favicon**: Add a small image for the browser tab.
6. **Test Your HTML**: Open the file in a browser and ensure everything displays correctly.
7. **Validate Your Code**: Use an HTML validator to check for errors.

---

## **Submission Checklist**
- [ ] Semantically correct HTML structure.
- [ ] Single-page layout with clearly defined sections.
- [ ] SEO meta tags in the `<head>` section.
- [ ] OG tags for social media sharing.
- [ ] A favicon linked in the `<head>` section.

---

## **Next Steps**
Once the HTML structure is complete, you can enhance the CV's appearance using CSS in future projects.

---

## **Resources**
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [HTML Validator](https://validator.w3.org/)
- [Favicon Generator](https://favicon.io/)

---

Happy Coding! 🚀