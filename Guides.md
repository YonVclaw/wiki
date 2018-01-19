# Moduel system
: _Requires: Achilles _
[initModules](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/init/fn_initModules.sqf)
```
["7Cav Logistics", "Create Starter Crate",{
    [(_this select 0)] call FUNC(moduleCreateStarterCrate);
}] call Ares_fnc_RegisterCustomModule;
```


[modules](https://github.com/7Cav/cScripts/tree/master/cScripts/CavFnc/functions/modules)


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