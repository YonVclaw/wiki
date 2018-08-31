<img align="right" width="0" height="0" src=""> wip

The function is applied manually via Eden or can be spawned using a [[7Cav Moduel|7Cav-Modules]].

You can also aply flag texture manually in eden via the fields pressen sometimes in the object attributes. (Below you'll find the texture paths.)
```
//Crossed swords
cScripts\Data\Objects\Flag_7CAV_00.paa

// Crossed swords with Cut
cScripts\Data\Objects\Flag_7CAV_02.paa

// Black Coat of arms
cScripts\Data\Objects\Flag_7CAV_01.paa
```

### Syntax
**Syntax:** `[this, 0] call cScripts_fnc_flag;`

**Parameters:**
```
 0: Object <OBJECT>
 1: flagType <INTEGER>   (Default: 0)  [0 (Crossed swords),1 (Crossed swords with Cut),2 (Black Coat of arms)]
```

**Return Value:** ```Nothing```

## See also
* [[Starter Crate]]