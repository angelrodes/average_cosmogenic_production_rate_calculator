# Average cosmogenic production rate calculator

Apparent cosmogenic exposure ages and erosion rates are usually calculated by scaling global (e.g. [Borchers *et al.*, 2016](https://doi.org/10.1016/j.quageo.2015.01.009)) and local (e.g. [Kaplan *et al.*, 2011](https://doi.org/10.1016/j.epsl.2011.06.018)) calibration data using time-dependent scaling schemes (e.g. [LSD](https://doi.org/10.1016/j.epsl.2013.10.052)). These exposure ages and erosion rates are typically obtained using one of the online calculators:

- [The online calculators formerly known as the CRONUS-Earth online calculators](https://hess.ess.washington.edu/)
- [The CRONUS Earth Web Calculators](http://cronus.cosmogenicnuclides.rocks/2.0/)
- [CREp (Cosmic Ray Exposure program)](https://crep.otelo.univ-lorraine.fr/#/)

When our geological problem is more complex than a constant exposure or an erosion-equilibrium at the surface (e.g. burial dating, or data from depth profiles), we need to interpret some of our cosmonuclide concentrations using models that require the input of constant production rates. Moreover, as these models usually include the simulation of cosmonuclide accumulation under the surface, they also require muonic production rates and attenuation lengths as input.

To make data from online calculators consistent with data obtained using methods based on constant-production models, I developed a spreadsheet that calculates average spallation and muonic production rates based on a cosmonuclide concentration and its associated apparent exposure age or erosion rate.

This calculation requires making some assumptions about the muon production at different latitudes, depths, and elevations. The average cosmogenic production rate calculator is an implementation of the production rate systematics used in [NUNAIT](https://github.com/angelrodes/NUNAIT), that fit the data produced by the scripts used in [the online calculators formerly known as the CRONUS-Earth online calculators v.3](https://hess.ess.washington.edu/).

The generated production rate data can be used in any model based on [Lal's formulae](https://doi.org/10.1016/0012-821X(91)90220-C).

# How to use this calculator

1. Decide which type of average do you need. If you need a "short-term" average (e.g. you are trying to fit a depth profile), you probably want to use a surface sample with its associated apparent exposure age. If you need a long-term average (e.g. Be-10 - Al-26 burial dating), you can use the concentrations of one of your "youngest" (shortest burial time) samples and their associated apparent erosion rates. 
2. Go to your favourite online calculator (see above) and calculate the apparent exposure ages or erosion rates using the desired reference calibration and scaling scheme.
3. Input your latitude (decimal degrees), elevation (m above sea level), nuclide data, and calculated data (Exposure age in years or erosion rate in m/Ma) in the Average cosmogenic production rate calculator spreadsheet, tab "Calculator". Remember to input the **external uncertainty** of your data, as this will be used to calculate the uncertainty of the spallation production rate. If you input the internal uncertainty, a minimum of 1% uncertainty will be considered.
4. Copy the production data and use it in your model.

If you find any bug, please [contact me](https://angelrodes.wordpress.com/contact/)!

# Citation

The systematics of this calculator are described in:

**Rodés, Á.** (2021) "The NUNAtak Ice Thinning (NUNAIT) Calculator for Cosmonuclide Elevation Profiles" *Geosciences* 11, no. 9: 362. doi:[10.3390/geosciences11090362](https://doi.org/10.3390/geosciences11090362 )

<!-- The file is protected by the main surface production process :) -->
