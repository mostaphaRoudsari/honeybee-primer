## ![](../../images/icons/Read_HVAC_Sizing.png) Read HVAC Sizing

![](../../images/components/Read_HVAC_Sizing.png)

This component parses an .eio file from an energy simulation and brings in the sizes of all of the HVAC equipment. - 

#### Inputs
* ##### eioFile [Required]
The file address of the eio file that comes out of the "Honeybee_Lookup EnergyPlus Folder" component.
* ##### keywords [Optional]
Optional keywords that will be used to search through the outputs.

#### Outputs
* ##### zoneSizingObjs
EnergyPlus code that should be plugged into the "simulationOutputs" parameter of the "Honeybee_Export to OpenStudio" component.
* ##### zoneSizingValues
Script variable readEio
* ##### systemSizingObjs
Script variable readEio
* ##### systemSizingVals
Script variable readEio
* ##### componentSizObjs
Script variable readEio
* ##### componentSizVals
Script variable readEio


[Check Hydra Example Files for Read HVAC Sizing](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Read HVAC Sizing)