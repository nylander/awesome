# Settings for the awesome windows manager

- Last modified: fre jan 29, 2021  01:23
- Sign: JN

## Description

Some notes about my settings of the  [awesome window manager](https://awesomewm.org/).

## Installation

    sudo apt install awesome awesome-extra
    cd ~/.config
    git clone https://github.com/nylander/awesome.git
    cd ~/.config/awesome
    git clone https://github.com/mokasin/apw.git
    git clone https://github.com/copycat-killer/awesome-freedesktop.git freedesktop
    # Note the freedesktop clone is not configured. Need to make sure I've cloned the correct branch (for 3.5.X)
    # ADD MORE DESCRIPTION HERE
    wget https://raw.githubusercontent.com/NuckChorris/assault/master/awesomewm/assault.lua
    # Note, assault.lua (Battery indicator) may need some local configuration
    # ADD MORE DESCRIPTION HERE

#### For additional packages

    sudo apt install vim-gnome chromium-browser blueman network-manager-gnome

## Files

- `rc.lua` - The main user resource file. Put in `~/.config/awesome/`
- `theme.lua` - System theme file. Put in `/usr/share/awesome/themes/default/`
- `bin/termx` - Launcher of `gnome-terminal` with random profiles. Put in `~/bin/`  # ADD MORE DESCRIPTION HERE
- `wallpapers/` - Folder with Desktop backround images. Put in `~/.config/awesome/`

