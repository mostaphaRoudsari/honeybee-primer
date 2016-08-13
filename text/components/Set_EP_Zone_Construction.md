## ![](../../images/icons/Set_EP_Zone_Construction.png) Set EP Zone Construction

![](../../images/components/Set_EP_Zone_Construction.png)

Update EP construction of zone based on type - 

#### Inputs
* ##### HBZone [Required]
Honeybee zone
* ##### wallEPConstruction [Optional]
Optional new construction for walls. This input can also accept lists of construction names and will assign different constructions based on cardinal direction, starting with north and moving counter-clockwise.
* ##### windowEPConstruction [Optional]
Optional new construction for windows
* ##### roofEPConstruction [Optional]
Optional new construction for roofs
* ##### floorEPConstruction [Optional]
Optional new construction for floors
* ##### expFloorEPConstruction [Optional]
Optional new construction for exposed floors
* ##### skylightEPConstruction [Optional]
Optional new construction for skylights

#### Outputs
* ##### modifiedHBZone
Honeybee zone with updated constructions


[Check Hydra Example Files for Set EP Zone Construction](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Set EP Zone Construction)