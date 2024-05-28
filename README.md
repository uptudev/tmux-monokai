# Monokai Pro for tmux

A customized version of the [Dracula theme](https://github.com/dracula/tmux) for [tmux](https://github.com/tmux/tmux/wiki), using colors from [Monokai Pro](https://monokai.pro/).

![Screenshot](./screenshot.png)

## Install

Using [tpm](https://github.com/tmux-plugins/tpm), add the following to your `.tmux.conf`:

```
set -g @plugin 'maxpetretta/tmux-monokai-pro'
```

## Configuration

Configuration and options can be found at [draculatheme.com/tmux](https://draculatheme.com/tmux).

**NOTE**: Replace all mentions of `@dracula` with `@monokai`

## Features

- Support for powerline
- Day, date, time, timezone
- Current location based on network with temperature and forecast icon (if available)
- Network connection status, bandwidth and SSID
- SSH session user, hostname and port of active tmux pane
- Git branch and status
- Battery percentage and AC power connection status
- Refresh rate control
- CPU usage (percentage or load average)
- RAM usage (system and/or tmux server)
- GPU usage
- Custom status texts from external scripts
- GPU VRAM usage
- GPU power draw
- Color code based on whether a prefix is active or not
- List of windows with the current window highlighted
- When prefix is enabled, a smiley face turns from green to yellow
- When charging, 'AC' is displayed
- If forecast information is available, a ☀, ☁, ☂, or ❄ unicode character corresponding with the forecast is displayed alongside the temperature
- Info if the Panes are synchronized
- Spotify playback (needs the tool spotify-tui installed)
- Music Player Daemon status (needs the tool mpc installed)
- Playerctl, get current track metadata
- Current kubernetes context
- Countdown to tmux-continuum save
- Current working directory of tmux pane

## Compatibility

Tested on macOS Monterey, with & without powerline symbols

## License

[MIT License](./LICENSE)

## Credits

All credit goes to [dracula/tmux](https://github.com/dracula/tmux), which this theme was forked from

Special thanks to [Monokai](https://monokai.nl/) for creating the One True Color Theme <3
