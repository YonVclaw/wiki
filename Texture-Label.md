This function applies a texture to a given supported vehicle (see below). All textures are per default available but any kind of texture can be used. Some textures have multiple behaviours depending on the vehicle. For instance, a UH60 tail number have smaller numbers then a C-130 tail number for instance.
The function is applied manually via Eden or can be spawned using a [[7Cav Moduel|7Cav-Modules]].

**Supported vehicles**
```
  C-130              3 PARMS     <LETTER and NUMBER> OR <SPECIAL>    (Locations: Tail)
  UH60 Black Hawks   2 PARMS     <LETTER and NUMBER> OR <SPECIAL>    (Locations: Tail)
  STRYKER            NONE        NONE                                (Locations: Front)
  MRAP               5 PARMS     <LETTER and NUMBER> OR <SPECIAL>    (Locations: Side)
  M1A1 Abrams        2 PARMS     <SPECIAL>                           (Locations: Front, Side)
  M2/M3 Bradley      1 PARMS     <SPECIAL>                           (Locations: Side)
```
**Texture library**
<img align="right" width="300" height="210" src="https://github.com/7Cav/cScripts/blob/main/resourses/wikigfx/Texture_Lable.png">
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

**Other textures**

To use other custom textures as a vehicle label by using the full path to the texture. Exsample: `cScripts\Data\Insignia\1-1-C-17.paa`

### Syntax
**Syntax:** `[this,"","","","","","","","",""] call cScripts_fnc_setVehicleLable`

**Parameters:**
```cpp
/* Arguments:
 * 0: Vehicles <OBJECT>
 * 1: Texture <STRING> (Optional)
 * 2: Texture <STRING> (Optional)
 * 3: Texture <STRING> (Optional)
 * 4: Texture <STRING> (Optional)
 * 5: Texture <STRING> (Optional)
 * 6: Texture <STRING> (Optional)
 * 7: Texture <STRING> (Optional)
 * 8: Texture <STRING> (Optional)
 * 9: Texture <STRING> (Optional)
 */

[this] call cScripts_fnc_setVehicleLable;
[this,"B","5"] call cScripts_fnc_setVehicleLable;
[this,"RedCross"] call cScripts_fnc_setVehicleLable;
[this,"RedCross","RedCross","S","6"] call cScripts_fnc_setVehicleLable;
```

## See also
* [[Vehicle Settings and Functions|Vehicle Settings and Functions]] 
* [[Vehicle Loadouts|Vehicle Loadouts]] 