<h1 align="center">
  dwm
</h1>

## What's special about this build?
This custom build include the necessary to support emoji & custom theming via [Pywal](https://github.com/dylanaraps/pywal).

List of patches:
* urg-border (change border colors)
* activetagindicatorbar (alt look for active tag)
* alwayscenter
* centeredwindowname
* fakefullscreen (to always fit fullscreen)
* fullgaps
* fullscreen
* swallow

New bindings:
* Customize gaps
* Sounds controls
* Backlight controls
* Screenshot with escrotum

## What is dwm?
dwm is an extremely fast, small, and dynamic window manager for X.


## Requirements
In order to build dwm you need the Xlib header files.


## Installation
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


## Running dwm
Add the following line to your .xinitrc to start dwm using startx:
```shell
  exec dwm
```
In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:
```shell
  DISPLAY=foo.bar:1 exec dwm
```
(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:
```shell
  while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
  do
    sleep 1
  done &
  exec dwm
```

# Configuration
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.
