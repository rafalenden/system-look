# System Design

A lightweight CSS library that provides beautiful defaults for native HTML elements without requiring any classes. Just include the CSS file and your semantic HTML will look great out of the box.

![Screenshot](./demo/screenshot.png)

[View the live demo](https://rafalenden.github.io/system-design/demo/)

## Installation

### npm

```bash
npm install system-design
```

With a bundler (Vite, webpack, Parcel, esbuild…), import it once from your entry file:

```js
import 'system-design';
```

or from your own stylesheet:

```css
@import 'system-design';
```

Without a bundler, link the file directly:

```html
<link rel="stylesheet" href="node_modules/system-design/system.css">
```

### CDN

```html
<link rel="stylesheet" href="https://unpkg.com/system-design/system.css">
```

Pin a version (`system-design@1/system.css`) in production so a new release can't change your page.

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

System Design automatically adapts to your system's dark/light mode preference using `prefers-color-scheme`. No configuration needed!

## Customization

Everything is driven by custom properties declared on `:root`. Override the ones you need after loading the stylesheet:

```css
:root {
  --system-font-size-base: 0.875rem;
  --system-spacing-md: 0.75rem;
  --system-control-height: 1.75rem;
}
```

| Property | Default | Used for |
| --- | --- | --- |
| `--system-ui` | `system-ui`, then common platform fonts | Body font |
| `--system-ui-mono` | `'SF Mono'`, then common monospace fonts | `kbd`, `samp`, `var` |
| `--system-spacing-xs` … `--system-spacing-3xl` | `0.25rem` … `3rem` | Margins and padding |
| `--system-font-size-xs` … `--system-font-size-4xl` | `0.75rem` … `2.5rem` | Text and heading sizes |
| `--system-control-height` | `2.1875rem` | Minimum height of buttons, inputs, selects and textareas |
| `--system-border-color` | `CanvasText` at 10% opacity | `kbd`, `hr` and `tfoot` borders |

Sizes are in `rem`, so changing the root font size scales the whole stylesheet. That is handy for compact interfaces such as browser extension popups:

```css
:root {
  font-size: 13px;
}
```

### Overriding rules

Rules only use element selectors (attribute and state checks are wrapped in `:where()`), so a single class in your own stylesheet always wins:

```css
.toolbar-button {
  min-height: 0;
  padding: 0;
}
```

If you would rather not think about source order at all, load the library into a [cascade layer](https://developer.mozilla.org/docs/Web/CSS/@layer); unlayered styles then take precedence over it:

```css
@import 'system-design' layer(system);
```

## Demo

The demo is a single static page with no dependencies. Open `demo/index.html` in a browser, or view it [online](https://rafalenden.github.io/system-design/demo/).

## License

[MIT](./LICENSE) - feel free to use in personal and commercial projects.
