## ![](../../images/icons/SplitBuildingMass2Floors.png) SplitBuildingMass2Floors - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_SplitBuildingMass2Floors.py)

![](../../images/components/SplitBuildingMass2Floors.png)

Use this component to divide up a brep (polysurface) representative of a complete building massing into floors.

#### Inputs
* ##### bldgMasses [Required]
A Closed brep or list of closed breps representing a building massing.
* ##### bldgsFlr2FlrHeights [Required]
A list of floor heights in Rhino model units that will be used to make each floor of the building.  The list should run from bottom floor to top floor.  Alternatively, you can input a text string that codes for how many floors of each height you want.  For example, inputting "2@4" (without quotations) will make two ground floors with a height of 4 Rhino model units.  Simply typing "@3" will make all floors 3 Rhino model units.  Putting in lists of these text strings will divide up floors accordingly.  For example, the list "1@5   2@4   @3"  will make a ground floor of 5 units, two floors above that at 4 units and all remaining floors at 3 units.
* ##### runIt [Required]
Script input _runIt.

#### Outputs
* ##### readMe!
...
* ##### splitBldgFloors
A series of breps that correspond to inputted floor heights. These can be inserted into the Honeybee_SplitBuildingFloor2ThermalZones component to further split the floors into thermal zones for energy simulation.


[Check Hydra Example Files for SplitBuildingMass2Floors](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_SplitBuildingMass2Floors)