# Security Policy

## Supported Version

Security fixes are currently focused on the latest published release and the current `main` branch.

| Version | Supported |
| --- | --- |
| 1.1.x | Yes |
| Earlier versions | Best effort |

## Intended Use and Clinical Safety

ShiftMate ER is an open-source workflow and educational project for Emergency Department shift management and handover.

It is **not a certified medical device**, electronic health record, hospital information system, or replacement for clinical judgement, local policy, approved handover procedures, or institutional systems.

Do not rely on ShiftMate ER as the sole source of clinically important information or as the only record of patient care.

## Data Storage and Privacy

The current application stores its records locally using browser/WebView `localStorage`.

Important limitations of the current implementation:

- Application records are stored locally on the device/browser profile.
- The current storage layer does **not provide application-level encryption at rest**.
- The current local sign-in/session mechanism is **not identity-grade authentication or access control**.
- Data may remain on the device until it is explicitly removed or the relevant application/browser storage is cleared.
- Anyone with sufficient access to the same device, operating-system account, browser profile, application data, backups, or developer tools may potentially access locally stored data.

Because of these limitations, the current public build should **not be used to store real identifiable patient information, protected health information, credentials, secrets, or other sensitive production clinical data**.

If ShiftMate ER is evaluated for real clinical use, the deployment must first undergo appropriate technical, privacy, security, governance, and regulatory review. Appropriate controls may include strong authentication, authorization, encryption, secure storage, auditability, retention controls, backup protection, device security, and compliance with applicable institutional and legal requirements.

## Reporting a Vulnerability

Please report suspected security vulnerabilities responsibly.

If GitHub's private vulnerability reporting is available for this repository, use **Security → Report a vulnerability**.

If private reporting is not available, open a minimal GitHub issue requesting a private security contact channel. Do **not** include exploit details, credentials, personal information, patient information, or other sensitive data in a public issue.

When reporting a vulnerability, include only the information necessary to reproduce and assess the issue, such as:

- Affected version or commit
- Web or desktop build
- Operating system and browser/WebView where relevant
- Reproduction steps
- Expected and observed behavior
- Security impact
- Suggested mitigation, if known

Never use real patient data or other sensitive information when demonstrating a vulnerability.

## Scope

Security reports may include issues involving:

- Local data exposure
- Session or access-control behavior
- Tauri desktop integration
- Dependency vulnerabilities
- Cross-site scripting or unsafe rendering
- Data import/export behavior
- Build and release integrity
- Other vulnerabilities that could compromise confidentiality, integrity, or availability

General feature requests, clinical-content questions, and non-sensitive bugs should use the normal GitHub Issues workflow.

## Disclosure

Please allow reasonable time for investigation and remediation before publicly disclosing a confirmed vulnerability.

No fixed response or remediation SLA is currently guaranteed.
