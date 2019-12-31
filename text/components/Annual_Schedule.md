## ![](../../images/icons/Annual_Schedule.png) Annual Schedule - [[source code]](https://github.com/ladybug-tools/honeybee-legacy/tree/master/src/Honeybee_Annual%20Schedule.py)

![](../../images/components/Annual_Schedule.png)

Use this component to generate schedules that can be assigned to HBZones. - 

#### Inputs
* ##### sun [Required]
Sunday. Connect a list of 24 values that represent the schedule value at each hour of the day.
* ##### mon [Required]
Monday. Connect a list of 24 values that represent the schedule value at each hour of the day.
* ##### tue [Required]
Tuesday. Connect a list of 24 values that represent the schedule value at each hour of the day.
* ##### wed [Required]
Wednesday. Connect a list of 24 values that represent the schedule value at each hour of the day.
* ##### thu [Required]
Thursday. Connect a list of 24 values that represent the schedule value at each hour of the day..
* ##### fri [Required]
Friday. Connect a list of 24 values that represent the schedule value at each hour of the day.
* ##### sat [Required]
Saturday. Connect a list of 24 values that represent the schedule value at each hour of the day.
* ##### holiday [Optional]
Optional input for holidays. Connect a list of 24 values that represent the schedule value at each hour of the day. If no value is input here, the schedule for Sunday will be used for all holidays.
* ##### coolDesignDay [Optional]
Optional input for the cooling design day that is used to size the system. Connect a list of 24 values that represent the schedule value at each hour of the day. If no value is input here, the schedule for Monday will be used for the cooling design day.
* ##### heatDesignDay [Optional]
Optional input for the heating design day that is used to size the system. Connect a list of 24 values that represent the schedule value at each hour of the day. If no value is input here, the schedule for Sunday will be used for the heating design day.
* ##### scheduleName [Required]
A text string representing a name for the schedule that this component will create.  This name should be unique among the schedules in your Grasshopper document to ensure that you do not overwrite other schedules.
* ##### schedTypeLimits [Default]
A text string from the scheduleTypeLimits output of the "Honeybee_Call From EP Schedule Library" component.  This value represents the units of the schedule input values.  The default is "Fractional" for a schedule with values that range between 0 and 1.  Other common inputs include "Temperature", "On/Off", and "ActivityLevel".
* ##### runIt [Required]
Set to "True to write the schedule to the Honeybee library such that you can assign the schedule with other Honeybee components.

#### Outputs
* ##### readMe!
...
* ##### schedule
The name of the schedule that has been written to the memory of the GH document.  Connect this to any shcedule input of a Honeybee component to assign the schedule.
* ##### weekSched
The name of the weekly schedule that has been written to the memory of the GH document.  If your final intended annual schedule is seasonal (composed of different weekly schedules), you can use this output with the "Honeybee_Seasonal Schedule" to create such schedules.
* ##### schedIDFText
The text needed to tell EnergyPlus how to run the schedule.  If you are done creating/editing a shcedule with this component, you may want to make your GH document smaller by internalizing this IDF text and using the "Honeybee_Add To EnergyPlus Library" component to add the schedule to the memory the next time you open the GH file.  Then you can delete this component.


[Check Hydra Example Files for Annual Schedule](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Annual Schedule)