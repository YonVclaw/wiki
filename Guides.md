# Moduel system
_Requires: Aries Achilles Expansion Addon_
Moduels are split in to 2 section the [initModuels.sqf](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/init/fn_initModules.sqf) were all moduels are defined, and the [modules](https://github.com/7Cav/cScripts/tree/master/cScripts/CavFnc/functions/modules) directly.

```
["7Cav Logistics", "Create Starter Crate",{
    [(_this select 0)] call FUNC(moduleCreateStarterCrate);
}] call Ares_fnc_RegisterCustomModule;
```



```
#include "..\script_component.hpp";

params ["_crate","_pos"];

_pos = _this select 0;

private _dialogResult = [
    "7th Cavalry Supply Crate",
    [
        ["Supply Size","SLIDER",1]
    ]
] call Ares_fnc_ShowChooseDialog;

if (count _dialogResult == 0) exitWith {};

private _supplieSize = _dialogResult select 0;

private _crate = "B_CargoNet_01_ammo_F" createVehicle _pos;
[_crate,_supplieSize] remoteExec ["cScripts_fnc_doSupplyCrate",0,true];
```