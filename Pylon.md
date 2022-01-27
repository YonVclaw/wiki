cScripts Pylon is a loadout system for vehicles.

## Adding a loadout
In order to add a loadout it is easiest to export the vehicles default loadout first inorder to get the turret numer. to get this run the following command in the debug console:
`magazinesAllTurrets cursorObject;`

When you now have this you can now edit this loadout to fit your needs.


### Loadout list

Path:
https://github.com/7cav/cscripts/blob/main/cScripts/functions/vehicle/fn_vehicle_getPylon.sqf

### Loadout Staging Selection Menu
This menu system is not automated. To add a menu item you need to create a pylon list.

Path: 
https://github.com/7Cav/cScripts/blob/main/cScripts/functions/vehicle/fn_vehicle_setupPylonCategories.sqf

### Spawn loadout

Path:
https://github.com/7Cav/cScripts/blob/main/cScripts/functions/vehicle/fn_vehicle_addPylonLoadout.sqf