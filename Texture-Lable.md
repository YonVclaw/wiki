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

  A<sup>[1]</sup> \n
  B<sup>[1]</sup> \n
  C<sup>[1]</sup> \n
  S<sup>[1]</sup> \n
  0 to 9<sup>[1]</sup><sup>[2]</sup>

<sup>[1]</sup> UH60 Black Hawks have a special variant of this texture when in use.
<sup>[2]</sup> C-130 have a special variant of this texture when in use.

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

## See also
* [[Logistical Crates]] [[Field Hospital]]