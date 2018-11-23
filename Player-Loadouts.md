cScripts automatically distribute loadouts via [Poppy](https://github.com/BaerMitUmlaut/Poppy/) "*A reliable, self configuring, error finding loadout framework for Arma.*". Each loadout is added automatically to a soldier when using the _Cav Class Definition_ as a unit variable name or on a unit with a matching classname and set as playable. Below you find a list of supported loadouts and its corresponding classname.

| Company   | Loadout Name               | Cav Class Definition              | Classname                             |
|:----------|:---------------------------|:----------------------------------|:--------------------------------------|
| Alpha     | Pilot                      | `CAV_Alpha_Helo_PILOT`            | `B_Helipilot_F`                       |
| Alpha     | Co-Pilot                   | `CAV_Alpha_Helo_COPILOT`          |                                       |
| Alpha     | Crew Chief                 | `CAV_Alpha_Helo_CHIEF`            | `B_T_Helicrew_F`                      |
| Alpha     | Crew                       | `CAV_Alpha_Helo_GNR`              | `B_Helicrew_F`                        |
|           |                            |                                   |                                       |
| Alpha     | Attack Rotary Pilot        | `CAV_Alpha_Helo_PILOT_ATT`        |                                       |
| Alpha     | Attack Rotary Co-Pilot     | `CAV_Alpha_Helo_COPILOT_ATT`      |                                       |
|           |                            |                                   |                                       |
| Alpha     | Fixed Wing Pilot           | `CAV_Alpha_Fixed_PILOT`           | `B_Fighter_Pilot_F`                   |
|           |                            |                                   |                                       |
| Bravo     | Officer                    | `CAV_Bravo_OFFCR`                 | `rhsusf_army_ocp_officer`             |
|           |                            |                                   |                                       |
| Bravo     | Crew Commander             | `CAV_Bravo_Crew_CDR`              | `rhsusf_army_ocp_combatcrewman`       |
| Bravo     | Crew Gunner                | `CAV_Bravo_Crew_GNR`              | `rhsusf_army_ocp_crewman`             |
| Bravo     | Crew                       | `CAV_Bravo_Crew_CREW`             | `rhsusf_army_ocp_driver`              |
|           |                            |                                   |                                       |
| Bravo     | Squad Leader               | `CAV_Bravo_SL`                    | `rhsusf_army_ocp_squadleader`         |
| Bravo     | Fire Team Leader           | `CAV_Bravo_TL`                    | `rhsusf_army_ocp_teamleader`          |
| Bravo     | Automatic Rifleman         | `CAV_Bravo_AR`                    | `rhsusf_army_ocp_autorifleman`        |
| Bravo     | Grenadier                  | `CAV_Bravo_GR`                    | `rhsusf_army_ocp_grenadier`           |
| Bravo     | Rifleman                   | `CAV_Bravo_RM`                    | `rhsusf_army_ocp_rifleman`            |
| Bravo     | Combat Life Saver          | `CAV_Bravo_CLS`                   | `rhsusf_army_ocp_medic`               |
|           |                            |                                   |                                       |
| Charlie   | HW Fire Team Leader        | `CAV_Bravo_Weapons_TL`            | `rhsusf_army_ocp_machinegunnera`      |
| Charlie   | HW Automatic Rifleman      | `CAV_Bravo_Weapons_MG`            | `rhsusf_army_ocp_machinegunner`       |
| Charlie   | HW Grenadier               | `CAV_Bravo_Weapons_GNR`           | `rhsusf_army_ocp_javelin`             |
|           |                            |                                   |                                       |
| Charlie   | Officer                    | `CAV_Charlie_OFFCR`               | `rhsusf_army_ocp_arb_riflemanl`       |
| Charlie   | Joint Fires Observer       | `CAV_Charlie_JFO`                 | `rhsusf_army_ocp_jfo`                 |
|           |                            |                                   |                                       |
| Charlie   | Squad Leader               | `CAV_Charlie_SL`                  | `rhsusf_army_ocp_arb_squadleader`     |
| Charlie   | Fire Team Leader           | `CAV_Charlie_TL`                  | `rhsusf_army_ocp_arb_teamleader`      |
| Charlie   | Automatic Rifleman         | `CAV_Charlie_AR`                  | `rhsusf_army_ocp_arb_autorifleman`    |
| Charlie   | Grenadier                  | `CAV_Charlie_GR`                  | `rhsusf_army_ocp_arb_grenadier`       |
| Charlie   | Rifleman                   | `CAV_Charlie_RM`                  | `rhsusf_army_ocp_arb_rifleman`        |
| Charlie   | Combat Life Saver          | `CAV_Charlie_CLS`                 | `rhsusf_army_ocp_arb_medic`           |
|           |                            |                                   |                                       |
| Charlie   | HW Squad Leader            | `CAV_Charlie_Weapons_SL`          | `B_T_Soldier_SL_F`                    |
| Charlie   | HW Fire Team Leader        | `CAV_Charlie_Weapons_TL`          | `B_T_Soldier_TL_F`                    |
| Charlie   | HW Automatic Rifleman      | `CAV_Charlie_Weapons_AR`          | `B_T_Engineer_F`                      |
| Charlie   | HW Grenadier               | `CAV_Charlie_Weapons_GR`          | `B_T_Soldier_Repair_F`                |
| Charlie   | HW Rifleman                | `CAV_Charlie_Weapons_RM`          | `B_T_soldier_mine_F`                  |
| Charlie   | HW Combat Life Saver       | `CAV_Charlie_Weapons_CLS`         | `B_T_Soldier_Exp_F`                   |
|           |                            |                                   |                                       |
| Medical   | PL/PSG/Bonesaw Team Leader | `CAV_Medical_OFFCR`               | `B_medic_F`                           |
| Medical   | Platoon Medics             | `CAV_Medical_PLMEDIC`             | `rhsusf_navy_marpat_d_medic`          |
| Medical   | Bonesaw Team Medic         | `CAV_Medical_BONESAW`             | `rhsusf_navy_marpat_wd_medic`         |
|           |                            |                                   |                                       |
| Ranger    | Officer                    | `CAV_Ranger_OIC`                  | `rhsusf_socom_marsoc_elementleader`   |
| Ranger    | Squad Leader               | `CAV_Ranger_2IC`                  | `rhsusf_socom_marsoc_teamchief `      |
| Ranger    | Fire Team Leader           | `CAV_Ranger_TL `                  | `rhsusf_socom_marsoc_teamleader`      |
| Ranger    | Automatic Rifleman         | `CAV_Ranger_AR `                  | `rhsusf_socom_marsoc_cso_mechanic`    |
| Ranger    | Grenadier                  | `CAV_Ranger_GR `                  | `rhsusf_socom_marsoc_cso_grenadier`   |
| Ranger    | Rifleman                   | `CAV_Ranger_RM `                  | `rhsusf_socom_marsoc_cso`             |
| Ranger    | Medic                      | `CAV_Ranger_MEDIC`                | `rhsusf_socom_marsoc_sarc `           |
|           |                            |                                   |                                       |
| Ranger    | Sniper                     | `CAV_Sniper`                      | `B_sniper_F  `                        |
| Ranger    | Spotter                    | `CAV_Spotter `                    | `B_spotter_F  `                       |
|           |                            |                                   |                                       |
| Special*  | Debug                      | `DEBUG` `_1` to `_5`              | N/A                                   |
| Special*  | S3 Mission Control         | `MissionControl` `_1` to `_5`     | N/A                                   |
| Special*  | S3 Mission Control         | `MissionControlUnit` `_1` to `_5` | N/A                                   |
| Special*  | S3 Mission Control         | `MC ` `_1` to `_5`                | N/A                                   |
| Special*  | S3 Mission Control         | `Zeus` `_1` to `_5`               | N/A                                   |
| Special*  | S3 Mission Control         | `ZeusUnit` `_1` to `_5`           | N/A                                   |
| Special*  | S3 Mission Control         | `S3` `_1` to `_5`                 | N/A                                   |
| Special   | S5 Cameraman               | `S5` `_1` to `_5`                 | N/A                                   |

_* This loadout use Bravo Officer loadout, are immune to damage and have full engineer and medical abilities._

## Loadout change requests
To make the prosess easy for everyone as well as speed up the process of loadout requests refraine from using names and use classnames. You can use use a ACE Arsenal export or send the individual Classname. This will avoid possible questions of what you meen or what variant of the given item you are requesting. 

If you have the ability edit the config loadout file directly this is the best way. This allows for a even quicker implementation of the requested loadout.

## See also
* [[Starter Crate]]
* [[Regear Trooper Module]]
* [[How to add a loadout]]