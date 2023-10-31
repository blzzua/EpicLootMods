# Procreation Plus
## Rewarding your breeding efforts in Valheim!
This mod is a very simple expansion to the taming and breeding system in Valheim. It allows each tamable creature (Boar, Lox, Wolf) to have a configurable chance of giving birth to a higher level offspring. Everything is configurable and gives you many options to tailor to your liking, including adjusting other breedable creatures introduced by other mods!

Why would this mod be useful?
- You won't need to spend so much time trying to track down a 1 or 2 star creature.
- When setting up a new base, you won't need to transport high level creatures from your first base to your new base if you wanted to relocate permanently. You could find some lower level ones and just breed up again.
- You can make breeding more rewarding by making higher level creatures possible, e.g. a 2 star Lox you could only ever get from breeding and that is not found in the wild.
- In the event your base got trashed and you lost your valuable 2 star creatures, all is not lost as you can work your way back up.
- You won't have to sit for hours and wait for a 2 star wolf offspring due to the night time despawn mechanics.

This mod does not work with the Chickens, as the way they breed uses item drops rather than direct creature spawning. This may be supported in the future if it's highly requested.

## Supported Creatures
Currently this mod supports the following creatures by default, and you can change these values, and add your own creatures that are already breedable from other mods (see Configuration section for details):

- **Boar**: Can reach up to 2 stars when breeding. Offspring have a 25% chance to level up.
- **Wolf**: Can reach up to 2 stars when breeding. Offspring have a 10% chance to level up.
- **Lox**: Can reach up to 1 star when breeding. Offspring have a 5% chance to level up.

## Configuration
Configuration is very simple and is given by a list of creatures, the maximum level they can obtain, and the probability that an offspring will be a level higher than the parent.

Note that adding creatures that are not currently tamable or breedable **does NOT give the creature the ability to be tamed or bred**. It only affects creatures that already have the Procreation script attached to them, whether vanilla or modded. 

If you want to make a creature breedable, you'll need another mod to do that, as this mod will not cover adding extra scripts to creatures for now or making baby creatures of currently existing ones. If it's a highly requested feature, I may look into it for the future, so do let me know if this is something you really want.

### Example configuration options and how to interpret them ###

Each creature entry in the configuration needs to be of the following form:
```
{Creature ID}:{Max Offspring Stars}:{Offspring Level Up Chance}
```
- **Creature ID**: Refers to the internal ID of the creature. Available on the Valheim Wiki for vanilla creatures. Localized names **will not work**.
- **Max Offspring Stars**: A whole number from 0 to 2. This determines how high offspring can level up to via breeding. **If you have Creature Level & Loot Control installed, you can set this value up to 5**.
- **Offspring level Up Chance**: A number from 0 to 1. This determines the chance the level up happens when an offspring is born. 0.3 would mean a 30% chance, for example.

An example would be
```
Boar:2:0.3
```

Each creature entry is then separated by a comma (,) to tell the config to move to the next creature. 

Here is an example of a configuration with multiple creatures, and how to interpret it.
```
Boar:2:0.4,Wolf:2:0.15,Lox:0:0
```
This config would read as:
- Boar can achieve a maximum of 2 stars through breeding, and the levelup chance of an offspring is 40%.
- Wolf can achieve a maximum of 2 stars through breeding, and the levelup chance of an offspring is 15%.
- Lox cannot level up through breeding.

Note that the creature names MUST be the internal ID of the creature. **Localized names will not work.** You can refer to the Valheim Wiki for details of any internal names for creatures, but these vanilla creatures happen to share the same name as the English localized names.

### Adding more creatures ###

If you want to add a new creature to the list, you need the following things:
- The internal name of the creature (a.k.a. its prefab name),
- Ensure the tamable creature has a Procreation script (mod authors who added new creatures should be able to confirm  this for you).
- If you are wanting to make your creature be able to spawn above 2 stars, ensure you've installed **Creature Level & Loot Control**.

For example let's say another mod added a tamable rabbit that can be bred called `Wild Rabbit` in localized text, wtth internal (prefab) name `WildRabbit_M`. Let's assume we've also installed CLLC as well so we can make our rabbit breed to a 3 star. To add this creature to be recognized by this mod, you simply add it to the end of your config like this: 
```
Boar:2:0.4,Wolf:2:0.15,Lox:0:0,WildRabbit_M:3:0.2
```
The above example would make the rabbit be able to obtain up to 3 stars via breeding, with a 20% chance for an offspring to be a level higher than its parent.

## Contact Me (Bug Reports & Suggestions)
If you have any suggestions, or experience bugs / problems using this mod please get in touch with me on my [Discord](https://discord.gg/K2gnt7ZMHX).

## Changelog

### Changelog 1.0.6

- Updated for Valheim Hildir's Request 0.217.24
- Fixed outdated ServerSync

### Changelog 1.0.5

- Updated for Valheim 0.216.9

### Changelog 1.0.4

**Fixes**
- Float parsing from some countries not being recognised and throwing errors have been fixed.

### Changelog 1.0.3

**Fixes**
- Probabilities should now work correctly instead of defaulting to 100%.

### Changelog 1.0.2

**Additions**
- ServerSync is now included in this mod and will push server configuration to clients now.

**Changes**
- Configs now load on ZNetScene.Awake to make sure internal classes get synchronised.

**Fixes**
- Console spam has been removed.
- Nullref when logging out and back in again has been fixed.

### Changelog 1.0.1

**Changes**
- Added **Creature Level & Loot Control** as a soft dependency for this mod.
- Config values of up to 5 stars is now only supported with CLLC installed in your mod list. The enemy HUD that shows the stars only goes up to 2 stars by default and CLLC already patches this, so in order to maintain as much compatibility as possible the config will only allow up to 2 stars without CLLC.

### Changelog 1.0.0

- Initial Release

## Installation
Move the 'plugins' and 'config' folders from the archive to your BepInEx folder.