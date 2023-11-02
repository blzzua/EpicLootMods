
# This is a RE-UPLOAD with the most up-to-date H&H version from nexus, **aedenthorn** is the author of this mod.

* Original Author of this mod is **aedenthorn** from nexus mods
* [Original Mod](https://www.nexusmods.com/valheim/mods/1245)

## Permissions as of 23/01/2022, Upload permission.
![Permissions](https://i.imgur.com/iZd10IE.png)

## Mod Information (Below is the original information from nexus):

This mod lets you customize existing item and piece recipes using json files.

Recipe data is stored as json files in **BepInEx\plugins\RecipeCustomization.** To create a template json file for a specific recipe, type the following command in the console (F5):

**recipecustomization save <ItemSpawnName>**

E.g. **recipecustomization save <ShieldWood>** will create a file called **ShieldWood.json** with the default recipe data for a wooden shield.  Edit that file as you
like, save it, then type the following command in the console:

**recipecustomization reload**

This will reload the file, applying the new values to the existing recipe.

The variables are mostly self-explanatory.

## reqs

**reqs** is a list of the actual recipe requirements. Each entry is a string separated with colons,e.g.:

    "reqs": [
        "FineWood:30:1:True",
        "DeerHide:10:1:True",
        "Resin:20:1:True",
        "BronzeNails:80:1:True"
    ]

The first part is the material's spawn name, the second is the amount, the third is the amount per level if the item being created is upgradeable, and the fourth is whether that material can be recovered on destroying the created item.

## craftingStation

**craftingStation** is the name tag of the crafting station required to build the piece. You can remove the requirement by setting this to "", or you can change it to the name tag of a different crafting station, e.g.

**"craftingStation": "$piece_stonecutter",**

I don't have a list of the name tags of all the crafting stations.


## disabled

If you set "disabled": true, it will remove this recipe from the game.

## Config

A config file **BepInEx/config/aedenthorn.RecipeCustomization.cfg** is created after running the game once with this mod.

You can adjust the config values by editing this file using a text editor or in-game using the Config Manager﻿.

To reload the config from the config file, type **recipecustomization reset** into the game's console (F5).

## Technical

To install manually, place the dll file in the BepInEx/plugins folder. You will need BepInEx.

Code is at https://github.com/aedenthorn/ValheimMods.

﻿﻿If you want to complain or ask for help or help me test my mods, you can visit my Discord server. ﻿https://www.discord.com/invite/bs6zHuj

[Click here for a list of all my mods for Valheim.](https://www.nexusmods.com/valheim/articles/104)