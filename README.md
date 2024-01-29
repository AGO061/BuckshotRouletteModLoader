# BuckshotRouletteModLoader
**Only avaliable for V1.1**\
A Mod Loader for Buckshot Roulette based on the [godot-mod-loader](https://github.com/GodotModding/godot-mod-loader) 4.x branch.\
\
![BRML Title Screen](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/BRMLMainScreen.png?raw=true "BRML Title Screen")
![BRML Mod Menu](https://github.com/AGO061/BuckshotRouletteModLoader/blob/main/img_docs/BRMLModMenu.png?raw=true "BRML Mod Menu")
## Info
I'm not allowed under any circumstance to give the executable or source files to the game, so i provide a xdelta patch file that has to be applied to the executable obtained from [itch.io](https://mikeklubnika.itch.io/buckshot-roulette)

## Currently supported features
- Basic mod support: allows to load custom mod zips to a mods folder in the same directory as the game.
- Normal fix: Fixed normals from the [GDRE Tools](https://github.com/bruvzg/gdsdecomp) decomp of the game.

## Advantages for users and developers
- Easy installation of mods
- Development of mods can be done on the decomp of the game and then used samelessly here, or you can try to decompile the patched game and work from there.

## Known issues
- The lighting in the bathroom is different from the original game
- The lighting of the rave is different from the original game

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

# Adding Mods
Create a `mods` folder in the same folder as your executable and drop all the mod zips in there.
Check the `mods` folder in this repo to see a test mod that simply moves the soap in the bathroom.
