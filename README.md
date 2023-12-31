<h1 align="center">Nekifoch</h1>
<h3 align="center">Neovim Kitty Font Changer</h3>
<hr>

<p align="center">
  <strong>Neovim plugin for managing Kitty terminal font settings.</strong>
</p>

<p align="center">
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#configuration">Configuration</a> •
  <a href="#credits">Credits</a> •
  <a href="#license">License</a> •
  <a href="#donations">Donations</a>
</p>

---

https://github.com/RAprogramm/nekifoch/assets/70325462/04a0d7e7-a42e-4588-a926-0945adacb3f0

## Installation

Install Nekifoch using your favorite plugin manager. For example, with [lazy.nvim](https://github.com/folke/lazy.nvim):

```lua
{
    'RAprogramm/nekifoch',
    cmd = 'Nekifoch',
    opts = {}
}
```

## Usage

Nekifoch provides the `:Nekifoch` command with the following syntax:

```vim
:Nekifoch [action] [font_family]
```

- `[action]` can be one of:
  - `check`,
  - `set_font`,
  - `set_size`,
  - `list`.
- `[font_family]`: New font family for the `set_font` action.

Examples:

- Check the current font family and size:

```vim
:Nekifoch check
```

- Replace the font family with "DejaVu Sans Mono":

```vim
:Nekifoch set_font DejaVu Sans Mono
```

- Replace the font size with "14":

```vim
:Nekifoch set_size 14
```

- List available fonts compatible with Kitty:

```vim
:Nekifoch list
```

## Configuration

Configure Nekifoch using the FontReplaceConfig dictionary:

Nekifoch can be configured by adding a Lua configuration to your Neovim configuration file (init.lua).

Here's an example configuration using Lua:

```lua
require('nekifoch').setup({
  kitty_conf_path = vim.fn.expand('~/.config/kitty/kitty.conf')
})
```

or

```lua
{
    'RAprogramm/nekifoch',
    opts = {
        kitty_conf_path = vim.fn.expand('~/.config/kitty/kitty.conf')
    }
}
```

Replace '~/.config/kitty/kitty.conf' with the actual path to your Kitty terminal configuration.

## Credits

Developed by RAprogramm. Contributions are welcome.

## License

Distributed under the ... (not chosen yet).

For in-depth details and usage instructions, refer to the documentation.

<hr>

Enhance your Kitty terminal experience with Nekifoch

## Donations

If you find this plugin helpful and would like to support its development, you can buy me a coffee through the following platforms:

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/rozanov)

[![buymeacoffee](https://img.buymeacoffee.com/button-api/?username=YOUR_BMC_USERNAME&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000)](https://www.buymeacoffee.com/raprogramm)

Your support is greatly appreciated!
