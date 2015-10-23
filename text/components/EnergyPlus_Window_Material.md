## ![](../../images/icons/EnergyPlus_Window_Material.png) EnergyPlus Window Material

![](../../images/components/EnergyPlus_Window_Material.png)

Use this component to create a custom window material that has no mass, which can be plugged into the "Honeybee_EnergyPlus Construction" component.

#### Inputs
* ##### name [Required]
A text name for your NoMass Window Material.
* ##### U_Value [Required]
A number representing the conductivity of the window in W/m-K.
* ##### SHGC [Required]
A number between 0 and 1 that represents the solar heat gain coefficient (SHGC) of the window. The solar heat gain coeffieceint is essentially the fraction of solar radiation falling on the window that makes it through the glass (at normal incidence).  This number is usually very close to the visible transmittance (VT) for glass without low-e coatings but can be might lower for glass with low-e coatings.
* ##### VT [Required]
A number between 0 and 1 that represents the visible transmittance (VT) of the window. The visible transmittance is essentially the fraction of visible light falling on the window that makes it through the glass (at normal incidence).  This number is usually very close to the solar heat gain coefficent (SHGC) for glass without low-e coatings but can be might higher for glass with low-e coatings.

#### Outputs
* ##### EPMaterial
A no-mass window material that can be plugged into the "Honeybee_EnergyPlus Construction" component.


[Check Hydra Example Files for EnergyPlus Window Material](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_EnergyPlus Window Material)