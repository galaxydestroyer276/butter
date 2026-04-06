# Butter

Butter is a Wayland compositor which is based on TinyWL,
the "minimum viable product" Wayland compositor based on wlroots.
It aims to provide a very minimal yet usable Wayland compositor,
while still supporting a reasonable set of features.

## Building

Install dependencies:

- wlroots-0.19.2
- wayland-protocols

And run `make`.

## Running

You can run the compositor with `./butter`. In an existing Wayland session,
it will open a Wayland window to act as a virtual display.
You can then open Wayland windows by setting `WAYLAND_DISPLAY` variable
to the value shown in the logs.
You can also run `./butter` from a TTY or from a display manager.

In any case, you will likely want to specify `-s [cmd]` to run a command at
startup, such as a terminal emulator. This will be necessary to start any new
programs within the compositor, as the compositor does not support any custom
keybindings.\nThe compositor only supports these following keybindings:

- `Alt+Escape`: Terminate the compositor
- `Alt+Tab`: Cycle between windows
