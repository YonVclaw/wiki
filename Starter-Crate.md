<img align="right" width="300" height="166" src="https://github.com/7Cav/cScripts/blob/master/resourses/wikigfx/Starter_Crate.png">The starter crate function transform a given object to a **7th Cavalry Start Crate** that allow you at the start of a mission, hence the name, to customize your gear, select a new loadout and/or add a insignia.

The crate inventory as well as loadout selections is based around a given platoon and, as default, only members of the given platoon will be able to select loadouts from this crate. (A player spawned in as charlie trooper will only be able to access a charlie crate loadouts. (This does not effect the crate inventory, jet.))

The function is applied manually via Eden or can be spawned using a [[7Cav Moduel|7Cav Moduels]].

### Syntax
**Syntax:** `[this,"none",true,true,true,true,false] call cScripts_fnc_doStarterCrate;`

**Parameters:**
```
 0: Object <OBJECT>
 1: Platoon <STRING>               (Default: "none") ["none","alpha","bravo","charlie","ranger","medical","full"]
 2: ReGear action <BOOL>          (Default: true)
 3: Heal action <BOOL>            (Default: true)
 4: Insignia Selection <BOOL>     (Default: true)
 5: Require Platoon variable <BOOL>  (Default: true)
 6: Arsenal <BOOL>                (Default: false)
```
**Return Value:** ```Nothing```

## See also
* [[Field Hospital]]
* [[Logistical Crates]]