# Overview

The [Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) mod is missing three entity definitions for it to properly apply its textures to permanently ruined ringworld sections.  It already has the correct graphics meshes, however the entity associations for the game to find them are missing.  This mod adds the three missing entities so that permanently ruined ringworld sections will can match the `machine_01` graphical culture - which includes sections destroyed by The Interloper with Origin: Shattered Ring.  In line with this mod's other prerequisite [Ringworld Graphical Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2628518102), habitable Machine ringworld sections feature clouds and use the Gaia planet textures (instead of continental).

This mod also features enhancements to the Machine Shipset habitats.  The tier 1 and 2 habitats have both been adjusted - T1 is color-matched to your empire flag, and T2 keeps its interior terrain after being upgraded.  The T3 habitats, which are mini-ringworlds, display their terrain and feature clouds.

Note: as of Stellaris version 3.7 "Canis Minor" changes to shaders mean that Machine ringworlds and T3 habitats no longer have animated clouds.

# Changes

This mod contains has four, very short new graphics entities.  It also replaces fire entries from the Machine Shipset to adjust the graphics definitions to apply the above effects.  All of these changes will only apply to empires with a graphical culture (shipset) of `machine_01`.

## Compatibility

Should work with practically everything that also works with Machine Shipset.

Built for Stellaris version 3.7 "Canis Minor" and backwards-compatible with versions 3.6 "Orion," 3.5 "Fornax," 3.4 "Cepheus," 3.3 "Libra," 3.2 "Herbert," 3.1 "Lem," and 3.0 "Dick."  Not compatible with achievements, but neither are the dependencies.

### Required Dependency Mods

* [Machine Shipset](https://steamcommunity.com/sharedfiles/filedetails/?id=2077186491) for the original graphics and other ship-related code
* [Ringworld Graphical Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2628518102) or [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) to apply the owner's graphical culture to the ringworld from Origin: Shattered Ring

### Recommended Companion Mods

* [Aesthetic Terraform Stations](https://steamcommunity.com/sharedfiles/filedetails/?id=2622411084) will give you back the very old-school terraform stations as visual markers for terraforming planets
* [Machine Shipset Add-on: Aesthetic Terraform Station Compatibility](https://steamcommunity.com/sharedfiles/filedetails/?id=2628972292) and this compatibility patch ensures the correct Machine Shipset graphics are used for the above terraform stations.  This mod adds missing graphical definitions to the Machine Shipset

### Known Issues

In order to adjust the graphics for the Machine Shipset habitats, it was necessary to overwrite their entity definitions (text files which tell the game how to attach models and textures, and how to shade them).  Overriding a graphics entity causes an error log - expect five entries similar to these:

```
[04:32:01][graphics/pdx_entity.cpp:2546]: Duplicate of machine_01_habitat_core_entity added to entity system
[04:32:01][graphics/pdx_entity.cpp:2546]: Duplicate of machine_01_habitat_phase_01_entity added to entity system
[04:32:01][graphics/pdx_entity.cpp:2546]: Duplicate of machine_01_habitat_phase_02_entity added to entity system
[04:32:01][graphics/pdx_entity.cpp:2546]: Duplicate of machine_01_habitat_phase_03_entity added to entity system
[04:32:01][graphics/pdx_entity.cpp:2546]: Duplicate of machine_01_habitat_phase_03_section_entity added to entity system
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
* 1.3.0 Mark as compatible with Stellaris version 3.3 "Libra" - no script changes
* 1.4.0 Mark as compatible with Stellaris version 3.4 "Cepheus" - no script changes
* 1.5.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax") - minor, backwards compatible tweaks
* 1.6.0 Add support for destroyed Machine dyson spheres (entity missing from the original mod)
* 1.7.0 Add compatibility trigger for other mods to check whether this one is active
    * Fix incorrect mesh for construction seams
* 1.8.0 Mark as compatible with Stellaris version 3.7 "Canis Minor" - no script changes

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/machine_shipset_destroyed_ringworld_entities)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.