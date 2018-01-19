## ![](../../images/icons/SplitFloor2ThermalZones.png) SplitFloor2ThermalZones - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_SplitFloor2ThermalZones.py)

![](../../images/components/SplitFloor2ThermalZones.png)

Use this component to divide up a brep (polysurface) representative of a building floor into smaller volumes that roughly correspond to how a generic EnergyPlus model should be zoned.

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