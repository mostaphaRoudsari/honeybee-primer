## ![](../../images/icons/Therm_Material_to_EnergyPlus_Material.png) Therm Material to EnergyPlus Material

![](../../images/components/Therm_Material_to_EnergyPlus_Material.png)

Use this component to create a custom opaque material, which can be plugged into the "Honeybee_EnergyPlus Construction" component. _ This component requires you to know a lot of the characteristics of the material and, you may want to borrow some characteristcs of a similar material in the library.  Use the "Honeybee_Call From EP Construction Library" and the "Honeybee_Decompose EP Material" to help with this. _ If you are not able to find all of the necessary material characteristcs and your desired material is relatively light, it might be easier for you to use a "Honeybee_EnergyPlus NoMass Opaque Material." - 

#### Inputs
* ##### thermMaterial [Required]
The name of a Therm material from the ThermMaterials output from the from the "Call from EP Construction Library" component.
* ##### roughness [Default]
A text value that indicated the roughness of your material.  This can be either "VeryRough", "Rough", "MediumRough", "MediumSmooth", "Smooth", and "VerySmooth".  The default is set to "Rough".
* ##### thickness [Required]
A number that represents the thickness of the material in meters (m).
* ##### density [Required]
A number representing the density of the material in kg/m3.  This is essentially the mass one cubic meter of the material.
* ##### specificHeat [Required]
A number representing the specific heat capacity of the material in J/kg-K.  This is essentially the number of joules needed to raise one kg of the material by 1 degree Kelvin.

#### Outputs
* ##### EPMaterial
An opaque material that can be plugged into the "Honeybee_EnergyPlus Construction" component.


[Check Hydra Example Files for Therm Material to EnergyPlus Material](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Therm Material to EnergyPlus Material)