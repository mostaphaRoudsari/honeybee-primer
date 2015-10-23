## ![](../../images/icons/Set_EnergyPlus_Zone_Thresholds.png) Set EnergyPlus Zone Thresholds

![](../../images/components/Set_EnergyPlus_Zone_Thresholds.png)

Use this component to set Zone Thresholds like daylighting thresholds and setpoints. - 

#### Inputs
* ##### HBZones [Required]
HBZones for which zone thresholds will be set.
* ##### coolingSetPt [Optional]
A number or list of numbers that represent the thermostat cooling setpoint in degrees Celcius.  The cooling setpoint is effectively the indoor temperature above which the cooling system is turned on.  This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.
* ##### coolingSetback [Optional]
A number or list of numbers that represent the thermostat cooling setback in degrees Celcius.  The cooling setback is the indoor temperature that the space will be kept at when it is unoccipied.  Note that not all building types have a setback.  This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.
* ##### heatingSetPt [Optional]
A number or list of numbers that represent the thermostat heating setpoint in degrees Celcius.  The heating setpoint is effectively the indoor temperature below which the heating system is turned on.  This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.
* ##### heatingSetback [Optional]
A number or list of numbers that represent the thermostat heating setback in degrees Celcius.  The heating setback is the indoor temperature that the space will be kept at when it is unoccipied.  Note that not all building types have a setback.  This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.

#### Outputs
* ##### readMe!
The execution information, as output and error streams
* ##### HBZones
HBZones with thresolds set.


[Check Hydra Example Files for Set EnergyPlus Zone Thresholds](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Set EnergyPlus Zone Thresholds)