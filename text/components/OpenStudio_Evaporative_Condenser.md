## ![](../../images/icons/OpenStudio_Evaporative_Condenser.png) OpenStudio Evaporative Condenser

![](../../images/components/OpenStudio_Evaporative_Condenser.png)

Evaporative Condenser - 

#### Inputs
* ##### uniqueName [Required]
... a required field to uniquely name the evaporative condenser
* ##### serviceType [Required]
... what does the evaporator serve: 0=single speed DX, 1=two speed DX, 2=VRF, or 3=commercial refrigeration system
* ##### hiSpeedEvaporativeEffectiveness [Default]
... Used for both one stage and two stage condensers, supply no information and the value defaults to 0.9
* ##### hiSpeedEvaporativeCondAirflowRate [Default]
Script variable EvaporativeCondenser
* ##### hiSpeedEvapPumpPower [Default]
... Used for both one stage and two stage condensers, power in Watts is autosized by default 0.004266 Watts/Watt cooling or 15 W/ton cooling
* ##### loSpeedEvaporativeEffectiveness [Default]
... only needed for two speed condenser, supply no information and the value defaults to 0.9
* ##### loSpeedEvaporativeCondAirflowRate [Default]
Script variable EvaporativeCondenser
* ##### loSpeedEvapPumpPower [Default]
... only needed for two-speed condenser, power in Watts is autosized by default 0.004266 Watts/Watt cooling or 15 W/ton cooling
* ##### storageTank [Default]
the description of a storage tank used to hold the evaporative condenser water, if any
* ##### Curves [Default]
this feature has not been implemented yet.

#### Outputs
* ##### out
The execution information, as output and error streams
* ##### evapCondenserDefinition
...description of an evaporative condenser returned for users.


[Check Hydra Example Files for OpenStudio Evaporative Condenser](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_OpenStudio Evaporative Condenser)