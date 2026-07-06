# opencode-themes

Custom themes for [OpenCode](https://opencode.ai).

## Themes

### eye-friendly

A soft pink background theme designed to be gentle on the eyes for long coding sessions. Uses warm pink tones (`#ef989b`) for background, with adjusted foreground colors for good contrast on the pink.

### system-snapshot

A JSON snapshot of OpenCode's built-in `opencode` (system) theme, extracted from the binary. Useful as a starting point for customization — copy this file, rename, and modify only the fields you want to change.

## Install

Copy the JSON file(s) to your OpenCode themes directory:

```bash
mkdir -p ~/.config/opencode/themes
cp eye-friendly.json ~/.config/opencode/themes/
```

Then activate in `~/.config/opencode/tui.json`:

```json
{
  "$schema": "https://opencode.ai/tui.json",
  "theme": "eye-friendly"
}
```

Restart OpenCode.

## Notes on colors and Display P3

On MacBook Pro Liquid Retina XDR displays, hex values you input (sRGB) are rendered through macOS ColorSync into Display P3. If you screenshot and pick colors, you'll read the P3 output — which differs from what you configured. Use Digital Color Meter → View → "Display in sRGB" to read the original sRGB value.

To convert a target P3 color `#ef989b` back to sRGB (what you'd write in the theme file):

```python
# P3 #ef989b → sRGB #fd9399
```

## Author

Configuration snippets shared for personal reference. Feel free to fork and adapt.
