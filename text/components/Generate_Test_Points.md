## ![](../../images/icons/Generate_Test_Points.png) Generate Test Points - [[source code]](https://github.com/ladybug-tools/honeybee-legacy/tree/master/src/Honeybee_Generate%20Test%20Points.py)

![](../../images/components/Generate_Test_Points.png)

Genrate Test Points - 

#### Inputs
* ##### testGeometry [Required]
Test surface as a Brep.
* ##### gridSize [Required]
Size of the test grid.
* ##### distBaseSrf [Required]
Distance from base surface.
* ##### moveTestMesh [Optional]
Set to 'False' if you want test mesh not to move. Default is 'True'.

#### Outputs
* ##### readMe!
...
* ##### testPoints
Test points
* ##### ptsVectors
Vectors
* ##### facesArea
Script output facesArea.
* ##### mesh
Analysis mesh


[Check Hydra Example Files for Generate Test Points](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Generate Test Points)