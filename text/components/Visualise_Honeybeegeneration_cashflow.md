## ![](../../images/icons/Visualise_Honeybeegeneration_cashflow.png) Visualise_Honeybeegeneration_cashflow

![](../../images/components/Visualise_Honeybeegeneration_cashflow.png)

Use this component to the calculate and visualise the financial value of Honeybee generation systems over 25 years. At present you can only create grid connected renewable energy systems without storage. For this reason you must specify both the grid electricity price and fed in tariff rate.

#### Inputs
* ##### inputData [Required]
To use this component please input all the outputs from the component readEP_generation_system_results here
* ##### discountFactor [Optional]
An optional input - specify the interest rate as a percentage to calculate a discount factor for each Honeybee generation system. A discount factor is a ratio used to calculate the present value of a future revenue or cost that occurs in any year of the system lifetime (25 years) using the equation - fd = 1/(1+i)^N where: i = real interest rate ,N = number of years. If this field is left blank no discount factor will be applied
* ##### gridElectCostSchedule [Required]
The cost of grid connected electricty per Kwh in US dollars
* ##### feedInTariffSchedule [Required]
The price that the utility will pay per Kwh in US dollars for power fed back into the grid. 
* ##### graphDataByHBSystem [Optional]
Set to True to visualise the the financial value of each Honeybee generation system.
* ##### graphDataByCost [Optional]
Set to True to sum each Honeybee generation system's costs and revenues together and then to visualise these figures by type e.g replacement costs, capital costs etc.
* ##### xScale [Default]
The scale of the X axis of the graph. The default will plot the X axis with a length of 215 Rhino model units 
* ##### zScale [Default]
The scale of the Y axis of the graph. The default will plot the Z axis with a length of 85 Rhino model units 
* ##### fontSize [Default]
An optional input, use a float to change the size of the font on the graph.
* ##### basePoint [Default]
An optional input, use a 3D point to locate the 3D chart in the Rhino Model.  The default is set to the Rhino origin at (0,0,0).

#### Outputs
* ##### Readme!
The execution information, as output and error streams
* ##### gensystem_value
The net present cost of each Honeybee generation system. The net present cost is the present value of all the costs of installing and operating that Honeybee generation system over 25 years minus the present value of the all the revenues that the system earns over 25 years. 
* ##### dataMeshes
Script output dataMeshes.
* ##### axisMeshes
Script variable HB_GeneratorCashflow
* ##### textSrfs
Script output textSrfs.


[Check Hydra Example Files for Visualise_Honeybeegeneration_cashflow](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Visualise_Honeybeegeneration_cashflow)