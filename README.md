# BuckshotRouletteModLoader
**Only avaliable for V1.1**\
A Mod Loader for Buckshot Roulette based on the [godot-mod-loader](https://github.com/GodotModding/godot-mod-loader) 4.x branch.\
\
![BRML Title Screen](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/BRMLMainScreen.png?raw=true "BRML Title Screen")
![BRML Mod Menu](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/BRMLModMenu.png?raw=true "BRML Mod Menu")
## Info
I'm not allowed under any circumstance to give the executable or source files to the game, so i provide a xdelta patch file that has to be applied to the executable obtained from [itch.io](https://mikeklubnika.itch.io/buckshot-roulette)

**I DO NOT PROVIDE SUPPORT FOR PIRATED COPIES OF THE GAME**\
if anyone decides to take that route (which I don't recommend as it is illegal + not donating to an indie developer isn't nice) I'm not gonna provide help for bugs/issues as I don't have any way of knowing if they are caused by the cracked exe.

## Avaliable Mods
- [TestMod](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/TestMod.md) by AGO061 ([ModLoader version support](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/ModLoaderVersionSupport.md#testmod-by-ago061)) - a basic test mod that moves the soap bar from one side of the sink to the other.
- [OpenGL3 Fix](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/OpenGL3Fix.md) by AGO061 ([ModLoader Version Support](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/ModLoaderVersionSupport.md#opengl3-fix-by-ago061)) - a mod that fixes glaring issues with the OpenGL3 renderer, it requires the `-cm` command line argument to work. Make a shortcut on windows and add at the end of the path this command `--rendering-driver opengl3 -cm` for an easier way to run with OpenGL3 + Fix.
- [Smarter Dealer](https://github.com/ITR13/BuckshotRouletteSmarterDealer/releases/latest) by ITR ([ModLoader Version Support](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/ModLoaderVersionSupport.md#smarter-dealer-by-itr)) - a deadly dealer that will absolutely shred you.
- [Native Resolution](https://github.com/EmK530/BRMods/tree/main/BRML/NativeResolution/Release) by EmK530 ([ModLoader Version Support](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/ModLoaderVersionSupport.md#native-resolution-by-emk530)) - a mod that increases the game's resolution to match your monitor.
- [Challenge Pack](https://github.com/StarPandaBeg/ChallengePack) by StarPandaBeg ([ModLoader Version Support](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/ModLoaderVersionSupport.md#challenge-pack-by-starpandabeg)) - a mod hides bullets, items with a configuration menu.
- [Dealer Face](https://github.com/ScientificGuy/BuckshotRouletteMods/releases/latest) by ScientificGuy ([ModLoader Version Support](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/ModLoaderVersionSupport.md#dealer-face-by-scientificguy)) - resets the Dealer's face in between rounds.
- [Bug Fixes](https://github.com/ScientificGuy/BuckshotRouletteMods/releases/latest) by ScientificGuy ([ModLoader Version Support](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/ModLoaderVersionSupport.md#bug-fixes-by-scientificguy)) - fixes bugs such as slow motion through resets.

Check [this](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/mods/ModLoaderVersionSupport.md) file in case i missed some mods here, or haven't added the Mod Version Support link.
## Currently supported features
- Basic mod support: allows to load custom mod zips to a mods folder in the same directory as the game.
- Normal fix: Fixed normals from the [GDRE Tools](https://github.com/bruvzg/gdsdecomp) decomp of the game.
- Default render pipeline: This version uses the Forward+ renderer by default (unlike the absolutely illegal web and mobile ports)
- **(NEW)** Possibility to add a custom config menu for your mod! (Check the TestMod source code to learn how as i currently don't have the time to write a wiki)

## Advantages for users and developers
- Easy installation of mods
- Development of mods can be done on the decomp of the game and then used samelessly here, or you can try to decompile the patched game and work from there.

## Known issues
- The lighting in the bathroom is different from the original game
- The lighting of the rave is different from the original game
- Missing checks for game version, mod dependencies and collisions.
- Music will stop working when the dealer cutscene starts (this bug only happens in version 1.1.0 pre-release 1)
- Heaven scene seems to be corrupted in 1.0.0

# Installation
## Requirements
- [Delta Patcher](https://www.romhacking.net/utilities/704/) (I used 3.0.1 to make the patch).
- The `BRML.xdelta` patch file in the releases of this repo.
- A copy of the game obtained [here](https://mikeklubnika.itch.io/buckshot-roulette) V1.1
- (optional) a test mod to try and see if it works
## Steps
- Open Delta Patcher\
\
![Delta Patcher UI](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/XdeltaOpen.PNG?raw=true "Delta Patcher UI")

- Add the path to the Buckshot Roulette executable\
\
![Delta Patcher Add Source](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/XdeltaBRSelect.PNG?raw=true "Delta Patcher Add Source")

- Add the path to the `BRML.xdelta` file\
\
![Delta Patcher Add Patch](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/XdeltaPatchSelect.PNG?raw=true "Delta Patcher Add Patch")

- Click on Apply patch and wait for it to finish
- You are done! Run the game and check if you see the version as `V1.1 (MODDED)` and a Mod Loader mod inside the `MODS` menu

## Future installs
In the newer versions i will include an xdelta file to update from the previous modded binary to the new one.\
For example, when i release `1.1.0`, to upgrade from `1.0.0` you will find a file in the `1.1.0` release with the name `V1-0-0_UPGRADE_BRML.xdelta`. You will just have to apply that file to the modded exe with the `1.0.0` version of the loader installed to upgrade to `1.1.0`.\
This will only be present when the release of the game is the same (For all updates to the V1.1 game for example), when the developer updates the game and i make a new release, you will have to download the new version and patch that one.\
If you lost some updates on the way, you will have to go step-by-step and install each xdelta in order until you arrive to the final version.

# Adding Mods
Create a `mods` folder in the same folder as your executable and drop all the mod zips in there.
Check the `mods` folder in this repo to see a test mod that simply moves the soap in the bathroom.

# Development
Check out the [BRML Development wiki](https://github.com/AGO061/BuckshotRouletteModLoader/wiki) for more info
