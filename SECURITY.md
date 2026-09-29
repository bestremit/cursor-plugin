# Security Policy

## Reporting a vulnerability

Please do not open a public issue for a suspected security vulnerability.

Report security issues to **support@bestremit.app** with enough information to reproduce and assess the issue.

## Plugin security model

The BestRemit plugin connects Cursor to the hosted BestRemit MCP endpoint over HTTPS.

The plugin does not require an API key, bank login, bank account number, card number, or payment credential. Its tools are intended for read-only comparison and reference-rate queries; they do not initiate transfers or modify financial accounts.

The source code for the separately hosted BestRemit service is not part of this plugin repository.
