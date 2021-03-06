# AM2R-Community-Updates

## Co-op Changes
String compression scripts are by Homunculus: https://marketplace.yoyogames.com/assets/4560/strict

Special thanks to Lojical/Lojemiru and ShirtyScarab for help with programming and art.

The source code here has the same requirements as the original repo in order for it to work. Only the code and my changes have been included.

Currently syncs all health, ammo, items, metroids, events, and power-ups. The Queen fight is synced, boss deaths are synced, the reactor explosion sequence is synced, the transition to the credits at the end is synced, and death is synced.

If players die, progress will be kept for a better user experience.

There is a Multitroid Settings menu under Options that allows you to change whatever mod settings you need to and connect/disconnect. There is no longer a need to manually edit the mod_settings.ini.

The server can be found here: https://github.com/lassiterm/AM2R-Server

## To-do List
 - The only remaining plan is to add a special game mode :)
 - If you have any suggestions, feel free to @milesthenerd in the AM2R Discord Server.

## What is this?
The source code for the AM2R Community Updates 1.5.x branch, free of copyrighted assets and trademarks.
If you have not played the AM2R Community Updates before, this will be of no use to you!

This source code is based on [AM2Rrc](https://gitlab.com/yellowafterlife/AM2Rrc) by YellowAfterlife. It could be considered a fork.

If you are looking for a playable build of the game, please download the [AM2RLauncher](https://www.reddit.com/r/AM2R/comments/iajukx/am2r_152_release_the_am2rlauncher/) to install the latest update.

## Copyright clarifications
This source code does not contain any copyrighted assets or trademarks - in fact, it does not contain *any* assets at all, just like the AM2Rrc repository.

Assets must be extracted from your copy of the AM2R Community Updates using [GMXDataSync](https://github.com/YAL-GameMaker-Tools/GmxDataSync/blob/master/Executable/GmxDataSync.exe) in order to compile this project properly.

Furthermore, there are two paid shader assets included in the Community Updates: 
[Pixelated Pope's Retro Palette Swapper](https://pixelatedpope.itch.io/retro-palette-swapper) and
[PixHammer's GameBoy Shader](https://pixhammer.itch.io/gameboy-shader).
We do not curently have permission to distribute either of these assets, so they are excluded from this repository.
You will need to replace them with default shader code in order for the project to compile.

Finally, we have excluded the datafiles and changelog from this repository to further enforce the removal of trademarks.

## License
Please read our [license](https://github.com/lassiterm/AM2R-Multitroid/blob/main/LICENSE) before distributing, modifying, contributing to, or otherwise interacting with this project.

## Contributing
Please read our [Contribution Guidelines](https://github.com/Lojemiru/AM2R-Community-Updates/blob/main/CONTRIBUTING.md) before opening any issues or creating pull requests.

Additionally, it would be most helpful if you joined the [Official AM2R Discord Server](https://discord.gg/HAeG8spkSu) if you plan on contributing to the project.

## Known issues
The vast majority of this source code is undocumented, as it is based on a bytecode reconstruction.

The default language files will display three empty fields when loaded due to recent name changes. This will be a non-issue once 1.5.3 releases.

Reordering assets created before the Community Updates began can have consequences throughout the entire project because of magic numbers: references to assets by numeric ID instead of name. Changing asset order will cause magic number references throughout the source code to begin referencing incorrect assets. Because of this, pull requests that attempt to reorganize assets will be denied.

Much of this code is messy, uses unusual solutions, and does not hold to our established formatting style - this is a result of AM2R's reconstruction and nature as a learning project passed down to multiple lead developers.

## Requirements
[GameMaker: Studio 1.4.1763](https://store.yoyogames.com/downloads/gm-studio/GMStudio-Installer-1.4.1763.exe) - the IDE for editing and compiling this project.

[GMXDataSync](https://raw.githubusercontent.com/YAL-GameMaker-Tools/GmxDataSync/master/Executable/GmxDataSync.exe) - a utility created by YellowAfterlife to populate project files with matching game assets.

A copy of the latest release build of the AM2R Community Updates, which can be installed via the [AM2RLauncher](https://www.reddit.com/r/AM2R/comments/iajukx/am2r_152_release_the_am2rlauncher/).

## Installation
This repository, being based on YellowAfterlife's source reconstruction, is installed in a very similar fashion. Please refer to his installation instructions [here](https://gitlab.com/yellowafterlife/AM2Rrc/-/tree/master/), but replace 1.1's `data.win` with the latest Community Update `AM2R.exe`.

Afterwards, replace the two blank shader assets with default GM:S shader skeletons or your own copy of each shader, as well as the accompanying script files for the Retro Palette Swapper: `pal_swap_init_system` and `pal_swap_set`.

Finally, you will need to install `modifiers.ini` as well as the `lang` and `mods` folders as datafiles within the GM:S project. The default ones do not contain the actual assets and are merely references. These can be copied over from your AM2R_15_2 folder.
