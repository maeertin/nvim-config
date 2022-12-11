# Install and setup

### Patched Fonts
Since statusline or file explorer plugins often use Unicode symbols not available in normal font,
we need to install a patched font from the [nerd-fonts](https://github.com/ryanoasis/nerd-fonts) project.

### Ripgrep
[Ripgrep](https://github.com/BurntSushi/ripgrep), aka, `rg`, is a fast grepping tool available for both Linux, Windows and macOS. It is used by several searching plugins. Install on macOS via homebrew.

```bash
brew install ripgrep
```

### Nvim
Install on macOS via homebrew.

```bash
brew install neovim
```

### Setting up Nvim

On Linux and macOS, the desination directory for the config is `~/.config/nvim`. On Windows, the config directory is `$HOME/AppData/Local/nvim`[^1].
First, we need to remove all the files under the config directory (including dot files), then go to this directory, and run the following command:

```
git clone --depth=1 git@github.com:maeertin/nvim-config.git .
```

After that, when we first open nvim, run command `:PackerSync` to install all the plugins. Use `:Mason` to install LSP related plugins like linters and formatters.
