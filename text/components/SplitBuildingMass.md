## ![](../../images/icons/SplitBuildingMass.png) SplitBuildingMass - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_SplitBuildingMass.py)

![](../../images/components/SplitBuildingMass.png)

Use this component to divide up a brep (polysurface) representative of a complete building massing into smaller volumes that roughly correspond to how a generic EnergyPlus model should be zoned. This generic zoning will divide the input mass into seprate floors based on an input floor height. This zoning can also divide up each floor into a core and perimeter zones, which helps account for the different microclimates you would get on each of the different orientations of a building. _ If you have a single mass representing two towers off of a podium, the two towers are not a continuous mass and you should therefore send each tower and the podium in as a separate Brep into this component.  The component will work for courtyard buildings. Core and perimeter zoneing should work for almost all masses where all walls are planar.  It works in a limited number of cases that have both curved and planar walls.  Also, it is important to note that, if your offset depth is so large in comparison to your building depth as to create perimeter zones that intersect one another, the whole floor will be returned as a single zone. While this component can usually get you the most of the way there, it is still recommended that you bake the output and check the geometry in Rhino before turning the breps into HBZones. _ The assumption about an E+ zone is that the air is well mixed and all at the same temperature. Therefore, it is usually customary to break up a building depending on the areas where you would expect different building microclimates to exist. This includes breaking up the building into floors (since each floor can have a different microclimate) and breanking up each floor into a core zone and perimeter zones (since each side of the buidling gets a different amount of solar gains and losses/gains through the envelope). This component helps break up building masses in such a manner. - 

#### Inputs
* ##### bldgMasses [Required]
A Closed brep or list of closed breps representing a building massing.
* ##### bldgsFlr2FloorHeights [Optional]
A list of floor heights in Rhino model units that will be used to make each floor of the building.  The list should run from bottom floor to top floor.  Alternatively, you can input a text string that codes for how many floors of each height you want.  For example, inputting "2@4" (without quotations) will make two ground floors with a height of 4 Rhino model units.  Simply typing "@3" will make all floors 3 Rhino model units.  Putting in lists of these text strings will divide up floors accordingly.  For example, the list "1@5   2@4   @3"  will make a ground floor of 5 units, two floors above that at 4 units and all remaining floors at 3 units.
* ##### perimeterZoneDepth [Optional]
A list of perimeter zone depths in Rhino model units that will be used to divide up each floor of the building into core and perimeter zones.  The list should run from bottom floor to top floor.  Alternatively, you can input a text string that codes for which floors you want at which zone depth.  For example, inputting "2@4" (without quotations) will divide up the two ground floors with a perimeter zone depth of 4 Rhino model units.  Simply typing "@3" will divide up all floors with a zone depth of 3 Rhino model units.  Putting in lists of these text strings will divide up floors accordingly.  For example, the list "1@5   2@4   @3"  will make a ground floor divided up with a zone depth of 5 units, two floors divided at 4 units and all remaining floors at 3 units.
* ##### runIt [Required]
Script variable Python

#### Outputs
* ##### readMe!
...
* ##### splitBldgMasses
The building mass split up into zone geometries.


[Check Hydra Example Files for SplitBuildingMass](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_SplitBuildingMass)