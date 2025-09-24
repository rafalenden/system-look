# System Styles

A lightweight CSS library that provides beautiful defaults for native HTML elements without requiring any classes. Just include the CSS file and your semantic HTML will look great out of the box.

## Installation

### CDN

```html
<link rel="stylesheet" href="https://unpkg.com/system-styles@latest/system.css">
```

### NPM

```bash
npm install system-styles
```

Then include in your HTML:

```html
<link rel="stylesheet" href="node_modules/system-styles/system.css">
```

### Download

Download `system.css` and include it in your project:

```html
<link rel="stylesheet" href="path/to/system.css">
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

## Dark Mode

System Styles automatically adapts to your system's dark/light mode preference using `prefers-color-scheme`. No configuration needed!

## Customization

You can customize System Styles by overriding CSS custom properties:

```css
:root {
  --font-size-base: 1rem;
  --spacing-md: 1rem;
  --system-ui: system-ui, sans-serif;
  /* ... and many more */
}
```

## License

MIT License - feel free to use in personal and commercial projects.
