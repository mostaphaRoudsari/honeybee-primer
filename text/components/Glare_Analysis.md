## ![](../../images/icons/Glare_Analysis.png) Glare Analysis

![](../../images/components/Glare_Analysis.png)

Glare Analysis

#### Inputs
* ##### HDRImagePath [Required]
Path to an HDR image file
* ##### taskPositionUV [Optional]
Task position in x and y coordinates
* ##### taskPositionAngle [Optional]
Task position opening angle in degrees
* ##### runIt [Required]
Set to True to run the analysis

#### Outputs
* ##### readMe
...
* ##### glareCheckImage
Path to HDR image of the glare study
* ##### DGP
Daylight glare probability. Imperceptible Glare [0.35 > DGP], Perceptible Glare [0.4 > DGP >= 0.35], Disturbing Glare [0.45 > DGP >= 0.4], Intolerable Glare [DGP >= 0.45]
* ##### DGI
Daylight glare index
* ##### imageWithTaskArea
Path to HDR image with task area marked with blue circle


[Check Hydra Example Files for Glare Analysis](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Glare Analysis)