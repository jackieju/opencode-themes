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

## License

Copyright (C) 2026 Jackie Ju

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.
