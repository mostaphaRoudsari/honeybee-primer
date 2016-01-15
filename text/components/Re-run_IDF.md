## ![](../../images/icons/Re-run_IDF.png) Re-run IDF

![](../../images/components/Re-run_IDF.png)

This is a component for running a previoulsy-generated .idf file through EnergyPlus with a different weather file. - 

#### Inputs
* ##### workingDir [Required]
The working directory of the energyPlus idf.
* ##### idfFileName [Required]
Name of the idf file (e.g. sample1.idf).
* ##### epwFileAddress [Required]
Address to epw weather file.
* ##### EPDirectory [Required]
[Optional] where EnergyPlus is installed on your system
* ##### writeIt [Required]
Set to true to create the new folder with batch file
* ##### runIt [Optional]
Set to 'True' to run the simulation.

#### Outputs
* ##### report
Report!
* ##### batchFileAddress
Script variable Re-Run IDF
* ##### resultFileAddress
The address of the EnergyPlus result file.


[Check Hydra Example Files for Re-run IDF](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Re-run IDF)