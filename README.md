# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

![Croquis](images/croquis.png)
![FM Feedback 1](images/Eval1.png)
![FM Feedback 2](#)

### Links

- Solution URL: [GitHub Repository](https://github.com/ezra1492/frontend-mentor-qr-code)
- Live Site URL: [GitHub Pages Deployment](https://ezra1492.github.io/frontend-mentor-qr-code/)

## My process

### Built with

- Semantic HTML5 markup
- CSS3 Custom Properties (Design Token Vault)
- Flexbox Architecture
- Mobile-first workflow
- Strict Atomic Scale & Primitive Tokenization

### What I learned

During this project, I focused heavily on transitioning from raw values to a strictly structured Design System and understanding the geometric physics of rendering engines.

Key architectural takeaways include:

1. **Orthogonal Axis Rotation:** Deepened my understanding of how changing `flex-direction` to `column` completely rotates the main and cross axes 90 degrees.

```css
/* FLEXBOX CENTERING + INHERITABLE FONT */
body {
  display: flex; /* Activate Flexbox context*/
  flex-direction: column; /* Main axis is now vertical, cross axis is horizontal*/
  align-items: center; /* CROSS AXIS (Horizontal): Takes the viewport width and centers the content horizontally */
  justify-content: center; /* MAIN AXIS (Vertical): Distributes the remaining vertical space between the article and footer */
  min-height: 100vh; /* Force body to take at least 100% of the viewport height */
  font-family: var(--ff-site);
  background-color: var(--clr-slate300);
}
```

2. **Inline Baseline Descender Bug:** Learned how switching the display of image elements to `block` completely eliminates unwanted whitespace wrapping.

```css
/* QR CODE IMAGE */
.qr-code__img {
  display: block; /* Eliminates the default inline baseline whitespace. The image perfectly respects the article's padding */
  width: 100%; /* Spans the full available width, preventing container overflow */
  height: auto; /* Maintains the original aspect ratio to prevent image distortion */
  border-radius: var(--br-s);
}
```

3. **Refactoring Hardcoded Values:** Successfully replaced arbitrary values with an atomic, strict primitive layout scale (`var(--sp-300)`).

```css
/* QR CODE CARD */
.qr-code {
  width: var(--width-qr-card);
  padding: var(
    --padding-qr-card
  ); /* Inner spacing: 16px top/left/right, and 40px bottom */
  border-radius: var(--br-l);
  box-shadow: var(
    --bs-qr-card
  ); /* Horizontal axis 0px, vertical 24px, blur 24px, spread 0px, and rgba black with 4.77% opacity */
  background-color: var(--clr-white);
}
```

### Continued development

- **Systematic Architecture:** I plan to continue enforcing strict Design Token structures from the very beginning of my upcoming layouts.
- **Git Mastery:** Transitioning towards more modular and atomic commit habits using professional standards.

### Useful resources (AI Collaboration)

- **Website:** [Gitmoji](https://gitmoji.dev/) - It made it significantly easier to understand and adopt the practice of **Atomic Commits** through visual semantic tracking.
- **Tool:** Gemini (NotebookLM style workflows)
- **Use Case:** Validating clean architecture, translating inline technical explanations into idiomatic English, and structuring a professional development workspace.
- **Outcome:** Significantly reduced friction between local Git staging and GitHub deployment, while accelerating the integration of advanced concepts like Design Tokens.

## Author

- Frontend Mentor - [@ezra1492](https://github.com/ezra1492)
- X / Twitter - [@RayG1492](https://x.com/RayG1492)
- Discord - `rayg._86220`
