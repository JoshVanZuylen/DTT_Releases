# FAQ & Troubleshooting

## Installation

### "Tool cannot be found" when launching PolyWrapper

Rerun the `PolyWrapper_MacroInstaller.ms` from your current release folder by dragging it into the Max viewport. This refreshes the stored path in Max's settings.

### Where should I put the install folder?

Anywhere stable on your machine — for example, `G:\Tools\PolyWrapper`. Do **not** place it inside Max's `scripts\startup` directory.

## Licensing

### Can I use my license on multiple Max versions?

Yes. Your license automatically transfers between Max versions on the **same PC**. You don't need to deactivate and reactivate when switching between Max 2024, 2025, and 2026 on the same machine.

### My license shows as activated on another machine

Deactivate the license on the other machine first via the About tab. If you no longer have access to that machine, you can force-activate the license on your new PC — this automatically releases the previous activation.

### Activation fails at my studio

Some corporate firewalls block the license verification request. PolyWrapper has a fallback network method — if the initial attempt fails, it automatically retries with an alternative approach. If problems persist, check with your IT team about outbound HTTPS connections.

## Hotspot

### Hotspot is taking a long time

Hotspot operates only on your **selected faces**, not the entire mesh. For better performance:
- Select only the faces you need processed
- Large selections on high-poly meshes take longer
- A 5-minute safety timeout automatically stops processing if it runs too long

### Hotspot results look wrong

Check your settings:
- **Texel Res** should match your texture resolution goals
- **Angle Threshold** controls how faces are grouped — lower values create more, smaller groups
- **Inset** prevents texture bleeding at UV edges — try 0 if trims look cut off

Hotspot is a complex tool and we're always working to improve it. If you have feedback or run into issues, please visit the [Discord](https://discord.gg/4Ds4asQ94X).

## Mesh Decals

### Auto-Conform is not available

The Conform modifier requires **3ds Max 2024.2** or later. On older 2024 builds, Auto-Conform is automatically disabled. Decals still place correctly as flat quads — they just won't wrap around curved surfaces.

### Decals are too large/small when placed

Adjust the **Scale** spinner before placing, or use **Ctrl + drag** during placement to scale interactively. The scale spinner accepts values down to 0.001 for micro-detail work.

## Quick Sets & Multi-Set Mode

### Shift+click isn't adding sets

Make sure you're holding Shift before clicking the Quick Set button. A normal click loads a single set exclusively, while Shift+click adds or removes sets from the multi-set view.

### Material IDs aren't displaying in multi-set mode

Make sure material assignments have been evaluated in the Material Assignment panel. Load the set normally first to trigger material matching.

## Updates

### How do I manually update?

Download the latest release from the [Releases page](https://github.com/JoshVanZuylen/DTT_Releases/releases), extract it, and drag `PolyWrapper_MacroInstaller.ms` into the Max viewport.

### Auto-update keeps reverting my version

If you intentionally installed an older version, auto-update should have disabled itself automatically (downgrade protection). If it didn't, toggle auto-update off in the About tab settings.

### I can't update to the latest version

Check your [maintenance window](licensing.md). If your maintenance has expired, you can't update to releases published after your window ended. Purchase a Maintenance key to extend your eligibility.

## General

### Where can I get help?

Join the [PolyWrapper Discord](https://discord.gg/4Ds4asQ94X) for community support and bug reports.

---

[Back to Home](../README.md)
