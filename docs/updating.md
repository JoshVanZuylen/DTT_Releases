# Updating

PolyWrapper includes a built-in auto-updater on the **About** tab. You can also update manually at any time.

![About tab showing Version Status and update controls](Images/About.png)

## Version Status

The About tab shows your current version and Max version (e.g. "2026 Alpha v0.5.0" on "3ds Max 2024.1"). It tells you whether you're up to date or if a newer version is available.

## Auto-Update

The **Auto-Update** toggle on the About tab controls whether PolyWrapper automatically downloads and installs updates. When enabled:

1. PolyWrapper checks for updates on launch.
2. If a newer version is found, it downloads and installs automatically.
3. The tool reloads after a successful update.
4. Release notes pop up so you can see what's new.

Toggle Auto-Update off if you prefer to update manually.

## Manual Update Controls

The About tab provides three buttons:

| Button | Description |
|--------|-------------|
| **Check for Updates** | Manually check if a newer version is available |
| **Show Release Notes** | View release notes for the current version |
| **Reload Tool** | Reload PolyWrapper without restarting Max |

## Updating from the About Tab

1. Click **Check for Updates**.
2. If a newer version is available, a dropdown appears with compatible releases for your Max version.
3. Select a version and click to install.
4. A progress bar shows download and installation progress.
5. PolyWrapper automatically reloads after installation.

## Manual Update via Download

If you prefer to update by downloading directly:

1. Visit the [Releases page](https://github.com/JoshVanZuylen/DTT_Releases/releases) (or click **Download Releases** on the About tab).
2. Download the zip matching your Max version.
3. Extract it to the same location as your current install (or a new location).
4. Drag `PolyWrapper_MacroInstaller.ms` into the Max viewport to register the new path.

## Downgrade Protection

If you manually install an older version, auto-update automatically disables itself to prevent immediately updating back to the newer version. This lets you stay on a specific version if needed.

## Maintenance Eligibility

Updates are subject to your [license maintenance window](licensing.md). If your maintenance has expired, you keep your current version but cannot update to releases published after your window ended.

## Resource Links

The About tab also provides quick links to:

| Link | Destination |
|------|-------------|
| **Documentation** | Opens the PolyWrapper documentation |
| **Download Releases** | GitHub releases page |
| **Discord** | Community Discord server |
| **Bug Reports** | Bug report channel on Discord |
| **ArtStation Portfolio** | Author's portfolio |
| **X (Twitter)** | Author's Twitter/X account |

---

[Back to Home](../README.md) | [Licensing](licensing.md) | [Installation](installation.md)
