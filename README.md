# Toastify

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://nosibbiswas22.github.io/toastify/)
[![GitHub stars](https://img.shields.io/github/stars/nosibbiswas22/toastify?style=flat)](https://github.com/nosibbiswas22/toastify/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/nosibbiswas22/toastify)](https://github.com/nosibbiswas22/toastify/issues)
[![Last commit](https://img.shields.io/github/last-commit/nosibbiswas22/toastify)](https://github.com/nosibbiswas22/toastify/commits/main)
[![License](https://img.shields.io/github/license/nosibbiswas22/toastify)](LICENSE)

Toastify is a lightweight, dependency-free JavaScript library for creating customizable toast notifications. It includes an interactive playground for configuring notifications and generating ready-to-use code.

## Demo

Try the [Toastify Playground](https://nosibbiswas22.github.io/toastify/) to preview toast notifications and experiment with the available options.

## Features

- Success, error, info, warning, and promise toast types.
- Light, dark, and colored themes.
- Top, bottom, and centered positions.
- Zoom, flip, slide, and bounce transitions.
- Configurable auto-close duration or persistent notifications.
- Pause on hover, close on click, and optional close button.
- Optional progress bar with configurable starting percentage.
- Custom messages, icons, colors, and fonts.
- No package installation or build process required.

## Quick Start

Copy `assets/js/toastify.js` into your project and load it before your application script:

```html
<script src="path/to/toastify.js"></script>
<script src="path/to/app.js"></script>
```

The library injects its toast styles into the document automatically.

## Usage

Use the main `showToast()` function or one of its type-specific helpers:

```javascript
showToast.success({
    message: "Your profile has been updated!",
    autoClose: 3000
});
```

```javascript
showToast.error({
    theme: "dark",
    message: "Failed to upload the file. Please try again.",
    position: "bottom-center",
    transition: "bounce",
    closeAble: true,
    pauseOnHover: true
});
```

For a persistent loading notification:

```javascript
showToast.promise({
    message: "Saving your changes...",
    autoClose: "none"
});
```

## Configuration

| Option | Type | Default | Description |
| --- | --- | --- | --- |
| `type` | `string` | `none` | `success`, `error`, `info`, `warn`, `promise`, or `none`. |
| `message` | `string` | Type-specific | Text displayed in the notification. |
| `theme` | `string` | `light` | `light`, `dark`, or `colored`. |
| `position` | `string` | `top-right` | `top-left`, `top-center`, `top-right`, `bottom-left`, `bottom-center`, or `bottom-right`. |
| `autoClose` | `number \| string` | `5000` | Duration in milliseconds. Use `none` to keep the toast open. |
| `transition` | `string` | `zoom` | `zoom`, `flip`, `slide`, or `bounce`. |
| `hideProgressBar` | `boolean` | `false` | Hides the progress bar when enabled. |
| `pauseOnHover` | `boolean` | `true` | Pauses the auto-close timer while the pointer is over the toast. |
| `closeAble` | `boolean` | `true` | Shows the close button when enabled. |
| `closeOnClick` | `boolean` | `false` | Closes the toast when its content is clicked. |
| `icon` | `string` | Type-specific | Custom icon HTML. Sanitize untrusted content before use. |
| `color` | `string` | Type-specific | Custom CSS color for the icon, progress bar, or colored theme. |
| `font` | `string` | Empty | Custom font family for the message. |
| `progressPercent` | `number` | `100` | Starting percentage for the progress bar. |

## Playground

The repository's `index.html` provides a visual configuration tool that lets you:

- Preview toast notifications live.
- Configure every supported option.
- Generate the corresponding JavaScript code.
- Copy the generated code for use in another project.

## Development

This is a static HTML, CSS, and JavaScript project. Open `index.html` directly in a browser or serve the repository with any local static web server. No build step is required.

Before submitting a change, test the affected toast types, positions, transitions, close behaviors, and responsive layout in a modern browser.

## Releases

Releases use [Semantic Versioning](https://semver.org/) and Git tags with a `v` prefix. The current stable release is [v1.0.0](https://github.com/nosibbiswas22/toastify/releases/tag/v1.0.0).

## Contributing

Bug reports, documentation improvements, and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for development and submission guidelines.

Please review the [Code of Conduct](CODE_OF_CONDUCT.md) before participating. For security concerns, see [SECURITY.md](SECURITY.md).

## License

Toastify is available under the [MIT License](LICENSE).
