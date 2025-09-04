# Settings for the awesome windows manager

- Last modified: tor sep 04, 2025  10:27
- Sign: JN

## Description

Some notes about my settings of the [awesome window manager](https://awesomewm.org/).

## Installation

Tested on Ubuntu 22.04.3 LTS.

Note Feb 2024: The deb package provided by Ubuntu 22.04 is old and I recently had issues.
Try instead to [install from source](https://github.com/awesomeWM/awesome#debian-based).

    # Old deb from apt sources would have been: `sudo apt install awesome awesome-extra`
    # Build your own deb from source:

    $ sudo apt install -y libxcb-xfixes0-dev feh
    $ sudo apt build-dep awesome
    $ git clone https://github.com/awesomewm/awesome
    $ cd awesome
    $ make package
    $ cd build
    $ sudo apt install ./*.deb

Also, make sure there is a file `/usr/share/xsessions/awesome.desktop`:

    $ curl https://raw.githubusercontent.com/awesomeWM/awesome/master/awesome.desktop | sudo tee /usr/share/xsessions/awesome.desktop

## Local configuration

- [X] Change wallpaper to `~/.config/awesome/wallpapers/Baertling-Oradalki.jpg`
  See <https://www.reddit.com/r/awesomewm/comments/w9ivm2/help_wallpaper_wont_stretch_even_though/>
- [X] Set terminal to `x-terminal-emulator`
- [X] Set editor to `os.getenv("EDITOR") or "editor"`
- [X] Set webbrowser to `firefox`
- [X] Add volume widget (<https://github.com/streetturtle/awesome-wm-widgets/tree/master/volume-widget>)
- [ ] Add wireless/network widget (<https://github.com/pltanton/net_widgets>)?
- [ ] Add bluetooth widget
- [ ] Add Debian menus (<https://github.com/lcpz/awesome-freedesktop/wiki>? <https://wiki.debian.org/Awesome>?, <https://thibaultmarin.github.io/blog/posts/2016-10-05-Awesome-wm_configuration.html#orge0a6031>?)
- [ ] Add battery indicator (<https://raw.githubusercontent.com/NuckChorris/assault/master/awesomewm/assault.lua>)?

Commands:

    $ cd ~/.config
    $ git clone https://github.com/nylander/awesome.git
    $ cd ~/.config/awesome
    $ git clone https://github.com/streetturtle/awesome-wm-widgets.git
    $ git clone https://github.com/pltanton/net_widgets.git

## Files

- `rc.lua` - The main user resource file. Put in `~/.config/awesome/`
- `theme.lua` - System theme file. Put in `/usr/share/awesome/themes/default/`
- `bin/termx` - Launcher of `gnome-terminal` with random profiles. Put in `~/bin/`.
- `wallpapers/` - Folder with Desktop backround images. Put in `~/.config/awesome/`
- `~/.xsession-errors` - Error messages for debugging.
