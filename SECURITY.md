# Security Policy

## Repository Rules

- Never commit `.env`, private keys, API tokens, cookies or wallet secrets.
- Store operational credentials outside the repository and load them from the environment.
- Redact secrets from logs, screenshots, traces and reports.
- Use isolated virtual environments or local dependency installations.
- Verify third-party scripts before executing them.

## Reporting

If a secret or unintended private file is found in the repository, stop work, identify the affected commit and rotate the exposed credential immediately. Do not copy the secret into an issue or public discussion.
