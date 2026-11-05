# Modern Gruvbox

A dark theme for [Zed](https://zed.dev), combining neutral Monokai Soft surfaces with defined Gruvbox-inspired syntax colors and warm red accents.

## Design

- Neutral dark editor background (`#1e1e1e`) and subdued panels.
- Warm red accents (`#e87868`) for focus borders, accent text, and icons.
- Distinct syntax colors with moderate saturation and no washed-out pastel effect.
- Complete UI, integrated terminal, Git status, diagnostic, and collaboration colors.

| Syntax element | Color |
| --- | --- |
| Keywords and tags | Red `#e87868` |
| Functions | Yellow `#e3bc62` |
| Strings | Green `#b1c45f` |
| Types, constructors, namespaces | Blue `#79afbf` |
| Properties and attributes | Aqua `#83bc98` |
| Operators and escape sequences | Orange `#e9a35d` |
| Numbers, booleans, constants | Purple `#c58bb5` |
| Variables and parameters | Cream `#e5dac3` |

Actual highlighting depends on each language grammar and semantic tokens.

## Install locally

This extension is not yet published to the Zed extension store.

1. Open the command palette in Zed.
2. Run `zed: install dev extension`.
3. Select this repository's root directory.
4. Run `theme selector: toggle` and select **Modern Gruvbox**.

Alternatively, copy `themes/modern-gruvbox.json` to `~/.config/zed/themes/` on Linux and select **Modern Gruvbox**.

## Customize

Edit `themes/modern-gruvbox.json`. This is the complete, standalone theme; Nix is not required. Reload the development extension after making changes.

The initial release preserves the approved Monokai Soft UI and terminal palette, replacing syntax colors and adding red UI accents. It was exported from a personal Nix configuration; this repository can now evolve independently.

## Publish

See [PUBLISHING.md](PUBLISHING.md) for the GitHub and Zed registry steps.

## Credits

Created by Fabiano Lima. The syntax palette is inspired by Gruvbox, with custom colors and a Monokai Soft-derived interface.

## License

[MIT](LICENSE)
