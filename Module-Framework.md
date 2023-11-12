# WIP

https://github.com/7Cav/cScripts/blob/main/cScripts/functions/init/fn_init_zenModuels.sqf
Simple module
```hpp
["7Cav Other", "Print a system chat",
    {
        params ["_modulePos", "_objectPos"];
        systemChat "Hello World"
    },
    "\a3\modules_f\data\portraitmodule_ca.paa"
] call zen_custom_modules_fnc_register;
```
Super small moduels that just do simple task can be just definined in fn_init_zenModuels file.
For more advanced moduels. once that have UI por specialized things ussaly is handled in its own funciton.

https://github.com/7Cav/cScripts/tree/main/cScripts/functions/modules

Start your zen function by accepting the following parameters passed down from the init collection.
```hpp
params ["_modulePos", "_objectPos"];
```
https://zen-mod.github.io/ZEN/#/frameworks/custom_modules

