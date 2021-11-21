**Added in: 4.4.0**

cScripts allow vehicles, defined by the CBA Setting Vehicle faction array, to be changed so to better retrofitted to better fit our needs and our way to play. The system changes vehicle cargo, appearance and radio.

This system also allow for radio to be predefined inside of the vehicles radios.

## M1A1 Abrams
### Tank Aperence
It is possible when you are inside of a staging zone to customize your Abrams. To do this open the Tank self interactions when occupying a crew seat. Here you can declare a tank callsign as well as a specific barrel art.

### Flag
When turned out it is possible to put up or take down the unit flag.

## Vehicle type
Per default the type of vehicle is automatically determined by its classname.

### Rack Radio

### Special vehicle type
But there are some special classes. Namely `MED` or `EMPTY`. The `MED` is used for setting vehicles to classes them as a medical vehicle and give it medical supplies and `EMPTY` make the inventory blank. 

```
this getVariable ["cScripts_Vehicle_Type", typeOf this];
this getVariable ["cScripts_Vehicle_Type", "EMPTY"];
this getVariable ["cScripts_Vehicle_Type", "MED"];
```

## See also
* [[Features]]
* [[Vehicle Settings and Functions|Vehicle Settings and Functions]] 
* [[Vehicle Texture Label|Texture Label]] 
