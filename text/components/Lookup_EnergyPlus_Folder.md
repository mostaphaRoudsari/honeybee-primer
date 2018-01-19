## ![](../../images/icons/Lookup_EnergyPlus_Folder.png) Lookup EnergyPlus Folder - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Lookup%20EnergyPlus%20Folder.py)

![](../../images/components/Lookup_EnergyPlus_Folder.png)

Search Energy Simulation Folder - 

#### Inputs
* ##### studyFolder [Required]
Path to base study folder. It can be a single simulation folder or a folder containing subfolders produced by parametric simulations
* ##### studyType [Optional]
Input for Honeybee EnergyPlus study type: 1 > Energy Plus 2 > OpenStudio
* ##### refresh [Optional]
Refresh

#### Outputs
* ##### readMe!
The execution information, as output and error streams
* ##### idfFiles
The file path of the Input Data File (idf) file that has been generated on your machine.
* ##### osmFiles
The file path of the OpenStudio Model (osm) file that has been generated on your machine.
* ##### resultFileAddress
The file path of the Comma-Separated Values file (csv)  result file that has been generated on your machine.
* ##### scheduleCsvFiles
The file paths to any CSV schedules in the study folder.
* ##### rddFiles
The file path of the Report Data Dictionary (rdd) file that has been generated on your machine.
* ##### errFiles
The file path of the Error (err) file that has been generated on your machine.
* ##### eioFiles
The file path of the EnergyPlus Invariant Output (eio) file that has been generated on your machine.
* ##### esoFiles
The file path of the EnergyPlus Simulation Output (eso) result file that has been generated on your machine.
* ##### sqlFiles
The file path of the Structured Query Language (sql) result file that has been generated on your machine.


[Check Hydra Example Files for Lookup EnergyPlus Folder](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Lookup EnergyPlus Folder)