
# Logistical function

## Starter Crate
### Syntax
**Syntax:** `[this,"none",true,true,true,true,false] call cScripts_fnc_doStarterCrate;`

**Parameters:**
```
 0: Object <OBJECT>
 1: Quick Select Scale <STRING>   (Default: "none") ["none","alpha","bravo","charlie","ranger","medical","full"]
 2: ReGear action <BOOL>          (Default: true)
 3: Heal action <BOOL>            (Default: true)
 4: Insignia Selection <BOOL>     (Default: true)
 5: Platoon variable <BOOL>       (Default: true)
 6: Arsenal <BOOL>                (Default: false)
```
**Return Value:** ```Nothing```

## Field Hospital
### Syntax
**Syntax:** `[this, true, 1] call cScripts_fnc_doFieldHospital;`

**Parameters:**
```
 0: Crate <OBJECT>
 1: Medical Facility <BOOL> (Default: true)
 2: Scale cargo ammount <NUMBER> (Default: 1)
```

**Return Value:** ```Nothing```

## Equipment and supply crates
### Functions
```
[this,1] call cScripts_fnc_doAmmoCrate;
[this,1] call cScripts_fnc_doExplosivesCrate;
[this,1] call cScripts_fnc_doGrenadesCrate;
[this,1] call cScripts_fnc_doLaunchersCrate;
[this,1] call cScripts_fnc_doMedicalCrate;
[this,1] call cScripts_fnc_doSupplyCrate;
[this,1] call cScripts_fnc_doWeaponsCrate;
```
### Syntax
**Syntax:** `[this, 1] call cScripts_fnc_[TYPE];`

**Parameters:**
```
 0: Crate <OBJECT>
 1: Scale cargo amount <NUMBER> (Default: 1)
```

**Return Value:** ```Nothing```

## Empty Crate
### Syntax
**Syntax:** `[this] call cScripts_fnc_doEmptyCrate;`

**Parameters:**
```
 0: Crate <OBJECT>
```

**Return Value:** ```Nothing```