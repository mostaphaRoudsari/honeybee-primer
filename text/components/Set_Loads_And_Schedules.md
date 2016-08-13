## ![](../../images/icons/Set_Loads_And_Schedules.png) Set Loads And Schedules

![](../../images/components/Set_Loads_And_Schedules.png)

Set schedules and loads for zones based on program  - 

#### Inputs
* ##### HBZones [Required]
A HBZone or list of HBZones for which you want to change the program (including schedules and loads).
* ##### zonePrograms [Optional]
The zone program that you want to assign to the HBZones.  This should be a value from the "Honeybee_ListZonePrograms" component.  This input can also be a list of programs tha aligns with the input HBZones.

#### Outputs
* ##### currentSchedules
The schedules that have been assigned to the zones.
* ##### currentLoads
The loads that have been assigned to the zones
* ##### HBZones
HBZones that have had their program set to the input zonePrograms_.


[Check Hydra Example Files for Set Loads And Schedules](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Set Loads And Schedules)