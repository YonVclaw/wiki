cScripts have extensive debugging capability and to avoid preformence loss they as little logging as done as possible outside debugging environment.

To enable debugging you [uncomment this](https://github.com/7Cav/cScripts/blob/master/cScripts/script_component.hpp#L7) or add `#define DEBUG_MODE`at the top of the function you wish to debug.

Ofcause you sometimes need or whant more logging during development. But after removing this logging you might whant to add debug logging to help future developer be able to know what happens after the function is executed or when it is executed.

There are three debug log functions in cScripts; `logError`, `logWarning` and `logInfo`. Mainly what this functions do is to format your error message and add a prefix. In the rpt log. Exsample:
```
>>> private _var = 'exsample';
>>> format['I am a %1 warning.', _var] call FUNC(logWarning)
[cScripts] WARNING: I am a Exsample warning.
```