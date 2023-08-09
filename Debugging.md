cScripts have functions for debugging  and to avoid preformence loss there are as little logging as done as possible outside debugging environment. 

To enable global debugging you uncomment the highlighted line in [script_component.hpp](https://github.com/7Cav/cScripts/blob/main/cScripts/script_component.hpp#L5) or add `#define DEBUG_MODE`at the top of the function you wish to debug.

Ofcause you sometimes need or whant more logging during development. But after removing this logging you might whant to add debug logging to help future developer be able to know what happens after the function is executed or when it is executed.

There are three [diagnostics functions](https://github.com/7Cav/cScripts/tree/main/cScripts/functions/diag) in cScripts; `error`, `warning` and `info`. Mainly what this functions do is to format your error message and add a prefix. In the rpt log. Exsample:
```
>>> private _var = 'exsample';
>>> [format['I am a %1 warning.', _var]] call FUNC(warning);
13:36:59 [cScripts] WARNING: I am a exsample warning.
```
<!--asdasd-->
This allow you to easy see and follow  your function in the rpt log.

In order to log only when you have debug is enable you write:
```
#ifdef DEBUG_MODE
    ["Exsample log", "Prefix Example"] call FUNC(log);
#endif
```
This will allow a message to only be shown when `#define DEBUG_MODE` is defined (written att the top of the file or enabled via [script_component.hpp](https://github.com/7Cav/cScripts/blob/master/cScripts/script_component.hpp#L7).)