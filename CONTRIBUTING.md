# Contributing to Toastify

Thank you for your interest in contributing to Toastify. Contributions are welcome, including bug fixes, documentation improvements, accessibility updates, and new toast features.

## Before You Start

- Check the existing issues before opening a new one.
- For larger changes, open an issue first so the proposed approach can be discussed.
- Keep changes focused and consistent with the existing vanilla JavaScript, HTML, and CSS structure.

## Development Setup

1. Fork the repository and clone your fork.
2. Open the project folder in a browser or use a local static web server.
3. Use `index.html` to test the Toast Playground.
4. Make changes in `assets/js/`, `assets/css/`, or the relevant documentation file.

The project does not currently require a build step or package installation.

## Making Changes

- Preserve the public `showToast` API unless the change intentionally updates it.
- Keep the library lightweight and avoid adding dependencies without a clear need.
- Follow the existing formatting and naming style.
- Update `README.md` when adding or changing public options or behavior.
- Ensure new user-facing functionality works on desktop and mobile layouts.
- Do not commit generated files, credentials, or unrelated formatting changes.
- By submitting a contribution, you agree that it may be distributed under the project's [MIT License](LICENSE).

## Testing

Before opening a pull request:

- Test the Toast Playground in a modern browser.
- Check all supported toast types, themes, positions, transitions, and close behaviors affected by your change.
- Test both automatic and manual toast closing where relevant.
- Check the browser console for errors.
- Verify that the generated example code matches the selected options.

## Pull Requests

Please include:

- A clear title and description of the change.
- The reason for the change and any relevant issue number.
- A short description of how you tested it.
- Screenshots or a live demo link for visible UI changes.

Maintainers may request changes before a pull request is merged. By participating, you agree to follow the project's [Code of Conduct](CODE_OF_CONDUCT.md).

## Releases

Releases follow [Semantic Versioning](https://semver.org/):

- Increase the patch version for backward-compatible fixes.
- Increase the minor version for backward-compatible features.
- Increase the major version for breaking API changes.

Release tags use the `vMAJOR.MINOR.PATCH` format, such as `v1.0.0`. Release notes should summarize user-facing changes and known limitations.
