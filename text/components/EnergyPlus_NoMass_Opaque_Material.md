## ![](../../images/icons/EnergyPlus_NoMass_Opaque_Material.png) EnergyPlus NoMass Opaque Material

![](../../images/components/EnergyPlus_NoMass_Opaque_Material.png)

Use this component to create a custom opaque material that has no mass, which can be plugged into the "Honeybee_EnergyPlus Construction" component.

#### Inputs
* ##### name [Required]
A text name for your NoMass Opaque Material.
* ##### roughness [Default]
A text value that indicated the roughness of your material.  This can be either "VeryRough", "Rough", "MediumRough", "MediumSmooth", "Smooth", and "VerySmooth".  The default is set to "Rough".
* ##### R_Value [Required]
Script variable Construction_NoMass
* ##### thermAbsp [Default]
An number between 0 and 1 that represents the thermal abstorptance of the material.  The default is set to 0.9, which is common for most non-metallic materials.
* ##### solAbsp [Default]
An number between 0 and 1 that represents the abstorptance of solar radiation by the material.  The default is set to 0.7, which is common for most non-metallic materials.
* ##### visAbsp [Default]
An number between 0 and 1 that represents the abstorptance of visible light by the material.  The default is set to 0.7, which is common for most non-metallic materials.

#### Outputs
* ##### EPMaterial
A no-mass opaque material that can be plugged into the "Honeybee_EnergyPlus Construction" component.


[Check Hydra Example Files for EnergyPlus NoMass Opaque Material](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_EnergyPlus NoMass Opaque Material)