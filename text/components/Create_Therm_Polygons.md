## ![](../../images/icons/Create_Therm_Polygons.png) Create Therm Polygons

![](../../images/components/Create_Therm_Polygons.png)

Use this component to create a THERM polygon with material properties. - 

#### Inputs
* ##### geometry [Required]
A closed planar curve or list of closed planar curves that represent the portions of a construction that have the same material type.  This input can also accept closed planar surfaces/breps/polysurfaces and even meshes!
* ##### material [Required]
Either the name of an EnergyPlus material from the OpenStudio library (from the "Call from EP Construction Library" component) or the output of any of the components in the "06 | Energy | Material" tab for creating materials.
* ##### name [Optional]
An optional name for the polygon to keep track of it through the creation of the THERM model.
* ##### RGBColor [Optional]
Script variable createThermPolygons

#### Outputs
* ##### readMe!
...
* ##### thermPolygon
A polygon representing material properties


[Check Hydra Example Files for Create Therm Polygons](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Create Therm Polygons)