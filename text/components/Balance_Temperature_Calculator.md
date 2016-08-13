## ![](../../images/icons/Balance_Temperature_Calculator.png) Balance Temperature Calculator

![](../../images/components/Balance_Temperature_Calculator.png)

Use this component to calculate a rough building (or zone) balance temperatrue from a Honeybee energy simulation.  The balance point is the outdoor temperature at which your building is usually neither heating or cooling itself.  If the outdoor temperture drops below the balance temperature, your building will usually be heating itself and, if the outdoor temperture is above the balance temperature, the building will usually be cooling itself. -  The balance temperture concept is useful for setting things such as automated blinds and airflow shcedules since having these things controlled by hourly cooling or heating can often introduce odd behavior resulting from idiosyncrasies in the building's schedule. This component works by taking the average combined heating/cooling values for each day and the average outdoor air temperature for each day.  The days with the smallest combined heating + cooling will have their daily mean outdoor air tempertures averaged to produce the balance temperture. - 

#### Inputs
* ##### thermalLoadBal [Required]
The output "thermalEnergyBalance" from the "Honeybee_Read EP Result" component.  This can be for a single zone if you select out one branch of this thermalEnergyBalance output or it can be for the whole simulated building if you connect the whole output.  Note that, in order to use this component correclty, you must run either a simulation with either an hourly or daily timestep.
* ##### outdoorAirTemp [Required]
The "dryBulbTemperature" output from the "Ladybug_Import epw" component.
* ##### numDaysToAverage [Optional]
An optional number of days with a low thermal energy load that will be averaged together to yield the balance point.  This is done to help avoid anomalies introduced by variations between weekday and weekend shcedules.  The default is set to 10 but you may want to drop this down if there is little variation between weekday and weekend schedule or you might increase this number is there is a high variation.

#### Outputs
* ##### energyUsedOnBalDay
The amount of energy used on the balbnce day.  This number should be close to 0 and is mostly meant to give a sense of the accuracy of the temperature value below
* ##### balanceTemperature
The outdoor balance temperature of the connected zone or building data.


[Check Hydra Example Files for Balance Temperature Calculator](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Balance Temperature Calculator)