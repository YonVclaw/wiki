cScripts Gear are our loadout script stronly inspired and taken from [Poppy](https://github.com/BaerMitUmlaut/Poppy/), our old loadout script. The gear system is rewritten and is greatly tailored to our community needs and have a extra simplification added to it. The loadout utalized a loadout array obtained from earher a ace export loadout or the bis [`getUnitLoadout`](https://community.bistudio.com/wiki/getUnitLoadout) script command. The config also for custumizing and can handle abilities and unit cosmetics such as rank and insignia.

### Loadouts
Loadouts are automatically applied to units on spawn based on the variable, variableName, classname or side. Loadouts are also saved when altered (*See below*). Loadouts using `Public` scope (*[See below](https://github.com/7Cav/cScripts/wiki/Gear#how-to-gear-up)*) in the config will also be pressent in loadout selectors such as ACE Arsenal default loadouts and [[staging]] and [[starter crate]] selectors.

### Loadout Saving
When you alter your loadout it automatically get saved and reapplied on respawn. The save event is run when you alter the loadout in arsenal or open the starter crate inventory. All gear related functions will honer the saved loadout. Permissions are also kept based on the core loadout used befor the save was committed.

## How to gear up
The gear system is quite simple it utalized config values to obtain and apply your loadout. The values are inherited from parent classnames.

```cpp
class CommonBlufor {};
class My_Loadout : CommonBlufor {
    regiment = "";
    company = "";

    displayName = "";
    scope = 0;
    category[] = {};
    loadout = [[],[],[],[],[],[],"","",[],["","","","","",""]];
    insignia = "";

    abilityMedic = 0;
    abilityEngineer = 0;
    abilityEOD = 0;

    preLoadout = "";
    postLoadout = "";
};
```
### Config Properties
- `regiment` (*STRING*) Style value
- `company` (*STRING*) Platoon prefix shown in documents and ACE Arsenal.
- `displayName` (*STRING*) Loadout name shown in documents Loadout selection menus and ACE Arsenal.
- `scope` (*NUMBER*) 0 PRIVATE, 1 PROTECTED, 2 PUBLIC. This is used to destinguish loadout types as well as for the script to know what is allowed to use for ACE Arsenal loadout and selectors. `PRIVATE` means that the the loadout will not be applied or used. `PROTECTED` means it can be applied but not added to any selectors. `PUBLIC` means it can be used and will be used by ACE Arsenal and selectors
- `category[]` (*ARRAY*) Under where the loadout should be placed this values are for the time being hardcoded and can be [found here](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/systems/fn_setupLoadoutCategories.sqf).
- `loadout` (*STRING ARRAY*) Loadout array with no wrapping quote
- `insignia` (*STRING*) classname for a insignia
- `abilityMedic` (*NUMBER*) 0 Nothing, 1 Medic, 2 Doctor
- `abilityEngineer` (*NUMBER*) 0 Nothing, 1 Repair Specialists, 2 Engineer
- `abilityEOD` (*NUMBER*) 0 Nothing, 1 EOD Specialist
- `preLoadout` (*STRING CODE*) This gets applied befor loadout and abilities are applied
- `postLoadout` (*STRING CODE*) This gets applied after loadout and abilities are applied

## Loadout applications
<img align="right" width="300" height="105" src="https://github.com/7Cav/cScripts/blob/master/resourses/wikigfx/gear_applyloadout_examples.png">Loadouts can be applied in several ways. The main system used is the classname based system but it can also apply to units with specific **variableName** or **setVariable** or **side**. The loadout also need to be public or private scope inorder to be obtained, public to be selectable via selectors.
```cpp
this setVariable ["cScripts_Gear_LoadoutClass", "Cav_B_C_Rifleman_F"];
```

## See Also
- [[Staging]]
- [[Starter Crate]]
