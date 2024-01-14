The Civilian Agent function allow you transform a AI civilian unit in to a agent. What the function does it that it removes the unint and recreates it as a agent.

To use this you need to place a soldier down a unit in eden editor and put `[this] call cScripts_fnc_makeAgent;` in the units init line.

```cpp
/* Arguments:
 * 0: Unit <OBJECT>
 */

[this] call cScripts_fnc_makeAgent;
```