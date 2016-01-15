## ![](../../images/icons/Create_Therm_Polygons.png) Create Therm Polygons

![](../../images/components/Create_Therm_Polygons.png)

Use this component to create a THERM polygon with material properties. - 

#### Inputs
* ##### geometry [Required]
A closed planar curve or list of closed planar curves that represent the portions of a construction that have the same material type.  This input can also accept closed planar surfaces/breps/polysurfaces and even meshes!
* ##### material [Required]
Either the name of an EnergyPlus material from the OpenStudio library (from the "Call from EP Construction Library" component) or the output of any of the components in the "06 | Energy | Material" tab for creating materials.
* ##### RGBColor [Optional]
An optional color to set the color of the material when you import it into THERM.  All materials from the Honyebee Therm Library already possess colors but materials from the EP material lib will have a default blue color if no one is assigned here.

#### Outputs
* ##### readMe!
...
* ##### thermPolygon
A polygon representing material properties


[Check Hydra Example Files for Create Therm Polygons](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Create Therm Polygons)