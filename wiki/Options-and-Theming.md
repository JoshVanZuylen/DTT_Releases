# Options & Theming

The Options tab gives you full control over Wrapper's appearance, behavior, and module configuration. Every tab can have its own color identity with animated backgrounds.

![Options tab — UI Customisation with per-tab color settings](images/Options-2.png)

### Theme Presets

| | |
|---|---|
| ![Blood theme — deep red tones](images/Themes-1.png) | ![Storm theme — cool teal gradient](images/Themes-2.png) |
| ![Monotone theme — clean greyscale](images/Themes-3.png) | ![Moss theme — natural green palette](images/Themes-4.png) |

## Help

| Button | Description |
|--------|-------------|
| **Wrapper Help** | Opens the documentation |
| **Open Data Directory** | Opens the folder where your set data is stored |
| **Open Install Directory** | Opens Wrapper's install location |
| **Launch Wrapper at 3ds Max startup** | Toggle to auto-launch when Max starts |
| **Uninstall Wrapper** | Cleanly removes Wrapper from 3ds Max (disabled in development mode) |

### Uninstalling Wrapper

The **Uninstall Wrapper** button walks you through a two-step confirmation:

1. Confirm you want to uninstall.
2. Optionally remove your preferences and set data.

The uninstaller removes the startup script, toolbar macro, Max directory registration, license data, and the install folder, then shows a summary of what was removed before closing the tool window.

## UI Customisation

### Layout Navigation

Choose where the tool tabs appear:

| Position | Description |
|----------|-------------|
| **Right side** | Tabs on the right edge (vertical) |
| **Left side** | Tabs on the left edge (vertical) |
| **Top** | Tabs along the top (horizontal) |

### UI Theme

Wrapper ships with several built-in color presets that completely restyle the interface:

| Preset | Description |
|--------|-------------|
| **Muted Colours** | Warm, distinct colors per tab — orange, green, blue, purple, red, teal |
| **Monotone** | Clean greyscale gradient across all tabs |
| **Blood** | Deep red tones throughout |
| **Storm** | Cool blue gradient inspired by stormy skies |
| **Gold** | Warm amber and bronze tones |
| **Moss** | Natural green palette |
| **Maker** | Mixed colors with a workshop/maker aesthetic |
| **Custom** | Your own saved configuration |

Select a preset from the **Themes** dropdown and it applies immediately. Click **Save theme** to save your current configuration as the Custom preset. Click **Delete** next to Save theme to remove a saved preset.

### Per-Tab Color Customization

Each tab has its own row showing:

- **Tab accent color** — the main color swatch. Click to change. Controls title bars, toggles, spinners, and borders for that tab.
- **Background color** — optional per-tab background tint. Click **Custom background colour** to set a unique background for each tab.
- **Custom button colours** — toggle to enable per-tab button styling with separate normal and pressed state colors.

Tabs listed: Trim Sheets, Mesh Decal, Strip Decals, Set Manager, Options, About, Materials, Assistant.

### Background

The **Use background texture** and **Use UI theme background** toggles are linked:
- Disabling "Use background texture" automatically disables "Use UI theme background".
- Enabling "Use UI theme background" automatically enables "Use background texture".
- When both are off, the background reverts to the default neutral colour.

| Setting | Description |
|---------|-------------|
| **Use background texture / Use UI theme background** | Toggle between a texture-based background or a solid theme color |
| **Background colour (Global)** | Base background color applied behind everything |
| **Texture** | Background texture file — click **Browse** to choose, **Clear** to remove |
| **Background opacity (%)** | How visible the background texture is (0–100) |
| **Button opacity (%)** | Transparency of tool buttons (0–100) |
| **Tab bar texture opacity (%)** | Transparency of the tab bar background (0–100) |

## Decals

| Setting | Description |
|---------|-------------|
| **Wire colour** | Custom wire colour for all created decals (default: orange). Applies to both Mesh Decals and Strip Decals |
| **Use object colour** | When enabled, new decals automatically inherit the wire colour of the mesh they are placed on |

## Material Assignment Settings

See [[Material-Matching]] for the full documentation on this section.

## Animations

![Animations and Trim Sheets sections of the Options tab](images/Options-1.png)

| Setting | Description |
|---------|-------------|
| **Enable animations** | Toggle all smooth UI animations on/off. When off, controls snap instantly |
| **Animation speed (s)** | Duration of UI animations in seconds (e.g. 0.25) |
| **Background animations** | Toggle the animated background texture on/off |
| **Background animation type** | **Scroll**, **Parallax**, or **Scroll + Parallax** |
| **Background animation amount** | Speed/intensity of the background animation |

## Trim Sheets

Advanced Trim Sheet options:

| Setting | Description |
|---------|-------------|
| **Fast Unwrap (Experimental)** | Enables a faster UV unwrapping algorithm |
| **Auto-apply cached material** | Automatically applies the cached material when loading a set |

> **Note:** The "Skip tris and n-gons" toggle has moved to the **Trim Settings** panel on the Trim Sheet tab for easier access.

---

[[Home]]
