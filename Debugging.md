cScripts have functions for debugging and to avoid preformence loss there are as little logging as done as possible outside debugging environment. 

To enable global debugging you uncomment the highlighted line in [script_component.hpp](https://github.com/7Cav/cScripts/blob/main/cScripts/script_component.hpp#L5) or add `#define DEBUG_MODE`at the top of the function you wish to debug.

Ofcause you sometimes need or whant more logging during development. But after removing this logging you might whant to add debug logging to help future developer be able to know what happens after the function is executed or when it is executed.

There are four [diagnostics functions](https://github.com/7Cav/cScripts/tree/main/cScripts/functions/diag) in cScripts; `error`, `warning`, `info` and `log` they have a coresponding wraped macro similar to [CBA loggin macros](https://cbateam.github.io/CBA_A3/docs/files/main/script_macros_common-hpp.html#Debugging). Mainly what this functions do is to format your error message and add a prefix. In the rpt log. Exsample:
```
>>> private _var = 'exsample';
>>> WARNING_1("", "I am a %1 warning.", _var);
13:36:59 [cScripts] WARNING: I am a exsample warning.
```
```
>>> private _var = 'exsample';
>>> WARNING_1("Prefix", "I am a %1 warning.", _var);
13:36:59 [cScripts] (Prefix) WARNING: I am a exsample warning.
```
This allow you to easy see and follow your function in the rpt log.

All logs are primarly hidden as default. But you can make them appear by using the `SHOW_` prefix. You can also show the messages in the system chat using `SHOW_CHAT_` as well to server `SHOW_SERVER_` or even both `SHOW_CHAT_SERVER_`.

```js
// PARAMS: PREFIX, MESSAGE
LOG()
INFO()
WARNING()
ERROR()

// Always show logs
// PARAMS: PREFIX, MESSAGE
SHOW_LOG()
SHOW_INFO()
SHOW_WARNING()
SHOW_ERROR()

// Format variant (works for LOG, INFO, WARNING, ERROR)
// PARAMS: PREFIX, MESSAGE, FORMAT
LOG_1()
LOG_2()
LOG_3()
LOG_4()
LOG_5()
LOG_6()
LOG_7()
LOG_8()

// Show log in chat or send to server (works for LOG, INFO, WARNING, ERROR)
// PARAMS: PREFIX, MESSAGE
SHOW_LOG()
SHOW_SERVER_LOG()
SHOW_CHAT_SERVER_LOG()
```