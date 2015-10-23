## ![](../../images/icons/Read_generation_system_results.png) Read_generation_system_results

![](../../images/components/Read_generation_system_results.png)

This component reads the results of an EnergyPlus simulation from the WriteIDF Component or any EnergyPlus result .csv file address.  Note that, if you use this component without the WriteIDF component, you should make sure that a corresponding .eio file is next to your .csv file at the input address that you specify.

#### Inputs
* ##### resultFileAddress [Required]
The result file address that comes out of the WriteIDF component.
* ##### idfFileAddress [Required]
The IDF file address that comes out of the WriteIDF component.

#### Outputs
* ##### Readme!
The execution information, as output and error streams
* ##### totalelectdemand
The total electricity demand of the facility in Kwh
* ##### netpurchasedelect
The net purchased electricity of the facility in Kwh
* ##### generatorproducedenergy
The electricity produced by each Honeybee generator in the facility
* ##### financialdata
The financial data of the Honeybee generators in the facility.


[Check Hydra Example Files for Read_generation_system_results](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Read_generation_system_results)