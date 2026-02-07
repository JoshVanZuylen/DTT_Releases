# Options & Theming

The Options tab gives you full control over PolyWrapper's appearance, behavior, and module configuration. Every tab can have its own color identity with animated backgrounds.

![Options tab — UI Customisation with per-tab color settings](Images/Options_%20(2).png)

### Theme Presets

| | |
|---|---|
| ![Blood theme — deep red tones](Images/Themes%20(1).png) | ![Storm theme — cool teal gradient](Images/Themes%20(2).png) |
| ![Monotone theme — clean greyscale](Images/Themes%20(3).png) | ![Moss theme — natural green palette](Images/Themes%20(4).png) |

## Help

| Button | Description |
|--------|-------------|
| **PolyWrapper Help** | Opens the documentation |
| **Open Data Directory** | Opens the folder where your set data is stored |
| **Open Install Directory** | Opens PolyWrapper's install location |
| **Launch PolyWrapper at 3ds Max startup** | Toggle to auto-launch when Max starts |

## UI Customisation

### Layout Navigation

Choose where the tool tabs appear:

| Position | Description |
|----------|-------------|
| **Right side** | Tabs on the right edge (vertical) |
| **Left side** | Tabs on the left edge (vertical) |
| **Top** | Tabs along the top (horizontal) |

### UI Theme

PolyWrapper ships with several built-in color presets that completely restyle the interface:

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

Select a preset from the **Themes** dropdown and it applies immediately. Click **Save theme** to save your current configuration as the Custom preset.

### Per-Tab Color Customization

Each tab has its own row showing:

- **Tab accent color** — the main color swatch (e.g. `rgb(204,97,20)` for Trim Sheets). Click to change. Controls title bars, toggles, spinners, and borders for that tab.
- **Background color** — optional per-tab background tint. Click **Custom background colour** to set a unique background for each tab.
- **Custom button colours** — toggle to enable per-tab button styling with separate normal and pressed state colors.

Tabs listed: Trim Sheets, Mesh Decal, Strip Decals, Set Creator, Options, About.

### Background

| Setting | Description |
|---------|-------------|
| **Use background texture / Use UI theme background** | Toggle between a texture-based background or a solid theme color |
| **Background colour (Global)** | Base background color applied behind everything |
| **Texture** | Background texture file — click **Browse** to choose, **Clear** to remove |
| **Background opacity (%)** | How visible the background texture is (0–100) |
| **Button opacity (%)** | Transparency of tool buttons (0–100) |
| **Tab bar texture opacity (%)** | Transparency of the tab bar background (0–100) |

## Material Assignment Settings

See [Material Matching](material-matching.md) for the full documentation on this section.

## Animations

![Animations and Trim Sheets sections of the Options tab](Images/Options_%20(1).png)

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
| **Skip triangles on quad trimming** | Ignores triangle faces when processing quad-based trim operations |
| **Fast Unwrap (Experimental)** | Enables a faster UV unwrapping algorithm |
| **Auto-apply cached material** | Automatically applies the cached material when loading a set |

---

[Back to Home](../README.md)
