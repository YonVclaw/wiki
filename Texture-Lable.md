This function apply a texture to a given supported vehicle (see below). The function is applied manually via Eden or can be spawned using a [[7Cav Moduel]].

**Supported vehicles**
```
  C-130              3 PARMS     <LETTER and NUMBER> OR <SPECIAL>    (Locations: Tail)
  UH60 Black Hawks   2 PARMS     <LETTER and NUMBER> OR <SPECIAL>    (Locations: Tail)
  STRYKER            NONE        NONE                                (Locations: Front)
  MRAP               5 PARMS     <LETTER and NUMBER> OR <SPECIAL>    (Locations: Side)
  M1A1 Abrams        2 PARMS     <SPECIAL>                           (Locations: Front, Side)
  M2/M3 Bradley      1 PARMS     <SPECIAL>                           (Locations: Side)
```
**Supported textures**

-  `A`<sup>[1]</sup>
-  `B`<sup>[1]</sup> 
-  `C`<sup>[1]</sup>
-  `S`<sup>[1]</sup> 
-  `0` to `9`<sup>[1]</sup><sup>[2]</sup>
-  `line`<sup>[A]</sup> 
-  `stryker`<sup>[B]</sup> 
-  `vic1` 
-  `vic2` 
-  `vic3` 
-  `vic4` 
-  `vic5` 
-  `vic6`

<sup>[1]</sup> UH60 Black Hawks have a special variant of this texture when in use. <br>
<sup>[2]</sup> C-130 have a special variant of this texture when in use. <br>
<sup>[A]</sup> This texture is automatically applyed to the UH 60 when using two parmeters `"B","2"`. <br>
<sup>[B]</sup> Gets applied to the striker front no arguments required. <br>

### Syntax
**Syntax:** `[this,"","","","","","","","",""] call cScripts_fnc_setVehicleLable`

**Parameters:**
```
 0: Vehicles <OBJECT>
 1: Texture <STRING> (Optional)
 2: Texture <STRING> (Optional)
 3: Texture <STRING> (Optional)
 4: Texture <STRING> (Optional)
 5: Texture <STRING> (Optional)
 6: Texture <STRING> (Optional)
 7: Texture <STRING> (Optional)
 8: Texture <STRING> (Optional)
 9: Texture <STRING> (Optional)
```
**Return Value:** ```Nothing```

### Example usage
```
 [this] call cScripts_fnc_setVehicleLable
 [this,"vic1"]
 [this,"B","5"] call cScripts_fnc_setVehicleLable
```

## See also