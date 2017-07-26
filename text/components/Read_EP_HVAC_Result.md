## ![](../../images/icons/Read_EP_HVAC_Result.png) Read EP HVAC Result

![](../../images/components/Read_EP_HVAC_Result.png)

This component reads the results of an EnergyPlus simulation from the WriteIDF Component or any EnergyPlus result .csv file address.  Note that, if you use this component without the WriteIDF component, you should make sure that a corresponding .eio file is next to your .csv file at the input address that you specify. _ This component reads only the results related to zone ideal air and earth tube HVAC systems.  For other results related to zones, you should use the "Honeybee_Read EP Result" component and, for results related to surfaces, you should use the "Honeybee_Read EP Surface Result" component. - 

#### Inputs
* ##### resultFileAddress [Required]
The result file address that comes out of the WriteIDF component.

#### Outputs
* ##### supplyVolFlow
The mass of supply air flowing into each zone in kg/s.
* ##### supplyAirTemp
The mean air temperature of the supply air for each zone (degrees Celcius).
* ##### supplyAirHumidity
The relative humidity of the supply air for each zone (%).
* ##### unmetHoursCooling
Time Zone Cooling Setpoint Not Met Time
* ##### unmetHoursHeating
Time Zone Heating Setpoint Not Met Time


[Check Hydra Example Files for Read EP HVAC Result](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Read EP HVAC Result)