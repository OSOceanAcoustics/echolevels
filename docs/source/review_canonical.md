# Canonical data processing levels

Weaver {cite}`weaver_processing_2014` summarized the key properties of processing levels adopted by NASA for EOS remote sensing products as involving the following data processing requirements:

- Time ordering of data and removal of duplicate packets
- Repackaging of satellite instrument data with additional spacecraft and engineering data
- Calibration of data to correct for instrument drift
- Conversion of data to environmental variables
- Resampling of data to convert to gridded Earth patterns
- Generation of higher-level science analysis and modeling products

## NASA EOS
The current NASA EOS definitions {cite}`nasa_data_2021` include five data processing levels that progress from raw data (Level 0, L0) to highly processed and regularized data products (Level 4, L4). Weaver {cite}`weaver_processing_2014` summarized an earlier version of these as follows:

- L0: Reconstructed, unprocessed data at full resolution; all communications artifacts have been removed
- L1: L0 data that has been time-referenced and annotated with ancillary information, including radiometric and geometric calibration coefficients, and geolocation information
- L2: Derived geophysical variables at the same resolution and location as the L1 data
- L3: Variables mapped on uniform space-time grids, usually with some completeness and consistency
- L4: Model output or results from analyses of lower-level data

Specifically, L1 data are reconstructed, time referenced but unprocessed raw sensor data with ancillary information and annotations, including radiometric and geolocation parameters, computed and appended but not applied to L0 data. In contrast, L2 data involve transformation to geophysical variables and the application of radiometric and geolocation parameters.

## CEOS
The CEOS definitions of data product levels {cite}`ceos_interoperability_2008` are broadly similar but contain subtle differences. For example, a distinction is made between "raw" and L0 data, and for L1 data optional radiometric and geometric correction are applied to produce parameters in physical units.

## NASA EOS and CEOS Comparison
Comparing the NASA EOS and CEOS definitions, Hagolle {cite}`hagolle_product_2014` points out ambiguities _between_ each level in definitions, such as the distinction between sensor, physical and geophysical units, as well as ambiguities _across_ the two definitions, such as the level at which georeferenced data may be available.

The specification of sub-levels is also different between the NASA and CEOS definitions. CEOS allows for sub-levels but does not specify them, whereas NASA EOS data processing levels, particularly L1 and L2, include sub-levels denoted by a sequence of letters (A, B, C; e.g., L1A) where the optional B sub-level represents A sub-level data processed to "sensor units" {cite}`nasa_data_2021`. However, sub-levels are poorly standardized across communities or agencies {cite}`hagolle_product_2014,mittaz_applying_2019`. For example, Landsat L1 data are available at three different sub-levels (L1TP, L1GT, L1GS) depending on the geometric correction type {cite}`usgs_what_2023`. 
