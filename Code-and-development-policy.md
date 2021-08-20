This is S3 1BN Scripting Department code and development policy.

# Development and goals
* Each member of the department work autonomous from each other but are not alone.
* Anyone are free to edit, update create new functions and systems. If you feal they will benefit the gaming experience your more then welcome to do it. _(__Note:__ Settings, rules, and alterations to equipment, inventories and loadouts are subject for review and needs to be approved by S3 lead and Platoon staff before merge. )_ 
* Our goal is to ensure everyone have fun and have as great experience as possible! With no performance loss.

# Code standard
## Documentation
When writing a script document as much as possible by adding comments and utalize the script header. If it's not clear what the script do. This to make it for anyone else to maintain later. 
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
* Use up to date syntax and code.
* Use CBA and [ACE3 code guidelines.](https://ace3mod.com/wiki/development/coding-guidelines.html) _(Linter will complain)_ 
* Use 4 spaces instead of tabs. 
_(Linter will complain)_

## Use cba functions and script macros
All our macros can be found in the [script_macros.hpp](https://github.com/7Cav/cScripts/blob/master/cScripts/script_macros.hpp).
