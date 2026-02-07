# Mesh Decal

The Mesh Decal tool lets you place decal geometry directly onto surfaces with an interactive, mouse-driven workflow. Click a decal thumbnail, hover over any surface, and click to place — with real-time scaling, rotation, and surface conforming.

![Mesh Decal tab with decal grid and placement settings](Images/MeshDecal.png)

![Mesh Decal placed on a surface in the viewport](Images/MeshDecal_Result.png)

## Settings

| Setting | Description |
|---------|-------------|
| **Scale** | Size of the placed decal (accepts values down to 0.001 for micro-detail) |
| **Push** | Offset distance from the surface to prevent z-fighting |

## Placement Modes

| Mode | Description |
|------|-------------|
| **Place Single Decal** | Place one decal, then exit placement mode |
| **Place Multiple Decals** | Keep placing decals continuously — scale and rotation are preserved between placements |

## Linking

| Option | Description |
|--------|-------------|
| **Link to Object** | Links the placed decal to the target object so they move together |
| **Link to Parent** | Links the decal to the target object's parent |

## Placing a Decal

1. Select your target object in the viewport.
2. In the Mesh Decal tab, click a decal thumbnail to enter **placement mode**.
3. Move your mouse over the surface — the decal follows the cursor in real time.
4. **Left-click** to place the decal.
5. **Right-click** or **Esc** to cancel placement.

## Mouse Controls

| Action | Control |
|--------|---------|
| Place decal | Left-click |
| Cancel placement | Right-click / Esc |
| Scale | Ctrl + drag |
| Free rotation | Shift + drag |
| 45-degree stepped rotation | Ctrl + Shift + drag |
| Precision mode (10x finer) | Hold Alt during any transform |

**Precision mode** works with all transforms — hold Alt while scaling or rotating for much finer control. You can switch between normal and precision mode seamlessly without jumps.

## Alignment Options

| Option | Description |
|--------|-------------|
| **Align to Edge** | Auto-rotates the decal to align with the longest face edge |
| **Align to UV** | Aligns to the UV direction for more stable results on complex topology |

Both options are enabled by default. Manual rotation (Shift + drag) works on top of alignment.

## Conform

PolyWrapper automatically detects whether the surface under the decal is flat or curved:

- **Flat surfaces:** The decal stays as a simple quad for best performance.
- **Curved surfaces:** A subdivided version is used and conforms to the surface curvature.

| Setting | Description |
|---------|-------------|
| **Auto-Conform** | Conform distance value — controls how strongly the decal wraps to the surface |
| **Auto-Optimize** | Percentage threshold for optimizing the conform mesh |
| **Subdivision** | Number of subdivisions for the conform mesh — higher values conform more smoothly to curved surfaces |

> **Note:** Auto-Conform requires 3ds Max 2024.2 or later. On older builds, it is automatically disabled and decals are placed as flat quads.

## Decal Swapping

With a placed decal selected in the viewport, click a different thumbnail to **swap** it. PolyWrapper preserves consistent scaling and adjusts to the new decal's UV aspect ratio.

Swapping works in:
- **Object mode** — when the decal is a simple 4-vertex quad
- **Face mode** — when you have quad faces selected

## Preview Scale

The **Preview Scale** draggable handle controls the size of decal thumbnails in the grid. Double-click the handle to auto-fit thumbnails so they fill the available space without scrolling.

---

[Back to Home](../README.md) | [UV Adjustments](uv-adjustments.md) | [Set Creator](set-creator.md)
