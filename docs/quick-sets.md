# Quick Sets

Quick Sets are preset slots that let you switch between your frequently used asset sets with a single click. They appear as numbered buttons in the Trim Sheet and Mesh Decal tabs.

![Quick Sets in multi-set mode with multiple trim sets loaded](Images/TrimSheets.png)

## Single Set Mode

Click any Quick Set button to load that set. This clears the current view and displays only the selected set. The Category/Style/Set dropdowns update to match.

## Multi-Set Mode

Multi-Set mode is enabled by default in v0.5.0 and allows loading multiple sets at once for side-by-side comparison and mixed workflows.

### Loading Multiple Sets

- **Shift + click** a Quick Set button to **add** that set to the current view.
- **Shift + click** the same button again to **remove** it from the view.
- Normal click (without Shift) loads a single set exclusively, clearing all others.

### Layout

When multiple sets are loaded:

- Each set's icons appear in their own section, separated by dividers.
- **Material ID columns** on the left show the material slot assignments for each set (e.g., `P:1 S:2` for Primary/Secondary).
- Sets display in the order they were added.

### View Modes

| Mode | Description |
|------|-------------|
| **List view** | Vertical list layout — one set per row |
| **Tile view** | Grid layout with adjustable column count |

Toggle between views with the List/Tile button. In tile mode, adjust the column count for your preferred grid arrangement.

### Per-Set Hotspot Processing

In multi-set mode within the Trim Sheet tab, each loaded set gets its own **Run Hotspot** button. Process hotspots for each set independently without affecting the others.

## Pre-Loading

Quick Sets that have been assigned are pre-loaded at startup, so switching between previously viewed sets is instant.

---

[Back to Home](../README.md) | [Trim Sheet](trim-sheet.md) | [Hotspot](hotspot.md)
