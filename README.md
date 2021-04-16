# AokanaPatch
An Aokana patcher made using BepInEx which allows the game to read assets directly from .../Aokana/Aokana_Data instead of from the encrypted .../Aokana/Aokana_Data/\*.dat files. 

If no unencrypted file with the correct folder structure is found in .../Aokana/Aokana_Data, the patch gets data from the game's encrypted \*.dat files the using the game's methods.

# Installation:
- Install BepInEx
https://bepinex.github.io/bepinex_docs/v5.0/articles/user_guide/installation.html

- Place AokanaPatch.dll in .../Aokana/BepInEx/Plugins/

# Usage:
As an example, edit .../Aokana/Aokana_Data/ui_hi/en/sgtitle990000.webp however you like and test that it displays on the title screen. 

The game has some checks for images of the wrong dimension and such so you might have to edit the original image if you get a black title screen or crash. If you don't have this folder or the original image, run my older data decryption tool and copy the results into .../Aokana/Aokana_Data

![image](https://user-images.githubusercontent.com/74600302/115036070-48db4980-9f21-11eb-9362-49ff5c15c8df.png)

This patch is intended for translators and others to change the game's contents easily without re-encrypting any files.

# Dependencies:

If you want to build this yourself, you need references to:
- 0Harmony.dll and BepInEx.dll from .../Aokana/BepInEx/core/ after installing BepInEx.
- Assembly-CSharp.dll, UnityEngine.dll, and UnityEngine.CoreModule.dll from .../Aokana/Aokana_Data/Managed/
