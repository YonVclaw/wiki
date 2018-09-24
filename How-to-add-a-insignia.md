To add an insignia involve two steps; [creation and conversion of an image](#Image-and-format) and [some minor scripting](#Image to cScripts)

## Image and format
First off you need the image in a PNG format with a transparent background with the size 512x512 that is converted to PAA the ARMA 3 image format. This is done with the Arma 3 Tools program; TexView2, ImageToPAA or [ARMAKE](https://github.com/KoffeinFlummi/armake)

## Image to cScripts
1. Naming the insignia (_Follow current name standard_).
1. Place your insignia in:
   `cScripts\Data\Insignia\`
1. Add the new patch to `cScripts\`[`CfgUnitInsignia.hpp`](https://github.com/7Cav/cScripts/blob/master/cScripts/CfgUnitInsignia.hpp)
   To make it easy for your self the following macro:
   `MACRO_UNITINSIGNIA(CONFIGNAME,picture-name.paa);`