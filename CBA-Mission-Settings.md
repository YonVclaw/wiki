<img align="right" width="300" height="182" src="https://github.com/7Cav/cScripts/blob/main/resourses/wikigfx/CBA_Mission_Settings.png">cScripts comes equipped with [CBA settings](https://github.com/CBATeam/CBA_A3/wiki/CBA-Settings-System). When you install cScripts for the first time you need to reload the mission in order to access the mission settings. In order to edit the mission settings in Eden-Editor select **Settings** → **Addon Options...** (*Shortcut: Ctrl + Alt + S*). This will open the control panel seen on the picture to the right. Now you need to select the **cScripts Mission Settings** in the drop down menu. You can now edit the mission settings freely. Alternative you can edit the settings directly in the [cba_settings.sqf](https://github.com/7Cav/cScripts/blob/master/cba_settings.sqf) file, located in the mission root. The mission values are not in the settings file per default and need to be manually added. Reason behind this is to allow the user to manually change the settings in a easy maner. [[Below you'll find the default values for cScripts Mission Settings|CBA-Mission-Settings#default-values]].

**Note:** Settings that you changed in the mission are saved in the mission.sqm file. But are over written by the cba_settings.sqf if they are pressen there.

### Default Values
```cpp
// cScripts Mission Settings
force force cScripts_Settings_addEarplugs = true;
force force cScripts_Settings_allowCustomTagging = true;
force force cScripts_Settings_allowInsigniaApplication = true;
force force cScripts_Settings_allowReplaceItem = true;
force force cScripts_Settings_enable7cavZeusModules = true;
force force cScripts_Settings_enableRadios = true;
force force cScripts_Settings_enableStagingSystem = true;
force force cScripts_Settings_enableVehicleInventory = true;
force force cScripts_Settings_enableVehiclePylon = true;
force force cScripts_Settings_enableVehicleRadios = false;
force force cScripts_Settings_enableVehicleSystem = true;
force force cScripts_Settings_jumpSimulation = 2;
force force cScripts_Settings_jumpSimulationGlasses = true;
force force cScripts_Settings_jumpSimulationHat = true;
force force cScripts_Settings_jumpSimulationNVG = true;
force force cScripts_Settings_primaryClanTag = "7CAV";
force force cScripts_Settings_replaceHandGrenades = 1;
force force cScripts_Settings_replaceMagazines = 0;
force force cScripts_Settings_replaceMedical = 1;
force force cScripts_Settings_replaceSmokeGrenades = 1;
force force cScripts_Settings_replaceStunGrenades = 1;
force force cScripts_Settings_setAiSystemDifficulty = 2;
force force cScripts_Settings_setMissionType = 1;
force force cScripts_Settings_setPlayerRank = true;
force force cScripts_Settings_setRadio = true;
force force cScripts_Settings_setRadioChannelNames = "[""UNUSED"",""AVIATION"",""VIKING"",""LANCER"",""BANSHEE"",""SABRE"",""BANDIT"",""MISFIT"",""HAVOC"",""IDF-1"",""IDF-2"",""CAS-1"",""CAS-2"",""GROUND-TO-AIR"",""ATLAS"",""FARP"",""CONVOY"",""ZEUS"",""CAG"",""COMMAND""]";
force force cScripts_Settings_showAllLoadouts = false;
force force cScripts_Settings_showDiaryRecords = true;
force force cScripts_Settings_vehicleFactions = "[""BLU_F"", ""BLU_CTRG_F"", ""BLU_T_F"", ""BLU_USA_7CAV_F"", ""rhs_faction_usaf"", ""rhs_faction_usarmy"", ""rhs_faction_usarmy_d"", ""rhs_faction_usarmy_wd"", ""rhs_faction_usmc"", ""rhs_faction_usmc_d"", ""rhs_faction_usmc_wd"", ""rhs_faction_usn"",""rhs_faction_socom"",""USAF""]";
```

## See also
* [[Features]]
* [[Starter Crate]]
* [cba_settings.sqf](https://github.com/7Cav/cScripts/blob/master/cba_settings.sqf) _(Function)_