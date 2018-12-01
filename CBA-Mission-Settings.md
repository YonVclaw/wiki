<img align="right" width="300" height="182" src="https://github.com/7Cav/cScripts/blob/master/resourses/wikigfx/CBA_Mission_Settings.png">cScripts comes equipped with [CBA settings](https://github.com/CBATeam/CBA_A3/wiki/CBA-Settings-System). When you install cScripts for the first time you need to reload the mission in order to access the mission settings. In order to edit the mission settings in Eden-Editor select **Settings** → **Addon Options...** (*Shortcut: Ctrl + Alt + S*). This will open the control panel seen on the picture to the right. Now you need to select the **cScripts Mission Settings** in the drop down menu. You can now edit the mission settings freely. Alternative you can edit the settings directly in the [cba_settings.sqf](https://github.com/7Cav/cScripts/blob/master/cba_settings.sqf) file, located in the mission root. The mission values are not in the settings file per default and need to be manually added. Reason behind this is to allow the user to manually change the settings in a easy maner. [[Below you'll find the default values for cScripts Mission Settings|CBA Mission Settings#Default-Values]].

**Note:** Settings that you changed in the mission are saved in the mission.sqm file. But are over written by the cba_settings.sqf if they are pressen there.

### Default Values
```
// cScripts Mission Settings
cScripts_Settings_allowCustomInit = true;
cScripts_Settings_allowCustomTagging = true;
cScripts_Settings_enable7cavZeusModules = true;
cScripts_Settings_enableStartHint = true;
cScripts_Settings_enforceEyewereBlacklist = true;
cScripts_Settings_jumpSimulation = 1;
cScripts_Settings_jumpSimulationGlasses = true;
cScripts_Settings_jumpSimulationHat = true;
cScripts_Settings_jumpSimulationNVG = true;
cScripts_Settings_setAiSystemDifficulty = 0;
cScripts_Settings_setCustomHintText = "I have design this mission! Yey for me!";
cScripts_Settings_setCustomHintTopic = "My custom Mission!";
cScripts_Settings_setMissionType = 1;
cScripts_Settings_setPlayerRank = true;
cScripts_Settings_setStartupDelay = 30;
cScripts_Settings_showDiaryRecords = true;
cScripts_Settings_useCustomSupplyInventory = false;
cScripts_Settings_useCustomVehicleInventory = true;
cScripts_Settings_useCustomVehicleSettings = true;
```

## See also
* [[Starter Crate]]