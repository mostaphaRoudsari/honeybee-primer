## ![](../../images/icons/Honeybee_Lighting_Density_Calculator.png) Honeybee Lighting Density Calculator

![](../../images/components/Honeybee_Lighting_Density_Calculator.png)

Use this component to calculate the Lighting Density Per Area Load from information about your bulb, fixture type, mainteneance, and required lighting level.

#### Inputs
* ##### lightLevel [Required]
A number representing the required light level in the room in lux. For instance, 500 lux for a typical office area or 300 lux for a typical residential space. Note that a lux value input here means that light level is reached everywhere on the room floor plan.
* ##### luminousEfficacy [Optional]
A value between 0 and 100 that represents how well a light source produces visible light in lumens/Watt. More specifically, it is the ratio of luminous flux (in Lumens) coming from a buld to electrical power (in Watts) going into the bulb. Here are some common options:
* ##### maintenanceFactor [Optional]
A number between 0 and 1 that represents how often the lights are cleaned and replaced (higher numbers mean more often). It takes into account such factors as decreased efficiency with age, accumulation of dust within the fitting itself and the depreciation of reflectance as walls and reflecting surfaces age. 
* ##### coefficientOfUtilization [Optional]
A number between 0 and 1 that represents the fraction of the lumens from the bulb that finally find their way to the work plane (higher values indicate a more efficient fixture). This number depends on the particular fixture type, the number of lamps in it, the lens used, its beam pattern, the shape of the room (Room Cavity Ratio, RCR) and the reflectances of the ceiling (Rc), walls (Rw) and floor (Rf).

#### Outputs
* ##### out
The execution information, as output and error streams
* ##### lightingDensityPerArea
(W/m2)The lighting load per square meter of floor, which can be plugged into the "Set EnergyPlus Loads" component.


[Check Hydra Example Files for Honeybee Lighting Density Calculator](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee Lighting Density Calculator)