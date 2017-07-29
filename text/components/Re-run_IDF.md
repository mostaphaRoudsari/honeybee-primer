## ![](../../images/icons/Re-run_IDF.png) Re-run IDF - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Re-run%20IDF.py)

![](../../images/components/Re-run_IDF.png)

This is a component for running a previoulsy-generated .idf file through EnergyPlus. - 

#### Inputs
* ##### idfFilePath [Required]
Name of the idf file (e.g. sample1.idf).
* ##### epwFileAddress [Required]
Address to epw weather file.
* ##### runIt [Required]
Set to 'True' to run the simulation.

#### Outputs
* ##### report
Report!
* ##### resultFileAddress
The address of the EnergyPlus result file.


[Check Hydra Example Files for Re-run IDF](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Re-run IDF)