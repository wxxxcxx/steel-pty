# Installation

Build Helix with steel (this also installs the `forge` package manager):

```sh
git clone https://github.com/mattwparas/helix.git
git checkout steel-event-system
cargo xtask steel
```

Install the plugin:

```sh
forge pkg install --git https://github.com/wxxxcxx/steel-pty
```

Load the plugin by adding the following line to `~/.config/helix/init.scm`:

```
(require "steel-pty/term.scm")
```

# Usage

This fork renders the terminal as a bottom panel and adds terminal workspace
controls. Bind the exported functions in your Helix configuration as needed.

- `open-term`: open or focus the terminal panel
- `new-term`: create and focus a new terminal
- `switch-term`: focus the next terminal
- `switch-term-previous`: focus the previous terminal
- `toggle-terminal-fullscreen`: toggle between the bottom panel and fullscreen
- `hide-terminal`: hide the terminal panel
- `kill-active-terminal`: kill the active terminal

When the terminal is focused, the following keys are handled directly:

- `Ctrl-Backtick`: hide the terminal panel
- `Ctrl-Shift-Backtick`: create a terminal
- `Ctrl-Enter`: toggle fullscreen
- `Ctrl-PageUp` / `Ctrl-PageDown`: switch terminals
- `Ctrl-Escape`: return focus to the editor while keeping the panel visible
