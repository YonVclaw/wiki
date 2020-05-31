On spawn your character gets assigned a bunch of variable to retrieve them you simply run `player getVariable 'my_variable'`. The variables are used in different parts of the script to assign or check if a system is initialized added or if the player have certain permissions and/or functionality. Below you find a list of player variables and what they store.

| Variable                       | Description                                                    | Value                              |
|--------------------------------|----------------------------------------------------------------|------------------------------------|
| `cScripts_Cav_Company`         | Store the loadout company selected on spawn or selected. Usually `alpha`, `bravo` or `charlie`.       | `STRING`                           |
| `cScripts_Cav_Rank`            | Store ARMA rank based on the 7Cav Regimental ranks.            | `STRING`                           |
| `cScripts_Cav_Trooper`         | Store a True value if loadout have been added have been setup. | `BOOL`                             |
| `cScripts_Player_Unit`         | Store a string of your squad callsign. This variable is **manually** applied in the editor. The variable is complimentary to the squad name check for the auto radio and insignia system.  | `STRING`                            |
| `cScripts_Player_Team`         | Store a string of your players team color you got assigned at mission start its ether `white`, `blue`, `red`  | `STRING`                            |
| `cScripts_Player_Announced`    | Store a True value if player have been announced.              | `BOOL`                             |
| `cScripts_Player_Documents`    | Store a True value if documents for the player have been setup.| `BOOL`                             |
| `cScripts_Player_VehiclePermission` | Store a array of permitted vehicles                       | `ARRAY` of `STRINGS` |
| `cScripts_Player_RadioChannel` | Store a array of radio and its channels.                       | `ARRAY` of `STRINGS` and `NUMBERS` |
| `cScripts_Player_Name`         | Store a trimmed player name with the cav rank removed.         | `STRING`                           |

## See also
- [Mission initialization](https://github.com/7Cav/cScripts/wiki/Mission-initialization)