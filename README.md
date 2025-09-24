# System CSS

A lightweight CSS library that provides beautiful defaults for native HTML elements without requiring any classes. Just include the CSS file and your semantic HTML will look great out of the box.

## Features

- **Classless**: Works with pure semantic HTML - no classes needed
- **Responsive**: Designed to work on all screen sizes
- **Dark mode**: Automatic dark/light theme switching based on system preference
- **Modern**: Uses CSS custom properties and modern CSS features
- **Lightweight**: Small footprint with no dependencies
- **Accessible**: Built with accessibility best practices

## Installation

### CDN

```html
<link rel="stylesheet" href="https://unpkg.com/system-css@latest/native.css">
```

### NPM

```bash
npm install system-css
```

Then include in your HTML:

```html
<link rel="stylesheet" href="node_modules/system-css/native.css">
```

### Download

Download `native.css` and include it in your project:

```html
<link rel="stylesheet" href="path/to/native.css">
```

## Usage

Just write semantic HTML and it will be styled automatically:

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" href="system.css">
</head>
<body>
<h1>My Website</h1>
<p>This paragraph will be automatically styled.</p>

<form>
    <label for="email">Email:</label>
    <input type="email" id="email" placeholder="Enter your email">

    <label for="message">Message:</label>
    <textarea id="message" placeholder="Your message"></textarea>

    <button type="submit">Send</button>
</form>

<table>
    <thead>
    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>John</td>
        <td>25</td>
    </tr>
    </tbody>
</table>
</body>
</html>
```

## Styled Elements

Native CSS provides beautiful defaults for:

### Typography
- Headings (`h1` - `h6`)
- Paragraphs (`p`)
- Links (`a`)
- Text formatting (`strong`, `em`, `mark`, `small`)
- Code (`code`, `pre`, `kbd`)
- Quotes (`blockquote`)

### Forms
- Text inputs (`input[type="text"]`, `input[type="email"]`, etc.)
- Textareas (`textarea`)
- Buttons (`button`)
- Select dropdowns (`select`)
- Checkboxes and radio buttons
- Form structure (`fieldset`, `legend`, `label`)

### Structure
- Lists (`ul`, `ol`, `dl`)
- Tables (`table`, `th`, `td`)
- Horizontal rules (`hr`)
- Images (`img`)
- Figures (`figure`, `figcaption`)

### Utility Classes

While Native CSS works without classes, a few optional utility classes are provided:

- `.text-center`, `.text-left`, `.text-right` - Text alignment
- `.mt-0` to `.mt-4`, `.mb-0` to `.mb-4` - Margin utilities
- `.sr-only` - Screen reader only content

## Dark Mode

System CSS automatically adapts to your system's dark/light mode preference using `prefers-color-scheme`. No configuration needed!

## Browser Support

System CSS works in all modern browsers that support:
- CSS Custom Properties (CSS Variables)
- `prefers-color-scheme` media query

This includes:
- Chrome 49+
- Firefox 31+
- Safari 9.1+
- Edge 16+

## Customization

You can customize System CSS by overriding the CSS custom properties:

```css
:root {
  --text-color: #333;
  --bg-color: #fff;
  --link-color: #007bff;
  --border-color: #ddd;
  /* ... and many more */
}
```

## License

MIT License - feel free to use in personal and commercial projects.