This is a little function that allow you to give a unit a loadout from a scroll wheel action.
The function is useful for temporarily loadouts.
```cpp
/* Arguments:
 * 0: Object <OBJECT>
 * 1: Lable <STRING>
 * 2: Loadout <CLASSNAME / VARIABLE / LOADOUT ARRAY>
 */
[this, "My Custom Loadout", "My_Loadout_Classname"] call cScripts_fnc_addLoadoutAction;
[this, "Rifleman", "B_Soldier_F"] call cScripts_fnc_addLoadoutAction;
[this, "Apply a special variable loadout", "Variable_Name"] call cScripts_fnc_addLoadoutAction;
[this, "Go Nude", [[],[],[],[],[],[],"","",[],["","","","","",""]]] call cScripts_fnc_addLoadoutAction;
```
The function is applied manually via Eden on the objects init.

## See also,
- [fn_addLoadoutAction.sqf](https://github.com/7Cav/cScripts/blob/main/cScripts/functions/mission/fn_addLoadoutAction.sqf) _(Function)_
- [[Loadout (Gear)|Gear]]
- [[Starter Crate]]
- [[Staging]] _(Feature)_


