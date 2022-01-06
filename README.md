# Outer Wilds planet creation template
 A template project for adding planets to Outer Wilds with New Horizons.

If you aren't comfortable using GitHub, there is a world creation page on the [Outer Wilds Mods website](https://outerwildsmods.com/custom-worlds) that automates most of the process. You can use that instead of directly using this template.

## Prerequisites
- Outer Wilds Mod Manager (get it from the [Outer Wilds Mods](https://outerwildsmods.com/) website)
- OWML installed in the Mod Manager
- A GitHub account (required for forking the repo and for releasing your mod to the public)

## How to use this template
1. Generate your repository from this template (click on Use This Template above).
2. Clone your repository to your machine into a new folder in OWML's `Mods` folder. Name this folder [your name].[your unique mod ID]. More on this later. You can use GitHub desktop for this, then click the green "Code" dropdown and select open with GitHub Desktop.
3. Follow the instructions in [Outer Wilds New Horizons](https://github.com/xen-42/outer-wilds-new-horizons) on how to create planet config files. Place your config files into the `planets` folder in [your name].[your unique mod ID]. You can delete the `example_config` file in there while you're at it. When you're done you can commit the changes to your repo.
5. Edit `NewHorizonsTemplate/manifest.json`. It will look like this:

```
{
  "filename": "NewHorizonsConfig.dll", 
  "author": "[your name]",
  "name": "[your readable mod name]",
  "uniqueName": "[your name].[your unique mod ID]",
  "version": "0.1.0",
  "owmlVersion": "2.1.0",
  "dependencies": [ "xen.NewHorizons" ]
}
```

- Replace `[your name]` with how you want your name to appear in the mod database.
- Replace `[your readable mod name]` with how you want your mod to appear in the database.
- Replace `[your unique mod ID]` with whatever you want, as long as it isn't already in use by another mod. Adding `[your name]` as a prefix helps to prevent overlaps but isn't required.

6. Edit the `README.md` file (you can do this on GitHub in your browser) and be sure to add some nice pictures of your planets.
7. Releasing the mod. See the "Releasing the mod" section on the  [Outer Wilds Mod Template](https://github.com/Raicuparta/ow-mod-template) repo for info on how to do this. Be sure to try out the mod by adding it to your OWML mods folder and make sure it works in game before releasing. When you zip your final mod be sure to exclude the README.md file and the config.json file (they aren't needed in the release). The zip file should contain: `planets`, `config`, `manifest`, and `NewHorizonsConfig.dll`.

NOTE: When you make an update to the mod try not to change any file names. The Mod Loader will not delete old files when updating and you can end up with duplicate planet configs. If you want to delete a file you can probably just erase its contents but leave it in the mod.
