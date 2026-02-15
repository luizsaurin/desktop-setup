# CopyQ setup

Notes on how to install CopyQ on Ubuntu.

## Installation

Follow the latest updated installation instructions on the [GitHub repository page](https://github.com/hluk/CopyQ).

## Wayland fix

If the clipboard is not capturing any records, try this tutorial. Verify is the current Ubuntu is using Wayland

Run:

```bash
echo $XDG_SESSION_TYPE
```

If it prints:

```bash
wayland
```

Then your system is using Wayland. For a permanent fix, go to CopyQ's Preferences, enable `Autostart` option, save and exit. This should trigger the autostart settings file creation. Edit autostart:

```bash
nano ~/.config/autostart/copyq.desktop
```

Change Exec line to:

```ini
Exec=env QT_QPA_PLATFORM=xcb copyq
```

## Clipboard history keyboard shortcut


1. Open Settings
1. Go to Keyboard
1. Scroll to Custom Shortcuts
1. Click Add

Fill in:
- Name: CopyQ Clipboard
-	Command:
	```bash
	copyq show
	```

Then assign your shortcut.