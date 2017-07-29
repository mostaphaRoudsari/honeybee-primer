## ![](../../images/icons/Constant_Schedule.png) Constant Schedule - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Constant%20Schedule.py)

![](../../images/components/Constant_Schedule.png)

Use this component to generate a schedule with a constant value or a schedule with 24 values that repeat in the same 24-hour pattern every day. - 

#### Inputs
* ##### value [Required]
A value or list of 24 values that will be repeated for every day of the year.
* ##### scheduleName [Required]
A text string representing a name for the schedule that this component will create.  This name should be unique among the schedules in your Grasshopper document to ensure that you do not overwrite other schedules.
* ##### schedTypeLimits [Default]
A text string from the scheduleTypeLimits output of the "Honeybee_Call From EP Schedule Library" component.  This value represents the units of the schedule input values.  The default is "Fractional" for a schedule with values that range between 0 and 1.  Other common inputs include "Temperature", "On/Off", and "ActivityLevel".

#### Outputs
* ##### readMe!
...
* ##### schedule
The name of the schedule that has been written to the memory of the GH document.  Connect this to any shcedule input of a Honeybee component to assign the schedule.
* ##### weekSched
The name of the weekly schedule that has been written to the memory of the GH document.  If your final intended annual schedule is seasonal (composed of different weekly schedules), you can use this output with the "Honeybee_Seasonal Schedule" to create such schedules.
* ##### schedIDFText
The text needed to tell EnergyPlus how to run the schedule.  If you are done creating/editing a shcedule with this component, you may want to make your GH document smaller by internalizing this IDF text and using the "Honeybee_Add To EnergyPlus Library" component to add the schedule to the memory the next time you open the GH file.  Then you can delete this component.


[Check Hydra Example Files for Constant Schedule](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Constant Schedule)