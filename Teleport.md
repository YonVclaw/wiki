This function allow you to set a teleporter from and to any kind of object taking in consideration the height (Z) of the destination. Note that this will not be applied for MARKER, LOCATION and TASK.

```cpp
/* 0: Object <OBJECT>
 * 1: Label text <STRING>
 * 2: Destination <MARKER/OBJECT/LOCATION/GROUP/TASK>
 */

[this, "Teleport - Airfield", Airstrip] call Cav_Mission_fnc_teleport;
[this, "Teleport - Base", MyBase] call Cav_Mission_fnc_teleport;
[this, "Teleport - Talon", "FOB_Talon"] call Cav_Mission_fnc_teleport;
[this, "Teleport - Base", "respawn_west"] call Cav_Mission_fnc_teleport;

```
The function is applied manually via Eden on the objects init.

**This function has been moved to cavAddons.**

## See also
- [[Features]]
- [fn_gate.sqf](https://github.com/7Cav/cScripts/blob/main/cScripts/functions/mission/fn_teleport.sqf) _(Function)_
- [[Staging Zone]] _(Mission Makers)_
- [[Gate]]