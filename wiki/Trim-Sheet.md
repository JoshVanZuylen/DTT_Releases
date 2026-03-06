# Trim Sheet

The Trim Sheet tool lets you apply trim textures to selected faces on your mesh. You can manually pick which trim region to apply, or let the [[Hotspot]] system assign trims automatically based on face size.

![Trim Sheet tab showing trim view with multi-set Quick Sets](images/TrimSheets.png)

## Concepts

A **trim sheet** is a texture atlas where multiple detail strips (trims) are packed into a single texture. Instead of creating unique textures for every surface, you map faces to specific regions of the trim sheet. Wrapper handles the UV math so the textures align cleanly.

## Choosing a Trim

1. Use the **Library Panel** at the top to select a Category, Style, and Set.
2. The trim icons load in the panel below — each icon represents a region on the trim sheet. Icons display at consistent widths regardless of how thin the trim is.
3. Select faces on your mesh in Face (4), Element (5), or **Edge** sub-object mode.
4. Click a trim icon to project UVs into that trim region.

## Edge Selection Support

You can select edges in edge sub-object mode and click a trim to assign it directly — no need to manually switch to face mode first. Wrapper automatically walks the edge ring to find the full quad strip. Walking stops at non-quad faces so only clean strips are selected, never branching geometry.

## Projection Methods

Wrapper offers two projection methods when applying trims, now found in the **Trim Settings** panel:

| Method | How It Works | Best For |
|--------|-------------|----------|
| **Average Normal** | Projects along the average normal of the selected faces | Flat or gently curved surfaces |
| **Longest Edge** | Aligns projection using the longest edge direction | Elongated strips, consistent alignment |

## Trim Settings Panel

A collapsible **Trim Settings** panel groups all trim processing controls:

| Setting | Description |
|---------|-------------|
| **Mapping Method** | Longest Edge or Average Normal (moved here from the top bar) |
| **Split Angle** | Toggle with adjustable angle threshold (0–180°, default 25°). When enabled, trim strips that bend around corners are automatically split at sharp turns so each segment produces straight, non-skewed UVs |
| **Skip tris and n-gons** | Ignores triangle and n-gon faces when processing quad-based trim operations (moved here from the Options tab) |

## Axis Orientation

Trims can be oriented **horizontally** or **vertically** on the trim sheet. This is defined during the [[Set-Creator|set creation]] process when you choose the Layout Type (Horizontal / Vertical).

## Multi-Group Projection

Select multiple non-contiguous face groups and right-click a projection button to project them all at once. Each group is processed independently with its own UV mapping.

## Element Mode Support

UV tools work in **Face mode (4)**, **Element mode (5)**, and **Edge mode**. Element selections are automatically converted to face selections behind the scenes.

## UV Adjustments

After applying a trim, use the [[UV-Adjustments]] panel to fine-tune positioning with flip, rotate, nudge, scale, and grow/shrink controls. Ctrl+Z undoes any UV adjustment operation. Ctrl+Y re-applies it.

## Automatic Placement

For large meshes where manual trim assignment would be tedious, switch to the Hotspot view. See [[Hotspot]] for details on automatic trim placement.

---

[[Home]] | [[Hotspot]] | [[Quick-Sets|Quick Sets]]
