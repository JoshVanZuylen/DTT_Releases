# Set Manager

The Set Manager lets you build and manage your own decal and trim sheet asset libraries. It has two views: a **Set Library** browser for browsing and managing sets, and a **Set Editor** for creating and editing sets.

![Set Manager tab with creation form and step-by-step guide](images/Set-Creator.png)

## Asset Tree Structure

Sets are organized in a three-level hierarchy:

```
Category / Style / Set
```

For example: `Environment / Generic / T_Concrete_hs_a`

Each set lives in its own folder containing JSON metadata, icon previews, and references to the source material.

## Set Library Browser

The library browser shows all your sets as a scrollable icon grid. Use the **Type**, **Category**, and **Style** filter dropdowns to narrow the view. Selecting "All" in the Type filter shows sets from every tool type at once.

- **Grid** dropdown controls how many set cells appear per row (Auto, 1–10) — defaults to 3.
- Set cells scale dynamically with the window size.
- Set icons within each cell are arranged in a compact grid layout (e.g. 2×2 for 4 icons, 3×3 for 9).
- Trim Sheet and Hotspot sets display icons stacked vertically. Vertically-oriented trim sets display icons side by side horizontally.
- Hovering over a set shows a themed colour highlight.
- **Ctrl+click** to select multiple sets at once — selected sets show a white highlight border.

### Set Actions

Clicking a set expands inline action buttons:

| Button | Description |
|--------|-------------|
| **Edit** | Opens the editor with all fields pre-populated |
| **Rename** | Renames the set — folder and JSON filenames update automatically |
| **Export** | Exports the set as a `.zip` file |
| **Delete** | Deletes the set with a confirmation prompt |

When **multiple sets** are selected (Ctrl+click), Edit and Rename are hidden, and Export/Delete are shown side by side.

### Import & Export

| Button | Description |
|--------|-------------|
| **Import Set** | Import one or more `.zip` files — supports batch selection |
| **Export Set** | Export selected set(s) as `.zip` files prefixed with `Wrapper_` |
| **View Set Data Folder** | Opens the DTT_Set_Data folder in Windows Explorer |

Import handles new categories and styles automatically — missing folders are created on the fly. If an imported set already exists, you are asked to confirm before overwriting. After exporting, the folder containing the zip opens automatically with the file highlighted.

**Batch export** (multiple sets selected) opens a single overlay where you can enter an optional prefix. Exported filenames follow the format `{Prefix}_Wrapper_{SetName}.zip`. A live preview shows the exact filename each set will be exported as.

**Batch delete** shows a single confirmation listing all selected sets, then a progress bar overlay tracking deletion (e.g. "1/4").

## Set Editor

Click **Create Set** (full-width button) to open the editor with empty fields for a new set. Click **Edit** on an existing set to pre-populate all fields.

A **Set List** button at the top of the editor returns you to the browser. The mode header reads **"Creating New Set"** or **"Updating Existing Set"** so you always know which mode you're in.

### Editor Fields

| Field | Description |
|-------|-------------|
| **Tool** | What the set is for — *Trim Sheet and Hotspot* or *Mesh Decal* |
| **Category** | Top-level group (e.g. Environment, Characters) |
| **Style** | Sub-group within the category |
| **Set** | The set name — type a new name to create, or select an existing set to update |
| **Layout Type** | **Horizontal (U Direction)** or **Vertical (V Direction)** — how trims are oriented on the texture |
| **Material ID** | Shift, Ctrl, and Alt material IDs used by the set |
| **Texture Name** | Optional override for the texture filename |
| **Material Name** | Auto-detected from your scene material, or manually entered |
| **Tags** | Comma-separated keywords for [[Material-Matching|material matching]] and search |
| **Texture Direction** | Arrow buttons to set the texture flow direction |
| **Inset Default** | Default hotspot inset value in pixels (px) — automatically applied when this set is loaded |
| **Render Style** | How icons are rendered |

**Auto-detection:** After typing a new set name and pausing for 2 seconds, Wrapper automatically searches the scene for a matching material and pre-fills the Material Name and Texture Name fields. Switching category/style or changing the set name clears these fields to prevent stale data carrying over.

Click **Create Trim Sheet and Hotspot Data** (or the equivalent for Mesh Decals) to generate the set.

### Changing Tool Type

