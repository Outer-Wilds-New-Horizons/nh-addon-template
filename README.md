# Outer Wilds planet creation template
 A template project for adding planets to Outer Wilds with [New Horizons](https://github.com/xen-42/outer-wilds-new-horizons).

The source code for the dll used is [here](https://github.com/xen-42/ow-new-horizons-mod-template).

## Prerequisites
- Outer Wilds Mod Manager (get it from the [Outer Wilds Mods](https://outerwildsmods.com/) website)
- OWML installed in the Mod Manager
- A GitHub account (required for forking the repo and for releasing your mod to the public)

## How to use this template

### **DO NOT FORK THIS REPOSITORY!**

1. Generate your repository from this template (click on Use This Template above). 

2. Clone your repository to your machine into a new folder in OWML's `Mods` folder. Name this folder [your name].[your unique mod ID]. More on this later. You can use GitHub desktop for this, then click the green "Code" dropdown and select open with GitHub Desktop.

3. Follow the instructions in [Outer Wilds New Horizons](https://nh.outerwildsmods.com/) on how to create planet config files. Place your config files into the `planets` folder in [your name].[your unique mod ID]. You can delete the `example_config` file in there while you're at it. When you're done you can commit the changes to your repo.

5. Edit `NewHorizonsTemplate/manifest.json`. It will look like this:

```
{
  "filename": "NewHorizonsConfig.dll", 
  "author": "[your name]",
  "name": "[your readable mod name]",
  "uniqueName": "[your name].[your unique mod ID]",
  "version": "0.1.0",
  "owmlVersion": "2.7.2",
  "dependencies": [ "xen.NewHorizons" ]
}
```

- Replace `[your name]` with how you want your name to appear in the mod database.
- Replace `[your readable mod name]` with how you want your mod to appear in the database.
- Replace `[your unique mod ID]` with whatever you want, as long as it isn't already in use by another mod. Adding `[your name]` as a prefix helps to prevent overlaps but isn't required.

6. Edit the `README.md` file (you can do this on GitHub in your browser) and be sure to add some nice pictures of your planets.

7. Select "Read and Write Permissions" under the `Actions > General` section of the repository settings![image](https://user-images.githubusercontent.com/25644444/168451761-43d3a0e7-c9a2-4f7f-b942-9aa7d5c3c793.png)

8. Releasing your mod: Be sure to try out the mod by adding it to your OWML mods folder and make sure it works in game before releasing. When you zip your final mod be sure to exclude the README.md file and the config.json file (they aren't needed in the release). When using the template when you update the manifest version from 0.0.0 to 0.1.0 or whatever you want, it will automatically make a new release. To make your mod show up in the Mod Manager and in [outerwildsmods.com](https://outerwildsmods.com), you need to add it to the database. [Click here to request for your mod to be added to the database](https://github.com/ow-mods/ow-mod-db/issues/new?labels=add-mod&template=add-mod.yml&title=%5BYour+mod+name+here%5D). Learn more about the Outer Wilds Mod Database in the [ow-mod-db repository](https://github.com/ow-mods/ow-mod-db).

9. Updating your mod. You can make any changes to your mod on your computer. Then from Github desktop you can commit and then push those changes to your repo online. When you are ready to release the new version of your mod, just changed the version number in `manifest.json`. Once the `manifest.json` version number is increased and pushed, a new release will automatically be created. 
