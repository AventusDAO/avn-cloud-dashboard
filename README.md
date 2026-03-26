# AVN Node Dashboard – Downloads

Official releases of the AVN Node Dashboard desktop application.

## Installation

Pre-built packages are available for all major platforms. Download the release that matches your operating system from the [**Releases**](../../releases) page, then follow the platform-specific instructions below.

| Platform | Download | Notes |
|----------|----------|-------|
| **macOS** | `.dmg` | Native macOS application. [Details ↓](#running-on-macos) |
| **Windows** | `.exe` | Windows installer. [Details ↓](#running-on-windows) |
| **Linux** | `.AppImage` | Portable executable, no installation required. [Details ↓](#running-on-linux) |
| **Docker** | `docker.tar.gz` | Cross-platform container image. [Details ↓](#running-with-docker) |

## Running on macOS

1. Download the `.dmg` asset from the [Releases](../../releases) page.
2. Open the `.dmg` file and drag the app to your **Applications** folder.
3. On first launch macOS will block the app because it is not yet code-signed. To open it:
   - Open **Finder** and navigate to **Applications**.
   - Right-click the app and choose **Open**.
   - Confirm in the dialog that appears.

## Running on Windows

1. Download the `.exe` installer from the [Releases](../../releases) page.
2. Run the installer. Windows SmartScreen may show a warning — click **More info** then **Run anyway**.
3. Follow the installer prompts to complete the installation.
4. Launch the app from the Start Menu or the desktop shortcut.

## Running on Linux

1. Download the `.AppImage` from the [Releases](../../releases) page.

**AppImage:**

2. Make the file executable:
   ```bash
   chmod +x avn-cloud-dashboard-<version>.AppImage
   ```
   Or right-click the file --> **Properties --> Permissions** --> check **Allow executing as program**.
3. Double-click the `.AppImage` to run it, or execute it directly:
   ```bash
   ./avn-cloud-dashboard-<version>.AppImage
   ```

## Running with Docker

[Docker](https://www.docker.com/) lets you run the dashboard in an isolated container without installing any native dependencies. This is useful for server deployments, CI environments, or when you want to avoid platform-specific setup. You will need [Docker Engine](https://docs.docker.com/engine/install/) (or Docker Desktop on Mac/Windows) installed before proceeding.

1. Download the `docker.tar.gz` asset from the [Releases](../../releases) page.
2. Load the image:
   ```bash
   docker load < avn-cloud-dashboard-<version>-docker.tar.gz
   ```
3. Run the container:
   ```bash
   docker run -p 8080:80 avn-cloud-dashboard:<version>
   ```
4. Open your browser at [http://localhost:8080](http://localhost:8080).

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

