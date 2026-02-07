# Installation

## System Requirements

- **3ds Max 2024**, **2025**, or **2026**
- Windows 10 or later
- A valid PolyWrapper license key ([purchase here](https://joshvanzuylen.gumroad.com/l/mwktte))

## Step-by-Step Install

### 1. Download & Extract

Download the latest release from the [Releases page](https://github.com/JoshVanZuylen/DTT_Releases/releases). Choose the zip that matches your 3ds Max version (e.g. `PolyWrapper_Alpha_v0.5.0_Max2026`).

Extract or copy the folder to a **stable location** on your machine — for example:

```
G:\Tools\PolyWrapper
```

> **Important:** Do not place the folder inside Max's `scripts\startup` directory. Keep it in its own location.

### 2. Run the Installer

1. Launch your version of 3ds Max.
2. Drag the `PolyWrapper_MacroInstaller.ms` file from the release folder into the 3ds Max viewport.
3. The installer registers the path so Max can always find the install tree, and the tool auto-launches on first install.

### 3. Set Up a Shortcut (Optional)

For quick access, assign PolyWrapper to a toolbar, button, or quad menu:

1. Go to **Customize > Customize User Interface**.
2. Find the PolyWrapper macro in the **"PolyWrapper"** category.
3. Drag it to a toolbar, or assign it to a hotkey, button, or quad menu.

### 4. Activate Your License

1. Open PolyWrapper and go to the **About** tab.
2. Enter your license key and click **Verify**.
3. Your license is now bound to this machine.

See [Licensing](licensing.md) for details on license tiers and managing your activation.

## Keeping Up to Date

PolyWrapper checks for updates automatically on launch. When an update is available, you can install it directly from the **About** tab. See [Updating](updating.md) for the full details.

To update manually, download the latest release from [GitHub Releases](https://github.com/JoshVanZuylen/DTT_Releases/releases) and repeat the install steps above.

## Troubleshooting

**"Tool cannot be found" error:**
If 3ds Max reports that it cannot find the tool, rerun the `PolyWrapper_MacroInstaller.ms` from your current release folder. This refreshes the stored path in Max's `Plugin.UserSettings.ini`.

**Multiple Max versions:**
Each Max version needs its own matching release folder (e.g. `Max2024`, `Max2026`). Run the installer once per Max version. Your license transfers automatically between Max versions on the same PC — no need to deactivate and reactivate.

---

[Back to Home](../README.md)
