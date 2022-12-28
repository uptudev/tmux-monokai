### [tmux](https://github.com/tmux/tmux/wiki)

#### Install using [tpm](https://github.com/tmux-plugins/tpm)

If you are a tpm user, you can install the theme and keep up to date by adding the following to your .tmux.conf file:

    set -g @plugin 'maxpetretta/tmux-monokai-pro'

Add any configuration options below this line in your tmux config.

#### Activating theme

1. Make sure `run -b '~/.tmux/plugins/tpm/tpm'` is at the bottom of your .tmux.conf
2. Run tmux
3. Use the tpm install command: `prefix + I` (default prefix is ctrl+b)

#### Configuration

To enable plugins set up the `@monokai-plugins` option in you `.tmux.conf` file, separate plugin by space.
The order that you define the plugins will be the order on the status bar left to right.

```bash
# available plugins: battery, cpu-usage, git, gpu-usage, ram-usage, network, network-bandwidth, network-ping, weather, time
set -g @monokai-plugins "cpu-usage gpu-usage ram-usage"
```

For each plugin is possible to customize background and foreground colors

```bash
# available colors: white, gray, black, cyan, blue, green, magenta, red, yellow
# set -g @monokai-[plugin-name]-colors "[background] [foreground]"
set -g @monokai-cpu-usage-colors "red black"
```

#### Status bar options

Enable powerline symbols

```bash
set -g @monokai-show-powerline true
```

Switch powerline symbols

```bash
# for left
set -g @monokai-show-left-sep 

# for right symbol (can set any symbol you like as seperator)
set -g @monokai-show-right-sep 
```

Enable window flags

```bash
set -g @monokai-show-flags true
```

Adjust the refresh rate for the status bar

```bash
# the default is 5, it can accept any number
set -g @monokai-refresh-rate 5
```

Switch the left smiley icon

```bash
# it can accept `session`, `smiley`, `window`, or any character.
set -g @monokai-show-left-icon session
```

Add padding to the left smiley icon

```bash
# default is 1, it can accept any number and 0 disables padding.
set -g @monokai-left-icon-padding 1
```

Enable high contrast pane border

```bash
set -g @monokai-border-contrast true
```

#### cpu-usage options

Customize label

```bash
set -g @monokai-cpu-usage-label "CPU"
```

Show system load average instead of CPU usage percentage (default)

```bash
set -g @monokai-cpu-display-load true
```

CPU usage percentage (default) - in percentage (output: %)
Load average – is the average system load calculated over a given period of time of 1, 5 and 15 minutes (output: x.x x.x x.x)

#### battery options

Customize label

```bash
set -g @monokai-battery-label "Battery"
```

#### gpu-usage options

Customize label

```bash
set -g @monokai-gpu-usage-label "GPU"
```

#### ram-usage options

Customize label

```bash
set -g @monokai-ram-usage-label "RAM"
```

#### network-ping options

You can configure which server (hostname, IP) you want to ping and at which rate (in seconds). Default is google.com at every 5 seconds.

```bash
set -g @monokai-ping-server "google.com"
set -g @monokai-ping-rate 5
```

#### time options

Disable timezone

```bash
set -g @monokai-show-timezone false
```

Swap date to day/month

```bash
set -g @monokai-day-month true
```

Enable military time

```bash
set -g @monokai-military-time true
```

#### git options

Hide details of git changes

```bash
set -g @monokai-git-disable-status true
```

Set symbol to use for when branch is up to date with HEAD

```bash
# default is ✓. Avoid using non unicode characters that bash uses like $, * and !
set -g @monokai-git-show-current-symbol ✓
```

Set symbol to use for when branch diverges from HEAD

```bash
# default is unicode !. Avoid bash special characters
set -g @monokai-git-show-diff-symbol !
```

Set symbol or message to use when the current pane has no git repo

```bash
# default is unicode no message
set -g @monokai-git-no-repo-message ""
```

Hide untracked files from being displayed as local changes

```bash
# default is false
set -g @monokai-git-no-untracked-files true
```

#### weather options

Switch from default fahrenheit to celsius

```bash
set -g @monokai-show-fahrenheit false
```

Set your location manually

```bash
set -g @monokai-fixed-location "Some City"
```

Hide your location

```bash
set -g @monokai-show-location false
```
