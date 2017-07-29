## ![](../../images/icons/Convert_EnergyPlus_Schedule_to_Values.png) Convert EnergyPlus Schedule to Values - [[source code]](https://github.com/mostaphaRoudsari/honeybee/tree/master/src/Honeybee_Convert%20EnergyPlus%20Schedule%20to%20Values.py)

![](../../images/components/Convert_EnergyPlus_Schedule_to_Values.png)

Use this component to make a 3D chart in the Rhino scene of any climate data or hourly simulation data. - 

#### Inputs
* ##### schName [Required]
Name of the EP schedule
* ##### weekStartDay [Default]
An integer or text descriptor to set the schedule start day of the week. The default is set to 0 - sun - sunday. - Choose from one of the following: 0 - sun - sunday 1 - mon - monday 2 - tue - tuesday 3 - wed - wednesday 4 - thu - thursday 5 - fri - friday 6 - sat - saturday
* ##### epwFileForHol [Optional]
The file address of an EPW file on your system.  This component will automatically look up the national holidays of the country listed in the epw file and factor them into the output "values".
* ##### customHol [Optional]
Connect a list of DOYs (from 1 to 365) or a list of strings (example: DEC 25). - These will be added to any holidays in the epwFile holidays (if connected).

#### Outputs
* ##### values
Hourly values that define the schedule.
* ##### holidays
Holidays that have been incorporated into the hourly values of the schedule.  Connect these to the 'holidays' output of the "Honeybee_Energy Simulation Par" component to have them factored into the simulation.


[Check Hydra Example Files for Convert EnergyPlus Schedule to Values](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Convert EnergyPlus Schedule to Values)