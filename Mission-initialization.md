cScripts make use of CBA [pre](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_preInit.sqf) and [post](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_postInit.sqf)-init this to allow usage of CBA Settings. 

The [pre init](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_preInit.sqf) hold the CBA Settings and global variables allowing eden to access them. This also means that code can be loaded in eden editor. The ACE Arsenal loadouts is one such example. 

On mission start the pre init is loaded setting up the global variables. Then Init is executed, after this post init.

> _**NOTE** In a single player environment init runs twise. First time before pre init and then after. This means that you need a check to stop this from loading in sp._

When on the map screen more or less everything is setup. When you launch your loadout is properly applied this also have a pre loadout and post loadout system.

We use [pre loadout](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/systems/fn_setPreInitPlayerSettings.sqf) to handle permissions and abilities. (Medical, Engineer immortality etc.)
In [post loadout](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/systems/fn_setPostInitPlayerSettings.sqf) whitelists, blacklists, gear manipulation and earplugs are handled as well as radio channels and insignia's. 


## Initialization order
Here is the basic initialization order when mission is loaded on the server.
1. **cScripts Pre-init** (_Half also in eden_)
1. **Init**
1. **Unit initfields**
1. **BIS Post-init** (_Poppy is inizialised_) 
1. **cScripts Post-init**
1. **Poppy Pre loadout** (_If applied_)
1. **Poppy Post loadout** (_If applied_) 