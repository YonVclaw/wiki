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

## See also