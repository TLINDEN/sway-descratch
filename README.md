[![status-badge](https://ci.codeberg.org/api/badges/15678/status.svg)](https://ci.codeberg.org/repos/15678)
[![Go Report Card](https://goreportcard.com/badge/codeberg.org/scip/swayipc)](https://goreportcard.com/report/codeberg.org/scip/sway-descratch) 
[![License](https://img.shields.io/badge/license-GPL-blue.svg)](https://codeberg.org/scip/sway-descratch/raw/branch/main/LICENSE)


# sway-descratch

This   is    a   more   practical   example    for   [swayipc   module
usage](https://codeberg.org/scip/swayipc).  With  sway you  can  move
windows  to a  "scratchpad", i.e.  like iconify  it. There  may be  an
official  way to  get back  such  windows, but  I didn't  find a  good
one. There's the  "scratchpad show" command, but it  doesn't allow you
to select a window, it just shows the next one (and it keeps it in the
floating state).

So, this example program lists all windows currently garaged on the
scratchpad. When called with a windows id, it gets back the window
to the current workspace and gives it focus - thus descratching it.

To add comfort to the process I  added a small script which you can
use as a ui to it. It uses  rofi which makes a handy ui. To use it,
compile descratch  with "go  build", copy  the descratch  binary to
some location within your $PATH and run the script.

## Install

Copy the binary and rofi script for your platform to your `$PATH`. Add
something like this to your sway config:

```default
# mv container to scratchpad
bindsym $mod+k move scratchpad

# interactively get container back to current workspace
bindsym $mod+b exec descratcher-rofi.sh
```

## Getting help

Although I'm happy to hear from sway-descratch users in private email, that's the
best way for me to forget to do something.

In order to report a bug,  unexpected behavior, feature requests or to
submit    a    patch,    please    open   an    issue    on    github:
https://codeberg.org/scip/sway-descratch/issues.

## See also

- [swayipc golang sway binding](https://codeberg.org/scip/swayipc)
- [sway-ipc(7) manpage](https://www.mankier.com/7/sway-ipc)
- [swaywm](https://github.com/swaywm/sway/)
- [swayfx](https://github.com/WillPower3309/swayfx)

## Copyright and license

This software is licensed under the GNU GENERAL PUBLIC LICENSE version 3.

## Authors

T.v.Dein <tom AT vondein DOT org>

## Project homepage

https://codeberg.org/scip/sway-descratch

## Copyright and License

Licensed under the GNU GENERAL PUBLIC LICENSE version 3.

## Author

T.v.Dein <tom AT vondein DOT org>
