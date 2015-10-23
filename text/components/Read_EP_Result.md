## ![](../../images/icons/Read_EP_Result.png) Read EP Result

![](../../images/components/Read_EP_Result.png)

This component reads the results of an EnergyPlus simulation from the WriteIDF Component or any EnergyPlus result .csv file address.  Note that, if you use this component without the WriteIDF component, you should make sure that a corresponding .eio file is next to your .csv file at the input address that you specify.

#### Inputs
* ##### resultFileAddress [Required]
The result file address that comes out of the WriteIDF component.
* ##### normByFloorArea [Optional]
Set to 'True' to normalize all zone energy data by floor area (note that the resulting units will be kWh/m2 as EnergyPlus runs in the metric system).  The default is set to "False."

#### Outputs
* ##### totalThermalEnergy
The total thermal energy used by each zone in kWh.  This includes cooling and heating.
* ##### thermalEnergyBalance
The thermal energy used by each zone in kWh.  Heating values are positive while cooling values are negative.
* ##### cooling
The cooling energy needed in kWh. For Ideal Air loads, this is the sum of sensible and latent heat that must be removed from each zone.  For distributed OpenStudio systems like Packaged Terminal Heat Pumps (PTHP), this will be electric energy for each zone. For central OpenStudio systems, this ouput will be a single list of chiller electric energy for the whole building.
* ##### heating
The heating energy needed in kWh. For Ideal Air loads, this is the sum of sensible and latent heat that must be removed from each zone.  For distributed OpenStudio systems like Packaged Terminal Heat Pumps (PTHP), this will be electric energy for each zone.  For central OpenStudio systems, this ouput will be a single list of boiler heat energy for the whole building.
* ##### electricLight
The electric lighting energy needed for each zone in kWh.
* ##### electricEquip
The electric equipment energy needed for each zone in kWh.
* ##### fanElectric
The fan electric energy for a central heating or cooling system in kWh.  This ouput will not appear when there is no central system assigned in OpenStudio.
* ##### peopleGains
The internal heat gains in each zone resulting from people (kWh).
* ##### totalSolarGain
The total solar gain in each zone(kWh).
* ##### infiltrationEnergy
The heat loss (negative) or heat gain (positive) in each zone resulting from infiltration (kWh).
* ##### outdoorAirEnergy
The heat loss (negative) or heat gain (positive) in each zone resulting from the outdoor air coming through the HVAC System (kWh).
* ##### natVentEnergy
The heat loss (negative) or heat gain (positive) in each zone resulting from natural ventilation (kWh).
* ##### operativeTemperature
The mean operative temperature of each zone (degrees Celcius).
* ##### airTemperature
The mean air temperature of each zone (degrees Celcius).
* ##### meanRadTemperature
The mean radiant temperature of each zone (degrees Celcius).
* ##### relativeHumidity
The relative humidity of each zone (%).
* ##### otherZoneData
Other zone data that is in the result file (in no particular order). Note that this data cannot be normalized by floor area as the component does not know if it can be normalized.


[Check Hydra Example Files for Read EP Result](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Read EP Result)