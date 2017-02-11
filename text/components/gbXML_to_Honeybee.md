## ![](../../images/icons/gbXML_to_Honeybee.png) gbXML to Honeybee

![](../../images/components/gbXML_to_Honeybee.png)

Import gbXML files as Honeybee zones.

#### Inputs
* ##### filepath [Required]
Full filepath to xml file.
* ##### zoneNames [Required]
The list of names for thermal zones that you want to be loaded
* ##### import [Required]
Set to True to import the model.

#### Outputs
* ##### readMe!

* ##### model
OpenStudio model which is created from the gbXML file. This output
* ##### HBZones
List of honeybee zones.
* ##### shadings
List of shading surfaces if any.


[Check Hydra Example Files for gbXML to Honeybee](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_gbXML to Honeybee)