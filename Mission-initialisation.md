cScripts make use of CBA pre and post-init this to allow usage of CBA Settings. 

The pre init hold the settings and global variables allowing eden to access them.

On mission start the pre init is loaded setting up the global variables. Then Init is executed, after this post init.

> _**NOTE** In a single player environment init runs twise. First time befor pre init and then after. This means that you need a check to stop this from loading in sp._

When on the map screen more or less everything is setup. When you launch your loadout is propperly applied this also have a pre loadout and post loadout system.

We use pre loadout to handle permissions and abilities. (Medical, Engineer immortality etc.)
In post loadout whitelists, blacklists, gear manipulation and earplugs are handled as well as radio channels and insignias. 