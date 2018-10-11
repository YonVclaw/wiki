We use [Poppy](https://github.com/BaerMitUmlaut/Poppy) A reliable, self-configuring, error finding loadout framework for Arma, to handle our loadouts and equipment distribution.
The system uses config style setup of the loadout files and is located here: [`cScripts`](https://github.com/7Cav/cScripts/tree/master/cScripts)`\`[`Loadouts`](https://github.com/7Cav/cScripts/tree/master/cScripts/Loadouts).
The loadouts use a simple inheritance system ware the actual unit loadout inherit from a higher class exsamle:
```
 >   - CommonBlufor
 >     - CAV_Charlie_Base
 >       - CAV_Charlie_SL
 >         - rhsusf_army_ocp_arb_squadleader
```
## Known Issues 
* RHS 'swamped' rifles (carry handle version) cannot be used in ACE Arsenal.