## ![](../../images/icons/Generate_Average_Sky.png) Generate Average Sky

![](../../images/components/Generate_Average_Sky.png)

Generate Average Climate Based Sky This component generate an average climate based data for a single hour during a month - 

#### Inputs
* ##### north [Optional]
Input a vector to be used as a true North direction for the sun path or a number between 0 and 360 that represents the degrees off from the y-axis to make North.  The default North direction is set to the Y-axis (0 degrees).
* ##### weatherFile [Required]
epw weather file address on your system
* ##### month [Required]
Month of the study [1-12]
* ##### hour [Required]
Hour of the study [1-24]

#### Outputs
* ##### radiationValues
Average direct and diffuse radiation during the month for the input hour
* ##### skyFilePath
Sky file location on the local drive


[Check Hydra Example Files for Generate Average Sky](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Generate Average Sky)