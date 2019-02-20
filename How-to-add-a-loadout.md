We use [Poppy](https://github.com/BaerMitUmlaut/Poppy) A reliable, self-configuring, error finding loadout framework for Arma, to handle our loadouts and equipment distribution.
The system uses config style setup of the loadout files and is located here: [`cScripts`](https://github.com/7Cav/cScripts/tree/master/cScripts)`\`[`Loadouts`](https://github.com/7Cav/cScripts/tree/master/cScripts/Loadouts).
The loadouts use a simple inheritance system ware the actual unit loadout inherit from a higher class example:

```
> CommonBlufor
> > CAV_Charlie_Base
> > > CAV_Charlie_SL
> > > > rhsusf_army_ocp_arb_squadleader (unit classname)
```

This means in short if you define anything for `rhsusf_army_ocp_arb_squadleader` it will overwrite all the above. This means that all uniforms for charlie units can be changed by editing the `CAV_Charlie_Base` instead of physically edit all charlie trooper classes.

As per default, the `_Base` classes for all companies use a rifleman loadout with its rifle attachments removed. This means that riflemens mostly only have a rifle defined in there loadout.

In order to add a new loadout you need to do the following:
1. Add a Poppy loadout (See documentation below) 
1. Add an Ace Arsenal Default Loadout (See documentation below)

## Add a Poppy Loadout
In order to create a loadout for Poppy, you need the weapon, magazine and item classnames and apply it to your loadout. The best way of doing it is to actually select object you want in ACE Arsenal and `CTRL` + `C`then pasting it into your loadout.

**Empty Template:**
```
class emptySoldierExample : CAV_Charlie_Base {
    backpack[] = {""};
    goggles[] = {""};
    headgear[] = {""};
    uniform[] = {""};
    vest[] = {""};

    primary[] = {""};
    secondary[] = {""};
    launcher[] = {""};

    binoculars[] = {""};

    magazines[] = {""};
    items[] = {""};

    compass[] = {""};
    gps[] = {""};
    map[] = {""};
    nvgs[] = {""};
    watch[] = {""};

    insignia[] = {""};
    preLoadout = "[(_this select 0), 'charlie', 0, 0] call cScripts_fnc_setPreInitPlayerSettings;";
    postLoadout = "[(_this select 0),true,true] call cScripts_fnc_setPostInitPlayerSettings;";
};
```
_**NOTE!** the exsample soldier loadout above will be completely naked. Even if it use `CAV_Charlie_Base` as a parent. Reason being that the `CAV_Charlie_Base` is being overridden in this example soldier. To avid for instance `map` to be empty you need to remove that line from the exdsample solider. This will in turn use `CAV_Charlie_Base` map line instead if it is defined there._

## Add a ACE Arsenal Loadout
**Added in 4.2.14**

In order to add an ACE Arsenal Loadout you need, at the moment, copy the loadout manually by exporting the loadout out from the ACE Arsenal after applying it. 

## Export equipment to arsenal filters
**Added in 4.2.14**

To simplify the process of setting up an ACE Arsenal filter you can use `cScripts_fnc_exportBoxToArsenal` and `cScripts_fnc_exportLoadoutsToArsenal` thease two function export the given objects to a easy to paste string or array.

**Export exsample parameters:**
```
[curstorTarget] call cScripts_fnc_exportBoxToArsenal;         // Return a given crate content to clipboard in a neat list.
["CAV_Charlie_AR"] call cScripts_fnc_exportLoadoutsToArsenal; // Return the "CAV_Charlie_AR" class loadout to clipboard in a neat list.
["charlie"] call cScripts_fnc_exportLoadoutsToArsenal;        // Return all charlie company loadouts to clipboard in a neat list.
```

## Disable the automatic loadout system
In order to compleetly disable the automatic loadout system you need to remove the loadout includes from the [description.ext](https://github.com/7Cav/cScripts/blob/master/description.ext) file. Line [51](https://github.com/7Cav/cScripts/blob/b4568cfa310ab151992211c60b710906d0f98c53/description.ext#L51), [55](https://github.com/7Cav/cScripts/blob/b4568cfa310ab151992211c60b710906d0f98c53/description.ext#L55) and alternatively [58](https://github.com/7Cav/cScripts/blob/b4568cfa310ab151992211c60b710906d0f98c53/description.ext#L58)

You can also disable the auto distrubution by simply stop the initialisation from being executed by editing line [4 and 5](https://github.com/7Cav/cScripts/blob/master/cScripts/Loadouts/script/CfgFunctions.hpp#L4-L5) of the Poppy [CfgFunctions.hpp](https://github.com/7Cav/cScripts/blob/master/cScripts/Loadouts/script/CfgFunctions.hpp). This will stop player from reviving loadouts in spawn and respawn but stil allow you to manually select them from a starter crate.

## Known Issues 
* RHS 'swamped' rifle classnames (example: Front grip version of a base weapon) cannot be used in ACE Arsenal.

## See also
* [[Player Loadouts]]