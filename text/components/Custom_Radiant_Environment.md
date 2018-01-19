## ![](../../images/icons/Custom_Radiant_Environment.png) Custom Radiant Environment - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Custom%20Radiant%20Environment.py)

![](../../images/components/Custom_Radiant_Environment.png)

Use this component to create a custon radiant environment for THERM boundary condition.  Assigning values here will create radiant conditions that are different from normal NFRC conditions (where radiant temperature equals air temperature, the emissivity of the environment is assumed to be 1, and viewFactor between the boundary and the envrionment is calculated using the geometry of the boundary).

#### Inputs
* ##### radiantTemp [Optional]
A value in degrees Celcius that represents the radiant temperature of the environment.  If no value is plugged in here, the radiant environment will be assumed to have the same temperature as the air.
* ##### envEmissivity [Optional]
A value between 0 and 1 that represents the emissivity of the environment. Use this ti account for environments made of atypical materials like metals. If no value is plugged in here, it will be assumed that the envrionment has an emissivity of 1.
* ##### viewFactor [Optional]
An optional value between 0 and 1 that sets the view factor of the boundary to the surrounding exterior/interior environment.
* ##### heatFlux [Optional]
An optional numerical value in W/m2 that represents additional energy flux across the boundary condition. You can use this to account for solar flux across the exterior boundary condition.

#### Outputs
* ##### customRadEnv
A list of radiant environmental properties that can be plugged into the 'Honeybee_Create Therm Boundaries' component in order to run a THERM simulation with a atypical radiant environment.


[Check Hydra Example Files for Custom Radiant Environment](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Custom Radiant Environment)