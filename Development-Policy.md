This is the script department's guide line

# Goal
Our goal Is to ensure everyone have funand have as great experience as possible! 

# Code standard
## Document everything 
When writing a script document everything by adding comments so it is easy to maintain.
```
/*
 * Author: myName, aGuyThatFixedTheFuctionName 
 * Description of my function.
 *
 * Arguments:
 * 0: Vehicle/Object/Crate <OBJECT>
 * 1: DescriptionOnParam <OBJECT/BOOL/NUMBER/STRING/ARRAY/CODE> (Optional) (Default; MyDefaultValue) 
 * 2: DescriptionOnParam <OBJECT/BOOL/NUMBER/STRING/ARRAY/CODE> (Optional) 
 *
 * Return Value:
 * PotentialReturnValueDescriprion <BOOL/NUMBER/STRING>
 *
 * Example:
 * [thus,true,1,"string"] call cScripts_fnc_exsampleFunction 
 *
 * Public: No
 */
```
## Follow format
* Use 4 spaces instead of tabs. 
* Use `params[]` instead of `_this select 0`. 

## Use cba functions and script macros
All our macros can be found in the [script_component.hpp] (https://github.com/7Cav/cScripts/blob/master/cScripts/script_component.hpp).

## Avoid edits in description.ext and init.sqf
Instead use `cScripts_preInit.sqf` and or `cScripts_postInit.sqf` or any of the init scripts. 