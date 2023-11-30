**Avalible only on dev branch**

The system is automatically enabled when Zone Markers are placed down in eden editor with the correct naming `cScripts_Civilian_Zone_[DENSITY]_[NrSUFFIX]`.
Example zones with supported density naming are as follow:

* `cscripts_civilan_zone_extream`
* `cscripts_civilan_zone_high`
* `cscripts_civilan_zone_medium`
* `cscripts_civilan_zone_low`
* `cscripts_civilan_zone_none`

_Zones can also have a suffix number example: `cscripts_civilan_zone_medium_69`._

The `extream`, `high`, `medium`, `low` and `none` determine the chance of causing casualties here are the values:
```
extream 0.65  (65% Chance)
high    0.40  (40% Chance)
medium  0.25  (25% Chance)
low     0.1   (10% Chance)
none    0.0   ( 0% Chance)
```

## See also
* [[Features]]
* [[Simulated Population Centers]]