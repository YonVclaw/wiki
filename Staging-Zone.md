## Make a staging zone
The staging zone is automatically created around all `respawn_west` (_number suffix `_123` also work_) marker as well as our `Starter crate`. They cover 60 meters around the marker and 25 meter around the create location.
You can also manually declare a zone using the magic marker name `zone_staging` (see below) or by using the following function:
```cpp
/* Arguments:
 * 0: Zone <OBJECT/STRING/ARRAY>
 * 1: Zone Size <NUMBER/STRING> (Optional) [Default; 12]
 */

[this] call cScripts_fnc_addStagingZone
[this, 3] call cScripts_fnc_addStagingZone
["zone_staging", 12] call cScripts_fnc_addStagingZone
["respawn_west", 12] call cScripts_fnc_addStagingZone
[[10,25,0], 12] call cScripts_fnc_addStagingZone
["ShapedZoneMarker", "RECTANGLE"] call cScripts_fnc_addStagingZone
["ShapedZoneMarker", "ELLIPSE"] call cScripts_fnc_addStagingZone
```
This function can be declared in `init.sqf` if you declare a VariableName of the object.

You can also place down a marker and name it `zone_staging` (_number suffix `_123` does also work_). This will automatically get a zone of 60 meters around them

## Zeus
### Disable/Enable all staging zones
Zeus can via a module disable access to all staging zones.

### Enable staging everywere
It is possible as Zeus to enable staging zones for all or targeted soldier using code execution.

Global execution will enable the staging zones for all player JIP players will not be effected.

```hpp
cScripts_Staging_ZoneStatus = true;
```
## Mission settings
### Disable staging system
It is possible to disable staging system in the mission settings under the staging category.

### Allow all loadouts
It is possible to removing the company blocker for loadouts in the missing settings under the staging category.

## See also
- [[Features]]
- [[Staging]] _(Feature)_
- [[Starter Crate]]
- [[Loadout|Gear]]
