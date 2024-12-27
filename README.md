######
<div align = center><img src="https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/hyprdots_banner.png"><br><br>
</div>

## Short video previews - version v3
[<img src="https://img.youtube.com/vi/JZlDUaCWGBI/maxresdefault.jpg">](https://youtu.be/JZlDUaCWGBI)
![setup_v3](https://github.com/user-attachments/assets/e2dea41e-fa46-41b7-a6e1-3fde068cb09a)
![setup_new2](https://github.com/user-attachments/assets/6ec89a21-435c-4e68-ae9f-8f6b8543b236)


## Version v1
[<img src="https://img.youtube.com/vi/N7HTsyyBR3Q/maxresdefault.jpg">](https://youtu.be/N7HTsyyBR3Q)
[<img src="https://img.youtube.com/vi/lvzLesF9u_o/maxresdefault.jpg">](https://youtu.be/lvzLesF9u_o)

## Version v2
![240825_12h51m23s_screenshot](https://github.com/user-attachments/assets/8318b1d3-75f1-4423-b1e7-d11621b17c96)
![240823_22h14m38s_screenshot](https://github.com/user-attachments/assets/cb6858c2-a0a0-402c-8974-08f931ea9011)

Note : You need to manually set soft links for nwg-dock and nwg-drawer css in the config folder for light/dark themes. And some env variables, preferences are set as per personal needs so modify accordingly.

## Installation

This configuration is based on the original repo from which it is forked, but contains some personal configurations and tweaks made by me like : 

- Bug fixes for Aylur GTK shell, ensuring smooth quick settings.
- A custom dock (nwg) crafted with CSS, offering both light and dark theme support.
- A custom app drawer (nwg) also styled with CSS.
- Performance optimization flags for NVIDIA Optimus users.
- Custom wallpapers added for Catppuccin themes
- Compatibility fixes for older Xwayland applications.
- DIY wallpapers and thematic tweaks.
- Tearing fixes for Electron-based applications.
- An automated screen magnification algorithm (since Hyprland doesn't offer this natively).
- A preconfigured Fish shell with theming support (both native and using Starship) and auto-completions.
- Convenient preconfigured touchpad gestures using dotool daemon and hyprland CLI utility.

And more...


The installation script is made for Arch, but **may** work on some Arch based distros with **systemd**. (Tested on Garuda Linux)

> [!IMPORTANT]
> Install script will auto-detect nvidia card and install nvidia-dkms drivers for your kernel.
> So please ensure that your Nvidia card supports [dkms](https://wiki.archlinux.org/title/NVIDIA) drivers and hyprland.

> [!CAUTION]
> The script modifies your grub config to enable Nvidia drm and theme.
> NOTE : Don't forget to remove VS Code login for sync, as this resets vscode configuration. After installation, login and sync with your remote data again.

After minimal Arch install (with grub and systemd), clone and execute -

```shell
pacman -Sy git
git clone --depth 1 https://github.com/yashlakhtariya/ysl-hyprdots ~/Hyprdots
cd ~/Hyprdots/Scripts
./install.sh
```

> [!TIP]
> You can also create your own list (for ex. `custom_apps.lst`) with all your favorite apps and pass the file as a parameter to install it -
>```shell
>./install.sh custom_apps.lst
>```

Please reboot after the install script completes and takes you to sddm login screen (or black screen) for the first time.
For more details, please refer [installation wiki](https://github.com/prasanthrangan/hyprdots/wiki/Installation)

## Themes

Modified by YSL : Catppuccin Latte, Catppuccin Mocha (rest same) 

To create your own custom theme, please refer [theming wiki](https://github.com/prasanthrangan/hyprdots/wiki/Theming)

> [!TIP]
> You can install/browse/create/maintain/share additional themes (ex. [Synth-Wave](https://github.com/prasanthrangan/hyprdots-mod)) using themepatcher.
> For more details please refer [themepatcher wiki](https://github.com/prasanthrangan/hyprdots/wiki/Theming#theme-patcher).
> For more details please refer [themepatcher wiki](https://github.com/prasanthrangan/hyprdots/wiki/Theming#theme-patcher).

<br><div align="center"><table><tr><td><img width="60" src="https://raw.githubusercontent.com/prasanthrangan/hyprdots/main/Source/assets/hyprdots_logo.png"></td><td>

</td></table>

## Packages

<table><tr><td>
<code>n</code><br><code>v</code><br><code>i</code><br><code>d</code><br><code>i</code><br><code>a</code></td><td><table>
    <tr><td>linux-headers</td><td>for main kernel (script will auto detect from /usr/lib/modules/)</td></tr>
    <tr><td>linux-zen-headers</td><td>for zen kernel (script will auto detect from /usr/lib/modules/)</td></tr>
    <tr><td>linux-lts-headers</td><td>for lts kernel (script will auto detect from /usr/lib/modules/)</td></tr>
    <tr><td>nvidia-dkms</td><td>nvidia drivers (script will auto detect from lspci -k | grep -A 2 -E "(VGA|3D)")</td></tr>
    <tr><td>nvidia-utils</td><td>nvidia utils (script will auto detect from lspci -k | grep -A 2 -E "(VGA|3D)")</td></tr></table>
</td></tr></table>

<table><tr><td>
<code>u</code><br><code>t</code><br><code>i</code><br><code>l</code><br><code>s</code></td><td><table>
    <tr><td>pipewire</td><td>audio and video server</td></tr>
    <tr><td>pipewire-alsa</td><td>for audio</td></tr>
    <tr><td>pipewire-audio</td><td>for audio</td></tr>
    <tr><td>pipewire-jack</td><td>for audio</td></tr>
    <tr><td>pipewire-pulse</td><td>for audio</td></tr>
    <tr><td>gst-plugin-pipewire</td><td>for audio</td></tr>
    <tr><td>wireplumber</td><td>audio and video server</td></tr>
    <tr><td>networkmanager</td><td>network manager</td></tr>
    <tr><td>network-manager-applet</td><td>nm tray</td></tr>
    <tr><td>bluez</td><td>for bluetooth</td></tr>
    <tr><td>bluez-utils</td><td>for bluetooth</td></tr>
    <tr><td>blueman</td><td>bt tray</td></tr></table>
</td></tr></table>

<table><tr><td>
<code>l</code><br><code>o</code><br><code>g</code><br><code>i</code><br><code>n</code></td><td><table>
    <tr><td>sddm-git</td><td>display manager for login</td></tr>
    <tr><td>qt5-wayland</td><td>for QT wayland XDP</td></tr>
    <tr><td>qt6-wayland</td><td>for QT wayland XDP</td></tr>
    <tr><td>qt5-quickcontrols</td><td>for sddm theme</td></tr>
    <tr><td>qt5-quickcontrols2</td><td>for sddm theme</td></tr>
    <tr><td>qt5-graphicaleffects</td><td>for sddm theme</td></tr></table>
</td></tr></table>

<table><tr><td>
<code>h</code><br><code>y</code><br><code>p</code><br><code>r</code></td><td><table>
    <tr><td>hyprland-git</td><td>main window manager (hyprland-nvidia-git if nvidia card is detected)</td></tr>
    <tr><td>dunst</td><td>graphical notification daemon</td></tr>
    <tr><td>rofi-lbonn-wayland-git</td><td>app launcher</td></tr>
    <tr><td>waybar-hyprland-git</td><td>status bar</td></tr>
    <tr><td>swww</td><td>wallpaper app</td></tr>
    <tr><td>swaylock-effects-git</td><td>lockscreen</td></tr>
    <tr><td>wlogout</td><td>logout screen</td></tr>
    <tr><td>grimblast-git</td><td>screenshot tool</td></tr>
    <tr><td>slurp</td><td>selects region for screenshot/screenshare</td></tr>
    <tr><td>swappy</td><td>screenshot editor</td></tr>
    <tr><td>cliphist</td><td>clipboard manager</td></tr></table>
</td></tr></table>

<table><tr><td>
<code>d</code><br><code>e</code><br><code>p</code><br><code>e</code><br><code>n</code><br><code>d</code><br><code>e</code><br><code>n</code><br><code>c</code><br><code>y</code></td><td><table>
    <tr><td>polkit-kde-agent</td><td>authentication agent</td></tr>
    <tr><td>xdg-desktop-portal-hyprland</td><td>XDG Desktop Portal</td></tr>
    <tr><td>pacman-contrib</td><td>for system update check</td></tr>
    <tr><td>python-pyamdgpuinfo</td><td>for amd gpu info</td></tr>
    <tr><td>parallel</td><td>for parallel processing</td></tr>
    <tr><td>jq</td><td>to read json</td></tr>
    <tr><td>imagemagick</td><td>for image processing</td></tr>
    <tr><td>qt5-imageformats</td><td>for dolphin image thumbnails</td></tr>
    <tr><td>ffmpegthumbs</td><td>for dolphin video thumbnails</td></tr>
    <tr><td>kde-cli-tools</td><td>for dolphin open with option</td></tr>
    <tr><td>brightnessctl</td><td>brightness control for laptop</td></tr>
    <tr><td>pavucontrol</td><td>audio settings gui</td></tr>
    <tr><td>pamixer</td><td>for waybar audio</td></tr></table>
</td></tr></table>

<table><tr><td>
<code>t</code><br><code>h</code><br><code>e</code><br><code>m</code><br><code>e</code></td><td><table>
    <tr><td>nwg-look</td><td>theming GTK apps</td></tr>
    <tr><td>kvantum</td><td>theming QT apps</td></tr>
    <tr><td>qt5ct</td><td>theming QT5 apps</td></tr></table>
</td></tr></table>

<table><tr><td>
<code>a</code><br><code>p</code><br><code>p</code><br><code>s</code></td><td><table>
    <tr><td>firefox</td><td>browser</td></tr>
    <tr><td>kitty</td><td>terminal</td></tr>
    <tr><td>neofetch</td><td>fetch tool</td></tr>
    <tr><td>dolphin</td><td>kde file manager</td></tr>
    <tr><td>visual-studio-code-bin</td><td>gui code editor</td></tr>
    <tr><td>vim</td><td>text editor</td></tr>
    <tr><td>ark</td><td>kde file archiver</td></tr></table>
</td></tr></table>

<table><tr><td>
    <code>s</code><br><code>h</code><br><code>e</code><br><code>l</code><br><code>l</code></td><td><table>
    <tr><td>zsh</td><td>main shell</td></tr>
    <tr><td>eza</td><td>colorful file lister</td></tr>
    <tr><td>oh-my-zsh-git</td><td>for zsh plugins</td></tr>
    <tr><td>zsh-theme-powerlevel10k-git</td><td>theme for zsh</td></tr>
    <tr><td>pokemon-colorscripts-git</td><td>display pokemon sprites</td></tr></table>
</td></tr></table>

## Keybindings

| Keys | Action |
| :--  | :-- |
| <kbd>Super</kbd> + <kbd>Q</kbd> | quit active/focused window
| <kbd>Super</kbd> + <kbd>Del</kbd> | quit hyprland session
| <kbd>Super</kbd> + <kbd>W</kbd> | toggle window on focus to float
| <kbd>Super</kbd> + <kbd>Enter</kbd> | toggle window on focus to fullscreen
| <kbd>Super</kbd> + <kbd>G</kbd> | toggle window group
| <kbd>Super</kbd> + <kbd>X</kbd> | launch kitty terminal
| <kbd>Super</kbd> + <kbd>E</kbd> | launch dolphin file explorer
| <kbd>Super</kbd> + <kbd>C</kbd> | launch vscode
| <kbd>Super</kbd> + <kbd>Space</kbd> | launch browser (default profile) (set manually in keybindings.conf)
| <kbd>Super</kbd> + <kbd>/</kbd> | launch browser (tmp profile) (set manually in keybindings.conf)
| <kbd>Super</kbd> + <kbd>A</kbd> | launch desktop applications (rofi)
| <kbd>Super</kbd> + <kbd>Tab</kbd> | switch open applications (rofi)
| <kbd>Super</kbd> + <kbd>R</kbd> | browse system files (rofi)
| <kbd>Super</kbd> + <kbd>F10</kbd> | mute audio output (toggle)
| <kbd>Super</kbd> + <kbd>F11</kbd> | decrease volume (hold)
| <kbd>Super</kbd> + <kbd>F12</kbd> | increase volume (hold)
| <kbd>Super</kbd> + <kbd>V</kbd> | clipboard history paste
| <kbd>Super</kbd> + <kbd>L</kbd> | lock screen
| <kbd>Super</kbd> + <kbd>Backspace</kbd> | logout menu
| <kbd>Super</kbd> + <kbd>K</kbd> | transparency and blur ON for all windows
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>K</kbd> | transparency and blur OFF for all windows
| <kbd>Super</kbd> + <kbd>P</kbd> | drag to select area or click on a window to print
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>P</kbd> | print current screen
| <kbd>Super</kbd> + <kbd>RightClick</kbd> | resize the window
| <kbd>Super</kbd> + <kbd>LeftClick</kbd> | change the window position
| <kbd>Super</kbd> + <kbd>MouseScroll</kbd> | cycle through workspaces
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>←</kbd><kbd>→</kbd><kbd>↑</kbd><kbd>↓</kbd>| resize windows (hold)
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>Ctrl</kbd> + <kbd>←</kbd><kbd>→</kbd><kbd>↑</kbd><kbd>↓</kbd>| move active window within the current workspace
| <kbd>Super</kbd> + <kbd>[0-9]</kbd> | switch to workspace [0-9]
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>[0-9]</kbd> | move active window to workspace [0-9]
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>[0-9]</kbd> | move active window to workspace [0-9] (silently)
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>S</kbd> | move window to special workspace
| <kbd>Super</kbd> + <kbd>S</kbd> | toogle to special workspace
| <kbd>Super</kbd> + <kbd>Alt</kbd> + <kbd>G</kbd> | disable hypr effects for gamemode
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>D</kbd> | toggle (theme <//> wall) based colors
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>T</kbd> | theme select menu
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>W</kbd> | wallpaper select menu
| <kbd>Super</kbd> + <kbd>Shift</kbd> + <kbd>A</kbd> | rofi style select menu

</td></tr></table>

**For queries/feedback contact me : yashlakhtariya1010@outlook.com**
