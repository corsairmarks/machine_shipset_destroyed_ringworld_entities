# Overview

The [Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) mod is missing three entity definitions for it to properly apply its textures to permanently ruined ringworld sections.  It already has the correct graphics meshes, however the entity associations for the game to find them are missing.  This mod adds the three missing entities so that permanently ruined ringworld sections will can match the `machine_01` graphical culture - which includes sections destroyed by The Interloper with Origin: Shattered Ring.

# Changes

This mod contains has three, very short graphics entities.  They will only apply to empires with a graphical culture (shipset) of `machine_01`.

## Compatibility

Should work with practically everything that also works with Machine Shipset.  This mod is technically achievement compatible, but Machine Shipset and any of the dependencies for Origin: Shattered Ring graphics swaps are not.

### Required Dependency Mods

[Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) for the original graphics and other ship-related code.

[Ringworld Graphical Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2628518102), [Shattered Ring Shipset Fix](https://steamcommunity.com/sharedfiles/filedetails/?id=2566249278), or [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) to apply the owner's graphical culture to the ringworld from Origin: Shattered Ring.

### Recommended Companion Mods

[Aesthetic Terraform Stations](https://steamcommunity.com/sharedfiles/filedetails/?id=2622411084) will give you back the very old-school terraform stations as visual markers for terraforming planets.

[Machine Shipset Add-on: Aesthetic Terraform Station Compatibility]() and this compatibility patch ensures the correct Machine Shipset graphics are used for the above terraform stations.  This mod adds missing graphical definitions to the Machine Shipset.

## Changelog

* 1.0.0 Initial version

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/machine_shipset_destroyed_ringworld_entities)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.