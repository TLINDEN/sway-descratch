# sway-descratch

This   is    a   more   practical   example    for   [swayipc   module
usage](https://github.com/TLINDEN/swayipc).  With  sway you  can  move
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
https://github.com/tlinden/sway-descratch/issues.

## See also

- [swayipc golang sway binding](https://github.com/tlinden/swayipc)
- [sway-ipc(7) manpage](https://www.mankier.com/7/sway-ipc)
- [swaywm](https://github.com/swaywm/sway/)
- [swayfx](https://github.com/WillPower3309/swayfx)

## Copyright and license

This software is licensed under the GNU GENERAL PUBLIC LICENSE version 3.

## Authors

T.v.Dein <tom AT vondein DOT org>

## Project homepage

https://github.com/tlinden/sway-descratch

## Copyright and License

Licensed under the GNU GENERAL PUBLIC LICENSE version 3.

## Author

T.v.Dein <tom AT vondein DOT org>
