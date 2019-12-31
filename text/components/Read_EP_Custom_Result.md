## ![](../../images/icons/Read_EP_Custom_Result.png) Read EP Custom Result - [[source code]](https://github.com/ladybug-tools/honeybee-legacy/tree/master/src/Honeybee_Read%20EP%20Custom%20Result.py)

![](../../images/components/Read_EP_Custom_Result.png)

This component reads the results of an EnergyPlus simulation from the "Export to OpenStudio" Component or any EnergyPlus result .csv file address. _ The component is built to bring in any result that you desire from the csv using _keywords to search through all of the results in the file.  As such, this is particularly useful when you have requested atypical E+ outputs using the "Honeybee_Read Result Dictionary" component. - 

#### Inputs
* ##### resultFileAddress [Required]
The result file address that comes out of the "Export to OpenStudio" component.
* ##### keywords [Required]
keywords that will be used to bring in the results that you are interested in.  These words should be the name of the output that you are requesting or should correspond to words in the top row of the csv file.

#### Outputs
* ##### results
The result data from the csv file (formatted with a Ladybug header on it).


[Check Hydra Example Files for Read EP Custom Result](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Read EP Custom Result)