## ![](../../images/icons/Apply_OpenStudio_Measure.png) Apply OpenStudio Measure - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Apply%20OpenStudio%20Measure.py)

![](../../images/components/Apply_OpenStudio_Measure.png)

This component applies an OpenStudio measure to an OpenStudio file. The component will eventually be integrated to Export to OpenStudio component. Read more about OpenStudio measures here: http://nrel.github.io/OpenStudio-user-documentation/reference/measure_writing_guide/ You can download several measures from here: https://bcl.nrel.gov/nrel/types/measure Many thanks to NREL team for their support during the process. See (https://github.com/mostaphaRoudsari/Honeybee/issues/214) and (https://github.com/mostaphaRoudsari/Honeybee/issues/290)for just two examples! - 

#### Inputs
* ##### osmFilePath [Required]
A file path of the an OpemStdio file
* ##### epwWeatherFile [Required]
An .epw file path on your system as a text string.
* ##### OSMeasure [Required]
Loaded OpenStudio measure. Use load OpenStudio measures to load the measure to Honeybee
* ##### runIt [Required]
set to True to apply the measure and run the analysis

#### Outputs
* ##### ReadMe!
The execution information, as output and error streams
* ##### projectFolder
Path to new project folder
* ##### outputFiles
Path to modified EnergyPlus file


[Check Hydra Example Files for Apply OpenStudio Measure](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Apply OpenStudio Measure)