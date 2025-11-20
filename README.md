# bauxwm – the GUI rice that speaks BAUX

`bauxwm` is the optional X11 layer for **RoxieOS** and **BAUX**.  
Install this single `.deb` on any Debian-based system (Raspberry Pi 4/5, laptop, VM) and `startx` instantly drops you into a perfectly themed, minimal, keyboard-driven cyberdeck desktop that feels like a natural extension of your BAUX console workflow.

No bloat. No mouse required. Everything flows.

### Key Features

- **dwm-roxanne** – heavily patched suckless `dwm` with:
  - `Option + hjkl` → tag navigation (exactly one layer above tmux’s `Alt + hjkl` panes)
  - Pink/black “Roxanne” Catppuccin-Mocha theme (matches BAUX truecolor status bar)
  - Single-key shortcuts for Alacritty, volume, brightness, screenshots, etc.
- **Alacritty-roxanne** – pre-configured terminal with perfect font rendering, ligatures, and the exact same colors as your BAUX tmux sessions
- **picom** – subtle shadows + transparency so floating BAUX windows look like they belong
- **status.sh** – DWM status bar that pulls live info from your running BAUX session (hostname badge, current path, SSH status, bot indicator when we add it)
- **xinitrc** – `startx` → straight into the rice, no display manager required
- Full keyboard layout consistency (`/etc/default/keyboard`) so `Alt`, `Option`, and `Ctrl` behave exactly the same on console and X

### The Flow Ladder (Zero Context Switch)

| Layer       | Movement Keys       | Action
|-------------|---------------------|----------------------------------------
| Neovim      | `hjkl`              | cursor
| tmux        | `Alt + hjkl`        | panes
| dwm         | `Option + hjkl`     | tags / virtual desktops
| Global      | `Ctrl + …`          | universal prefix (tmux, system, etc.)

You never have to think about “which layer am I in?” again.

### Installation (30 seconds)

```bash
# On any Debian / Raspberry Pi OS / RoxieOS system
wget https://github.com/badlandz/bauxwm/releases/download/v0.1.0/bauxwm_0.1.0_arm64.deb
sudo apt install ./bauxwm_0.1.0_arm64.deb

# Then just
startx
