# Security Policy

## Supported releases

Security fixes target the current release line. Older packages may lack current protections and installer behavior.

## Report a vulnerability

Send security reports to ryanklemetson13@gmail.com. Include the affected version, operating system, reproduction steps, observed result, and expected result.

Keep license keys, customer content, vault files, and active exploit details out of public issues. A private report enables coordinated review before disclosure.

## Local security model

Guardian processes checked content locally. User Vault content uses encrypted local storage. License validation runs locally. The status widget binds to a local service rather than a public network endpoint.

Guardian also integrates with third-party AI clients. Their authentication, transport, storage, and retention policies remain outside Guardian's local security boundary.

## Release integrity

Each release includes SHA-256 checksums. Compare the downloaded asset with `SHA256SUMS.txt` before installation. Report any mismatch and retain the original filename and download source for investigation.

