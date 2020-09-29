## How to get this mod running
1. Clone this repo and checkout the RocketMod branch. You can do this with the following bash commmands
   - git clone https://github.com/JasonMolisani/Quake4.git
   - cd Quake4
   - git checkout RocketMod
2. Open the folder containing this Repo, and open the visual studio solution 'q4sdk.sln' (This  may not work well in a version of Visual Studio other than Visual Studio 2013)
3. Make sure you are in 'relase' mode
4. Build idlib
5. Build Game
6. Go into the folder containing this repository. There should be a folder called Win32 containing a folder called Release. Navigate to this folder and copy the file 'gamex86.dll' contained within.
7. Paste the copy of the 'gamesx86.dll' file in the "ModdedFiles" folder of the repo. This folder now contains all the files we will need to implement this mod (step 12).
8. If you don't already have it, obtain and install an unmodified version of Quake 4.
9. Navigate to the folder containing the game. I will refer to it as "~/Quake 4", but your install may have used a different name.
10. Create a new folder there and name it RocketMod. Enter that folder. (The new path into that folder should be "~/Quake 4/RocketMod")
11. You will need to fill this folder with the modified .pk4 files. Go into "~/Quake 4/q4base" and bring copies of the following .pk4 files from there into "~/Quake 4/RocketMod"
    - game000.pk4
    - pak022.pk4
12. These .pk4 files are essentially zip folders containing vanilla versions of the files we will be replacing. You need to go into these .pk4 and replace the vanilla versions with the modded versions from the "ModdedFiles" folder of the repo:
    - In game000.pk4 replace:
      - gamesx86.dll
    - In pak022.pk4 replace:
      - rocketlauncher.def (located in pak022.pk4/def/weapons)
13. Open Quake 4
14. Click mods in the lower horizontal menu
15. Select "rocketmod" and click "Load Mod"