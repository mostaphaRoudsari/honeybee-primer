## ![](../../images/icons/Vertical_Sky_Component.png) Vertical Sky Component

![](../../images/components/Vertical_Sky_Component.png)

Analysis Recipie for Vertical Sky Component The idea Based on this discussion on RADIANCE: http://www.radiance-online.org/pipermail/radiance-general/2006-September/004017.html - 

#### Inputs
* ##### testPoints [Required]
Test points
* ##### ptsVectors [Optional]
Point vectors
* ##### testMesh [Optional]
Script variable verticalSkyComponent
* ##### ad [Default]
Number of ambient divisions. "The error in the Monte Carlo calculation of indirect illuminance will be inversely proportional to the square root of this number. A value of zero implies no indirect calculation."
* ##### uniformSky [Optional]
Set to true to run the study under a CIE uniform sky. Default is set to cloudy sky

#### Outputs
* ##### analysisRecipe
Recipe for vertical sky component


[Check Hydra Example Files for Vertical Sky Component](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Vertical Sky Component)