<img align="right" width="300" height="166" src="https://github.com/7Cav/cScripts/blob/main/resourses/wikigfx/Starter_Crate.png">The starter crate function transform a given object to a **7th Cavalry Start Crate** that allow you at the start of a mission, hence the name, to customize your gear, select a new loadout and/or add a insignia. The starter crate now creates a staging zone around it allowing for the same functionality as the create.

The crate inventory, as well as loadout selections, is based around a given platoon and, as default, only members of the given platoon will be able to select loadouts from this crate. (A player spawned in as Charlie trooper will only be able to access a charlie crate loadouts. (This does not affect the crate inventory, jet.))

The function is applied manually via Eden or can be spawned using a [[7Cav Moduel|7Cav-Modules]].
```cpp
/* Arguments:
 * 0: Object <OBJECT>
 * 1: Selection type <STRING>       (Default: "none")
 * 2: ReGear action <BOOL>          (Default: true)
 * 3: Heal action <BOOL>            (Default: true)
 * 4: Insignia Selection <BOOL>     (Default: true)
 * 5: Company variable <BOOL>       (Default: true)
 * 6: Arsenal <BOOL>                (Default: false)
 * 7: Staging <BOOL>                (Default: true)
 */

[this] call cScripts_fnc_doStarterCrate;
[this,"none",true] call cScripts_fnc_doStarterCrate;
[this,"none",true,true,true,true,false] call cScripts_fnc_doStarterCrate;
[this,"none",true,true,true,true,false,true] call cScripts_fnc_doStarterCrate;
```

## Alternative: Base Crate
There are a alternative function called Base Crate this have exsactly the same functionality to the startercrate with less parameters.

```cpp
/* Arguments:
 * 0: Object <OBJECT>
 * 1: Crate Type <STRING>       (Default: "none")
 */

[this] call cScripts_fnc_addBaseCrate;
[this, "charlie"] call cScripts_fnc_addBaseCrate;
[this, "all"] call cScripts_fnc_addBaseCrate;
```

## See also
* [[Field Hospital]]
* [[Logistical Crates]]
* [[How to add a insignia]]
* [[Regear Trooper Module]]