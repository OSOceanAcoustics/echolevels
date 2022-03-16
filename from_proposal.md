# Specification of data processing levels

The decades-long experience from the satellite remote sensing community has shown that a set of robust and well-articulated definitions of 
"data processing levels" [22], [39] can lead directly to broad and highly productive use of the data. However, no such community agreement 
exists for active acoustic data, and the ambiguity associated with the interoperability and inter-comparability of processed 
sonar data products has hindered efficient collaboration and integrative use of the rapidly accumulated data archive across 
research institutions and agencies.

We propose to develop a clearly defined progression of data processing levels for active ocean sonar data, leveraging the accumulated 
experience from remote sensing and large-scale, long-term ocean and ecological observatories [40]–[43]. In Table 1 we present a 
draft proposal for the representative sonar data processing pipeline we aim to develop in this project. 
We will engage NCEI and the WGFAST community to generate a mature set of definitions, with cloud-optimized implementation in 
Echopype and in the project demonstration, and publish the combined data provenance and processing levels approach 
as an Ocean Best Practice for sonar data [44].

Table 1. Draft data processing levels for the representative sonar data processing pipeline we aim to develop in this project. We expect that the definitions will be revised with community inputs and expanded to include other common processing outputs (see table footnotes).

Level | Description | Implementation in the proposed pipeline | Required ancillary data
------|-------------|-----------------------------------------|------------------------
0 | Raw data in vendor sensor format | Instrument-dependent raw data records |
1 | Standardized raw data packaged with ancillary information | Zarr encoded data in SONAR-netCDF4 format | Instrument and other deployment metadata
2 | Calibrated acoustic quantities at raw data resolution | Volume backscattering strength (Sv) | Sound speed and absorption computed from associated temperature, conductivity and depth (CTD) measurements
3* | Averaged and/or regridded calibrated acoustic quantities | Mean volume backscattering strength (MVBS) over uniform local depth and time grids with seafloor echoes removed | Geographical location and depth of the sonar hosting platform; platform attitude (pitch, roll, heave)
4** | Acoustically derived biological features | Multi-frequency classification results in the form of nautical area backscattering coefficients (NASC or sA) | Biological data from net trawls or underwater camera images; empirical or physics-based acoustic scattering models

- \*Can be expanded to include removal of other noise sources, such as electronic or acoustic interference.
- \*\*Can be expanded to include outputs from other common analyses of lower-level data, such as acoustically detected animal aggregations, target strength (TS, units: dB re 1 m2) of individual animals, summary statistics of echogram features, biomass estimation, as well as species-level data labels useful for supervised machine learning developments
