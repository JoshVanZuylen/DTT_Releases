# Mesh Decal

The Mesh Decal tool lets you place decal geometry directly onto surfaces with an interactive, mouse-driven workflow. Click a decal thumbnail, hover over any surface, and click to place — with real-time scaling, rotation, and surface conforming.

![Mesh Decal tab with decal grid and placement settings](images/MeshDecal.png)

![Mesh Decal placed on a surface in the viewport](images/MeshDecal_Result.png)

## Settings

| Setting | Description |
|---------|-------------|
| **Scale** | Size of the placed decal (accepts values down to 0.001 for micro-detail). Displayed with unit labels (e.g. "5 cm") |
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

> **Note:** Clicking a different thumbnail while placement is active cancels the current placement and starts fresh with the new decal.

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
| **Align to Edge** | Auto-rotates the decal to align with the longest face edge — locks to the polygon's longest boundary edge and stays stable as the cursor moves |
| **Align to UV** | Aligns to the UV direction for more stable results on complex topology |

Both options are enabled by default. Manual rotation (Shift + drag) works on top of alignment.

## Conform

Wrapper automatically detects whether the surface under the decal is flat or curved:

- **Flat surfaces:** The decal stays as a simple quad for best performance.
- **Curved surfaces:** A subdivided version is used and conforms to the surface curvature.

| Setting | Description |
|---------|-------------|
| **Auto-Conform** | Conform distance value — controls how strongly the decal wraps to the surface. Enabled by default. |
| **Auto-Optimize** | Percentage threshold for optimizing the conform mesh |
| **Subdivision** | Number of subdivisions for the conform mesh (up to 20) — higher values conform more smoothly to curved surfaces. Defaults to 12. |

> **Note:** Auto-Conform requires 3ds Max 2024.2 or later. On older builds, it is automatically disabled and decals are placed as flat quads.

Curvature detection scales with decal size — small decals on curved surfaces correctly activate conform.

## Smart Instances

When **Smart Instances** is enabled, placing a decal on an instanced or referenced object automatically creates the same decal on every other instance in the scene.

- All created decals are true instances of each other — editing one updates all of them.
- Each decal is correctly positioned relative to its target instance, even when instances are rotated or scaled differently.
- Decals are parented to their respective target instances following the current **Link Type** setting.

## Smart Modifiers

Mesh Decals adopt certain modifiers as instances when you create them — this includes **Symmetry**, **Chamfer**, **Array**, **Smooth**, and **Bend**. Decals behave the same way as your source mesh.

- Modifier gizmos (Symmetry, Array, Bend) align correctly — the decal's pivot is matched to the source object before modifiers are applied.
- Chamfer modifiers using "From Material ID" with "Edge Verts Selected" are automatically excluded.
- **Link to Object** and **Link to Parent** are preserved after Smart Modifiers are applied.

## Isolation Mode

Decal placement respects 3ds Max isolation mode — only visible objects receive placements. Hidden and frozen objects are excluded from placement raycasting.

## Decal Swapping

With placed decals selected in the viewport, click a different thumbnail to **swap** them. Wrapper preserves consistent scaling and adjusts to the new decal's UV aspect ratio.

- **Right-click** a thumbnail to swap multiple selected decals at once — each decal maintains its own size and position, only the texture and material are replaced.
- Swapping works on decals with Smart Modifiers (e.g. Symmetry).

Swapping works in:
- **Object mode** — when the decal is a simple 4-vertex quad
- **Face mode** — when you have quad faces selected (supports multiple quads across several decals in a combined mesh)

## Preview Scale

The **Preview Scale** draggable handle controls the size of decal thumbnails in the grid. Double-click the handle to auto-fit thumbnails so they fill the available space without scrolling.

---

[[Home]] | [[UV-Adjustments|UV Adjustments]] | [[Set-Creator|Set Creator]]
