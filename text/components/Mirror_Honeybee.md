## ![](../../images/icons/Mirror_Honeybee.png) Mirror Honeybee - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Mirror%20Honeybee.py)

![](../../images/components/Mirror_Honeybee.png)

Mirror Honeybee Objects - 

#### Inputs
* ##### HBObj [Required]
Honeybee surface or Honeybee zone.
* ##### plane [Required]
Mirror plane.
* ##### name [Default]
An optional text string that will be appended to the name of the transformed object(s).  If nothing is input here, a default unique name will be generated.
* ##### keepAdj [Optional]
Set to 'False' to remove existing adjacencies and boundary conditions (this is useful if you plan to re-solve adjacencies after this component). If left blank or set to 'True', the component will preserve adjacencies with other zones.

#### Outputs
* ##### HBObj
Transformed objects


[Check Hydra Example Files for Mirror Honeybee](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Mirror Honeybee)