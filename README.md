A DXML script mod for STALKER Anomaly (Open X-Ray) to inject alignment and layout attributes into user interface files as they are loaded by the engine.

> [!NOTE]
> This mod is in *active development* and should be considered *work in progress* but safe to use.
> It can be installed in your game in its current version, an official ModDB release is pending.
> This warning will be removed once the mod has been tested and is considered fully playable.

## Approach

This mod effectively fixes *vertical alignment of text labels* by using the engine's complex text mode (`complex_mode` attribute) and vertical alignment setting (`vert_align="c"` attribute) and applying them to all elements in user interface files by a set of match patterns. Additionally, the mod allows doing *arbitrary adjustments to any UI element* to patch any remaining misalignments and positioning issues, and to revert any changes made by the automatic patching module. A number of fixes to misaligned elements are included.

Using complex mode for text may reduce performance on low-end systems but this has not been observed during testing. It may be that at the time of the game's original release around 2007, the impact of complex mode was more significant but has become negligible with modern hardware. A side effect of enabling the engine's vertical alignment over manual or computed vertical offsets is that all labels will be correctly aligned across all resolutions and aspect ratios.

In its default configuration, the mod also overhauls the *layout of the item details panel* to make it more compact. Item weight is moved from left below the name to the top right corner next to the name, unused space is significantly trimmed, indentation of graphical elements is made consistent, the bullet points for stats are slightly reduced in size and given some padding, and dual-column layouts are moved closer together and given the same insets.

The mod uses DXML to patch user interface files as they are loaded by the game and is compatible with all mods and mod packs, even ones that modify the game's UI XML files or add entirely new interfaces.

## Features

The mod provides the following core features:

- Automatically patch vertical alignment of text labels (highly configurable)
- Allow defining element attribute patching for arbitrary user interface elements

With its *default configuration*, the mod also does the following:

- Fix misalignment of magnifying glass effect in main menu (`shniaga_wnd`)
- Fix text to button misalignment in options and MCM menus
- Update layout of item details panel (weight, cost, description, stats box, ammo, crafting)
- Fix misalignment of player money label in inventory
- Fix misalignment of time, captions, and messages in PDA message notifications

## License

This mod was created by Saint for free use by the STALKER modding community with basic attribution under the MIT license. This mod may be distributed with mod packs. DXML was created by Demonized (https://github.com/themrdemonized).