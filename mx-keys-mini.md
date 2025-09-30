# Keyboard setup

Notes on how to remap keyboard buttons to work consistently across Windows and Ubuntu systems. These settings are focused on Logitech's MX Keys Mini keyboard. Nothing fancy, just a few tweaks to increase productivity.

## Keyboard layout

This keyboard is built using `United Kingdom QWERTY` layout. To use special characters like `çáéàèãê`, it is possible using other keyboard layouts.

- Windows: United States-International QWERTY
- Ubuntu: (to be added)

## Desired settings

| Button | Action |
| - | - |
| Fn + F6 | Previous Track |
| Fn + F7 | Next Track |
| Fn + F8 | Print Screen |

## Windows 11

1. Download and install [Microsoft PowerToys](https://learn.microsoft.com/en-us/windows/powertoys/)
1. Open PowerToys Settings -> Keyboard Manager
1. Under **Remap a Shortcut**, add the remappings:

| Select | To |
| - | - |
| Win (Left) + H | Previous Track |
| Win (Left) + Ctrl (Left) + Alt (Left) + Shift (Left) + Space | Next Track |
| Win (Left) + Shift (Left) + S | Print Screen |


### Disable unused PowerToys modules

1. Open PowerToys -> Settings -> Modules
1. Turn off:
    - Awake
    - Command Palette
    - PowerToys Run