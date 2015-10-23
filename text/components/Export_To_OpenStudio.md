## ![](../../images/icons/Export_To_OpenStudio.png) Export To OpenStudio

![](../../images/components/Export_To_OpenStudio.png)

Use this component to export HBZones into an OpenStudio file, and run them through EnergyPlus. _ The component outputs the report from the simulation, the file path of the IDF file, and the CSV result file from the EnergyPlus run, and two other result files that record outputs in different formats. - 

#### Inputs
* ##### north [Optional]
Input a vector to be used as a true North direction for the energy simulation or a number between 0 and 360 that represents the degrees off from the y-axis to make North.  The default North direction is set to the Y-axis (0 degrees).
* ##### epwWeatherFile [Required]
Script variable exportToOpenStudio
* ##### analysisPeriod [Default]
An optional analysis period from the Ladybug_Analysis Period component.  If no Analysis period is given, the energy simulation will be run for the enitre year.
* ##### energySimPar [Default]
Optional Energy Simulation Parameters from the "Honeybee_Energy Simulation Par" component.  If no value is connected here, the simulation will run with the following parameters: 1 - 6 timeSteps per hour 2 - A shadow calculation that averages over multiple days (as opposed to running it for each timeStep) 3 - A shadow calculation frequency of 30 (meaning that the shadow calulation is averaged over every 30 days) 4 - A maximum of 3000 points used in the shadow calculation. (This may need to be higher if you have a lot of detailed context geometry) 5 - An colar energy calculation that includes both interior and exterior light reflections. 6 - A simulation including a zone sizing calculation, a system sizing calculation, a plat sizing calculation, and a full run of the energy use ofver the analysis period.  The simulation is not run for the sizing period by default. 7 - A system sizing period that runs from the extreme periods of the weather file and not a ddy file. 8 - City terrian.
* ##### HBZones [Required]
The HBZones that you wish to write into an OSM file and/or run through EnergyPlus.  These can be from any of the components that output HBZones.
* ##### HBContext [Optional]
Optional HBContext geometry from the "Honeybee_EP Context Surfaces." component.
* ##### simulationOutputs [Optional]
A list of the outputs that you would like EnergyPlus to write into the result CSV file.  This can be any set of any outputs that you would like from EnergyPlus, writen as a list of text that will be written into the IDF.  It is recommended that, if you are not expereinced with writing EnergyPlus outputs, you should use the "Honeybee_Write EP Result Parameters" component to request certain types of common outputs. 
* ##### writeOSM [Required]
Set to "True" to have the component take your HBZones and other inputs and write them into an OSM file.  The file path of the resulting OSM file will appear in the osmFileAddress output of this component.  Note that only setting this to "True" and not setting the output below to "Tru"e will not automatically run the file through EnergyPlus for you.
* ##### runSimulation [Optional]
Set to "True" to have the component run your OSM file through EnergyPlus once it has finished writing it.  This will ensure that a CSV result file appears in the resultFileAddress output.
* ##### fileName [Optional]
Optional text which will be used to name your OSM, IDF and result files.  Change this to aviod over-writing results of previous energy simulations.
* ##### workingDir [Optional]
An optional working directory to a folder on your system, into which your OSM, IDF and result files will be written.  NOTE THAT DIRECTORIES INPUT HERE SHOULD NOT HAVE ANY SPACES OR UNDERSCORES IN THE FILE PATH.

#### Outputs
* ##### ReadMe!
The execution information, as output and error streams
* ##### osmFileAddress
The file path of the OSM file that has been generated on your machine.
* ##### idfFileAddress
The file path of the IDF file that has been generated on your machine. This only happens when you set "runSimulation_" to "True."
* ##### resultsFileAddress
Script variable exportToOpenStudio
* ##### sqlFileAddress
The file path of the SQL result file that has been generated on your machine. This only happens when you set "runSimulation_" to "True."
* ##### meterFileAddress
The file path of the building's meter result file that has been generated on your machine. This only happens when you set "runSimulation_" to "True."


[Check Hydra Example Files for Export To OpenStudio](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Export To OpenStudio)