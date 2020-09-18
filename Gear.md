cScripts Gear are our loadout heavenly built appon [Poppy](https://github.com/BaerMitUmlaut/Poppy/) our old loadout script. Gear uses similar setup but is more tailored to our community needs. The loadout utalized a loadout array obtained from earher a ace export loadout or the bis `getUnitLoadout` script command. The config also handle permissions, abilities and cosmetics.

### Loadouts
Loadouts are automatically applied to units soon spawn based on the variable, variableName, classname or side.

### Loadout Saving
When you alter your loadout it automatically get saved and reapplied on respawn. The save event is run when you alter the loadout in arsenal or open the starter crate inventory. All gear related functions will honer the saved loadout. Permissions are also kept based on the core loadout used befor the save was committed.

## How to gear up
The gear system is quite simple it utalized config values to obtain and apply your loadout.

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
- `Regiment` (*STRING*) Value is not used yet
- `Company` (*STRING*) Platoon prefix shown in documents and ACE Arsenal.
- `displayName` (*STRING*) Loadout name shown in documents and ACE Arsenal.
- `category[]` (*ARRAY*) Under where the loadout should be placed this values are for the time being hardcoded and are listed below.
- `loadout` (*STRING ARRAY*) a loadout array with no wrapping quote
- `insignia` (*STRING*) classname for a insignia
- `abilityMedic` (*NUMBER*) 0 nothing, 1 Medic, 2 Doctor
- `abilityEngineer` (*NUMBER*)
- `abilityEOD` (*NUMBER*)
- `preLoadout` (*STRING CODE*)
- `postLoadout` (*STRING CODE*)

## See Also
- [[Staging]]
- [[Starter Crate]]
