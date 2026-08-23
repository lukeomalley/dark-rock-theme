<p align="center"><img src="./images/dark-rock-header-transparent.png"></p>

<p align="center">Deep dark theme with a hint of gruvbox for a /comfy/ experience</p>

<p align="center">
  <a href="https://vscodethemes.com/e/lukeomalley.dark-rock-theme/dark-rock">Preview the VS Code theme</a>
</p>

<div align="center">

[![VS Code Marketplace](https://img.shields.io/badge/VS%20Code%20Marketplace-blue?logo=visualstudiocode&logoColor=white)](https://marketplace.visualstudio.com/items?itemName=lukeomalley.dark-rock-theme)
![Installs](https://img.shields.io/visual-studio-marketplace/i/lukeomalley.dark-rock-theme?label=installs)
![Rating](https://img.shields.io/visual-studio-marketplace/stars/lukeomalley.dark-rock-theme?label=rating)

[![Open VSX](https://img.shields.io/badge/Open%20VSX-purple?logo=eclipse&logoColor=white)](https://open-vsx.org/extension/lukeomalley/dark-rock-theme)
![Downloads](https://img.shields.io/open-vsx/dt/lukeomalley/dark-rock-theme?label=downloads)
![Rating](https://img.shields.io/open-vsx/stars/lukeomalley/dark-rock-theme?label=rating)

</div>

## Variants

| Theme | Background | Description |
|-------|-----------|-------------|
| Dark Rock | `#1a1a20` | The original. Deep dark with warm gruvbox tones. |
| Night Rock | `#08080d` | Even darker with a subtle blue undertone. |
| Light Rock | `#f2e5bc` | Light variant for the daylight hours. |

## VS Code

Install from the [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=lukeomalley.dark-rock-theme) or [Open VSX](https://open-vsx.org/extension/lukeomalley/dark-rock-theme), then select **Dark Rock**, **Night Rock**, or **Light Rock** from the color theme picker.

## Neovim

The three variants are available as Lua colorschemes in `nvim/`.

### Install

Clone this repo and add the `nvim` directory to your runtime path:

```lua
vim.opt.runtimepath:append("/path/to/dark-rock-theme/nvim")
vim.cmd.colorscheme("dark-rock")
```

To use a transparent background, set the option before loading the colorscheme:

```lua
vim.g.dark_rock_transparent = true
vim.cmd.colorscheme("night-rock")
```

You can also change the NvimTree folder color. Palette keys like `fgAlt`, `green`, `aqua`, `blue`, `yellow`, and `purple` work, as do hex colors:

```lua
vim.g.dark_rock_nvim_tree_folder_color = "fgAlt"
vim.cmd.colorscheme("night-rock")
```

Or configure both directly:

```lua
require("dark-rock").setup("night-rock", {
  transparent = true,
  nvim_tree_folder_color = "fgAlt",
})
```

Available colorschemes:

```vim
:colorscheme dark-rock
:colorscheme night-rock
:colorscheme light-rock
```

### Regenerate

Neovim themes are generated from the VS Code theme JSON files:

```bash
npm run generate:nvim
```

## OpenCode

The Night Rock variant is available as a custom theme for [OpenCode](https://opencode.ai).

### Install

```bash
mkdir -p ~/.config/opencode/themes
curl -o ~/.config/opencode/themes/night-rock.json \
  https://raw.githubusercontent.com/lukeomalley/dark-rock-theme/main/.opencode/themes/night-rock.json
```

### Activate

Add `"theme": "night-rock"` to your OpenCode config (`~/.config/opencode/config.json` or `opencode.json`):

```json
{
  "theme": "night-rock"
}
```

Or use the `/theme` command inside OpenCode to select it.

### Color palette

| Role | Color | Hex |
|------|-------|-----|
| Background | ![#08080d](https://placehold.co/16x16/08080d/08080d) | `#08080d` |
| Panel | ![#1a1a20](https://placehold.co/16x16/1a1a20/1a1a20) | `#1a1a20` |
| Text | ![#d4be98](https://placehold.co/16x16/d4be98/d4be98) | `#d4be98` |
| Keywords | ![#ea6962](https://placehold.co/16x16/ea6962/ea6962) | `#ea6962` |
| Operators | ![#e78a4e](https://placehold.co/16x16/e78a4e/e78a4e) | `#e78a4e` |
| Strings | ![#d8a657](https://placehold.co/16x16/d8a657/d8a657) | `#d8a657` |
| Functions | ![#a9b665](https://placehold.co/16x16/a9b665/a9b665) | `#a9b665` |
| Types | ![#7daea3](https://placehold.co/16x16/7daea3/7daea3) | `#7daea3` |
| Numbers | ![#d3869b](https://placehold.co/16x16/d3869b/d3869b) | `#d3869b` |
| Comments | ![#928374](https://placehold.co/16x16/928374/928374) | `#928374` |

## Omarchy

Night Rock is available as a native [Omarchy](https://omarchy.org/) theme. It
styles the Omarchy shell, terminals, tmux, btop, browser accents, supported
editors, and the desktop background from the same Night Rock palette.

Install and activate it with:

```bash
omarchy theme install https://github.com/lukeomalley/omarchy-night-rock-theme.git
```

The canonical source files live in [`omarchy/night-rock`](./omarchy/night-rock).
They are published at the root of the dedicated installable theme repository
because Omarchy clones a theme repository directly into its user theme folder.

## Screenshots

<p align="center"><img src="./images/samples/dark-rock-typescript.png"></p>

<p align="center"><img src="./images/samples/dark-rock-go.png"></p>

<p align="center"><img src="./images/samples/dark-rock-html.png"></p>

<p align="center"><img src="./images/samples/dark-rock-css.png"></p>

<p align="center"><img src="./images/samples/dark-rock-c.png"></p>
