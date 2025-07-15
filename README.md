# dwm-statusbar
> ⚠️ This project has moved to [Codeberg](https://codeberg.org/tsugibayashi/output_status).

A statusbar for dwm

## Prerequisites

1. Install xsetroot.
1. Install packages if you use the following modules:

| Component | Required package (Arch) |
----|----
| battery | upower |
| audacious | audacious |

## Installation

Install dwm-statusbar.

For example,
```bash
$ git clone https://github.com/tsugibayashi/dwm-statusbar.git
$ cp -p dwm-statusbar/dwm-statusbar ~/bin/
```

## Displaying information in the dwm statusbar

Edit $HOME/.xsession.
```bash
# Statusbar loop for dwm
while true; do
    $HOME/bin/dwm-statusbar hms b_d
    sleep 1s
done &

# Window Manager
/usr/bin/dwm
```

## Module name

| Module | Description |
----|----
| d & hm | Date and time in '%F %R'. |
| d & hms | Date and time in '%F %T'. |
| b | Battery percentage. This module uses upower. |
| c | CPU temperature. |
| a | Audacious status using audtool. |

