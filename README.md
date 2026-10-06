# ShiftMate ER

[![CI](https://github.com/ShaheenMedTech/ShiftMate-ER/actions/workflows/ci.yml/badge.svg)](https://github.com/ShaheenMedTech/ShiftMate-ER/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/ShaheenMedTech/ShiftMate-ER)](https://github.com/ShaheenMedTech/ShiftMate-ER/releases/latest)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A lightweight Emergency Department shift management and clinical handover application.

ShiftMate ER is available as both a **web application** and a **cross-platform desktop application built with Tauri**.

## Live Demo

https://shaheenmedtech.github.io/ShiftMate-ER/

## Desktop Release

Latest release: **v1.1.0**

Available for:

- Linux
  - AppImage
  - DEB
  - RPM
- Windows
  - NSIS installer
  - MSI installer

[Download ShiftMate ER v1.1.0 →](https://github.com/ShaheenMedTech/ShiftMate-ER/releases/tag/v1.1.0)

See [CHANGELOG.md](CHANGELOG.md) for release notes.

## Features

- Shift management
- Cases, tasks, notes, and reminders
- Clinical handover management
- Arabic / English
- RTL / LTR
- Light / Dark themes
- Local data storage
- Responsive web interface
- Cross-platform desktop application support

## Tech Stack

- React
- Vite
- Tailwind CSS
- Tauri
- Rust

## Clinical Safety and Privacy

ShiftMate ER is an open-source workflow and educational project. It is **not a certified medical device, electronic health record, hospital information system, or replacement for clinical judgement, approved handover procedures, institutional systems, or local policy**.

The current implementation stores application records locally using browser/WebView `localStorage`.

The current storage and session model:

- does not provide application-level encryption at rest
- does not provide identity-grade authentication or access control
- may leave locally stored records accessible to users or processes with sufficient access to the same device, operating-system account, browser profile, application data, backups, or developer tools

**Do not use the current public build to store real identifiable patient information, protected health information, credentials, secrets, or other sensitive production clinical data.**

For the full policy and vulnerability-reporting process, see [SECURITY.md](SECURITY.md).

## Development

Install dependencies:

```sh
npm ci
```

Run the web application:

```sh
npm run dev
```

Build the web application:

```sh
npm run build
```

Run the Tauri desktop application after installing the required Rust and platform dependencies:

```sh
npm run tauri -- dev
```

More detailed contribution instructions are available in [CONTRIBUTING.md](CONTRIBUTING.md).

## Continuous Integration

Pull requests and pushes to `main` are checked with GitHub Actions.

The CI workflow currently verifies:

- reproducible npm dependency installation with `npm ci`
- successful production web build
- Rust formatting for the Tauri code
- successful `cargo check` for the Tauri backend

Tagged releases continue to use the dedicated desktop release workflow, while `main` deploys the web application to GitHub Pages.

## Project Policies

- [Contributing](CONTRIBUTING.md)
- [Security and Privacy](SECURITY.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Changelog](CHANGELOG.md)
- [MIT License](LICENSE)

Bug reports and feature requests should use the repository's GitHub Issue templates.

## License

ShiftMate ER is licensed under the [MIT License](LICENSE).
