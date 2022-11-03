# MorphoSedimentaryMapper
A browser-based tool for Doodling on NAIP imagery to make morpho-sedimentary roughness maps for hurricane model simulations

The user will be presented with a web map interface to
1. select a ROI
2. download NAIP imagery from that ROI at a selected time
3. doodle on the image and create a label image
4. convert the label image into a roughness raster based on a lookup table
5. perhaps, offer post-processing options for map tweaking/filtering/smoothing

This tool will modify and combine two existing functionality from the Doodleverse 

1. HoloDoodler, for providing the doodling interface
2. doodler_engine, for providing the ML used to turn doodles into labels
3. Seg2Map, for providing a web-map interface based on ipyleaflets, similar to CoastSeg
4. s2m_engine, for providing functionality to convert Gym model outputs to geotiffs

Additionally, this tool will use

1. a lookup table to map discrete morphosedimentary classes to numerical roughness values
2. perhaps post-processing tools to smooth the labels, etc
