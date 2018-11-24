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
In order to create a loadout for Poppy you need the weapon, magazine and item classnames.

## Add a ACE Arsenal Loadout ([Upcoming](https://github.com/7Cav/cScripts/pull/198))
In order to add an ACE Arsenal Loadout, you copy the loadout manually by exporting the loadout out from the ACE Arsenal after applying it. 

## Export equipment to arsenal filters ([Upcoming](https://github.com/7Cav/cScripts/pull/229))
To simplify the process of setting up an ACE Arsenal filter you can use `cScripts_fnc_exportBoxToArsenal` and `cScripts_fnc_exportLoadoutsToArsenal` respected function export the given objects to a easy to paste string or array.

**Export exsample parameters:**
```
[curstorTarget] call cScripts_fnc_exportBoxToArsenal;         // Return a given crate content to clipboard in a neat list.
["CAV_Charlie_AR"] call cScripts_fnc_exportLoadoutsToArsenal; // Return the "CAV_Charlie_AR" class loadout to clipboard in a neat list.
["charlie"] call cScripts_fnc_exportLoadoutsToArsenal;        // Return all charlie company loadouts to clipboard in a neat list.
```

## Known Issues 
* RHS 'swamped' rifle classnames (example: Front grip version of a base weapon) cannot be used in ACE Arsenal.

## See also
* [[Player Loadouts]]