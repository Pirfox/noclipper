# No Clipper # 

A pleasant, simple and fast no-clip script for [FiveM][5m].

## Setup ##

Just clone this repo to your ressource folder of your [FiveM][5m] server. You might also need to edit your `server.cfg` to
auto-load the resource.

### Permissions ###

Remember that No Clipper **doesn't** do any permission management. By default, it allows **EVERY** player to no-clip.

To prevent this, you can set the `EnableToggleNoClip` value in the `config.lua` file to `false`.

Then, you can use the exported `ToggleNoClipMode` function to your liking, granted that your server loads No Clipper first.

This will effectively makes No Clipper act more like a library than a standalone ressource.

## Speeds ##

Config present 3 default speed `normal` `fast` `slow`

You can change these to your liking.

### Sounds ###

No Clipper plays, by default, different sounds while toggling no-clip mode.

To mute No Clipper, just set the `EnableNoClipSound`  value to `false`.

## Controls ##

The controls are intuitive, and works just like your typical GTA controls.

| Input                               | Controls                |
|-------------------------------------|-------------------------|
| "Next Radio Station" (<kbd>></kbd>) | Enable / Disable NoClip |
| <kbd>WASD</kbd> / Left Stick        | Move / Strafe           |
| Mouse / Right Stick                 | Turn                    |
| <kbd>Shift-r</kbd> / `A`            | Go faster (Hold)        |
| <kbd>Ctrl</kbd> / `A`               | Go slower (Hold)        |
| <kbd>Spacebar</kbd>                 | Move Up                 |
| <kbd>A</kbd>                        | Move Down               |

To toggle no-clipping, you can either use the `ToggleNoClipMode` exported function or, if `EnableToggleNoClip` is set to `true`, use the <kbd>F2</kbd> key.

## Commands ##

With `EnableToggleNoClip` set to `true`, you also have access to many FiveM console commands:

| Command           | Does                                                          |
|-------------------|---------------------------------------------------------------|
| `\noClip <0,1>`   | Enables/disables no-clipping based on the provided argument   |
| `\+noClip`        | Enables no-clipping                                           |
| `\-noClip`        | Disables no-clipping                                          |
| `\toggleNoClip`   | Toggles on or off no-clipping                                 |

## Stats ##

An event is triggered when entering or exiting noclip `esx_status:pauseStatus`.
You can use to prevent loss of different status.

## Exports ##

The resource also exports a `ToggleNoClipMode` function that can be called to toggle no-clip from another resource.

[5m]: https://fivem.net "FiveM"