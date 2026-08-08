# Install Guardian

Choose the package that matches the target system. Verify the downloaded file before running it.

## Windows

The primary package is `guardian-windows-standalone-v2.8.26.exe`.

1. Download the EXE from the GitHub Release.
2. Compare its SHA-256 value with `SHA256SUMS.txt`.
3. Run the installer.
4. Select the requested client targets and license option.
5. Restart affected clients when the installer requests it.

The Windows package installs within the current user profile. It includes its own Node.js runtime and does not require administrator rights.

The `.cmd` asset provides a fallback when local policy blocks the EXE. The Windows ZIP contains the same payload for inspection or managed deployment.

Supported Windows switches include:

| Switch | Function |
| --- | --- |
| `--target <all|claude|codex|vscode|copilot|openai>` | Select one client target or all supported local targets |
| `--license <key>` | Supply a license key |
| `--quiet` | Run without confirmation prompts |
| `--no-restart` | Leave Claude Desktop running |
| `--repair` | Refresh the runtime and selected client entries |
| `--uninstall` | Remove selected client entries and installed runtime files while retaining Guardian user data |
| `--no-launch` | Skip widget shortcut creation |
| `--report <path>` | Write a JSON result report |
| `--help` | Display the installer option list |

The `openai` target records the current remote-service requirement. It does not claim a local OpenAI Desktop connection.

## macOS

Use `guardian-standalone-v2.8.26.zip`.

1. Install Node.js 24 LTS.
2. Extract the ZIP.
3. Review `EULA.md` and `TERMS.md`.
4. Run `install-guardian.command`.
5. Accept the license dialog and restart the configured client.

The package also includes `uninstall-guardian.command` for local cleanup.

## Claude plugin package

Use `guardian-enterprise-v2.8.26.plugin` with a compatible Claude plugin installation flow. The package includes the Guardian server, hooks, skills, and agent references.

## Prompt kit

Use `guardian-prompt-kit-v2.8.26.zip` when the target surface cannot load the local MCP server. Extract the archive and follow its included README. The prompt kit provides instructions and reference agents without the automated local server features.

## Verify a download

Windows PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\guardian-windows-standalone-v2.8.26.exe
```

macOS:

```bash
shasum -a 256 guardian-standalone-v2.8.26.zip
```

Linux:

```bash
sha256sum guardian-prompt-kit-v2.8.26.zip
```

Match the result exactly with the corresponding line in `SHA256SUMS.txt`.

