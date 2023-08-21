This article handle how you setup, change and modify loadouts for our vehicle loadout system pylon.
The loadout system allow you to quickly select a predefined template and equip your vehicle with it. The actions are added when the vehicle is inside of a staging zone.

## Adding and modifying loadout
In order to add or mosify loadout it is easiest to export the vehicles current magazines first inorder to get the turret index.
Tondo this its easiets to run the folowing command in the debug console when looking at the vehicle:

```
magazinesAllTurrets cursorObject;
```
Some times you can modifie the ammunition types and so on in the eden object view. 
When doing so you can then export diffrent magazines wirhout opening the config viewer.


For aircrafts this is diffent and more simple however.
First fo you can change the pylon of the given aircraft directly on the object view 
 
> ***NOTE:** Sometimes you are blocled form selecting a specific pylon.
> However in cScripts we dont care about this limitaion when applying and can apply anything anywhere.*

Once we happy with our loadout, we can now export it using the following command in the debug console while looning at the aircraft.

```
getPylonMagazines cursorObject
```

Now when we have a array containing our pylon can now add it or edit it to fit your needs better.

In the file [cScripts/functions/vehicle/fn_vehicle_getPylon.sqf](https://github.com/7cav/cscripts/blob/main/cScripts/functions/vehicle/fn_vehicle_getPylon.sqf)
We you define the loadout.

### Loadout list
All loadouts used are handled by the getPylon script file.
This file is called when you reference the loadout on it's creation or application.

Path:
https://github.com/7cav/cscripts/blob/main/cScripts/functions/vehicle/fn_vehicle_getPylon.sqf

### Loadout Staging Selection Menu
This menu system is not automated. To add a menu item you need to create a pylon list.

Path: 
https://github.com/7Cav/cScripts/blob/main/cScripts/functions/vehicle/fn_vehicle_setupPylonCategories.sqf

### Spawn loadout

Path:
https://github.com/7Cav/cScripts/blob/main/cScripts/functions/vehicle/fn_vehicle_addPylonLoadout.sqf