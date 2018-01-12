# thunderbird-tray
## A script that starts and iconifies Thunderbird using kdocker and xdotool.

### Requierements
- thunderbird executable (placed in PATH)
- kdocker
- xdotool 

Please place this script in a location form PATH environment variable and make it executable (`/usr/bin`; `/usr/local/bin`; `~/bin`):

##### $ sudo chmod +x \[thunderbird-tray path\]/thunderbird-tray

In `thunderbird.desktop` (wherever that is: `/usr/share/applications/`; `/usr/local/share/applications/`; `~/.local/share/applications/`) change `Exec=zotero` line to `Exec=zotero-tray`.

If you keep your home partition unformatted from one install to another, you can cp `thunderbird.desktop` to `~/.local/share/applications/` and make the changes there. Then:
##### $ sudo update-desktop-database
The local `thunderbird.desktop` should override global file. I this doesn't happen, the surrest thing is to Logout/Login. To avoid this you can try to restart your interface:
- Gnome-Shell: 'Alt+F2', type 'r' folowed by 'Return' key or just run `gnome-shell --replace` in Alt+F2 menu
- Cinnamon: 'Alt+F2', type 'r' folowed by 'Return' key or just run `cinnamon --replace` in Alt+F2 menu
- etc.

Be sure that `Iconify when minimized` is checked in the options of the tray icon, so that you can also hide zotero running this script, or using the modified launcher.

### Tested on 
- Linux Mint 18.3 Cinnamon 64-bit - for now

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)


