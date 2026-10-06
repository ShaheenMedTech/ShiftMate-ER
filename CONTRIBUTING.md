# Contributing to ShiftMate ER

Thank you for your interest in contributing to ShiftMate ER.

ShiftMate ER is an open-source Emergency Department shift-management and handover project. Contributions are welcome when they improve reliability, usability, accessibility, localization, maintainability, or workflow quality.

## Before You Start

Please review:

- [README.md](README.md) for the project overview
- [SECURITY.md](SECURITY.md) for security, privacy, and responsible-disclosure guidance
- Existing [GitHub Issues](https://github.com/ShaheenMedTech/ShiftMate-ER/issues) before opening a duplicate report or request

Use the provided issue templates for bug reports and feature requests.

## Privacy and Clinical Safety

**Never include real patient information in this repository.**

Do not submit:

- Patient names or identifiers
- Medical record or case numbers from real systems
- Protected health information
- Screenshots containing real clinical data
- Credentials, API keys, tokens, or secrets
- Confidential institutional information

Use synthetic examples and test data only.

The current application is not a certified medical device, electronic health record, or hospital information system. Contributions must not present the application as a replacement for clinical judgement, approved handover processes, institutional systems, or local policy.

For security vulnerabilities or sensitive privacy concerns, follow [SECURITY.md](SECURITY.md) rather than opening a public issue with exploit details.

## Development Setup

### Requirements

For web development:

- Git
- A current Node.js LTS release
- npm

For Tauri desktop development, you will also need:

- Rust stable
- Tauri's platform-specific system dependencies

Refer to the official Tauri documentation for operating-system-specific prerequisites.

### Clone and Install

```sh
git clone https://github.com/ShaheenMedTech/ShiftMate-ER.git
cd ShiftMate-ER
npm ci
```

### Run the Web Application

```sh
npm run dev
```

### Build the Web Application

```sh
npm run build
```

### Preview the Production Web Build

```sh
npm run preview
```

### Run the Tauri Desktop Application

After installing the required Rust and platform dependencies:

```sh
npm run tauri -- dev
```

### Build the Tauri Desktop Application

```sh
npm run tauri -- build
```

## Branches and Changes

Create a focused branch from the latest `main` branch:

```sh
git switch main
git pull --ff-only
git switch -c <short-descriptive-branch-name>
```

Keep each contribution focused on one logical change.

Examples:

```text
fix/handover-filter
feature/export-settings
docs/privacy-guidance
```

Avoid unrelated formatting, refactoring, or dependency changes in the same pull request unless they are required for the proposed change.

## Validation

There is not yet a dedicated automated application test suite.

Before opening a pull request, at minimum:

1. Run `npm ci`.
2. Run `npm run build` and confirm it completes successfully.
3. Manually verify the affected workflow using synthetic data.
4. Check both light and dark themes when the UI is affected.
5. Check Arabic/English and RTL/LTR behavior when text or layout is affected.
6. Confirm that no sensitive data, credentials, or local-only artifacts were added.

For desktop-specific changes, also test the relevant Tauri build or development workflow when practical.

GitHub Pages deployment runs automatically from `main`, and tagged releases trigger the desktop release workflow.

## Pull Requests

A good pull request should include:

- A concise title
- What changed
- Why the change is useful
- How it was tested
- Screenshots for meaningful UI changes, using synthetic data only
- Any privacy, security, clinical-safety, migration, or compatibility implications

Keep pull requests small enough to review effectively.

If the change addresses an existing issue, reference it in the pull request description.

## Clinical and Workflow Content

When changing wording or behavior that may influence clinical workflow:

- Keep claims conservative and explicit
- Avoid implying clinical validation that has not occurred
- Avoid introducing diagnostic or treatment recommendations without appropriate review
- Prefer established, authoritative references when factual clinical guidance is added
- Clearly distinguish workflow assistance from clinical decision-making

## Dependencies

Avoid adding dependencies unless they provide clear value.

When proposing a new dependency, consider:

- Maintenance status
- Security history
- Bundle size
- Desktop compatibility
- Licensing
- Privacy impact

Do not commit generated dependency directories such as `node_modules/`.

## Commit Messages

Use short, descriptive commit messages.

Examples:

```text
Fix handover status filtering
Improve Arabic task layout
Document local storage limitations
```

## License

By contributing to this repository, you agree that your contributions will be distributed under the project's [MIT License](LICENSE).
