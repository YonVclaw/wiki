**Added in 4.3.31**
 
**Staging** or **Staging Zones** are a location were you can access our loadout and customization system from your ACE self interaction system. They are automatically created around a respawn (`respawn_west` markers or staging markers) and cover [60 meters around it](https://github.com/7Cav/cScripts/blob/master/cScripts/functions/init/fn_initStaging.sqf#L36) or Starter Crate and cover [25 meters surrounding the starter crate](https://github.com/7Cav/cScripts/blob/master/cScripts/functions/logistics/fn_doStarterCrate.sqf#L99).

This system is meant to eventually replace the starter crate entirely.

## Adding custom zones
**Added in 4.4.0**

It is possible to add custom staging zones by calling `cScripts_fnc_addStagingZone` in init.sqf or on a objectInit. The function accept markers and objects.
```cpp
[this, 12] call cScripts_fnc_addStagingZone
```

## See also
- [[Features]]
- [[Starter Crate]]
- [[Loadout|Gear]]