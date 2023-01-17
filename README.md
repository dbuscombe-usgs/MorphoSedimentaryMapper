# MorphoSedimentaryMapper
A browser-based tool for Doodling on NAIP imagery to make morpho-sedimentary roughness maps for hurricane model simulations

The user will be presented with a web map interface to
1. select a ROI
2. download NAIP imagery from that ROI at a selected time
3. doodle on the image and create a label image
4. convert the label image into a roughness raster based on a lookup table
5. perhaps, offer post-processing options for map tweaking/filtering/smoothing

This tool will modify and combine two existing functionality from the Doodleverse 

1. [HoloDoodler](https://github.com/Doodleverse/holodoodler), for providing the doodling interface
2. [doodler_engine](https://github.com/Doodleverse/doodler_engine), for providing the ML used to turn doodles into labels
3. [Seg2Map](https://github.com/Doodleverse/seg2map), for providing a web-map interface based on ipyleaflets, similar to CoastSeg
4. [s2m_engine](https://github.com/Doodleverse/s2m_engine), for providing functionality to download NAIP imagery

Additionally, this tool will use

1. a lookup table to map discrete morphosedimentary classes to numerical roughness values
2. perhaps post-processing tools to smooth the labels, etc


## Numerical roughness

### Mattock
NLCD land cover classes with assigned values for the Manning’s–n friction coefficient, surface roughness length and forest canopy sheltering factor (based on Mattocks et al., 2006)

![ManningsN_Mattock](https://user-images.githubusercontent.com/3596509/212981315-02ff457b-d3a5-4e08-845d-3a00700c3e09.PNG)

* van der Lugt, M.A., Quataert, E., van Dongeren, A., van Ormondt, M. and Sherwood, C.R., 2019. Morphodynamic modeling of the response of two barrier islands to Atlantic hurricane forcing. Estuarine, Coastal and Shelf Science, 229, p.106404.

![Manning_VanderLugt](https://user-images.githubusercontent.com/3596509/212985271-1ef709c8-0124-42b8-9071-a5421bdb8649.PNG)

Refs

* Mattocks, C. and Forbes, C., 2008. A real-time, event-triggered storm surge forecasting system for the state of North Carolina. Ocean Modelling, 25(3-4), pp.95-119.

* Mattocks, C., Forbes, C., Ran, L., 2006. Design and implementation of a real-time storm surge and flood forecasting capability for the State of North Carolina. UNC–CEP Technical Report, November 30, 2006, 103 pp.

* Arcement, G., Schneider, V., 1989. Guide for selecting Manning’s roughness coefficients for natural channels and flood plains. United States Geological Survey Water Supply Paper 2339, USGS, 38 pp.


### Machineni

![ManningN_2](https://user-images.githubusercontent.com/3596509/212982346-01b3cf54-b6a7-45a3-baa0-b1a8ac0807e3.PNG)

* Machineni, N., Sinha, V.S., Singh, P. and Reddy, N.T., 2019. The impact of distributed landuse information in hydrodynamic model application in storm surge inundation. Estuarine, Coastal and Shelf Science, 231, p.106466. https://www.sciencedirect.com/science/article/pii/S027277141930469X

### Zhang

![ManningN_3](https://user-images.githubusercontent.com/3596509/212982940-5e8c8341-d85e-4fc0-b347-f9db87afbd6f.PNG)

* Zhang, K., Liu, H., Li, Y., Xu, H., Shen, J., Rhome, J. and Smith III, T.J., 2012. The role of mangroves in attenuating storm surges. Estuarine, Coastal and Shelf Science, 102, pp.11-23.


### Others

* Ferreira, C.M., Irish, J.L. and Olivera, F., 2014. Uncertainty in hurricane surge simulation due to land cover specification. Journal of Geophysical Research: Oceans, 119(3), pp.1812-1827.

* Lapetina, A. and Sheng, Y.P., 2014. Three-dimensional modeling of storm surge and inundation including the effects of coastal vegetation. Estuaries and coasts, 37(4), pp.1028-1040.

* Lapetina, A. and Sheng, Y.P., 2015. Simulating complex storm surge dynamics: three‐dimensionality, vegetation effect, and onshore sediment transport. Journal of Geophysical Research: Oceans, 120(11), pp.7363-7380.

* Orton, P.M., Sanderson, E.W., Talke, S.A., Giampieri, M. and MacManus, K., 2020. Storm tide amplification and habitat changes due to urbanization of a lagoonal estuary. Natural Hazards and Earth System Sciences, 20(9), pp.2415-2432.

![Manning5](https://user-images.githubusercontent.com/3596509/212986558-eaa2b84f-e34d-431a-b4b2-d3f3c8fee731.PNG)

* Seenath, A., 2015. Modelling coastal flood vulnerability: Does spatially-distributed friction improve the prediction of flood extent?. Applied Geography, 64, pp.97-107.

![Manning6](https://user-images.githubusercontent.com/3596509/212986812-e9c5f5f7-13aa-48a5-9aef-c9344650dd79.PNG)

* Johnson, C.L., Chen, Q., Ozdemir, C.E., Xu, K., McCall, R. and Nederhoff, K., 2021. Morphodynamic modeling of a low-lying barrier subject to hurricane forcing: The role of backbarrier wetlands. Coastal Engineering, 167, p.103886.

More details as they become available ...
