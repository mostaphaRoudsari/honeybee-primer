## ![](../../images/icons/Scale_Honeybee.png) Scale Honeybee

![](../../images/components/Scale_Honeybee.png)

Scale Honeybee Objects Non-Uniformly - 

#### Inputs
* ##### HBObj [Required]
Honeybee surface or Honeybee zone
* ##### plane [Default]
Base Plane
* ##### X [Default]
Scaling factor in {x} direction
* ##### Y [Default]
Scaling factor in {y} direction
* ##### Z [Default]
Scaling factor in {z} direction
* ##### name [Default]
An optional text string that will be appended to the name of the transformed object(s).  If nothing is input here, a default unique name will be generated.
* ##### keepAdj [Optional]
Set to 'False' to remove existing adjacencies and boundary conditions (this is useful if you plan to re-solve adjacencies after this component). If left blank or set to 'True', the component will preserve adjacencies with other zones.

#### Outputs
* ##### HBObj
Transformed objects


[Check Hydra Example Files for Scale Honeybee](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Scale Honeybee)