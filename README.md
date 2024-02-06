# Settings for the awesome windows manager

- Last modified: tis feb 06, 2024  10:37
- Sign: JN

## Description

Some notes about my settings of the [awesome window manager](https://awesomewm.org/).

## Installation

Tested on Ubuntu 22.04.3 LTS.

Note Feb 2024: The deb package provided by Ubuntu 22.04 is old and I recently had issues.
Try instead to [install from source](https://github.com/awesomeWM/awesome#debian-based).

    # Old deb from apt sources would have been: `sudo apt install awesome awesome-extra`
    # Build your own deb from source:

    $ sudo apt build-dep awesome
    $ sudo apt install libxcb-xfixes0-dev
    $ git clone https://github.com/awesomewm/awesome
    $ cd awesome
    $ make package
    $ cd build
    $ sudo apt install ./*.deb

Also, make sure there is a file `/usr/share/xsessions/awesome.desktop`:

    $ curl https://raw.githubusercontent.com/awesomeWM/awesome/master/awesome.desktop | sudo tee /usr/share/xsessions/awesome.desktop

Local configuration:

    $ cd ~/.config
    $ git clone https://github.com/nylander/awesome.git
    $ cd ~/.config/awesome
    $ git clone https://github.com/mokasin/apw.git
    $ git clone https://github.com/copycat-killer/awesome-freedesktop.git freedesktop

    # Note the freedesktop clone is not configured. Need to make sure I've cloned the correct branch (for 3.5.X)
    # ADD MORE DESCRIPTION HERE

    $ wget https://raw.githubusercontent.com/NuckChorris/assault/master/awesomewm/assault.lua

    # Note, assault.lua (Battery indicator) may need some local configuration
    # ADD MORE DESCRIPTION HERE

#### For additional packages

    $ sudo apt install vim-gnome chromium-browser blueman network-manager-gnome cool-retro-term

## Files

- `rc.lua` - The main user resource file. Put in `~/.config/awesome/`
- `theme.lua` - System theme file. Put in `/usr/share/awesome/themes/default/`
- `bin/termx` - Launcher of `gnome-terminal` with random profiles. Put in `~/bin/`  # ADD MORE DESCRIPTION HERE
- `wallpapers/` - Folder with Desktop backround images. Put in `~/.config/awesome/`
- `~/.xsession-errors` - Error messages fro debugging.
