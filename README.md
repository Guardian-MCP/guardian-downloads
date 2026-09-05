# Guardian

Guardian reshapes what your AI writes before you rely on it. It clears the patterns that mark machine writing, pushes claims back toward their sources, and holds every document to one standard. It runs inside Claude Desktop as a plugin, with a lighter skill for claude.ai. The free Scout plan runs without a license key.

## Which file do I download?

Every download lives on the [current release page](https://github.com/Guardian-MCP/guardian-downloads/releases/latest).

- Claude Desktop on Mac or Windows: the .plugin file. Open Claude Desktop, go to Settings, then Extensions, and drag it in. Click Agree on the license when it appears.
- Windows, and you would rather run an installer: the .exe file. Double-click it. If Windows blocks it, the .cmd file on the same page does the same job.
- A Mac or PC that already has Node.js 24: the .zip file.
- claude.ai in a browser: the guardian-deliver skill folder inside the .zip. This is a lighter, rules-only setup.

The install guide PDF walks through every step with pictures. [INSTALL.md](INSTALL.md) carries the same steps as text.

## Download options

| Asset | Intended use |
| --- | --- |
| [`guardian-windows-standalone-v2.8.30.exe`](https://github.com/Guardian-MCP/guardian-downloads/releases/download/v2.8.30/guardian-windows-standalone-v2.8.30.exe) | Primary Windows installer with a bundled Node.js runtime |
| [`guardian-windows-standalone-v2.8.30.cmd`](https://github.com/Guardian-MCP/guardian-downloads/releases/download/v2.8.30/guardian-windows-standalone-v2.8.30.cmd) | Windows script fallback when local policy blocks the EXE |
| [`guardian-windows-standalone-v2.8.30.zip`](https://github.com/Guardian-MCP/guardian-downloads/releases/download/v2.8.30/guardian-windows-standalone-v2.8.30.zip) | Windows payload archive for inspection or managed deployment |
| [`guardian-standalone-v2.8.30.plugin`](https://github.com/Guardian-MCP/guardian-downloads/releases/download/v2.8.30/guardian-standalone-v2.8.30.plugin) | Plugin package for compatible Claude plugin hosts |
| [`guardian-standalone-v2.8.30.zip`](https://github.com/Guardian-MCP/guardian-downloads/releases/download/v2.8.30/guardian-standalone-v2.8.30.zip) | macOS and traditional Windows installer package using an existing Node.js 24 installation |

Release assets are attached to the [current release page](https://github.com/Guardian-MCP/guardian-downloads/releases/latest). Verify each download against `SHA256SUMS.txt`.

## Product behavior

Guardian supports three operating modes:

- OFF stands down the Guardian agent and rule pool.
- MONITOR reviews work and reports findings.
- ENFORCE applies the full release gate to deliverables.

Feature access also depends on the active license tier. Scout runs without a license key. Paid tiers use a key issued for the user or organization.

## Data handling

Guardian processes checked content locally, collects no telemetry for the owner, and stores User Vault files in encrypted local storage. Content sent to an AI provider remains subject to that provider's data practices.

See [DATA_AND_PRIVACY.md](DATA_AND_PRIVACY.md) for the technical disclosure.

## Documentation

<!-- guardian-release-pdfs:start -->
- [Install guide PDF v2.8.30](docs/releases/v2.8.30/Guardian_Install_v2.8.30.pdf)
- [Quick Start PDF v2.8.30](docs/releases/v2.8.30/Guardian_QuickStart_v2.8.30.pdf)
- [Troubleshooting PDF v2.8.30](docs/releases/v2.8.30/Guardian_Troubleshooting_v2.8.30.pdf)
<!-- guardian-release-pdfs:end -->

- [Installation](INSTALL.md)
- [Security policy](SECURITY.md)
- [Support](SUPPORT.md)
- [Data and privacy](DATA_AND_PRIVACY.md)
- [End User License Agreement](EULA.md)
- [Terms of Use](TERMS.md)
- [Release notes](docs/releases/v2.8.30.md)

## Source availability

This repository distributes approved documentation and release packages. Guardian's development source remains in a separate private repository.

## Ownership

Guardian is owned by Ryan Klemetson. The EULA and Terms were approved by the owner on 2026-08-12. Owner-approved legal review controls those documents.
