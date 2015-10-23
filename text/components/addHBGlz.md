## ![](../../images/icons/addHBGlz.png) addHBGlz

![](../../images/components/addHBGlz.png)

Use this component to add a custom glazing surface to a HBSurface or HBZone.

#### Inputs
* ##### HBObj [Required]
A HBZone or HBSurface to which you would like to add a customized glazing surface.
* ##### childSurfaces [Required]
A surface or list of surfaces that represent the custom window(s) that you would like to add.  Note that these surfaces should be co-planar to the connected HBSurface or one of the surfaces of the connected HBZones.
* ##### EPConstruction [Optional]
An optional EnergyPlus construction to set the material construction of the window added to the HBSurface or HBZone.  This can be either the name of a window construction from the OpenStudio library (coming out of the 'Honeybee_Call from EP Construction Library' component) or a custom window construction you created from the 'Honeybee_EnergyPlus Construction' component.
* ##### RADMaterial [Optional]
An optional Radiance material to set the material of the window added to the HBSurface or HBZone.  This can be either the name of a window material from the default Radaince library (coming out of the 'Honeybee_Call from Radiance Library' component) or a custom window material you created from any of the Radiance material components (like the 'Honeybee_Radiance Glass Material' component).

#### Outputs
* ##### HBObjWGLZ
The Honeybee surface or zone with assigned glazing (in case of success).


[Check Hydra Example Files for addHBGlz](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_addHBGlz)