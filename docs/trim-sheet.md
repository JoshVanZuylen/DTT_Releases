# Trim Sheet

The Trim Sheet tool lets you apply trim textures to selected faces on your mesh. You can manually pick which trim region to apply, or let the [Hotspot](hotspot.md) system assign trims automatically based on face size.

![Trim Sheet tab showing trim view with multi-set Quick Sets](Images/TrimSheets.png)

## Concepts

A **trim sheet** is a texture atlas where multiple detail strips (trims) are packed into a single texture. Instead of creating unique textures for every surface, you map faces to specific regions of the trim sheet. PolyWrapper handles the UV math so the textures align cleanly.

## Choosing a Trim

1. Use the **Library Panel** at the top to select a Category, Style, and Set.
2. The trim icons load in the panel below — each icon represents a region on the trim sheet.
3. Select faces on your mesh in Face (4) or Element (5) mode.
4. Click a trim icon to project UVs into that trim region.

## Projection Methods

PolyWrapper offers two projection methods when applying trims:

| Method | How It Works | Best For |
|--------|-------------|----------|
| **Average Normal** | Projects along the average normal of the selected faces | Flat or gently curved surfaces |
| **Longest Edge** | Aligns projection using the longest edge direction | Elongated strips, consistent alignment |

Switch between methods using the dropdown in the set window.

## Axis Orientation

Trims can be oriented **horizontally** or **vertically** on the trim sheet. This is defined during the [set creation](set-creator.md) process when you choose the Layout Type (Horizontal / Vertical).

## Multi-Group Projection

Select multiple non-contiguous face groups and right-click a projection button to project them all at once. Each group is processed independently with its own UV mapping.

## Element Mode Support

UV tools work in both **Face mode (4)** and **Element mode (5)**. Element selections are automatically converted to face selections behind the scenes — no need to switch modes manually.

## UV Adjustments

After applying a trim, use the [UV Adjustments](uv-adjustments.md) panel to fine-tune positioning with flip, rotate, nudge, scale, and grow/shrink controls.

## Automatic Placement

For large meshes where manual trim assignment would be tedious, switch to the Hotspot view. See [Hotspot](hotspot.md) for details on automatic trim placement.

---

[Back to Home](../README.md)
