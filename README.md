# Guardian

> Review status: this repository and its release are private review candidates. Release publication has not been approved.

Guardian is an MCP-based quality governance framework for AI-assisted work. It provides writing checks, enforcement modes, release-ready workflows, reference agents, and a local status interface across supported AI development surfaces.

## Download options

| Asset | Intended use |
| --- | --- |
| `guardian-windows-standalone-v2.8.25.exe` | Primary Windows installer with a bundled Node.js runtime |
| `guardian-windows-standalone-v2.8.25.cmd` | Windows script fallback when local policy blocks the EXE |
| `guardian-windows-standalone-v2.8.25.zip` | Windows payload archive for inspection or managed deployment |
| `guardian-enterprise-v2.8.25.plugin` | Plugin package for compatible Claude plugin hosts |
| `guardian-standalone-v2.8.25.zip` | macOS and traditional Windows installer package using an existing Node.js 24 installation |
| `guardian-prompt-kit-v2.8.25.zip` | Prompt and reference-agent kit for surfaces without a local MCP connection |

Release assets are attached to the repository's GitHub Release. Verify each download against `SHA256SUMS.txt`.

## Install

Windows users can start with the EXE package. macOS users can extract the standalone ZIP and run `install-guardian.command`. Plugin and prompt-kit users can follow the package-specific instructions.

See [INSTALL.md](INSTALL.md) for platform steps, installer switches, and checksum commands.

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

- [Installation](INSTALL.md)
- [Security policy](SECURITY.md)
- [Support](SUPPORT.md)
- [Data and privacy](DATA_AND_PRIVACY.md)
- [End User License Agreement](EULA.md)
- [Terms of Use](TERMS.md)
- [Release notes](docs/releases/v2.8.25.md)

## Source availability

This repository distributes approved documentation and release packages. Guardian's development source remains in a separate private repository.

## Ownership

Guardian is owned by Ryan Klemetson. The EULA and Terms in this review project remain drafts until their approval banners are removed.

