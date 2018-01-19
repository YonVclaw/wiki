# Add a moduel
_Requires: Aries Achilles Expansion Addon_

Moduels are split in to 3 section the [initModuels.sqf](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/init/fn_initModules.sqf) were all moduels are defined and the [modules](https://github.com/7Cav/cScripts/tree/master/cScripts/CavFnc/functions/modules) directly were the functions are located. The final section is the function you call for.

# Add a new moduel
To add a moduel you need to first create the function. Place the moduel in the... (WIP) 


```
["7Cav Logistics", "Create Starter Crate",{
    [(_this select 0)] call FUNC(moduleCreateStarterCrate);
}] call Ares_fnc_RegisterCustomModule;
```


Here is the exsample on location based placement moduel.
```
#include "..\script_component.hpp";

params ["_crate","_pos"];

_pos = _this select 0; 

// Defining dialog options
private _dialogResult = [
    "Topic Shown In The Spawn Window",
    [
        ["My slider option with 0 to 1 set as default 1","SLIDER",1], 
        ["My bool action with false as default",["True lable","false"],1],
        ["My multi selector with default Empty",["Full","Half Full","Half Empty","Empty"],3]
    ]
] call Ares_fnc_ShowChooseDialog;

// Exit if no option is selected or you abort.
if (count _dialogResult == 0) exitWith {};

// Add dialog option values
private _firstSliderOption = _dialogResult select 0;
private _secondBoolOption = if (_dialogResult select 1 == 0) then {true} else {false};
private _thirdSelectionOption = switch (_dialogResult select 2) do {
    case 0: {"stringOptionA";};
    case 1: {"stringOptionB";};
    case 2: {"stringOptionC";};
    case 3: {"stringOptionD";};
};

// Applying moduel effects
[_firstSliderOption,_secondBoolOption, _thirdSelectionOption] remoteExec ["cScripts_fnc_exampleFunction",0,true];
```

Here is a Exsample for a object placed moduel
```
#include "..\script_component.hpp";

params ["_vehicle"];

_vehicle = [_logic, false] call Ares_fnc_GetUnitUnderCursor;
_vehicleType = ["RHS_UH60M_d", "RHS_UH60M_MEV2_d", "RHS_UH60M_MEV_d", "RHS_UH60M", "RHS_UH60M_MEV2", "RHS_UH60M_MEV"];

if (typeOf _vehicle in _vehicleType) then {

    _dialogResult = [
        "Helicopter Tailnumber Selection",
        [
            ["Tail number",["B1","B2","B3","B4"],0]
        ]
    ] call Ares_fnc_ShowChooseDialog;

    _texture = switch (_dialogResult select 0) do {
        case 0: {"b1";};
        case 1: {"b2";};
        case 2: {"b3";};
        case 3: {"b4";};
    };

    [_vehicle,_texture] remoteExec ["cScripts_fnc_UH60TailNumber",0,true];
} else {
    ["No or wrong type helicopter selected!"] call Ares_fnc_ShowZeusMessage;
    playSound "FD_Start_F";
};
```