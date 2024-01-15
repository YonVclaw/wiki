The gate function creates a automated open and close gate system without requirement of setting up triggers.

```cpp
/* Arguments:
 * 0: Object <OBJECT>
 * 1: Side <STRING> (Optional) (Default; WEST)
 * 2: Distance <STRING> (Optional) (Default; 30)
*/

["gate"] call cav_mission_fnc_gate;
["gate","WEST"] call cav_mission_fnc_gate;
["gate","WEST", 30] call cav_mission_fnc_gate;
```

The function is applied manually via Eden on the objects init.

## See also
- [[Features]]
- [fn_gate.sqf](https://github.com/7Cav/cScripts/blob/main/cScripts/functions/mission/fn_gate.sqf) _(Function)_
- [[Staging Zone]] _(Mission Makers)_
- [[Teleport]]