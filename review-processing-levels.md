# Review of Data Processing Levels

The use of data processing levels arose in the 1970's and 1980's particularly in the US research satellite community and in World Climate Research Program (WCRP) initiatives (Gutman & Ignatov, 1997; Weaver, 2014). The 1986 NRC CODMAC report in particular (NRC, 1986) defined a set of common terms for data levels or types with the goal of alleviating confusion in the user community with respect to data processing steps and data products. This report was aimed at guiding future NASA data management practices and led directly to Data Processing (or Product) Levels definitions adopted by NASA for the Earth Observing System (EOS) in the early 1990's (Parkinson et al, 2006; NASA, 2021); in turn, NASA EOS practices influenced the international Committee on Earth Observation Satellites (CEOS) definition of data product levels (CEOS, 2008). Programs that adopted the WCRP data-level categories, which are based originally on Global Atmospheric Research Program (GARP) work from the 1970’s, have been heterogeneous and ranged from in-situ monitoring to satellite products (Gutman & Ignatov, 1997; Weaver, 2014).


## Canonical data processing levels

Weaver (2014) summarized the key properties of the processing levels adopted by NASA for EOS remote sensing products as involving the following data processing requirements:

- Time ordering of data and removal of duplicate packets.
- Repackaging of satellite instrument data with additional spacecraft and engineering data.
- Calibration of data to correct for instrument drift.
- Conversion of data to environmental variables.
- Resampling of data to convert to gridded Earth patterns.
- Generation of higher-level science analysis and modeling products.

The definitions currently used by NASA for Earth Science products are found in NASA (2021). Five data processing levels progress from raw data (Level 0, L0) to highly processed and regularized data products (Level 4, L4). Weaver (2014) summarized an earlier version of these as follows:

- L0: Reconstructed, unprocessed data at full resolution; all communications artifacts have been removed.
- L1: Level 0 data that has been time-referenced and annotated with ancillary information, including radiometric and geometric calibration coefficients, and geolocation information.
- L2: Derived geophysical variables at the same resolution and location as the Level 1 data.
- L3: Variables mapped on uniform space-time grids, usually with some completeness and consistency.
- L4: Model output or results from analyses of lower-level data.

L1 data is reconstructed, time referenced but unprocessed sensor data raw with ancillary information and annotations, including radiometric and geolocation parameters, “computed and appended but not applied to L0 data” (NASA, 2021). In contrast, L2 data involve transformation to geophysical variables and the application of radiometric and geolocation parameters. CEOS (2008) “data product levels” definitions are broadly similar but reflect subtle differences; for example, a distinction is made between “Raw” and L0 data, and for L1 “optional radiometric and geometric correction [are] applied to produce parameters in physical units”. Hagolle (2014) points out ambiguities between each level in both the NASA and CEOS definitions, such as the distinction between sensor, physical and geophysical units; and across the two definitions, such as the level at which georeferenced data may be available and the specification of sub-levels, where CEOS allows for sub-levels but does not specify them. 

NASA EOS data processing levels, particularly L1 and L2, include sub-levels denoted by a sequence of letters (A, B, C; e.g., L1A) where the optional B sub-level represents A sub-level data processed to “sensor units” (NASA, 2021). However, sub-levels are poorly standardized across communities or agencies (Hagolle, 2014; Mittaz et al., 2019). For example, Landsat L1 data are available at three different sub-levels (L1TP, L1GT, L1GS) depending on the geometric correction type (USGS, 2023). 


## Variations on canonical processing levels

