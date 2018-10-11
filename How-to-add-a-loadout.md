We use [Poppy](https://github.com/BaerMitUmlaut/Poppy) A reliable, self-configuring, error finding loadout framework for Arma, to handle our loadouts and equipment distribution.
The system uses config style setup of the loadout files and is located here: [`cScripts`](https://github.com/7Cav/cScripts/tree/master/cScripts)`\`[`Loadouts`](https://github.com/7Cav/cScripts/tree/master/cScripts/Loadouts).
The loadouts use a simple inheritance system ware the actual unit loadout inherit from a higher class example:

```
> CommonBlufor
>> CAV_Charlie_Base
>>> CAV_Charlie_SL
>>>> rhsusf_army_ocp_arb_squadleader (unit classname)
```

This means in short if you define anything for `rhsusf_army_ocp_arb_squadleader` it will overwrite all the above. This means that all uniforms for charlie units can be changed by editing the `CAV_Charlie_Base` instead of physically edit all charlie trooper classes.

As per default, the `_Base` classes for all companies use a rifleman loadout with its rifle attachments removed.

## Ace arsenal default loadouts
**Not implemented yet**

## Known Issues 
* RHS 'swamped' rifles (carry handle version) cannot be used in ACE Arsenal.