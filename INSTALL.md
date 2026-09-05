# Install Guardian

Every download lives on the current release page: https://github.com/Guardian-MCP/guardian-downloads/releases/latest

## Which file do I download?

- Claude Desktop on Mac or Windows: the .plugin file. Open Claude Desktop, go to Settings, then Extensions, and drag it in. Click Agree on the license when it appears.
- Windows, and you would rather run an installer: the .exe file. Double-click it. If Windows blocks it, the .cmd file on the same page does the same job.
- A Mac or PC that already has Node.js 24: the .zip file.
- claude.ai in a browser: the guardian-deliver skill folder inside the .zip. This is a lighter, rules-only setup.

The free Scout plan runs without a license key. The install guide PDF on the release page walks through every step with pictures.

## Claude Desktop (Mac and Windows)

1. Download the .plugin file.
2. Open Claude Desktop, then Settings, then Extensions.
3. Drag the file into the window and drop it. The Add extension button reaches the same place if you prefer menus.
4. Click Agree when the license appears. Guardian stays inactive until you do.
5. Restart Claude Desktop if it asks.

Check that it worked: start a new conversation and type Guardian status. The reply names your plan and your current mode.

## Windows installer

1. Download the .exe file.
2. Run it. If Windows shows a SmartScreen warning, choose More info, then Run anyway. If company policy blocks the .exe, use the .cmd file instead.
3. Keep All when it asks which apps to connect.
4. Enter a license key if you have one, or skip that step for Scout.
5. Let it restart Claude Desktop when it finishes.

The installer runs inside your user profile, brings its own Node.js runtime, and asks for no administrator rights.

## The .zip package (Node.js 24 already installed)

1. Download and extract the .zip file.
2. Read EULA.md and TERMS.md inside the folder.
3. Run install-guardian.command on a Mac, or install-guardian.bat on Windows.
4. Accept the license dialog and restart the configured client.

The folder also holds uninstall-guardian.command for cleanup on a Mac. The Windows installer's uninstall switch is listed at the end of this page.

## claude.ai in a browser

Open Settings, then Capabilities, choose Upload skill, and pick the guardian-deliver folder from the extracted .zip. One upload covers your whole account. This path applies Guardian's writing rules without the desktop plugin's checker, so it is lighter than a desktop install.

## Verify a download

Each release publishes SHA256SUMS.txt. Compare your file's checksum with the matching line.

Windows PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\<downloaded file>
```

Mac:

```bash
shasum -a 256 <downloaded file>
```

## For IT administrators: Windows installer switches

| Switch | Function |
| --- | --- |
| `--target <all\|claude\|codex\|vscode\|copilot\|openai>` | Select one client target or all supported local targets |
| `--license <key>` | Supply a license key |
| `--quiet` | Run without confirmation prompts |
| `--no-restart` | Leave Claude Desktop running |
| `--repair` | Refresh the runtime and selected client entries |
| `--uninstall` | Remove selected client entries and installed runtime files while retaining Guardian user data |
| `--no-launch` | Skip widget shortcut creation |
| `--report <path>` | Write a JSON result report |
| `--help` | Display the installer option list |

The openai target records the current remote-service requirement. It does not claim a local OpenAI Desktop connection.
