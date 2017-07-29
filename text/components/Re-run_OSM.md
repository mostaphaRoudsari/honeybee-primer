## ![](../../images/icons/Re-run_OSM.png) Re-run OSM - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Re-run%20OSM.py)

![](../../images/components/Re-run_OSM.png)

This is a component for running a previoulsy-generated .osm file through EnergyPlus. - 

#### Inputs
* ##### osmFilePath [Required]
A file path of the an OpemStdio file
* ##### epwFileAddress [Required]
Address to epw weather file.
* ##### runIt [Required]
Set to "True" to have the component generate an IDF file from the OSM file and run the IDF through through EnergyPlus.  Set to "False" to not run the file (this is the default).  You can also connect an integer for the following options: 0 = Do Not Run OSM and IDF thrrough EnergyPlus 1 = Run the OSM and IDF through EnergyPlus with a command prompt window that displays the progress of the simulation 2 = Run the OSM and IDF through EnergyPlus in the background (without the command line popup window). 3 = Generate an IDF from the OSM file but do not run it through EnergyPlus

#### Outputs
* ##### readMe!
Report!
* ##### idfFileAddress
Script variable Re-Run OSM
* ##### resultFileAddress
The address of the EnergyPlus result file.
* ##### studyFolder
The directory in which the simulation has been run.  Connect this to the 'Honeybee_Lookup EnergyPlus' folder to bring many of the files in this directory into Grasshopper.


[Check Hydra Example Files for Re-run OSM](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Re-run OSM)