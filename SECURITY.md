# Security policy

## Reporting a vulnerability
Report it privately through GitHub's private vulnerability reporting on the public releases repository:
**github.com/JeremiePineau/terminallyllm-releases → Security → Report a vulnerability.** Please don't open a public issue.

- **What to include:** the version (Settings › Updates & about, or the installer's name), the OS, what an attacker can do, and the steps to reproduce.
- **What happens next:** an acknowledgement within 5 business days and an assessment within 10. A fix ships as a new release, and the advisory is published on the releases repository once that release is out. Reporters are credited unless they ask not to be.
- **Disclosure:** coordinated. Please give us 90 days, or until a fix is released, whichever comes first, before disclosing publicly.

## Security contact
The maintainer, JeremiePineau on GitHub, through the reporting channel above. The project has one maintainer, the only person with access to the source, the build's secrets and the signing certificate (GitHub account with two-factor authentication).

## Supported versions
Only the latest release receives fixes. The app checks for updates at startup, and every fix ships as a new release on the same feed. A release stops being supported as soon as a newer one is published.

## Contributions
The source is private and public contributions are not accepted.

## More
The security review pack lives with the (private) source and is shared with IT reviewers on request.