The NASA EOS categories are particularly applicable to passive remote sensing instruments. The complexity of active sensors that emit an electromagnetic beam and process the returned signals have led to modifications to the NASA EOS data processing level categories. NASA’s GEDI (Global Ecosystem Dynamics Investigation) instrument provides one example of a lidar (laser) - based active system designed to characterize the three-dimensional, above-ground structure of forests (Dubayah et al, 2020; ESDS, 2021). GEDI defines 5 data product levels, L0 - L4, with sub-levels. L1 products contain the raw (L1A) and geolocated (L1B) waveforms. L2 products contain laser-footprint-scale canopy structure heights and metrics, where L2B metrics are more processed than those in L2A. L3 provides some of these same products on a regular grid rather than at a footprint scale. Finally, L4 provides model output of above-ground biomass in two spatial representations: laser footprint (L4A) and gridded (L4B). As is evident, there are some deviations from the NASA EOS definitions of levels and sub-levels; for example, L4 sub-levels contain the same products but at different spatial representations, where L4A retains the footprint spatial resolution from the L2 product. 

Another active-sensing example is the ESA (European Space Agency) Sentinel-1 SAR (Synthetic Aperture Radar, microwave) instrument. L0 to L2 products are provided (Copernicus, 2023). However, a first challenge is that data are acquired in one of four “acquisition modes” (Stripmap, Interferometric Wide Swath, etc), each of which leads to a sequence of L0 - L2 products. L1 data from each mode is available as two subproducts (sub-levels) by processing into either “Single Look Complex” (L1-SLC) or “Ground Range Detected” (L1-GRD) products. L2 consists of up to 3 geolocated products: Ocean Wind field, Ocean Swell spectra and Surface Radial Velocity. However, the availability of each of those products and the source L1 inputs used depend on the acquisition mode, potentially necessitating L2 qualifiers for the source input and acquisition mode.

The WCRP system mentioned earlier divides processing into three levels (Gutman & Ignatov, 1997; Weaver, 2014): 1) primary instrument readings; 2) retrieved geophysical parameters; and 3) derived analysis or fields. In contrast to the satellite remote sensing focus of NASA and CEOS, WCRP programs adopting these processing levels have also included significant in-situ observing systems. For example, the Tropical Ocean Global Atmosphere program (TOGA) deployed an array of 70 moored buoys along the equatorial Pacific Ocean, the Tropical Atmosphere Ocean (TAO) Array, providing sensor-based in-situ meteorological and sea water temperature via telemetry. For L3, TOGA refined the WCRP definition to “homogeneous data fields derived from level 2 by an analysis technique” (Gutman & Ignatov, 1997). 

Other groups that primarily collect in-situ data have also developed data processing levels for their data collections that are likely influenced by both NASA / CEOS and WCRP categories. IFREMER (French Research Institute for Exploitation of the Sea) uses a categorization consisting of 5 levels, L0 - L5, for data collected by French oceanographic research vessels (IFREMER, 2019). IFREMER L0 to L2 largely mirror NASA EOS levels and are consistent with WCRP L1 - L2. While L3 data are described as being on “identical and standardized space-time reference scales”, it’s unclear if this is analogous to the gridded, sometimes resampled and binned data that characterizes NASA EOS L3. L4 & L5 fall within the scope of NASA EOS L4 as well as WCRP L3. OOI (Ocean Observatories Initiative) maintains an extensive collection of in-situ sensors on moorings, gliders and other platforms, mainly in the US. The OOI data product levels (OOI, 223) distinguish Raw data (raw data files transmitted by the instrument or the host platform) from L0, where L0 is analogous to NASA EOS L1 and is stored in standardized formats. L1 contains calibrated data, while L2 contains products derived from multiple L1 products and may involve multiple sensors. Unlike other categorizations, these processing level definitions do not emphasize the spatio-temporal regularization and regridding as determining characteristics. They focus more on the calibration and quality control of instrument data and generation of higher-level products that may involve more complex algorithms and multiple inputs. Finally, like OOI, NEON (National Ecological Observatory Network) is a US observatory managing a large collection of in-situ sensors and other data sources, with deployments on land and water. The NEON data processing levels range from L0 to L4, with L0 and L1 similar to the definitions from NASA EOS and others (NEON, 2023). However, L2 and L3 are distinguished instead by the application of temporal (L2) and spatial (L3) interpolation or mosaicking, while L4 is similar to OOI L2.