## ![](../../images/icons/SplitFloor2ThermalZones.png) SplitFloor2ThermalZones - [[source code]](https://github.com/ladybug-tools/honeybee-legacy/tree/master/src/Honeybee_SplitFloor2ThermalZones.py)

![](../../images/components/SplitFloor2ThermalZones.png)

Use this component to divide up a brep (polysurface) representative of a building floor into smaller volumes that roughly correspond to how a generic EnergyPlus model should be zoned. This zoning divide up each floor into a core and perimeter zones, which helps account for the different microclimates you would get on each of the different orientations of a building. Note: This component is intended mainly for convex geometry. Most concave geometries will fail, and any shapes with holes in them will fail. You should therefore prepare the massing of your building by dividing it into convex volumes before using this component. _ If you have a single mass representing two towers off of a podium, the two towers are not a continuous mass and you should therefore send each tower and the podium in as a separate Brep into this component. Core and perimeter zoneing should work for almost all masses where all walls are planar. While this component can usually get you the most of the way there, it is still recommended that you bake the output and check the geometry in Rhino before turning the breps into HBZones. _ The assumption about an E+ zone is that the air is well mixed and all at the same temperature. Therefore, it is usually customary to break up a building depending on the areas where you would expect different building microclimates to exist. This includes breaking up the building into floors (since each floor can have a different microclimate) and breaking up each floor into a core zone and perimeter zones (since each side of the buidling gets a different amount of solar gains and losses/gains through the envelope). This component helps break up building masses in such a manner. - 

#### Inputs
* ##### bldgFloors [Required]
A Closed brep or list of closed breps representing building floors. In this WIP only convex geometries and very simple concave geometries will succeed. You should prepare the massing of your building by dividing it into convex volumes before using this component. You can use the Honeybee_SplitBuildingMass2Floors to generate floors from a building mass.
* ##### perimeterZoneDepth [Required]
A number for perimeter depths in Rhino model units that will be used to divide up each floor of the building into core and perimeter zones.
* ##### runIt [Required]
Script input _runIt.

#### Outputs
* ##### readMe!
...
* ##### splitBldgZones
A series of breps that correspond to the recommended means of breaking up building geometry into zones for energy simulations. All zones for each floor will have its own list.


[Check Hydra Example Files for SplitFloor2ThermalZones](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_SplitFloor2ThermalZones)