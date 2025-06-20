This is a temporary doc to mention nm088 framework until there is a link for it.

From his own description:


My Skin Framework goal is to allow users with no coding skills to create and customize mods for the game. By simply organizing PNG files into the correct folder structures and using a basic XML configuration, users can add new skins, weapons, walls, clothing, and more.

Zero coding required: Users can create mods using only PNG files and simple XML files.
Flexible folder structure: Each mod is organized into its own folder, making it easy to manage and maintain.

The framework uses Spine runtime to dynamically replace slots during runtime.

Bench system: The skin manager includes various benches along with their corresponding recipes.
Configurable Drop Rates: It supports configuration of drop rates, allowing mods to include diverse crafting and recipe acquisition mechanics.

Custom mod targets: Each mod folder contains targets to be replaced, along with specific crafting requirements, drop rates, and options to choose whether a recipe is required for each component or bench.

Slot variations: The system supports multiple skins per slot, giving users the ability to offer variations for the same equipment or part.

Mod Scanning and Integration
Automatic Folder Scanning: The framework scans folders to automatically determine available mods and targets, streamlining the integration process.
UI Enhancements: Current developments include a UI that recognizes modded icons in the player’s inventory without interfering with the main game code. This feature is nearly complete, with only a few minor bugs remaining.

In the futur: An external GUI tool
Simplified Mod Creation: Plans are underway to develop an external GUI tool. This tool will simplify the process of creating and editing mods without having to dig in the game folder.

Unique Stats and Skills: When the framework is fully completed, it will allow mods to assign unique stats, skills, and additional features such as customizable particle effects for specific equipment etc.

Its a bit ambitious