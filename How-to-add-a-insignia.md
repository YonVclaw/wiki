<img align="right" width="320" src="https://github.com/7Cav/cScripts/blob/master/resourses/wikigfx/Insignia_Crate.png">To add a image in to Arma you first need to [creation and conversion of an image](#Image-and-format). Upload it to the [7th Cavalry Community Addon](https://github.com/7Cav/7CavAddon) then [add it to the selector](#Image-to-cScripts)

## Image and format
First off you need the image in a PNG format with a transparent background with the size of 512x512.

This image should be converted to PAA  with DXT5 encode. This is done with the Arma 3 Tools program; TexView2, ImageToPAA or [ARMAKE](https://github.com/KoffeinFlummi/armake).
## Image to 7CavAddon and cScripts
1. Naming the insignia (_Follow current name standard_).
1. Add your insignia to the [insignia addon](https://github.com/7Cav/7CavAddon/tree/master/addons/insignia) located:
   [`7CavAddon`](https://github.com/7Cav/7CavAddon/tree/master/addons/insignia/)`\`[`Data`](https://github.com/7Cav/7CavAddon/tree/master/addons/insignia/data)
1. Add the new insignia to [`CfgUnitInsignia.hpp`](https://github.com/7Cav/7CavAddon/blob/master/addons/insignia/CfgUnitInsignia.hpp)<br>
   To make it easy to add more insignia's we have developed a [macro](https://github.com/7Cav/7CavAddon/blob/master/addons/insignia/CfgUnitInsignia.hpp#L2-L8) to be used:
   `MACRO_UNITINSIGNIA(insigna_name);`
1. _(OPTIONAL)_ If you add a complete new insignia remeber to also add the name to the [stringtable](https://github.com/7Cav/7CavAddon/blob/master/addons/insignia/stringtable.xml). 
1. Add the insignia to the selector script; [`fn_addInsigniaSelectionList.sqf`](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/systems/fn_addInsigniaSelectionList.sqf)
   To make it easy for your self to add more insignia to the selector just copy paste an insignia function from a previous category.
   Example:
   ```
   [_object,"Squad Insignia 1/1/C/1-7","Charlie_1_1","z\cav\addons\insignia\data\Charlie_1_1.paa",['ACE_MainActions','cScriptInsigniaSelectionMenu','cScriptInsigniaSelectionCharlie']] call FUNC(addInsigniaSelection);
   ```

## See also
* [[Starter Crate]] 
* [[Platoon & Squad Insignia's|Platoon and Squad Insignias]]