## ![](../../images/icons/Add_Internal_Mass_to_Zone.png) Add Internal Mass to Zone - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Add%20Internal%20Mass%20to%20Zone.py)

![](../../images/components/Add_Internal_Mass_to_Zone.png)

Use this component to assign internal thermal masses to zones, which can be used to account for the effects of furniture inside zones or massive building components like hearths and chimneys. _ The component accepts either surfaces of Rhino geometry (representing furniture or building elements) or a numerical value of the mass's surface area.  Several of these components can be used in a series to descibe internal masses (or furniture) made of different materials). _ Note that internal masses assigned this way cannot "see" solar radiation that may potentially hit them and, as such, caution should be taken when using this component with internal mass objects that are not always in shade. Masses are only factored into the the thermal calculations of the zone by undergoing heat transfer with the indoor air. - 

#### Inputs
* ##### HBZones [Required]
HBZones for which internal masses are to be assigned.
* ##### internalMassName [Optional]
An optional text name for the internal mass.  This can be useful for keeping track of different internal mass types if you use several of this component in series.
* ##### srfsOrSrfArea [Required]
A list of Rhino breps representing the surfaces of internal masses (or furniture) that are exposed to the air of the zone.  Alternatively, this can be a number or list of numbers representing the surface area of the internal masses (or furniture) that are exposed to the zone air. _ In the case of breps representing the surfaces of internal masses, this component is smart enough to know which zone the surfaces are in.  However, all surfaces must lie COMPLETELY inside a single zone and cannot span between zones or span outside the building.  If you have an object that lies between two zones, please split it in two along the boundary between the zones. _ In the case of numbers representing the the surface area of the internal masses, inputs can be either a single number (which will be used to put internal masses into all zones using the specified surface area), or it can be a list of numbers that matches the input zones, which can be used to assign different levels of mass surface area to different zones.
* ##### EPConstruction [Required]
An EnergyPlus Construction that represents the type of material that the thermal mass is composed of.  This can be either a construction from the "Call from EP Construction Library" component or a custom construction from the "EnergyPlus Construction" component.

#### Outputs
* ##### readMe!
The execution information, as output and error streams
* ##### HBZones
HBZones with internal masses assigned.


[Check Hydra Example Files for Add Internal Mass to Zone](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Add Internal Mass to Zone)