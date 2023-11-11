**Avalible only on dev branch**

The system is automatically enabled when zones are setup.
To enable the system place down any number of zone marker named using any of the following names:

* `cscripts_civilan_zone_high`
* `cscripts_civilan_zone_medium`
* `cscripts_civilan_zone_low`

_Zones can also have a suffix number exampe: `cscripts_civilan_zone_medium_92`._

The `high`, `medium` and `low` determince the chance of causing casualties here are the values:
```
high    0.40
medium  0.35
low     0.1
```

> **NOTE:** Using impropper naming for decety level the will default to medium numbers but it will also show decety type diary records.
> Example: `cscripts_civilan_zone_banana_123` will result in: "_The location have banana dencety._"

## See also
* [[Features]]
* [[Simulated Population Centers]]