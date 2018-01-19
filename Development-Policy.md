This is the script department's guide line

Our goal Is to ensure everyone have funand have as great experience as possible! 

When writing a script document everything by adding comments so it is easy to maintain.
Secondly make sure it do not drain the frame rate and avoid loops (if a loop is required use already added CBA functions.)
Update the script header
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