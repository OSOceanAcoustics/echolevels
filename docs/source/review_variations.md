# Variations of canonical processing levels

## Remote sensing data
The NASA EOS categories are particularly applicable to passive remote sensing instruments. The complexity of active sensors that emit an electromagnetic beam and process the returned signals have led to modifications to the NASA EOS data processing level categories.

### NASA GEDI
NASA’s GEDI (Global Ecosystem Dynamics Investigation) instrument provides one example of a lidar(laser)-based active sensing system designed to characterize the three-dimensional, above-ground structure of forests {cite}`dubayah_global_2020,blumenfeld_earth_2020`. GEDI defines 5 data product levels (L0-L4) with sub-levels. L1 products contain the raw (L1A) and geolocated (L1B) waveforms. L2 products contain laser-footprint-scale canopy structure heights and metrics, where L2B metrics are more processed than those in L2A. L3 provides some of these same products on a regular grid rather than at a footprint scale. Finally, L4 provides model output of above-ground biomass in two spatial representations: laser footprint (L4A) and gridded (L4B). As is evident, there are some deviations from the NASA EOS definitions of levels and sub-levels. For example, L4 sub-levels contain the same products but at different spatial representations, where L4A retains the footprint spatial resolution from the L2 product. 

### ESA
Another active sensing example is the ESA (European Space Agency) Sentinel-1 SAR (Synthetic Aperture Radar) instrument, for which L0-L2 products are provided {cite}`copernicus_2023`. Here, data are acquired in one of four “acquisition modes” (Stripmap, Interferometric Wide Swath, etc), each of which leads to a sequence of L0-L2 products. L1 data from each mode is available as two subproducts (sub-levels) by processing into either "Single Look Complex" (L1-SLC) or "Ground Range Detected" (L1-GRD) products. L2 consists of up to 3 geolocated products: Ocean Wind field, Ocean Swell spectra and Surface Radial Velocity. However, the availability of each of those products and the source L1 inputs used depend on the acquisition mode, potentially necessitating L2 qualifiers for the source input and acquisition mode.

### WCRP
The WCRP system mentioned earlier divided processing into three levels {cite}`gutman_towards_1997,weaver_processing_2014`: 1) primary instrument readings, 2) retrieved geophysical parameters, and 3) derived analysis or fields. In contrast to the satellite remote sensing focus of NASA and CEOS, programs adopting the WCRP processing levels have also included many in-situ observing systems. For example, the Tropical Ocean Global Atmosphere program (TOGA) deployed an array of 70 moored buoys along the equatorial Pacific Ocean - the Tropical Atmosphere Ocean (TAO) Array - and provided sensor-based in-situ meteorological and sea water temperature via telemetry. For L3, TOGA refined the WCRP definition to "homogeneous data fields derived from level 2 by an analysis technique."


## In-situ data

Other groups that primarily collect in-situ data have also developed data processing levels that are likely influenced by both NASA / CEOS and WCRP categories.

### IFREMER
IFREMER (French Research Institute for Exploitation of the Sea) uses a categorization consisting of 6 levels (L0-L5) for data collected by French oceanographic research vessels {cite}`ifremer_processing_2019`. IFREMER L0 to L2 largely mirror NASA EOS levels and are consistent with WCRP L1 s-L2. While IFREMER L3 data are described as being on "identical and standardized space-time reference scales," it’s unclear if this is analogous to the gridded and sometimes resampled and binned data that characterizes NASA EOS L3. IFREMER L4 and L5 fall within the scope of NASA EOS L4 and WCRP L3.

### OOI
The US OOI (Ocean Observatories Initiative) maintains an extensive collection of in-situ sensors on moorings, gliders and other platforms, mainly in the US. The OOI data product levels {cite}`ooi_2023` distinguish raw data (raw data files transmitted by the instrument or the host platform) from L0, where L0 is analogous to NASA EOS L1 and is stored in standardized formats. L1 contains calibrated data, whereas L2 contains products derived from multiple L1 products and may involve multiple sensors. Unlike other categorizations, these processing level definitions do not emphasize the spatio-temporal regularization and regridding as determining characteristics. They focus more on the calibration and quality control of instrument data and generation of higher-level products that may involve more complex algorithms and multiple inputs.

### NEON
Similar to OOI, NEON (National Ecological Observatory Network) is a US observatory managing a large collection of in-situ sensors and other data sources, with deployments on land and water. The NEON data processing levels consist of 5 levels (L0-L4). NEON L0 and L1 are similar to the definitions from NASA EOS and others {cite}`neon_2023`. However, NEON L2 and L3 are distinguished instead by the application of temporal (L2) and spatial (L3) interpolation or mosaicking, with NEON L4 being similar to OOI L2.
