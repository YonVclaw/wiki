To add an insignia involve two steps; [creation and conversion of an image](#Image-and-format), [some minor scripting](#Image-to-cScripts)

## Image and format
First off you need the image in a PNG format with a transparent background with the size 512x512 that is converted to PAA the ARMA 3 image format. This is done with the Arma 3 Tools program; TexView2, ImageToPAA or [ARMAKE](https://github.com/KoffeinFlummi/armake)

## Image to cScripts
1. Naming the insignia (_Follow current name standard_).
1. Place your insignia in:
   [`cScripts`](https://github.com/7Cav/cScripts/tree/master/cScripts)`\`[`Data`](https://github.com/7Cav/cScripts/tree/master/cScripts/Data)`\`[`Insignia`](https://github.com/7Cav/cScripts/tree/master/cScripts/Data/Insignia)`\`
1. Add the new patch to [`CfgUnitInsignia.hpp`](https://github.com/7Cav/cScripts/blob/master/cScripts/CfgUnitInsignia.hpp)<br>
   To make it easy to add more insignias we have developed a [macro](https://github.com/7Cav/cScripts/blob/master/cScripts/script_macros.hpp#L39-L44) to be used:
   `MACRO_UNITINSIGNIA(CONFIGNAME,picture-name.paa);`
1. Add the insignia to the selector script; [`fn_initInsigniaSelections.sqf`](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/selections/fn_initInsigniaSelections.sqf)
   To make it easy for your self to add more insignia to the selector just copy paste an insignia function from a previous category.
   Example:
   ```
   [_object,"Squad Insignia 1/1/C/1-7","11C_17_Insignia","cScripts\Data\Insignia\1-1-C-17.paa",['ACE_MainActions','cScriptInsigniaSelectionMenu','cScriptInsigniaSelectionCharlie']] call FUNC(addInsigniaSelection);
   ```