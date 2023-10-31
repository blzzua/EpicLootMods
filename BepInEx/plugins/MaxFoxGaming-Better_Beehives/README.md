# Better Beehives
## Rewarding your beekeeping efforts in Valheim!
This mod is a very simple expansion to the beehive system in Valheim. It gives player-made beehives a configurable chance to drop a queen bee when the honey is harvested. Additionally, if a queen bee is harvested, you may also find some royal jelly in the hive as well.

Why would this mod be useful?
- There are a finite number of beehives in a Valheim world, and these are the only source of queen bees.
- Servers with a lot of players have no way to generate additional queen bees, meaning all players may not have enough.
- This mod fixes this issue and allows you to get queen bees from your beekeeping activities.

## Configuration
Configuration is extremely simple. 

### Queen Bee Drop Chance
The value set is the chance that a queen bee will drop when the hive is at its maximum honey level.

Example: Setting the value to 0.2 (20%) means that a queen bee has a 20% chance to drop when you harvest 4 honey. If there is less honey in the hive, the probability will be scaled down based on how much honey is in the hive.

```
Chance of Queen Bee when harvesting = (Amount of Honey / Maximum Honey Level) x Chance of Queen Bee when hive is full
```

So in our above example, if the beehive had 3 honey in when harvested, the probability of getting a queen would be 15%.

### Royal Jelly Drop Chance
Whenever a queen bee is harvested, this value sets the chance that you will also receive royal jelly.

### Royal Jelly Drop Attempts
This is how many times the royal jelly will be attempted to spawn, with equal probability of success depending on Royal Jelly Drop Chance.

## Contact Me (Bug Reports & Suggestions)
If you have any suggestions, or experience bugs / problems using this mod please get in touch with me on my [Discord](https://discord.gg/K2gnt7ZMHX).

## Changelog

### Changelog 1.0.2

- Updated for Valheim Hildir's Request 0.217.24
- Fixed outdated ServerSync

### Changelog 1.0.1

- Updated for Valheim 0.216.9

### Changelog 1.0.0

- Initial Release

## Installation
Move the 'plugins' and 'config' folders from the archive to your BepInEx folder.