## ![](../../images/icons/Read_Hourly_Results_from_Annual_Daylight_Study.png) Read Hourly Results from Annual Daylight Study

![](../../images/components/Read_Hourly_Results_from_Annual_Daylight_Study.png)

Read the results of the annual study for a single hour of the year - 

#### Inputs
* ##### illFilesAddress [Required]
List of .ill files
* ##### testPoints [Required]
List of 3d Points
* ##### annualProfiles [Optional]
Script variable readDSHourlyResults
* ##### HOY [Required]
Hour of the year

#### Outputs
* ##### iIllumLevelsNoDynamicSHD
Illuminance values without dynamic shadings
* ##### iIllumLevelsDynamicSHDGroupI
Illuminance values when shading group I is closed
* ##### iIllumLevelsDynamicSHDGroupII
Illuminance values when shading group II is closed
* ##### iIlluminanceBasedOnOccupancy
Illuminance values based on Daysim user behavior
* ##### shadingGroupInEffect
0: no blind, 1: shading group I, 2: shading group II


[Check Hydra Example Files for Read Hourly Results from Annual Daylight Study](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Read Hourly Results from Annual Daylight Study)