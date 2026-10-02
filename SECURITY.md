# Security Policy

## Supported Versions

Toastify is currently maintained on the default branch. Security fixes are applied to the latest version available in this repository.

| Version | Supported |
| ------- | --------- |
| Latest  | Yes       |
| Older releases | No    |

## Reporting a Vulnerability

Please do not disclose security vulnerabilities in a public issue.

Report a suspected vulnerability privately through GitHub's private vulnerability reporting feature, if it is enabled for this repository. Otherwise, contact the repository maintainer privately through their GitHub profile. Do not include sensitive details in a public issue. Include:

- A clear description of the issue.
- The affected file, feature, or version.
- Steps to reproduce the issue or a minimal proof of concept.
- The potential impact.
- Any suggested mitigation, if available.

You will receive an acknowledgement when the report has been reviewed. Please allow reasonable time for investigation and a fix before making the issue public.

## Security Considerations

Toastify supports custom message and icon HTML. Applications using untrusted content should sanitize or validate that content before passing it to the library. Do not place secrets, tokens, or private information in toast messages or generated code.

The project uses external CDN resources in the playground. Review and pin external dependencies appropriately before using Toastify in a production environment with strict supply-chain requirements. See the [MIT License](LICENSE) for the terms under which the project is distributed.
