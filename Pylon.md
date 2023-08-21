This article handle how you setup, change and modify loadouts for our vehicle loadout system pylon.
The loadout system allow you to quickly select a predefined template and equip your vehicle with it. The actions are added when the vehicle is inside of a staging zone.

## Adding and modifying loadout

### Obtain and Change Loadout
In order to add or mosify loadout it is easiest to export the vehicles current magazines first inorder to get the turret index.
Tondo this its easiets to run the folowing command in the debug console when looking at the vehicle:

```cpp
magazinesAllTurrets cursorObject;
```
Some times you can modifie the ammunition types and so on in the eden object view. 
When doing so you can then export diffrent magazines wirhout opening the config viewer.


For aircrafts this is diffent and more simple however.
First fo you can change the pylon of the given aircraft directly on the object view 
 
> ***NOTE:** Sometimes you are blocled form selecting a specific pylon.
> However in cScripts we dont care about this limitaion when applying and can apply anything anywhere.*

Once we happy with our loadout, we can now export it using the following command in the debug console while looning at the aircraft.

```cpp
getPylonMagazines cursorObject
```

### Loadout format
Each export return a one liner long array what we do is to reformat it to make it more readable and manageable.
The loadout system support 2 types of formats the vehicle magazine array with the id and owner part at the end removed. For aircrafts the pylon return a much simpler array with each item (usually) represent left to right wing position.

Below you can find exsample formaring.

#### Ground vehicles
```hpp
    [ "default", [
        ["rhs_mag_smokegen",[-1],999],
        ["rhs_mag_M829A3_max",[0],28],
        ["rhs_mag_M830A1_max",[0],16],
        ["rhs_mag_762x51_M240_1200",[0],1200],
        ["rhs_mag_762x51_M240_1200",[0],1200],
        ["rhs_mag_762x51_M240_1200",[0],1200],
        ["rhs_mag_762x51_M240_1200",[0],1200],
        ["rhs_mag_762x51_M240_1200",[0],1200],
        ["rhs_mag_762x51_M240_1200",[0],1200],
        ["rhs_mag_762x51_M240_1200",[0],1200],
        ["rhs_mag_762x51_M240_1200",[0],1200],
        ["rhs_LaserFCSMag",[0],99],
        ["rhs_LaserFCSMag",[0],99],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhs_mag_100rnd_127x99_mag_Tracer_Red",[0,0]],
        ["rhsusf_mag_L8A3_12",[0,0],12],
        ["rhs_mag_762x51_M240_200",[0,2]],
        ["rhs_mag_762x51_M240_200",[0,2]],
        ["rhs_mag_762x51_M240_200",[0,2]]
    ]]
```
#### Airframes
```cpp
    ["default", [
        "USAF_PylonRack_2Rnd_AIM9X_LAU105",
        "USAF_PylonRack_1Rnd_ANAAQ28",
        "USAF_PylonRack_2Rnd_AGM65K",
        "USAF_PylonRack_1Rnd_GBU54",
        "USAF_PylonRack_1Rnd_GBU12",
        "",
        "USAF_PylonRack_1Rnd_GBU12",
        "USAF_PylonRack_1Rnd_GBU54",
        "USAF_PylonRack_2Rnd_AGM65D",
        "USAF_PylonRack_7Rnd_APKWS",
        "USAF_PylonRack_1Rnd_ANALQ131"
    ]]
```

### Add Loadout
Now when we have a array containing our pylon can now add it or edit it to fit your needs better.
In the file [`cScripts/functions/vehicle/fn_vehicle_getPylon.sqf`](https://github.com/7cav/cscripts/blob/main/cScripts/functions/vehicle/fn_vehicle_getPylon.sqf)
we define all our loadouts.
The loadout file have 2 parts the actuall loadouts then the vehicle kind that reference the loadout.

```cpp
private _rhsusf_m1a1tank_base = createHashMapFromArray [
    ["hard",    [ /* SNIPP */ ]],
    ["default", [ /* SNIPP */ ]],
    ["hard",    [ /* SNIPP */ ]]
];

// Loadout vehicle list
private _pylons = createHashMapFromArray [
    ["rhsusf_m1a1tank_base", _rhsusf_m1a1tank_base]
];
```

### Add laodout to selector

> **WIP**

[`cScripts/functions/vehicle/fn_vehicle_setupPylonCategories.sqf`](https://github.com/7Cav/cScripts/blob/main/cScripts/functions/vehicle/fn_vehicle_setupPylonCategories.sqf)

```cpp
if (_vehicle iskindOf "rhsusf_m1a1tank_base") then {
    _pylonList = [
        // TypeOf,               DisplayName,   Name,           Icon
        ["rhsusf_m1a1tank_base", "Hard",        "hard",         ""],
        ["rhsusf_m1a1tank_base", "Soft",        "soft",         ""],
        ["rhsusf_m1a1tank_base", "Default",     "default",      ""]
    ];
};
```


## Defaut Loadout
> NOTE: Default loadouts in <4.5.1 are manually defined.<br />
>They are defined in [`cScripts/functions/vehicle/fn_vehicle_addDefaultLoadout.sqf`](https://github.com/7Cav/cScripts/blob/main/cScripts/functions/vehicle/fn_vehicle_addDefaultLoadout.sqf).<br />
> In >4.5.2 they are automatically applied.

Loadouts that are named `default` are automatically applied to a vehicle. If non-exist none will be applied.

## See also
* [[Vehicle Pylon]] (Feature)
* [[Vehicle Customization|Vehicle Customization]] 
* [[Vehicle Texture Label|Texture Label]] 
