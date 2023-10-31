## Imported Mod From NexusMods

This mod was imported from NexusMods. No changes were made to the mod. [Click here to go to the original mod at NexusMods](https://www.nexusmods.com/valheim/mods/829).

## About

This is a simple quality of life mod that lets you see the contents of a container, as well as its remaining capacity in the interact hover text.

You can configure the following:

Maximum entries to show - default -1, meaning unlimited
Sort type - Name, Value, or Weight - default **Value**
Sort ascending - default **false**
Entry text - default **<color=#AAAAAAFF>{0} {1}</color>** ({0} is replaced by the amount and {1} is replaced by the item name)
Overflow text - if more items than max entries - default **<color=#AAAAAAFF>...</color>**
Capacity text - default **<color=#FFFFAAFF> {0}/{1}</color>** ({0} is replaced by the slots used and {1} is replaced by total slots)


Colors are RRGGBBAA hexadecimal (Alpha doesn't seem to do anything). For example, to get the colors in the first screenshot:

**EntryText = <color=#FFFFAAFF>{0}</color> <color=#AAFFAAFF>{1}</color>**

Apparently if you use BetterUI, you need to set the following in the BetterUI config file:

**chestHasRoomStyle = 0**



## Config

A config file **BepInEx/config/aedenthorn.ShowContainerContents.cfg** is created after running the game once with this mod).

You can adjust the config values by editing this file using a text editor or in-game using the [Config Manager.](https://www.nexusmods.com/valheim/mods/740)

To reload the config from the config file, type **showcontainercontents reset** into the game's console (F5).



## Technical

To install manually, place the dll file in the BepInEx/plugins folder. You will need BepInEx.

Code is at https://github.com/aedenthorn/ValheimMods.

If you want to complain or ask for help or help me test my mods, you can visit [my Discord server.](https://discord.gg/bs6zHuj)

[Click here for a list of all my mods for Valheim.](https://www.nexusmods.com/valheim/articles/104)