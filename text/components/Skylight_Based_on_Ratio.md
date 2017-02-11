## ![](../../images/icons/Skylight_Based_on_Ratio.png) Skylight Based on Ratio

![](../../images/components/Skylight_Based_on_Ratio.png)

Use this component to generate windows for a HBSurface or HBZone based on a desired window-to-wall ratio. In addition to generating window geometry that corresponds with the input ratio, this component also allows you a fairly high level of control over the window geometry.

#### Inputs
* ##### HBObjects [Required]
Honeybee thermal zones or surfaces for which glazing should be generated.
* ##### skyLightRatio [Required]
If you have input a full zone or roof surface as your HBObjects, use this input to generate skylights on the roof surfaces. A single window for each surface is good for making energy simulations run fast while several distributed windows is often necessary to have accurate daylight simulations or high-resolution thermal maps. The default is set to "True" to generate multiple distributed windows.
* ##### breakUpSkylight [Optional]
Set to "True" to generate a distributed set of multiple windows for skylights and set to "False" to generate just a single window per roof surface.
* ##### skyLightBreakUpDist [Optional]
An optional number in Rhino model units that sets the distance between individual skylights when the breakUpSkylight_ input above is set to 'True'.  The default is set to 3 meters.
* ##### EPConstruction [Optional]
A optional text string of an EnergyPlus construction name that sets the material construction of the window. The default will assign a generic double pane window without low-e coatings.
* ##### RADMaterial [Optional]
A optional text string of an Radiance glass material name that sets the material of the window.
* ##### runIt [Required]
set runIt to True to generate the glazing

#### Outputs
* ##### readMe!
...
* ##### HBObjWGLZ
Newhoneybee zones that contain glazing surfaces based on the parameters above. 


[Check Hydra Example Files for Skylight Based on Ratio](https://hydrashare.github.io/hydra/index.html?keywords=Honeybee_Skylight Based on Ratio)