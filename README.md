# Bash Script for Setting Up a Projector with a Laptop

## Introduction 

This is a modest Bash script that sets up a projector with a
Laptop. It assumes that the preferred resolution for the LCD is
**1366x768**. If you want a different resolution as the default then
edit the script and change it to whichever resolution you want.

It assumes that your laptop has an
[HDMI](https://secure.wikimedia.org/wikipedia/en/wiki/HDMI) output
and/or a
[Mini Display Port](https://secure.wikimedia.org/wikipedia/en/wiki/Mini_DisplayPort). If
your laptop has different outputs you must edit the code and
change/add the output name as reported by
[xrandr](https://secure.wikimedia.org/wikipedia/en/wiki/RandR).

## Installation 

Clone the repo or just download the snapshot tarball and unpackit in a
directory you have set either the `PATH` to or define an `alias` in
your `.bash_aliases` or `.bashrc` file.

## Caveats

Be mindful that the script turns off the screensaver and the power
saving options. You should re-enable them after the presentation with:

    xset +dpms
    xset s on

You can also define a handy alias for it. 

    echo "alias projector-off='xset +dmps; xset s on'" >> ~/.bash_aliases
    
Then source the file `source ~/.bash_aliases`. Now issue
`projector-off` to re-enable the power sabing options and screensaver.    
