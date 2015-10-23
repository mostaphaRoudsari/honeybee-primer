## ![](../../images/icons/Re-run_IDF.png) Re-run IDF

![](../../images/components/Re-run_IDF.png)

This is a component for running a previoulsy-generated .idf file through EnergyPlus with a different weather file. - # # Honeybee: A Plugin for Environmental Analysis (GPL) started by Mostapha Sadeghipour Roudsari #  # This file is part of Honeybee. #  # Copyright (c) 2013-2015, Mostapha Sadeghipour Roudsari <Sadeghipour@gmail.com>  # Honeybee is free software; you can redistribute it and/or modify  # it under the terms of the GNU General Public License as published  # by the Free Software Foundation; either version 3 of the License,  # or (at your option) any later version.  #  # Honeybee is distributed in the hope that it will be useful, # but WITHOUT ANY WARRANTY; without even the implied warranty of  # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the  # GNU General Public License for more details. #  # You should have received a copy of the GNU General Public License # along with Honeybee; If not, see <http://www.gnu.org/licenses/>. #  # @license GPL-3.0+ <http://spdx.org/licenses/GPL-3.0+> Based on a work at https://github.com/mostaphaRoudsari/ladybug. - Check this link for more information about the license: http://creativecommons.org/licenses/by-sa/3.0/deed.en_US - Source code is available at: https://github.com/mostaphaRoudsari/ladybug - 

#### Inputs
* ##### workingDir []
The working directory of the energyPlus idf.
* ##### idfFileName []
Name of the idf file (e.g. sample1.idf).
* ##### epwFileAddress []
Address to epw weather file.
* ##### EPDirectory []
[Optional] where EnergyPlus is installed on your system
* ##### runIt []
Set to 'True' to run the simulation.

#### Outputs
* ##### report
Report!
* ##### resultFileAddress
The address of the EnergyPlus result file.


[Check Hydra Example Files for Re-run IDF](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Re-run IDF)