Switching to a different tool type preserves your category, style, and set selections if they still exist in the new type — only selections that no longer apply are cleared.

## Icon Rendering

The **Render Style** dropdown controls how set preview icons are generated. Icons are saved as JPG by default for smaller file sizes; sets with opacity or transparency maps use PNG to preserve alpha.

| Render Style | Requirements | Description |
|-------------|-------------|-------------|
| **Render Material Previews** | PBR material with 2+ texture maps | Renders icons using the Quicksilver hardware renderer with full PBR lighting, ambient occlusion, and shadows. Falls back to single-texture rendering if only one map is assigned. |
| **Render Texture Previews** | At least one texture map | Samples icons directly from the source texture. Fast and lightweight. |
| **ISO Icon** | Displacement/height map (required), Mesh Decal type only | Renders each decal at a 45-degree isometric angle with displacement applied. Supports **Height Map Center** (0.0–1.0, default 0.5) and **Disp Strength** (default 8.0 cm) controls for fine-tuning displacement. |

## Set Creation Guide

The Set Manager tab includes a built-in step-by-step guide that walks through the full creation process. The guide updates dynamically based on whether you're creating a Trim Sheet or Mesh Decal set.

## Mesh Generator

Click **Generate MeshDecal Source Mesh** on the Set Manager tab to open the Mesh Generator overlay.

![Mesh Generator canvas with detected bounding boxes](images/MeshGenerator.png)

### Material Selection

| Field | Description |
|-------|-------------|
| **Multi/Sub Material** | Select the Multi/Sub-Object material from your scene. Individual (non-Multi/Sub) materials are also listed and can be used to preview textures. |
| **Material ID** | Choose which sub-material slot to use for detection |

A **brightness slider** next to the texture info label lets you darken or brighten the preview — double-click to reset.

### Trim Sheet / Hotspot Mode

For Trim Sheet and Hotspot set types, the Mesh Generator uses a **line-based editor** instead of bounding boxes:

- **Primary-axis lines** define trim rows.
- **Secondary-axis lines** define column boundaries within rows (Hotspot only).
- Boundary lines at texture edges are created automatically and cannot be deleted.

**Line interaction controls:**

| Action | Control |
|--------|---------|
| Place a new line | Click on empty space |
| Reposition a line | Drag existing line |
| Delete a line or segment | Ctrl+click |
| Place a secondary line (partial span) | Ctrl+Shift+click |
| Split secondary line into segments | Double-click |
| Unsplit back to full-span | Double-click a split line |

Lines cannot cross adjacent lines during drag. Opening an existing set reconstructs the line layout from saved data.

### Mesh Decal / Strip Decal Mode

The canvas displays your texture with detected decal regions shown as numbered bounding boxes.

- **Click and drag** to draw new bounding boxes
- **Click a box** to select it
- **Drag a selected box** to move it
- **Drag the edges** of a selected box to resize it
- **Delete key** to remove a selected box
- **Mouse wheel** to zoom the canvas

#### Detection Settings

| Setting | Description |
|---------|-------------|
| **Min Edge Size** | Minimum size in pixels for detected regions — filters out noise |
| **Threshold** | Sensitivity for shape detection — lower values detect more shapes |
| **Box Padding** | Percentage of padding added around each detected shape |
| **Detect Channel** | Which texture channel to analyze — **Alpha** for opacity-based detection |
| **Image Scale** | Scale factor for the detection pass (e.g. x4) — higher values are more precise but slower |

#### Detection Options

| Option | Description |
|--------|-------------|
| **No Overlap** | Automatically resolves overlapping bounding boxes |
| **Group Touching** | Groups adjacent detected regions into single bounding boxes |

### Actions

| Button | Description |
|--------|-------------|
| **Detect Islands** | Run auto-detection on the texture to find decal shapes |
| **Delete Selected** | Remove selected bounding boxes |
| **Clear All** | Remove all bounding boxes |
| **Create Mesh** | Generate mesh geometry from the bounding boxes |
| **Create Mesh Decal Set Data** | Generate meshes and create/update the set data in one step |

## "All" Category Filter

A special "All" category displays sets from all teams and styles at once, letting you browse your entire library without changing filters.

---

[[Home]] | [[Material-Matching|Material Matching]] | [[Quick-Sets|Quick Sets]]
