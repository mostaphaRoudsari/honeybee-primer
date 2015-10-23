## ![](../../images/icons/R-Value_With_Air_Films.png) R-Value With Air Films

![](../../images/components/R-Value_With_Air_Films.png)

Use this component to account for air films in the U-Value and R-Value of any decomposed Honeybee construction or material. Note that EnergyPlus has its own means of calculating the effects of air films on either side of a construction but, here, we provide an apporximate method based on an input surfaceType_. - 

#### Inputs
* ##### uValue_SI [Required]
The U-Value_SI out of either the "Honeybee_Decompose EP Construction" or the "Honeybee_Decompose EP Material."
* ##### surfaceType [Optional]
An integer value from 0 to 3 that represents one of the following surface types: 0 - Exterior Wall/Window 1 - Interior Wall/Window 2 - Exterior Roof 3 - Exposed Interior Floor

#### Outputs
* ##### UValue_SI_wAir
Script variable Python
* ##### UValue_IP_wAir
Script variable Python
* ##### RValue_SI_wAir
Script variable Python
* ##### RValue_IP_wAir
Script variable Python


[Check Hydra Example Files for R-Value With Air Films](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_R-Value With Air Films)