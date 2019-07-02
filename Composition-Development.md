**This page is a work in progress**
# Guidelines

# Composition types
## 7Cav Unit Deployments
### Placements of units
Placing down units is rather straight forward. To ensure the that they come in a decent order in the mission select screen can be fiddly. Remember that they appear in the selection screen as you put it down. The order is based on the group name seen in the editor.

Make sure to place down the CavAddon Named Squads.

### Functions and variables
cScripts comes with a bunch of functions and autoassignation systems. For a players **group name** or **variable** is important in order to get the correct radio channel, insignia or other hidden functionalities. 

As per default the squad name is enough to assign your radio channel and insignia but if a squad leader is not precent on mission init this fall apart quite fast. This mean that the squad name is not set for the squad and the squad will revive the default channel and no insignia. 

To by pass this the variable `cScripts_Player_Unit` was introduced. This variable store the players group name and is manually added to each unit in a group. (Including lead elements, all playable units.)

Below here you can find two exsamples extracted from the Bandit composition:

Squad leader:
``` cpp
init="call{this setgroupID[""BANDIT-1""];" \n "this setVariable [""cScripts_Player_Unit"", ""BANDIT-1""];}";
```
Trooper in Bandit one:
``` cpp
init="call{this setVariable [""cScripts_Player_Unit"", ""BANDIT-1""];}";
```

### Naming A 7Cav deployment
``` cpp
cav_{Optional Sort Tag}_{Name And Squad or Team Type}_Deployment_{Optional Terrain Type}
```

### Header of unit placement

Template:
```
version=53;
name="Apollo Team And Vehicle Deployment (D) [DEVBUILD]";
author="";
category="Cav_EdSubcat_Deploy_Platoon";
```

# See also
- BIS [Custom Composition](https://community.bistudio.com/wiki/Eden_Editor:_Custom_Composition)
