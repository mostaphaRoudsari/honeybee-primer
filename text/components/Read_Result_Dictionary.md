## ![](../../images/icons/Read_Result_Dictionary.png) Read Result Dictionary - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Read%20Result%20Dictionary.py)

![](../../images/components/Read_Result_Dictionary.png)

This component parses an .rdd file from an energy simulation to show all possible outputs that could be requested. - 

#### Inputs
* ##### rddFile [Required]
The file address of the rdd file that comes out of the "Honeybee_Lookup EnergyPlus Folder" component.
* ##### keywords [Optional]
Optional keywords that will be used to search through the outputs.
* ##### timestep [Default]
Specify a timestep by inputing the words 'hourly', 'daily', 'monthly' or 'annual'.  The default is set to hourly.

#### Outputs
* ##### simOutputs
EnergyPlus code that should be plugged into the "simulationOutputs" parameter of the "Honeybee_Export to OpenStudio" component.


[Check Hydra Example Files for Read Result Dictionary](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Read Result Dictionary)