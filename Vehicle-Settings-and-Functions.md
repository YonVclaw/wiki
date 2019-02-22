All vehicles that have there parent class as `RHS_C130J_Base` (_the RHS C130_) or `Helicopter_Base_F` (_basically all two door helicopters_) will get settings applied to them. The settings varies depending on the type of vehicle.

### Jump action
The jump action allow you to make a simulated static combat jump over a DZ. The action is only visible when the conditions have been met (_Default conditions; Altitude min 180 max 350, Max speed 300, and the door or ramp need to be open_).

### Get out actions
The get out actions allow players to exit thru a desired door of a helicopter (Left or Right). This allow for a better and more coordinated insertions in to AO's. The settings is always available when inside of a cargo position of a airframe and is automatically added to all supported helicopter classes.

It is possible to manually add the function. This is done by adding it to the init field of the helicopter `[this] call cScripts_fnc_addGetOutHelo;`. By default the options is colored blue and red this can be turned off by adding `false` to the second parameter of the function.

> _**NOTE**_
> _Adding the function manually will cause a warning in the RPT log. This warning can be ignored. It is used to control the setting is not be added multiply times mid mission._<br>
> _The warning look like this:<br>```13:36:59 [cScripts] WARNING: Helicopter Get out setting already applied for b1.```_

## See also
* [[Vehicle Loadouts|Vehicle Loadouts]] 
* [[Vehicle Texture Label|Texture Label]] 
