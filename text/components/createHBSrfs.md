## ![](../../images/icons/createHBSrfs.png) createHBSrfs

![](../../images/components/createHBSrfs.png)

Create a Honeybee surface, which can be plugged into the "Run Daylight Sumilation" component or combined with other surfaces to make HBZones with the "createHBZones" component.

#### Inputs
* ##### geometry [Required]
List of Breps
* ##### srfName [Optional]
Optional name for surface
* ##### srfType [Optional]
Optional input for surface type >
* ##### EPBC [Optional]
'Ground', 'Adiabatic', 'Outdoors'
* ##### EPConstruction [Default]
Optional EnergyPlus construction
* ##### RADMaterial [Default]
Optional Radiance Material

#### Outputs
* ##### readMe!
...
* ##### HBSurface
Honeybee zone as the result


[Check Hydra Example Files for createHBSrfs](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_createHBSrfs)