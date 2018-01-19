## ![](../../images/icons/Find_Non-Convex.png) Find Non-Convex - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Find%20Non-Convex.py)

![](../../images/components/Find_Non-Convex.png)

In EnergyPlus, Solar distribution determines how EnergyPlus treats the beam solar radiation and reflectances from exterior surfaces that strike the building, and ultimately, enter the zone. There are five choices: MinimalShadowing, FullExterior and FullInteriorAndExterior, FullExteriorWithReflections, FullInteriorAndExteriorWithReflections. If you intend to use either of FullInteriorAndExterior, FullExteriorWithReflections, FullInteriorAndExteriorWithReflections, you must make sure that all your zones are convex.

#### Inputs
* ##### breps [Required]
A list of breps that you wish to scan for non-convex surfaces

#### Outputs
* ##### readMe!
Messages
* ##### nonConvex
A list of non-convex surfaces, if found in breps provided.
* ##### faultyGeometry
A list of faultyGeometry if found in breps provided. Typically these are surfaces with more edge curves than the visibale edges of the surface. If such surfaces are found in your model, please use native  grasshopper Deconstruct Brep component to analyze the faultyGeometry.


[Check Hydra Example Files for Find Non-Convex](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Find Non-Convex)