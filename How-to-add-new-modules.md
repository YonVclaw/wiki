*Mod dependencies: [Achilles](https://github.com/ArmaAchilles/Achilles)*
cScripts have zeus modules using the Achilles user custom module system. 

*Note that you need to have Achillies mod active to use the moduels else the script will terminate the cScripts module system.*

In order to add a module you need registrate it in [fn_initModules.sqf](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/init/fn_initModules.sqf).
Below you find a template:
```
["7Cav MyCategory ", "My Topic Lable",{
    [_this select 0] call FUNC(moduleMyFunction);
}] call Ares_fnc_RegisterCustomModule;
```
Depending of the functionality of the function you need define eather `_this select 0` for location under cursor or `_this select 1` for object under cursor.

Secondly you need to create the module function... (wip)