# Overview

The [Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) mod is missing three entity definitions for it to properly apply its textures to permanently ruined ringworld sections.  It already has the correct graphics meshes, however the entity associations for the game to find them are missing.  This mod adds the three missing entities so that permanently ruined ringworld sections will can match the `machine_01` graphical culture - which includes sections destroyed by The Interloper with Origin: Shattered Ring.  In line with this mod's other prerequisite [Ringworld Graphical Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2628518102), habitable Machine ringworld sections feature animated clouds and use the Gaia planet textures (instead of continental).

This mod now also features enhancements to the Machine Shipset habitats.  The tier 1 and 2 habitats have both been adjusted - T1 is now color-matched to your empire flag, and T2 keeps its interior terrain after being upgraded.  The T3 habitats, which are mini-ringworlds, now display their terrain and feature animated clouds.

# Changes

This mod contains has four, very short new graphics entities.  It also replaces fire entries from the Machine Shipset to adjust the graphics definitions to apply the above effects.  All of these changes will only apply to empires with a graphical culture (shipset) of `machine_01`.

## Compatibility

Should work with practically everything that also works with Machine Shipset.  This mod is technically achievement compatible, but Machine Shipset and any of the dependencies for Origin: Shattered Ring graphics swaps are not.

Built for Stellaris version 3.1.\* "Lem."

### Required Dependency Mods

[Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) for the original graphics and other ship-related code.

[Ringworld Graphical Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2628518102) or [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) to apply the owner's graphical culture to the ringworld from Origin: Shattered Ring.

### Recommended Companion Mods

[Aesthetic Terraform Stations](https://steamcommunity.com/sharedfiles/filedetails/?id=2622411084) will give you back the very old-school terraform stations as visual markers for terraforming planets.

[Machine Shipset Add-on: Aesthetic Terraform Station Compatibility](https://steamcommunity.com/sharedfiles/filedetails/?id=2628972292) and this compatibility patch ensures the correct Machine Shipset graphics are used for the above terraform stations.  This mod adds missing graphical definitions to the Machine Shipset.

### Known Issues

In order to adjust the graphics for the Machine Shipset habitats, it was necessary to overwrite their entity definitions (text files which tell the game how to attach models and textures, and how to shade them).  Overriding a graphics entity causes an error log - expect five entries similar to these:

```
[17:08:32][pdx_entity.cpp:2583]: Duplicate of machine_01_habitat_core_entity added to entity system
[17:08:32][pdx_entity.cpp:2583]: Duplicate of machine_01_habitat_phase_01_entity added to entity system
[17:08:32][pdx_entity.cpp:2583]: Duplicate of machine_01_habitat_phase_02_entity added to entity system
[17:08:32][pdx_entity.cpp:2583]: Duplicate of machine_01_habitat_phase_03_entity added to entity system
[17:08:32][pdx_entity.cpp:2583]: Duplicate of machine_01_habitat_phase_03_section_entity added to entity system
```

## Changelog

* 1.0.0 Initial version
* 1.1.0 More visual enhancements:
    * Machine ringworlds are now colored with your empire's primary color
    * Machine ringworlds now have animated cloud cover
    * Machine ringworlds use the Gaia planet texture, to better match the planetview graphics
    * Machine habitats (phase 1) are now properly colored with their owner's primary color
    * Machine habitats (phase 2) now properly display their landmasses
    * Machine habitats (phase 3/fully-upgraded) now have landmasses (using a continental planet texture, in accordance with the planetview graphics) and now have animated cloud cover
* 1.2.0 Mark as compatible with Stellaris version 3.2 "Herbert" - no script changes

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/machine_shipset_destroyed_ringworld_entities)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.