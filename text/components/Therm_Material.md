## ![](../../images/icons/Therm_Material.png) Therm Material - [[source code]](https://github.com/ladybug-tools/honeybee-legacy/tree/master/src/Honeybee_Therm%20Material.py)

![](../../images/components/Therm_Material.png)

Use this component to create a custom THERM material, which can be plugged into the "Honeybee_Create Therm Polygons" component. - 

#### Inputs
* ##### materialName [Required]
A text name for your THERM Material.
* ##### conductivity [Required]
A number representing the conductivity of the THERM material in W/m-K.
* ##### absorptivity [Optional]
A number between 0 and 1 that represents the solar absorptivity of the material. The default is set to 0.5.
* ##### emissivity [Optional]
A number between 0 and 1 that represents the emissivity of the material. The default is set to 0.9.
* ##### cavityModel [Optional]
An integer that represents the cavity model to use for the material (if it is a gas).  If you are creating a solid material, just leave this input blank.  Cavity models (4 - ISO 15099) and (5 - ISO 15099 ventilated) are used for most situations.  Choose from the following options: 0 - NFRC 1 - CEN 2 - CEN (slightly ventilated) 3 - NFRC with user dimensions 4 - ISO 15099 5 - ISO 15099 ventilated
* ##### RGBColor [Optional]
An optional color to set the color of the material when you import it into THERM.

#### Outputs
* ##### thermMaterial
A therm material that can be plugged into the "Honeybee_Create Therm Polygons" component.


[Check Hydra Example Files for Therm Material](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Therm Material)