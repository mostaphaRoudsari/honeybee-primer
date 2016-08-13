## ![](../../images/icons/Import_WINDOW_IDF_Report.png) Import WINDOW IDF Report

![](../../images/components/Import_WINDOW_IDF_Report.png)

Use this component to import an EnergyPlus window construction from LBNL WINDOW.  This construction can then be assigned to any Honebee window for an EnergyPlus model. - 

#### Inputs
* ##### windowIDFReport [Required]
A filepath to a 'EnergyPlus IDF' report exported by LBNL WINDOW.

#### Outputs
* ##### EPConstruction
An EnergyPlus construction that can be assigned to any window in Honeybee using components like 'Honeybee_addHBGlz', 'Honeybee_Glazing based on ratio', or 'Honeybee_Set EP Zone Construction'.


[Check Hydra Example Files for Import WINDOW IDF Report](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Import WINDOW IDF Report)