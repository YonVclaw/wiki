This function allow you to set a teleporter from and to any kind of object taking in consideration the height (Z) of the destination. Note that this will not be applied for MARKER, LOCATION and TASK.

```cpp
/* 0: Object <OBJECT>
 * 1: Label text <STRING>
 * 2: Destination <MARKER/OBJECT/LOCATION/GROUP/TASK>
 */

[this, "Teleport - Airfield", Airstrip] call cScripts_fnc_teleport;
[this, "Teleport - Base", MyBase] call cScripts_fnc_teleport;
[this, "Teleport - Talon", "FOB_Talon"] call cScripts_fnc_teleport;
[this, "Teleport - Base", "respawn_west"] call cScripts_fnc_telepor;

```
The function is applied manually via Eden on the objects init.

## See also
* [fn_teleport.sqf](https://github.com/7Cav/cScripts/blob/main/cScripts/functions/mission/fn_teleport.sqf) _(Function)_
* [[Loadout Button]]
* [[Gate]]