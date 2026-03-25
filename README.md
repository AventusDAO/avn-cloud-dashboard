# AVN Node Dashboard – Downloads

Official releases of the AVN Node Dashboard desktop application.

## Installation

| Platform | Download | Notes |
|----------|----------|-------|
| **macOS** | `.dmg` | Open the DMG and drag to Applications. Until the app is code-signed, macOS will block it on first launch — open Finder, navigate to Applications, right-click the app, and choose **Open**, then confirm in the dialog |
| **Windows** | `.exe` | Run the installer – may show SmartScreen warning until code-signed |
| **Linux** | `.AppImage` | Right-click the `.AppImage` file, go to **Properties → Permissions**, and check "Allow executing as program" (or run `chmod +x` in the terminal), then double-click to run. Alternatively, install the `.deb` on Debian/Ubuntu |

Head to the [**Releases**](../../releases) page to download the latest version.

## Verifying Downloads

Each release includes SHA-256 checksums. To verify:

```bash
# macOS / Linux
shasum -a 256 <downloaded-file>

# Windows (PowerShell)
Get-FileHash <downloaded-file> -Algorithm SHA256
```

## Feedback & Issues

Please report issues via [GitHub Issues](../../issues).

