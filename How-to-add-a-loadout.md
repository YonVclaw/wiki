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

Inorder to add a new loadout you need to do the following:
1. Add a Poppy loadout (See documentation below) 
1. Add a Ace Arsenal Default Loadout (See documentation below)

## Add a Poppy Loadout

## Add a ACE Arsenal Loadout ([Upcoming](https://github.com/7Cav/cScripts/pull/198))
In order to add a ACE Arsenal Loadout you can use the `cScripts_fnc_exportToArsenal` function or copy the loadout manually by exporting the loadout ut from the Arsenal.

Export script exsample parameters:
```
_loadouts = [true] call cScripts_fnc_exportToArsenal; // Export all hardcoded Poppy loadouts to clipboard.
_loadouts = ['charlie'] call cScripts_fnc_exportToArsenal; // Export only the selected company loadout to clipboard.
_loadouts = ['CAV_Charlie_SL'] call cScripts_fnc_exportToArsenal; // Export only the selected classname to clipboard.
```

## Known Issues 
* RHS 'swamped' rifle classnames (example: Front grip version of a base weapon) cannot be used in ACE Arsenal.

## See also
* [[Player Loadouts]]