# Security Policy

## Scope

AI Trust Observatory is an early-stage research framework. Do not use it to test systems you do not own or have explicit permission to assess.

## Safe testing requirements

- Use synthetic canary values only.
- Use isolated cloud accounts with no production access.
- Never use live AWS keys, API tokens, customer data or personal data.
- Do not probe third-party providers without authorisation and compliance with their terms.
- Keep callback infrastructure under your control and document what it logs.

## Reporting

Please report suspected vulnerabilities privately to the project maintainer before public disclosure. Include a minimal reproduction, affected version/commit, impact and suggested mitigation. Do not include real secrets or personal data.
