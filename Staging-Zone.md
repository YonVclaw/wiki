## Make a staging zone
The staging zone is automatically created around all `respawn_west` (_suffix `_0` up to `_10` does also work_) marker as well as our `Starter crate`.
You can also manually declare a zone using the following function:
```cpp
/* Arguments:
 * 0: Zone <OBJECT/STRING>
 * 1: Zone Size <NUMBER> (Optional) [Default; 12 meter]
*/
[this, 25] call cScripts_fnc_addStagingZone;
```
This function can be declared in `init.sqf` if you declare a VariableName of the object.

You can also place down a marker and name it `zone_staging` (_suffix `_0` up to `_15` does also work_). This will automatically get a zone of 60 meters around them

## See also
- [[Features]]
- [[Staging]] _(Feature)_
- [[Starter Crate]]
- [[Loadout|Gear]]
