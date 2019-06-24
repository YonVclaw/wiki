# Setup

## Guidelines

## Placements of units
Placing down units is rather straight forward. To ensure the that they come in a decent order in the mission select screen can be fiddly. Remember that they appear in the selection screen as you put it down. The order is based on the group name seen in the editor.

Make sure to place down the CavAddon Named Squads.

## Functions and variables
cScripts comes with a bunch of functions and autoassignation systems. For a players squad name or variable name is important in order to get the correct radio channel, insignia or other hidden functionalities. 

``` cpp
init="call{this setgroupID[""BANDIT-1""];" \n "this setVariable [""cScripts_Player_Unit"", ""BANDIT-1""];}";				
```

``` cpp
init="call{this setVariable [""cScripts_Player_Unit"", ""BANDIT-1""];}";
```
# Saving
## Naming
``` cpp
cav_{Optional Sort Tag}_{Name And Squad or Team Type}_Deployment_{Optional Terrain Type}
```

