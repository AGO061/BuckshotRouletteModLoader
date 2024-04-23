# BuckshotRouletteModLoader
**NOW AVAILABLE FOR V1.2.2 (STEAM AND ITCH.IO), WINDOWS AND LINUX!**\
A Mod Loader for Buckshot Roulette based on the [godot-mod-loader](https://github.com/GodotModding/godot-mod-loader) 4.x branch.\
\
![BRML Title Screen](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/BRMLMainScreen.png "BRML Title Screen")
![BRML Mod Menu](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/BRMLModMenu.png "BRML Mod Menu")
## Info
This repository does not contain the source code for Buckshot Roulette by Mike Klubnika. It contains an .xdelta patch (with an installer .exe) to mod the latest version (v1.2.2) of the original game [available for purchase on Steam](https://store.steampowered.com/app/2835570) or [also available on itch.io](https://mikeklubnika.itch.io/buckshot-roulette).

**WE DO NOT PROVIDE SUPPORT FOR PIRATED COPIES OF THE GAME.**
Mike Klubnika and Critical Reflex have worked hard on this game. Please show them respect and don't pirate the game. Any requests to see the source code without verification of ownership will be ignored.

## Avaliable Mods
_This list is outdated due to the latest updates and will be updated soon!_
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
## Windows
### Requirements
- Buckshot Roulette.exe (v1.2.2 Hotfix 1)
- BRML_setup.exe ([available here or in the "Releases" section](https://github.com/AGO061/BuckshotRouletteModLoader/releases/latest))
  _or_
- A delta patching software (not recommended)

Run the setup .exe after you have installed the original game. The mod will be installed to `Documents`. Then use the created shortcut, the included `brml.bat` file, or the modded .exe to run the game. It's that easy!

## Linux
### Requirements
 - Buckshot Roulette.x86_64 (v1.2.2 Hotfix 1)
 - xdelta3 (`sudo apt install xdelta3`)
 - unzip (`sudo apt install unzip`)

Once `Buckshot Roulette.x86_64` is in a directory on your computer, run the following commands from the folder where the original game file is:
```
mkdir Buckshot\ Roulette
cd Buckshot\ Roulette
mkdir mods override configs
wget https://github.com/AGO061/BuckshotRouletteModLoader/releases/download/2.0.2/brml2_linux.xdelta
wget https://github.com/AGO061/BuckshotRouletteModLoader/releases/download/2.0.2/brml.sh
xdelta3 -d -s ../Buckshot\ Roulette.x86_64 brml2_linux.xdelta Buckshot\ Roulette.x86_64
rm brml2_linux.xdelta
chmod +x brml.sh Buckshot\ Roulette.x86_64
```
You can now run the BRML using the command `./brml.sh` in the `Buckshot Roulette` directory.

## Troubleshooting
To run the Windows installer version with OpenGL3, change the following line in `brml.bat`:
```
start "" "%%i"
```
  to this:
```
start "" "%%i" --rendering-driver opengl3
```
For the Linux `brml.sh` file, change the following line:
```
$game
```
  to this:
```
$game --rendering-driver opengl3
```
Report any other issues with installation to the Issues page.

# Adding Mods
If you used the installation methods above, you should already have a `mods` folder. Otherwise, Create a `mods` folder in the same folder as your executable. Drop all the mod zips in there. Check the `mods` folder in this repo to see a test mod that simply moves the soap in the bathroom.

# Development
Check out the [BRML Development wiki](https://github.com/AGO061/BuckshotRouletteModLoader/wiki) for more info
