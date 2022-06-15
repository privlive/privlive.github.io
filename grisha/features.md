---
layout: page
permalink: /grisha/features/
title: "Features"
---

Stracciatella walks a fine line between preserving the original gameplay, adding ease-of-life
improvements and providing new inobtrusive optional features.

  - [GUI Launcher](#gui-launcher)
  - [High Resolution Support](#high-resolution-support)
  - [Dead is Dead mode](#dead-is-dead-mode)
  - [Infinite save games](#infinite-save-games)
  - [Bundled optional mini-mods](#bundled-optional-mini-mods)
  - [Wildfire support](#wildfire-support)
  - [Integrated Editor](#integrated-editor)
  - [Debug screens](#debug-screens)

On the internal side, good code as-a-feature has been a major focus of the project, easily
illustrated by comparing the amount of code in related engines (as of March 2021):

<table>
  <thead>
    <tr>
      <th>Engine</th>
      <th>Lines of code</th>
      <th>Difference</th>
      <th>Languages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Original JA2</td>
      <td style="text-align: right;">1,222,384</td>
      <td style="text-align: center;">-</td>
      <td>C</td>
    </tr>
    <tr>
      <td><strong>Stracciatella</strong></td>
      <td style="text-align: right;">851,152</td>
      <td style="text-align: center;">-30,4 %</td>
      <td>C++, Rust, (LUA)</td>
    </tr>
    <tr>
      <td>JA2 1.13</td>
      <td style="text-align: right;">2,184,310</td>
      <td style="text-align: center;">+78,7 %</td>
      <td>C++, (LUA)</td>
    </tr>
  </tbody>
</table>


## GUI Launcher
*Note: added in 0.16.0.*

A GUI Launcher is included to facilitate changing settings and tweaking the game.
<img src="/assets/photo_GR/features/launcher-tab1.jpg" style="max-width: 32.5%" alt="launcher tab 1">
<img src="/assets/photo_GR/features/launcher-tab2.jpg" style="max-width: 32.5%" alt="launcher tab 2">
<img src="/assets/photo_GR/features/launcher-tab3.jpg" style="max-width: 32.5%" alt="launcher tab 3">


## High Resolution Support

Added support for high video resolutions. For example, game can be started in 1680x1050  mode like this: `ja2.exe -res 1680x1050`.

<img src="/assets/photo_GR/features/high-res.jpg" style="max-width: 50%" alt="JA2 Stracciatella in 1680x1050 resolution">


## Dead is Dead mode
*Note: added in 0.16.0.*

Dead is Dead is a new game mode for players looking for a new challenge, and who think IronMan doesn't cut it just yet. With the Dead is Dead mode the game takes the burden of saving and savegame management from your shoulders so you can concentrate on the important bits. 

You select one savegame slot at the beginning of a new game, and the game will stick to that slot throughout your playthrough. The game will also make sure to save before you leave, so you can rest assured you will always be able to pick up at where you left.

With Dead is Dead there is no going back. If mercs die, there is no way of bringing them back. If you make a mistake, there is no way of reverting it. So be careful, play it safe, and prepare to be frustrated.


## Infinite save games

The engine now supports saving and loading of arbitrarily named saved games, and an arbitrary number of them.
The load screen is enhanced with game mode, difficuly and mod info plus a scrollbar.

<img src="/assets/photo_GR/features/new_saveload.jpg" style="max-width: 50%" alt="enhanced load screen">

## Bundled optional mini-mods
*Note: added in 0.16.0.*

A few data-altering [mods](https://github.com/ja2-stracciatella/ja2-stracciatella/tree/master/assets/mods) are included, but must be explicitly selected to be used:
- Generous Rebels, From Russia With Love: extra items in Omerta
- Honest IMP quiz questions: the satirical answers now include the personality aspect that they would contribute to
- O Fortuna: dramatic intro music for Jagged Alliance 2

Several additional mods can be downloaded, conveniently [bundled in a single file](https://github.com/ja2-stracciatella/ja2-stracciatella-modpacks/releases/latest).
They are not included with the engine due to scope or license problems. Unpack them alongside the others in the `mods` directory and run them the
same way. For *JA2: Wildfire* read the next section.

If you're wondering how to run the game with mods, read [these instructions](how-to-run.md#extra-configuration-and-modding).


## Wildfire support
*Note: added in 0.17.0.*

Basic Wildfire support is present, with most of the data differences externalized. You need
to have JA2, Wildfire and [this conversion](https://github.com/ja2-stracciatella/mod-wildfire-maps/releases)
installed to start a Wildfire game. It is implemented as other [mods](#bundled-optional-mini-mods), so you can
still play vanilla games too.

Read the included [README](https://github.com/ja2-stracciatella/mod-wildfire-maps/blob/master/README.md)
for detailed instructions and caveats.


## Integrated Editor

The map editor is now integrated into the game. Start it through the launcher or like this: `ja2.exe -editor`.

<img src="/assets/photo_GR/features/integrated-editor.jpg" style="max-width: 50%" alt="Editor">


## Debug screens
*Note: added in 0.15.0.*

Some debug screens are accessible when using the `-debug` parameter.

Tactical Screen:

- `F11` for Quest Debug Screen
- `CTRL+f` for FPS Display
- `CTRL+z` to toggle z-buffer
- `ALT+m` for level node debug mode
- `ALT+n` to play quotes of hovered merc
- `q` for soldier and land debug mode
- `y` for struct debug mode

To exit any screen press `q`. To cycle through different pages use `pageup` and `pagedown`.

Examples:

<img src="/assets/photo_GR/features/debug-soldier.png" style="max-width: 49%" alt="Debug soldier">
<img src="/assets/photo_GR/features/debug-land.png" style="max-width: 49%" alt="Debug land">
<img src="/assets/photo_GR/features/debug-z-buffer.png" style="max-width: 49%" alt="Debug z-buffer">
