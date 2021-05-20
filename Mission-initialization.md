cScripts make use of CBA [pre](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_preInit.sqf) and [post](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_postInit.sqf)-init this to allow usage of CBA Settings. 

The [pre init](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_preInit.sqf) hold the CBA Settings and global variables allowing eden to access them. This also means that code can be loaded in eden editor. The ACE Arsenal loadouts is one such example. 

On mission start the pre init is loaded setting up the global variables. Then Init is executed, after this post init.

> _**NOTE** In a single player environment init runs twise. First time before pre init and then after. This means that you need a check to stop this from loading in sp._

When on the map screen more or less everything is setup. When you launch your loadout is properly applied this also have a pre loadout and post loadout system.

## Initialization order
Here is the basic initialization order when mission is loaded on the server.
1. **cScripts Pre-init** (_Parts in eden_)
1. **Init**
1. **Unit initfields**
1. **cScripts Post-init**
1. **cScripts Loadouts is applied**

### Player init
Once the mission have reached the mission screen the Poppy loadout system take over for players.

## See also
* [Player variables](https://github.com/7Cav/cScripts/wiki/Player-variables)
* [BIS Initialization Order](https://community.bistudio.com/wiki/Initialization_Order) 