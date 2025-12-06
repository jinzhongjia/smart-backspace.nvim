<h1 align="center">✨ Smart Backspace for Neovim ✨</h1>

<p align="center">Neovim plugin to save time removing indentation written in lua. Inspired by the JetBrains IDE <a href="https://www.jetbrains.com/idea/">IntelliJ</a>'s backspace functionality.</p>

## 🚀 Demo

https://github.com/user-attachments/assets/395f18ee-1346-4ac2-8b5c-79597cffe995

## 📦 Installation

### 📋 Requirements

- Neovim 0.8.0 or higher

> [!WARNING]
> If using with [nvim-autopairs](https://github.com/windwp/nvim-autopairs), in `opts`, ensure that `map_bs = false`.

### For 💤 [lazy.nvim](https://lazy.folke.io) users:

```lua
{
    "qwavies/smart-backspace.nvim"
}
```

### For 📦 [packer.nvim](https://github.com/wbthomason/packer.nvim) users:

```lua
use {
    "qwavies/smart-backspace.nvim"
}
```

### For 🔌 [vim-plug](https://github.com/junegunn/vim-plug) users:

```vim
Plug "qwavies/smart-backspace.nvim"
```

## ⚙  Configuration

### 💤 Lazy Loading

If you want to lazy load Smart Backspace, you could set a event condition.
For example, if you use [lazy.nvim](https://lazy.folke.io):

```lua
{
    "qwavies/smart-backspace.nvim",
    event = {"InsertEnter", "CmdlineEnter"}
}
```

### 🧩 Default configuration

Using [lazy.nvim](https://lazy.folke.io):

```lua
{
    "qwavies/smart-backspace.nvim",
    opts = {
        enabled = true, -- enables/disables smart-backspace
        silent = true, -- if set to false, it will send a notification if smart-backspace is toggled
        disabled_filetypes = { -- filetypes to automatically disable smart-backspace
            "py",
            "hs",
            "md",
            "txt",
        }
    }
}
```

### ⚡ Toggling smart-backspace

Using the `:SmartBackspaceToggle` command, smart-backspace can be toggled on/off.

If you want to set a keybind to toggle smart-backspace, you can implement the following into your neovim config:

```lua
vim.keymap.set("n", "<leader>bs", "<cmd>SmartBackspaceToggle<CR>", { desc = "Toggle Smart Backspace" })
```

## 👨‍💻 Planned Changes/Additions

- [x] A `:SmartBackspaceToggle` command
- [ ] True compatibility with [nvim-autopairs](https://github.com/windwp/nvim-autopairs), or act as an alternative
  - [x] Delete pairs of brackets like [nvim-autopairs](https://github.com/windwp/nvim-autopairs)
  - [ ] Remove the need to set `map_bs = false`
- [x] Using `<C-BS>` to use as a regular backspace
- [x] User configuration for more flexibility (feel free to recommend me more configuration changes!)

## 🥇 Load times

Smart-Backspace prides itself in its almost instant load times.

Compare load times against some other plugins!

<img width="3839" height="2072" alt="image" src="https://github.com/user-attachments/assets/1be85339-88c0-4305-b0a0-fd54f295b7ac" />
