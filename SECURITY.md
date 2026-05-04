# Security Policy

## Credentials Management

*   **Environment Variables**: All sensitive keys (API Keys, Secrets, Connection Strings) must be stored in `.env` files and never committed to version control.
*   **Git Ignore**: The `.gitignore` file must always include `.env`, `.env.local`, and related files.
*   **Client-Side Exposure**: Avoid exposing secret keys in the client-side code whenever possible. For services like Firebase or Supabase that require public-facing keys, ensure proper domain restriction and security rules in their respective dashboards.

## Handling User Data

*   **Authentication**: We use Firebase Authentication for secure user signup and login. Passwords and personal credentials are never stored in our application's database or code.
*   **Data Storage**: Project data is stored in `localStorage` for performance and synchronized to a secure Supabase instance.

## Reporting a Vulnerability

Please do not report security vulnerabilities through public GitHub issues. If you discover a security-related bug, please follow these steps:

1. **Direct Contact**: Email the details to the maintainer.
2. **Responsible Disclosure**: We request that you do not disclose the issue publicly until a fix is released.

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |