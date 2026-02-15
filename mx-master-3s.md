# Mouse setup

Notes on how to remap mouse buttons to work consistently across Windows and Ubuntu systems. These settings are focused on Logitech's MX Master 3S mouse. Nothing fancy, just a few tweaks to increase productivity.

## Desired settings

| Button | Action |
| - | - |
| First customizable button | Previous workspace |
| Second customizable button | Next workspace |
| Gesture button | Open Apps view *(Ubuntu only)* |

## Windows 11

Download the [AutoHotKey](https://www.autohotkey.com/) utility tool

Create a new script with the following code:

```ahk
; MX Master 3S side buttons → Cycle workspaces
XButton1::Send, ^#{Left}   ; Previous workspace
XButton2::Send, ^#{Right}  ; Next workspace
```

Save, Run and Test if worked (double click the .ahk file to run)

If worked, add it to the system startup applications. Open the Run app, and enter the command:

```
shell:startup
```

This will open a directory. Create here a shortcut to the original .ahk file. Windows will open this file every time it boots up.

### Hide tray icon

To run the script and keep the tray icon hidden, add this line at the top of the script:

```ahk
#NoTrayIcon
```

### Test inputs

Its possible to create a script to visualize the ID of the buttons being pressed. Create and run the script:

```ahk
#InstallKeybdHook
#Persistent
KeyHistory
```

## Ubuntu

Download and install [Input Remapper](https://github.com/sezanzeb/input-remapper) utility tool

Select the Logitech MX Master 3S device

Create a new preset `Cycle Workspace`

Add 3 mappings:

| Command | Input Key | Output Macro |
| - | - | - |
| Next Workspace | Button EXTRA | Super_L+Alt_L+KEY_RIGHT |
| Previous Workspace | Button SIDE | Super_L+Alt_L+KEY_LEFT |
| Open Menu | Button FOWARD | Super_L |

`Apply` and enable `Autoload` option
