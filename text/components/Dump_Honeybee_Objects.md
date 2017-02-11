## ![](../../images/icons/Dump_Honeybee_Objects.png) Dump Honeybee Objects

![](../../images/components/Dump_Honeybee_Objects.png)

Dump Honeybee Objects Use this component to dump Honeybee objects to a file on your system. You can use load Honeybee objects to load the file to Grasshopper. WARNING: The component is WIP and it doesn't currently save the following properites:     1) custom schedules     2) custom materials     3) hvac airDetails, heatingDetails, coolingDetails     4) adjacencies between zones - 

#### Inputs
* ##### HBObjects [Required]
A list of Honeybee objects
* ##### filePath [Required]
A valid path to a file on your drive (e.g. c:\ladybug\20ZonesExample.HB)
* ##### dump [Required]
Set to True to save the objects to file

#### Outputs
* ##### readMe!
...
* ##### filePath
The location of the file where the HBZones have been saved.


[Check Hydra Example Files for Dump Honeybee Objects](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Dump Honeybee Objects)