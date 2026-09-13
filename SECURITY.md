# Security Policy

This repository contains academic architecture documentation only.

## Sensitive Information
Do not commit:
- AWS access keys, secret keys, session tokens, passwords, or private keys
- `.env` files or credential exports
- AWS account identifiers unless intentionally sanitized
- Unnecessary IP addresses, resource identifiers, emails, or usernames
- Screenshots containing browser profiles or unrelated personal information

## Reporting an Issue
If sensitive information is accidentally committed, remove it from the repository and its Git history, rotate the affected credential immediately, and review AWS activity logs.
