## ![](../../images/icons/Find_Non-Convex.png) Find Non-Convex - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Find%20Non-Convex.py)

![](../../images/components/Find_Non-Convex.png)

In EnergyPlus, Solar distribution determines how EnergyPlus treats the beam solar radiation and reflectances from exterior surfaces that strike the building, and ultimately, enter the zone. There are five choices: MinimalShadowing, FullExterior and FullInteriorAndExterior, FullExteriorWithReflections, FullInteriorAndExteriorWithReflections. If you intend to use either of FullInteriorAndExterior, FullExteriorWithReflections, FullInteriorAndExteriorWithReflections, you must make sure that all your zones are convex. _ If you encounter a severe error saying, "DetermineShadowingCombinations: There are # surfaces which are casting surfaces and are non-convex," you should find those non-convex surface in your model and turn them into convex surfaces by splitting them. _ Spotting a non-convex surface is quite easy. While this component is here to quickly help you detect non-convex surfaces in your model, having conceptual understanding about what it means to have a no-convex surface will make you aware of such surfaces while you are creating zones.  _ Following are a couple ways to eyeball a non-convex surface. _ 1. Imagine you’re drawing lines from one vertice of a surface to all other vertices of the same surface and you’re doing this for all the vertices of the surface. Now if all those lines fall totally inside the surface then it’s a convex surface. If any of the lines, or even a part of it falls outside of the surface then it’s a non-convex surface. _ 2. Imagine you are walking from one vertice of a surface to the next verice of the same surface, and you are travelling to all the vertices of the surface like that. While making this journey, you'll make turns. If all those turns that you took at vertices, are either clockwise or counter-clockwise, then the surface is convex. If at least one of the turns was in the opposite direction, meaning, if total number of turns you took were 6, and out of those, 5 times you turned clockwise (or counter-clockwise) and one time you turned counter-clockwise (or clockwise), then it is a non-convex surface. _ 3. EnergyPlus displays severe error for non-convex zones. So if any of the face of the zone is made of more than one planar surfaces, and none of those surfaces are non-convex, however, if the resultant zone is not convex then EnergyPlus will still announce a severe error. To address this, in addition to providing your breps as input to this component,  please also pass your breps through the native grasshopper Merge Faces (FMerge) component. And then provide the output of FMerge component (Simplified Brep) to the input of this component. _ Please visit the following link to know why EnegyPlus does not like non-convex surfaces. http://bigladdersoftware.com/epx/docs/8-2/input-output-reference/group-simulation-parameters.html#field-solar-distribution - 

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