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
    icon = "";
    scope = 0;
    category[] = {};
    loadout = [[],[],[],[],[],[],"","",[],["","","","","",""]];

    role = "";

    abilityMedic = 0;
    abilityEngineer = 0;
    abilityEOD = 0;

    insignia = "";

    preLoadout = "";
    postLoadout = "";
};
```
### Config Properties
```cpp
class CommonBlufor {};
class My_Loadout : CommonBlufor {
    regiment = "";       // Style value
    company = "";        // Used for selector filter and arsenal loadout name

    displayName = "";    // Selector display name shown in selectors and arsenal
    icon = "";           // classname of icon
    scope = 0;           // 0 private: not obtainable. 1 protected: can be used but not selected. 2 public: can be selected and used
    category[] = {};     // Hardcoded category paths found in ".\cScripts\CavFnc\functions\systems\fn_setupLoadoutCategories.sqf"
    loadout = [[],[],[],[],[],[],"","",[],["","","","","",""]]; // loadout array none quoted wraped

    role = "";           // Loadout role utalized by arsenal to figure out extended items [office, squadleader,  fireteamleader, medic]

    abilityMedic = 0;    // 0 Nothing, 1 Medic, 2 Doctor
    abilityEngineer = 0; // 0 Nothing, 1 Repair Specialists, 2 Engineer
    abilityEOD = 0;      // 0 Nothing, 1 EOD Specialist

    insignia = "";       // classname of a insignia

    preLoadout = "";     // code that gets applied befor loadout and abilities are applied
    postLoadout = "";    // code that gets applied after loadout and abilities are applied
};
```

## Loadout applications
<img align="right" width="300" height="105" src="https://github.com/7Cav/cScripts/blob/master/resourses/wikigfx/gear_applyloadout_examples.png">Loadouts can be applied in several ways. The main system used is the classname based system but it can also apply to units with specific **variableName** or **setVariable** or **side**. The loadout also need to be public or private scope inorder to be obtained, public to be selectable via selectors.
```cpp
this setVariable ["cScripts_Gear_LoadoutClass", "Cav_B_C_Rifleman_F"];
```

## See Also
- [[Staging]]
- [[Starter Crate]]
