# Contributing to AndroidCallLogSync

Android Call Log Sync sends call-log entries to a user-selected endpoint. Contributions can improve Android behaviour, transport reliability, privacy, accessibility and documentation of the endpoint contract.

## Before you start

Read [README.md](README.md), [PRIVACY.md](PRIVACY.md), [build.gradle](build.gradle) and the [application configuration](app/build.gradle). Check current issues and pull requests before substantial work. Preserve the documented payload fields and headers, and explain any compatibility changes for existing receiving services.

For bugs, provide the affected version or commit, environment, minimal reproduction, expected result and observed result. For a substantial proposal, describe the use case and compatibility impact before expanding implementation scope. Use existing issue templates when offered.

## Development and validation

Use the committed Gradle wrapper and the Android SDK/toolchain requirements declared by the project. Select the relevant build, lint and test tasks exposed by that configuration and report their exact names and results. There is no repository-documented single full-validation command to substitute for that inspection.

Use an emulator or dedicated development device with invented call records and an endpoint you control. Exercise relevant permission states, denied permissions, missing connectivity, retry behaviour and malformed or unsuccessful endpoint responses. For UI work, inspect the affected screens and accessibility. Add focused automated tests where behaviour can be checked deterministically.

Keep real phone numbers, device tokens, call histories and private endpoint addresses out of fixtures, screenshots and logs. A successful build does not prove background delivery or permission behaviour on every supported Android version; identify the versions and scenarios actually exercised.

## Pull requests

Create a focused branch from the current `main` branch and submit a pull request to this repository. Link the relevant issue or existing project task, explain the resulting behaviour, and update affected examples and documentation. Keep unrelated changes in separate pull requests.

Report executed commands, outcomes and the commit they validate. Identify unavailable checks and remaining limitations explicitly. Follow the repository's existing review and automated-check requirements; retain required gates and current ownership. Address findings and verify the final head before integration. Repository changes do not themselves authorise a release or external operational action.

## Security, rights and conduct

Follow the [security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Use private vulnerability reporting if available; otherwise request a private contact without publishing vulnerability details. Keep credentials, personal information and restricted source material out of issues, fixtures, logs and artifacts.

Read the [existing licence](LICENSE) and preserve attribution and third-party terms. Follow the [code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md) and keep technical discussions respectful.

## Basis for this guide

This guide follows [GitHub's contribution-guideline guidance](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors) and the contribution-process and testing principles in [OpenSSF Best Practices](https://www.bestpractices.dev/en/criteria). It does not assert certification.
