**Added in 4.3.31**
 
**Staging** or **Staging Zones** are a location were you can access our loadout and customization system from your ACE self interaction system. They are automatically created around a respawn (`respawn_west` markers or staging markers) and cover [60 meters around it](https://github.com/7Cav/cScripts/blob/main/cScripts/functions/init/fn_init_staging.sqf#L58) or Starter Crate and cover [25 meters surrounding the starter crate](https://github.com/7Cav/cScripts/blob/main/cScripts/functions/logistics/fn_doStarterCrate.sqf#L94).

This system is meant to eventually replace the starter crate entirely.

## Adding custom zones
**Added in 4.4.0**

It is possible to add custom staging zones by calling `cScripts_fnc_addStagingZone` in init.sqf or on a objectInit. The function accept markers and objects.
```cpp
[this, 12] call cScripts_fnc_addStagingZone
```

### Trigger zone
**Added in 4.4.0**
It is possible to make a trigger to act as a stageing zone. You need to be a little bit carful with this system and follow the guide below carfully so you dont accedently give everyone on the map stageing options mid mission.

- **Type:** `None`
- **Activation:**: `AnyPlayer`
- **Activation Type:** `Present`
- **Condition:** `player inArea thisTrigger`
- **On Activation:** `cScripts_Staging_ZoneStatus = true;`
- **On Deactivation:** `cScripts_Staging_ZoneStatus = false;`

## See also
- [[Features]]
- [[Starter Crate]]
- [[Loadout|Gear]]