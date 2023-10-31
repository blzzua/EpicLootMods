### 1.7.0
- Fixed mod for Linux clients.
- Changed the default plant spacing.
	- Removed [General]StandardizeGridSpacing and replaced with MinimizeGridSpacing.
	- With this change, standardized spacing is the new default. Set the new setting to true to restore old behavior.

### 1.6.3
- Updated for Valheim v0.217.22.
- Compiled against BepInEx 5.4.22.
- AutoReplant now correctly places plants for free when noCost cheat is active.
- Misc code improvements.

### 1.6.2
- Added keyboard shortcut support for configurable toggle keys (e.g. Left Ctrl + F8).

### 1.6.1
- Fixed randomized piece / grid rotation introduced in Hildir's Request when crops or saplings are selected in the build menu.
	- Previous grid rotation is once again remembered for subsequent placements.

### 1.6.0
- Updated for Valheim v0.217.14 (Hildir's Request).
- Now allows placement of all valid ghosts even when root ghost is invalid.
- Added visual feedback for toggle keys.
- Set process filter to prevent the mod from running on server.

### 1.5.0
- Added [General]GloballyAlignGridDirections setting.
	- Defaults to true.
	- Aligns row and column directions with the global grid.
- Added [General]StandardizeGridSpacing setting.
	- Defaults to false.
	- Allows for uniformly spaced grids between diverse plant types at the cost of requiring more physical space.
- Added [Controls]ToggleAutoReplantKey setting.
	- Defaults to null, user must set the key to utilize.
	- Toggles [Harvesting]ReplantOnHarvest setting on/off.
- Fixed snapping of pickable resources.
	- Snap points for all pickables now correctly detect position validity and won't attempt to snap on top of themselves or prevent placement in valid locations.
- Compatiblity fix with mods adding custom pickables.

### 1.4.4
- Added the ability to rotate an entire grid of pieces any time during placement instead of only while snapping to existing grids.

### 1.4.3
- Bulk placement no longer applies to viable pieces unless built with the cultivator.

### 1.4.2
- Updated for Valheim v0.216.9.

### 1.4.1
- Fixed [Harvesting]ReplantOnHarvest functionality in multiplayer environments.

### 1.4.0
- Completely overhauled grid snapping!
- By default, new grids will no longer expand to overlap with an existing grid, nor will new grids diagonally snap to old grids.
- Added 2 new config settings: GridSnappingStyle and StandardizeGridRotations.

### 1.3.2
- Fixed functionality of HarvestStyle.LikeResources that was broken with the release of 1.3.0.

### 1.3.1
- Massively reduced system memory use.
- Additional miscellaneous performance and code optimizations.
- Compiled against BepInEx 5.4.2105.

### 1.3.0
- Bulk harvesting now applies to Beehives in addition to all Pickables.
- Added CostDisplayStyle and CostDisplayLocation configuration settings to [UI] category.
- Fixed resource cost of placement when PreventPartialPlanting is disabled.

### 1.2.0
- Added auto crop replanting when [Harvesting]ReplantOnHarvest is enabled (defaults to off).
- Increased sapling spacing from 200% of growth radius to 220%.
- Added [General]UseStamina config setting.
- Replaced ExtraPlantSpacing setting with ExtraCropSpacing and ExtraSaplingSpacing.
- Performance improvements.
- Mod compatibility improvements.

### 1.1.2
- Added support for CraftFromContainers, OdinsCraftyBoxes, and similar mods.
- Cost for planting multiple resources now reflected in build UI.
	- Can be toggled on/off with new [UI]ShowCost config setting.

### 1.1.1
- Fixed plant spacing to ensure crops can grow (saplings may need more tweaking).
- Fixed casting error when using bulk harvest while interacting with a non-applicable object.
- Added [General]ExtraPlantSpacing config option to allow for spacing customization.

### 1.1.0
- Harvest Easily!
	- Added highly requested bulk harvesting features.
	- Added [Harvesting] section and 4 additional configuration settings.
- Organized the order that configuration options are listed in the BepInEx Configuration Manager.

### 1.0.4
- Fixed plant validity check when [Crops]CropsRequireSunlight is set to false in PlantEverything.

### 1.0.3
- Changed default keybind for toggling snapping features.
- Added config option [Pickables]PreventOverlappingPlacements (defaults to true).
	- When enabled, pickable resources can no longer be placed over top of one another or on any other colliding obstructions.

### 1.0.2
- Fixed biome validity check on pieces with Plant components.
- Appropriate and localized error messages now display when placement is prevented by either PreventPartialPlanting or PreventInvalidPlanting.

### 1.0.1
- Bumped version to correct documentation.

### 1.0.0
- Created Mod.