## ![](../../images/icons/Read_Microclimate_Matrix.png) Read Microclimate Matrix - [[source code]](https://github.com/ladybug-tools/honeybee-legacy/tree/master/src/Honeybee_Read%20Microclimate%20Matrix.py)

![](../../images/components/Read_Microclimate_Matrix.png)

This component reads the results of an Adaptive Indoor Comfort Analysis.  Note that this usually takes about a minute - 

#### Inputs
* ##### comfResultFileAddress [Required]
Any one of the result file addresses that comes out of the 'Honeybee_Microclimate Map Analysis' component or the 'Honeybee_Thermal Comfort Autonomy Analysis' component.

#### Outputs
* ##### comfResultsMtx
A matrix of comfort data that can be plugged into the "Visualize Comfort Results" component.


[Check Hydra Example Files for Read Microclimate Matrix](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Read Microclimate Matrix)