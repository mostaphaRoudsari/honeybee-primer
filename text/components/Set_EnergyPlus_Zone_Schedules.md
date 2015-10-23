## ![](../../images/icons/Set_EnergyPlus_Zone_Schedules.png) Set EnergyPlus Zone Schedules

![](../../images/components/Set_EnergyPlus_Zone_Schedules.png)

Use this component to change the schedules of your HBZones. - 

#### Inputs
* ##### HBZones [Required]
HBZones for which you want to change shcedules.
* ##### occupancySchedules [Optional]
...
* ##### occupancyActivitySchs [Optional]
A text string representing the shceudle for the metabolic rate of the occupants that you want to use.  This can be either a shcedule from the schedule libirary or a CSV file path to a CSV schedule you created with the "Honeybee_Create CSV Schedule" component. If this is a CSV schedule, the values in it should be Watts and the "units_" input should be "ActivityLevel."
* ##### heatingSetPtSchedules [Optional]
...
* ##### coolingSetPtSchedules [Optional]
...
* ##### lightingSchedules [Optional]
...
* ##### equipmentSchedules [Optional]
...
* ##### infiltrationSchedules [Optional]
...
* ##### HVACAvailabilitySchs [Optional]
Script variable setEPZoneSchedules

#### Outputs
* ##### schedules
A report of what shcedules are assigned to each zone.
* ##### HBZones
HBZones that have had thier shcedules modified.


[Check Hydra Example Files for Set EnergyPlus Zone Schedules](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Set EnergyPlus Zone Schedules)