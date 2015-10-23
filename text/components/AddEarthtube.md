## ![](../../images/icons/AddEarthtube.png) AddEarthtube

![](../../images/components/AddEarthtube.png)

Use this component to add an Energy Plus earth tube to a Zone.

#### Inputs
* ##### HBZones [Required]
The Honeybee zones to which Earthtubes will be added to. Only one earth tube will be added to each zone.
* ##### epwFile [Required]
An .epw file path on your system as a text string. Used to find the ground temperature of the site so Earthtube calculations can be undertaken.
* ##### schedules [Optional]
This field can be a schedule or a list of schedules which correspond sequentially to the _HBZones. If no schedule is given for a zone the default schedule "ALWAYS ON" will be used.
* ##### designFlowrates [Required]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float (noted as Edesign in the EarthTubeFlowRate equation) is the maximum amount of air mass flow rate of the earth tube expected at design conditions the default is 0 m3/s.
* ##### mincoolingTemps [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones.
* ##### maxheatingTemps [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float is the indoor temperature (in Celsius) above which the earth tube is shut off the default is 100 degrees C.
* ##### deltaTemps [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float is the temperature difference (in Celsius) between the indoor and outdoor air dry-bulb temperatures below which the earth tube is shut off the default is 2 degrees C.
* ##### earthTubeTypes [Default]
This field can be integer or a list of integers between 1 and 3 which correspond sequentially to the _HBZones. Each integer from 1 to 3 defines the type of earth tube as one of the following options: Natural a value of 1, Exhaust a value of 2, or Intake a value of 3. 
* ##### fanPrises [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float is the pressure rise experienced across the fan in Pascals (N/m2) the default is 150 Pascals which will be used if no value is given for a zone.
* ##### fanEfficiencies [Default]
This field can be a float or a list of floats between 0 and 1 which correspond sequentially to the _HBZones. Each float is the earth tube fan efficiency which is a decimal number between 0.0 and 1.0 the default is 1 which will be used if no value is given for a zone.
* ##### pipeRadii [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float is the radius of the earth tube(in meters) the default is 0.5 meter which will be used if no value is given for a zone. This plays a role in determining the amount of heat transferred from the surrounding soil to the air passing along the pipe. 
* ##### pipeThicknesses [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float is the thickness of the earth tube wall (in meters) the default is 0.2 meters which will be used if no value is given for a zone. 
* ##### pipeLengths [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float is the total length of the pipe (in meters) the default is 15 meters which will be used if no value is given for a zone. 
* ##### pipeDepths [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float is the depth of the pipe under the ground surface (in meters) the default is 3 meters which will be used if no value is given for a zone. 
* ##### soilCondition [Default]
An integer between 1 to 4 that defines the actual condition of the soil surrounding ALL the earth tubes: HeavyAndSaturated a value of 1, HeavyAndDamp a value of 2, HeavyAndDry a value of 3 or LightAndDry a value of 4. 
* ##### conditionGroundSurface [Default]
An integer between 1 to 8 and defines the condition of the ground surface above ALL the earth tubes.
* ##### pipeThermalConductivity [Default]
This field can be a float or a list of floats which correspond sequentially to the _HBZones. Each float is the thermal conductivity of the pipe (in W/m-K) the default is 200 W/m-K. 

#### Outputs
* ##### Readme
Details of the earth tubes created.
* ##### earthTubeHBZones
The Honeybee zones that have been modified by this component - these zones now contain an earth tube


[Check Hydra Example Files for AddEarthtube](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_AddEarthtube)