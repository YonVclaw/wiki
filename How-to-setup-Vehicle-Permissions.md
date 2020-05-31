The cScripts Vehicle Permissions utilizes the CBA event handlers applied to vehicles automatically and is enabled via [[CBA Mission Settings]]. The restrictions are automatically applied to all Tanks, Helicopters, Planes, APC, and IFV of all factions and sides. Making it impossible for a Player not trained to operate a aircraft to steal and operate enemy aircraft's.

# How to
To enable the **Restrict Vehicle Usage** under **Custom Initialization** setting in [[CBA Mission Settings]].

To allow a unit to operate a vehicle you are required to apply a player variable.
This is done automatically via cScripts built in units but for custom units loadouts and factions this is to be applied manually.

To add a vehicle training simply add a the variable `cScripts_player_AllowedVehicle` and define the vehicle group or classname of the given vehicle or vehicles. Below you can see examples on how to apply:
```
_this setVariable ["cScripts_player_AllowedVehicle", []]; // None allowed vehicles (default)
_this setVariable ["cScripts_player_AllowedVehicle", ["AllVehicles"]]; // Allow all available vehicles
_this setVariable ["cScripts_player_AllowedVehicle", ["Helicopters"]]; // Allow all helicopters
_this setVariable ["cScripts_player_AllowedVehicle", ["RHS_UH60M_d"]]; // Allow only this classname
_this setVariable ["cScripts_player_AllowedVehicle", ["RHS_UH60M_d", "RHS_UH60M2_d"]]; // Allow only this classnames
```
# See also
- [[CBA Mission Settings]]