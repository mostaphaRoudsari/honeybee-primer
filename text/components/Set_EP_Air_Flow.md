## ![](../../images/icons/Set_EP_Air_Flow.png) Set EP Air Flow

![](../../images/components/Set_EP_Air_Flow.png)

Use this component to edit the airlfow between your zones and set up natural ventilation, if desired.  The natural ventilation that this component performs can address three main types of natural ventilation strategies:     1 - Single-sided Ventilation - ventilation driven by the height difference across a window on a single building side.     2 - Cross Ventilation - ventilation driven by the pressure difference across two sides of a building.     3 - Chimney Ventilation - ventilation driven by a stack that is attached to a zone or group of zones. _ The component can model "multi-zone" natural ventilation so long as there are no major vertical differences in height over multiple zones and the user understands that "mixing objects" of constant air flow are used to dsitribute cool incoming air between zones that are connected by an air wall.  As such, this method is not meant to model atriums or any method relying on inter-zone bouyancy-driven flow. _ The ventilation can be either fan-driven (using a constant flow rate) or natural by using an area of operable window to compute an esimated airflow for the zone. _ The latter uses the following equation to compute airflow to the zone. Ventilation Wind = Cw * Opening Area * Schedule * WindSpd  Ventilation Stack = Cd * Opening Area * Schedule * SQRT(2*g*DH*(|(Tzone-Todb)|/Tzone))  Total Ventilation = SQRT((Ventilation Wind)^2 + (Ventilation Stack)^2) - 

#### Inputs
* ##### HBZones [Required]
The HBZones out of any of the HB components that generate or alter zones.
* ##### interZoneAirFlowRate [Optional]
An optional number that represents airflow in m3/s per square meter of air wall contatct surface area between zones.  By default, this value is set to 0.0963 m3/s for each square meter of air wall contact surface area, which is a decent assumption for conditions of relatively low indoor air velocity.  In cases of higher indoor air velocity, such as those that might occur with consistent wind-driven ventilation or ventilation with fans, you will likely want to increase this number. This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.
* ##### interZoneAirFlowSched [Optional]
An optional schedule of fractional values to set when the air flows in between zones.
* ##### naturalVentilationType [Required]
Choose from the following options.       -1 - REMOVE NATURAL VENTILATION - Choose this option if want to remove previously-set natural ventilation objects with this component.       0 - NO NATURAL VENTILATION - Choose this option if you do not want to add any natrual ventilation objects to your zones with this component.       1 - WINDOW NATURAL VENTILATION - Choose this to have the component automatically calculate natural ventilation potential based on ALL of your zone's windows and a specified fraction of operable glazing.  Note that your zone must have windows for this ventilation to occur.  It will be assumed that each window is divided into two equally-sized openings (one placed at the top and another at the bottom).       2 - CUSTOM STACK / WIND VENTILATION - Choose this option either if you have window ventilation and it does not fit the description above or if you are trying to model a custom ventilation object like a chimney.  You will have to specify an effective window area for the object and the height between inlet and outlet.  You will also have to specify the angle2North for wind-driven calculations.  Note that you can eliminate either the wind or the stack part of the equation by setting the respective discharge coefficent to 0.       3 - FAN-DRIVEN VENTILATION - Choose this option to have your zones ventilated at a constant rate, representing fan-driven ventilation.  You will have to specify the design flow rate that the fan gives to the zone in m3/s.  You can also change the default fan efficiency, which will affect the electic consumption of the fan in the output.
* ##### minIndoorTempForNatVent [Optional]
A number or list of numbers between -100 and 100 that represents the minimum indoor temperature at which to naturally ventilate.  This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.
* ##### maxIndoorTempForNatVent [Optional]
A number or list of numbers between -100 and 100 that represents the maximum indoor temperature at which to naturally ventilate.  Use this to design mixed-mode buildings where you would like occupants to shut the windows and turn on a cooling system if it gets too hot inside.  This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.
* ##### minOutdoorTempForNatVent [Optional]
A number or list of numbers between -100 and 100 that represents the minimum outdoor temperature at which to naturally ventilate.  This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.
* ##### maxOutdoorTempForNatVent [Optional]
A number or list of numbers between -100 and 100 that represents the minimum outdoor temperature at which to naturally ventilate.  Use this to design night flushed buildings where windows are closed for daytime temperatures and opened at night or a mixed-mode buildings where you would like occupants to shut the windows and turn on a cooling system if it gets too hot outside. This can be either a single number to be applied to all connected zones or a list of numbers for each different zone.
* ##### openingAreaFractionalSched [Optional]
An optional schedule to set the fraction of the window that is open at each hour.
* ##### operableEffectiveArea [Required]
A number representing the effective area of operable ventilation in square meters.  Note that effective area references both inlet and outlet area through the following formula: EffectiveArea = 1 / sqrt( (1/InletArea^2) + 1/OutletArea^2) ). This value will be decreased if there is further friction introduced by objects in between the inlet and outlet.
* ##### inletOutletHeight [Required]
A number representing the height between the inlet and outlet of the custom ventilation object in meters.  This is needed for the bouyancy calculation.  Note that this heght should be from the midpoint of the height of the inlet to the midpoint of the height of the outlet.
* ##### windDischargeCoeff [Optional]
A number between 0.0 and 1.0 that will be multipled by the area of the window to account for the angle at which the wind hits the window.  This is the 'Cw' variable in the equation given in this component's description.  If no value is input here, it is autocalculated based on the angle of the cardinal direction from North and the hourly wind direction.  More often than not, you want to use this autocalculate feature.  Set to 0 to completely discount wind from the natural ventilation calculation.
* ##### stackDischargeCoeff [Optional]
A number between 0.0 and 1.0 that will be multipled by the area of the window to account for additional friction from window geometry, insect screens, etc.  This is the 'Cd' variable in the equation of this component's description.  If left blank, this variable will be autocalculated by the following equation - Cd = 0.4 + 0.0045*|(Tzone-Toutdoor).  Some common values for this coefficient include the following:   0.65 - For bouyancy with TWO windows of different heights, each of wehich have NO insect screens.   0.45 - For bouyancy with TWO windows of different heights, each of wehich HAVE insect screens.   0.25 - For bouyancy with ONE window with NO insect screen.   0.17 - For bouyancy with ONE window WITH an insect screen.   0.0 - Completely discounts stack ventilation from the natural ventilation calculation and only accounts for wind.
* ##### windowAngle2North [Required]
A number between 0 and 360 that sets the angle in degrees from North counting clockwise to the direction the window faces.  An angle of 0 denotes that the opening faces North, 90 denotes East, 180 denotes South, and 270 denotes West.

#### Outputs
* ##### readMe
...
* ##### HBZones
HBZones with their airflow modified.


[Check Hydra Example Files for Set EP Air Flow](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Set EP Air Flow)