cScripts make use of CBA [pre](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_preInit.sqf) and [post](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_postInit.sqf)-init this to allow usage of CBA Settings. 

The [pre init](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/cScripts_preInit.sqf) hold the CBA Settings and global variables allowing eden to access them. This also means that code can be loaded in eden editor. The ACE Arsenal loadouts is one such example. 

On mission start the pre init is loaded setting up the global variables. Then Init is executed, after this post init.

> _**NOTE** In a single player environment init runs twise. First time before pre init and then after. This means that you need a check to stop this from loading in sp._

When on the map screen more or less everything is setup. When you launch your loadout is properly applied this also have a pre loadout and post loadout system.

We use [pre loadout](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/systems/fn_setPreInitPlayerSettings.sqf) to handle permissions and abilities. (Medical, Engineer immortality etc.)
In [post loadout](https://github.com/7Cav/cScripts/blob/master/cScripts/CavFnc/functions/systems/fn_setPostInitPlayerSettings.sqf) whitelists, blacklists, gear manipulation and earplugs are handled as well as radio channels and insignia's. 


## Initialization order
Here is the basic initialization order when mission is loaded on the server.
1. **cScripts Pre-init** (_Parts in eden_)
1. **Init**
1. **Unit initfields**
1. **cScripts Post-init**
1. **Poppy a loadouts is applied**

### Player init
Once the mission have reached the mission screen the Poppy loadout system take over for players.
1. **Poppy Pre loadout** (_If applied_)
   1. Cav_Trooper variable is set true
   1. Cav_Company variable is set to selected slot company (Usaly Alpha, Bravo or Charlie)
   1. Player_Name variable store player named with firmed clan rank.
   1. Ace medical settings is applied
   1. Ace engineer settings is applied
   1. Ace WOD settings is applied
   1. Player_Rank is changed to reflect cav rank
   1. Player announcement runs
1. **Poppy Loadout is applied**
1. **Poppy Post loadout** (_If applied_)
   1. Current weapon is set to safe
   1. Earplugs is applied
   1. Banned eye were is removed
   1. stored or squad Insignia is applied
   1. team color is set and stored based on classname name
   1. radio channel is changed based on squad name or, if exist, unit variable (manually applied)

## See also
* [Player variables](https://github.com/7Cav/cScripts/wiki/Player-variables) 