<img align="right" width="300" height="204" src="https://github.com/7Cav/cScripts/blob/master/resourses/wikigfx/Logistical_Crates.png">The logistical crates are several functions built to give players in the fieald a quick way to resupply and give logistical people a easier way to moving equipment around. When the system is applyed the crate will get the sprayed CAV insignia.

The functions is applied manually via Eden or can be spawned using a [[7Cav Moduel|7Cav-Modules]]. Only the supply crate is avalible as a module.

### Functions
```
[this,1] call cScripts_fnc_doSupplyCrate;

[this,1] call cScripts_fnc_doAmmoCrate;
[this,1] call cScripts_fnc_doExplosivesCrate;
[this,1] call cScripts_fnc_doGrenadesCrate;
[this,1] call cScripts_fnc_doLaunchersCrate;
[this,1] call cScripts_fnc_doMedicalCrate;
[this,1] call cScripts_fnc_doWeaponsCrate;

[this] call cScripts_fnc_doEmptyCrate;
```
### Syntax
**Syntax:** `[this, 1] call cScripts_fnc_[TYPE];`

**Parameters:**
```
 0: Crate <OBJECT>
 1: Scale cargo amount <NUMBER> (Default: 1)
```

**Return Value:** ```Nothing```

## See also
* [[Field Hospital]]
* [[Starter Crate]]