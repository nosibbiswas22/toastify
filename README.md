# toastify

A lightweight and customizable JavaScript library for creating toast notifications. This repository also includes an interactive "Toast Playground" to visually build, configure, and generate code for your toast notifications.

## Live Demo

Experience the Toast Playground live and generate your own custom toast notifications with ease.

**[Toastify Playground](https://nosibbiswas22.github.io/toastify/)**

## Features

- **Multiple Toast Types**: Pre-styled `success`, `error`, `info`, `warn`, and `promise` notifications.
- **Customizable Themes**: Choose between `light`, `dark`, and `colored` themes.
- **Flexible Positioning**: Place toasts at any corner or center of the screen (`top-right`, `top-left`, `top-center`, `bottom-right`, `bottom-left`, `bottom-center`).
- **Engaging Animations**: Animate toasts with `zoom`, `flip`, `slide`, or `bounce` transitions.
- **Auto-Close Control**: Set a custom duration for toasts to automatically disappear, or disable it entirely.
- **Interactive Options**: Pause auto-close on hover, close toast on click, and toggle the close button.
- **Progress Bar**: A visual indicator for the auto-close timer which can be hidden.
- **Fully Customizable**: Define custom messages, icons (using HTML), colors, and fonts.
- **Zero Dependencies**: A single JavaScript file that dynamically injects the required CSS.

## Getting Started

1.  Download the `toastify.js` file from the `assets/js/` directory.
2.  Include the script in your HTML file. The necessary CSS is automatically injected into the `<head>` of your document.

```html
<script src="path/to/toastify.js"></script>
```

## Usage

To display a toast, call the `showToast()` function with a configuration object. You can also use helper methods for specific toast types.

### Basic Example

```javascript
// A simple success toast that auto-closes after 3 seconds
showToast.success({
    message: "Your profile has been updated!",
    autoClose: 3000
});
```

### Advanced Example

```javascript
// A custom dark-themed error toast with a bounce animation
showToast.error({
    theme: "dark",
    message: "Failed to upload file. Please try again.",
    position: "bottom-center",
    autoClose: 5000,
    transition: "bounce",
    closeAble: true,
    pauseOnHover: true
});
```

### Promise Example

```javascript
// A toast that shows a loading state
showToast.promise({
    message: "Saving your changes...",
    autoClose: 'none' // Stays until manually closed or updated
});
```

## Configuration Options

The `showToast()` function accepts the following options:

| Option          | Type     | Default                                | Description                                                                                                                                |
| --------------- | -------- | -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| `type`          | `string` | `'none'`                               | The type of toast. Can be `success`, `error`, `info`, `warn`, or `promise`.                                                                |
| `message`       | `string` | Varies by type                         | The text message to display in the toast.                                                                                                  |
| `theme`         | `string` | `'light'`                              | The color theme of the toast. Can be `light`, `dark`, or `colored`.                                                                        |
| `position`      | `string` | `'top-right'`                          | The position of the toast on the screen. e.g., `top-left`, `bottom-center`.                                                                |
| `autoClose`     | `number` | `5000`                                 | Time in milliseconds before the toast automatically closes. Set to `'none'` to disable.                                                    |
| `transition`    | `string` | `'zoom'`                               | The entry/exit animation. Can be `zoom`, `flip`, `slide`, or `bounce`.                                                                     |
| `hideProgressBar`| `boolean`| `false`                                | If `true`, the progress bar indicating the remaining time is hidden.                                                                       |
| `pauseOnHover`  | `boolean`| `true`                                 | If `true`, the auto-close timer pauses when the mouse is over the toast.                                                                   |
| `closeAble`     | `boolean`| `true`                                 | If `true`, a close button (X) is displayed.                                                                                                |
| `closeOnClick`  | `boolean`| `false`                                | If `true`, the toast closes when clicked anywhere on it.                                                                                   |
| `icon`          | `string` | Varies by type                         | Custom icon HTML (e.g., `<i class="fa fa-rocket"></i>`).                                                                                   |
| `color`         | `string` | Varies by type                         | Custom color for the icon, progress bar, or background (in `colored` theme). Accepts any valid CSS color.                                |
| `font`          | `string` | `''`                                   | Custom font family for the toast message (e.g., `"Roboto", sans-serif`).                                                                   |
| `progressPercent` | `number` | `100`                                | The starting percentage of the progress bar. The bar will animate from this value down to 0. A value of 50 would start the bar halfway. |

## Toast Playground

The `index.html` in this repository serves as a powerful playground for `toastify`. It provides a user-friendly interface to:

-   Visually configure all available options.
-   See a live preview of your toast notification.
-   Automatically generate the required JavaScript code.
-   Copy the generated code with a single click to use in your own projects.
