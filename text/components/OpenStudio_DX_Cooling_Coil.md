## ![](../../images/icons/OpenStudio_DX_Cooling_Coil.png) OpenStudio DX Cooling Coil

![](../../images/components/OpenStudio_DX_Cooling_Coil.png)

EPlus DX Coil

#### Inputs
* ##### dxCoilSpeed [Required]
...0 = 1 speed, 1 = 2 speed
* ##### name [Required]
...provide a unique coil for each one that you use
* ##### availabilitySchedule [Default]
... an OpenStudio or Honeybee can be plugged in here to limit the availability of the cooling coil.
* ##### ratedHighSpeedAirflowRate [Default]
Script variable 2SpeedDXCoil
* ##### ratedHighSpeedTotalCooling [Default]
...This value is typically blank, it can be autosized (the Units are in Watts)/
* ##### ratedHighSpeedSensibleHeatRatio [Default]
... This value is typically blank.  Its value must be between 0 and 1.  
* ##### ratedHighSpeedCOP [Default]
... the efficiency at design conditions for the DX coil
* ##### ratedLowSpeedAirflowRate [Default]
Script variable 2SpeedDXCoil
* ##### ratedLowSpeedTotalCooling [Default]
Script variable Python
* ##### ratedLowSpeedSensibleHeatRatio [Default]
Script variable Python
* ##### ratedLowSpeedCOP [Default]
Script variable Python
* ##### condenserType [Default]
Script variable Python
* ##### evaporativeCondenserDescription [Default]
Script variable Python
* ##### Curves [Default]
Script variable Python
* ##### unitInternalStaticPressure [Default]
Script variable 2SpeedDXCoil

#### Outputs
* ##### out
The execution information, as output and error streams
* ##### DXCoil
...return DX coil definition


[Check Hydra Example Files for OpenStudio DX Cooling Coil](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_OpenStudio DX Cooling Coil)