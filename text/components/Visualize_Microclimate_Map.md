## ![](../../images/icons/Visualize_Microclimate_Map.png) Visualize Microclimate Map

![](../../images/components/Visualize_Microclimate_Map.png)

Use this component to produce a colored mesh from a comfResultsMtx. - 

#### Inputs
* ##### comfResultsMtx [Required]
Any matrix output from the 'Honeybee_Microclimate Map Analysis' component, the 'Honeybee_Thermal Comfort Autonomy Analysis' component, or the 'Honeybee_Read Microclimate Matrix' component.
* ##### viewFactorMesh [Required]
The list of view factor meshes that comes out of the  'Honeybee_Indoor View Factor Calculator'.  These will be colored with result data.
* ##### legendPar [Optional]
Optional legend parameters from the Ladybug Legend Parameters component.
* ##### runIt [Optional]
Set boolean to 'True' to run the component and visualize indoor comfort.

#### Outputs
* ##### readMe!
...
* ##### resultMesh
A list of colored meshes showing the results form the comfResultsMtx.
* ##### legend
A legend for the colored mesh. Connect this output to a grasshopper "Geo" component in order to preview the legend spearately in the Rhino scene.
* ##### legendBasePt
The legend base point, which can be used to move the legend with the grasshopper "move" component.
* ##### resultValues
The values of results that are being used to color the results.
* ##### resultColors
The colors used for each mesh face.


[Check Hydra Example Files for Visualize Microclimate Map](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Visualize Microclimate Map)