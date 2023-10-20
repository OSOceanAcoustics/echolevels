# Review of Data Processing Levels

The use of data processing levels arose in the 1970's and 1980's particularly in the US research satellite community and in World Climate Research Program (WCRP) initiatives (Gutman & Ignatov, 1997; Weaver, 2014). The 1986 NRC CODMAC report in particular (NRC, 1986) defined a set of common terms for data levels or types with the goal of alleviating confusion in the user community with respect to data processing steps and data products. This report was particularly aimed at guiding future NASA data management practices and led directly to Data Processing (or Product) Levels definitions adopted by NASA for the Earth Observing System (EOS) in the early 1990's (Parkinson et al, 2006; NASA, 2021); in turn, NASA EOS practices influenced the international Committee on Earth Observation Satellites (CEOS) definition of data product levels (CEOS, 2008). Programs influenced by WCRP were often heterogeneous and ranged from in-situ monitoring to satellite products (Gutman & Ignatov, 1997).


## Canonical data processing levels

Weaver (2014) summarized the key properties of the processing levels adopted by NASA for EOS remote sensing products as involving the following data processing requirements:

- Time ordering of data and removal of duplicate packets
- Repackaging of satellite instrument data with additional spacecraft and engineering data
- Calibration of data to correct for instrument drift
- Conversion of data to environmental variables
- Resampling of data to convert to gridded Earth patterns
- Generation of higher-level science analysis and modeling products

The definitions currently used by NASA for Earth Science products are found in NASA (2021). Five data processing levels progress from raw data (Level 0, L0) to highly processed and regularized data products (Level 4, L4). Weaver (2014) summarized an earlier version of these as follows:

- L0: Reconstructed, unprocessed data at full resolution; all communications artifacts have been removed
- L1: Level 0 data that has been time-referenced and annotated with ancillary information, including radiometric and geometric calibration coefficients, and geolocation information
- L2: Derived geophysical variables at the same resolution and location as the Level 1 data
- L3: Variables mapped on uniform space-time grids, usually with some completeness and consistency
- L4: Model output or results from analyses of lower-level data

L1 data is reconstructed, time referenced but unprocessed sensor data raw with ancillary information and annotations, including radiometric and geolocation parameters, “computed and appended but not applied to L0 data” (NASA, 2021). In contrast, L2 data involve transformation to geophysical variables and the application of radiometric and geolocation parameters. CEOS (2008) “data product levels” definitions are broadly similar but reflect subtle differences; for example, a distinction is made between “Raw” and L0 data, and for L1 “optional radiometric and geometric correction [are] applied to produce parameters in physical units”. Hagolle (2014) points out ambiguities between each level in both the NASA and CEOS definitions, such as the distinction between sensor, physical and geophysical units; and across the two definitions, such as the level at which georeferenced data may be available and the specification of sub-levels, where CEOS allows for sub-levels but does not specify them. NASA EOS data processing levels, particularly L1 and L2, include sub-levels denoted by a sequence of letters (A, B, C; e.g., L1A) where the optional B sub-level represents A sub-level data processed to “sensor units” (NASA, 2021). However, sub-levels are poorly standardized across communities or agencies (Hagolle, 2014; Mittaz et al., 2019). For example, Landsat L1 data are available at three different sub-levels (L1TP, L1GT, L1GS) depending on the geometric correction type (USGS, 2023). Finally, WCRP divides processing into three levels (Gutman & Ignatov, 1997; Weaver, 2014): 1) primary instrument readings; 2) retrieved geophysical parameters; and 3) derived analysis or fields.

Cite Mittaz et al 2019 here, too, as providing a more fleshed out, systematic and abstract presentation (something Gutman & Ignatov, 1997 also attempted, from a different perspective and a more pragmatic objective)


## Adaptation to heterogeneous observing systems / sensor types

Satellite remote sensing systems not based on passive electromagnetic observations. Lidar (GEDI, or maybe ICESAT-2) and radar (Sentinel SAR) or maybe GRACE. Maybe also mention Landsat again.

In-situ data /  observation programs: OOI, NEON, IFREMER (and Argo?). Where the scheme may involve the WCRP lineage more directly (including IMOS?).
