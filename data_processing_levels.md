# Proposed Echosounder Data Proccesing Levels (DRAFT)

(PLACEHOLDER FOR A BRIEF INTRODUCTORY PARAGRAPH)

### Level 0 (L0)

**Description:**  Raw data in vendor sensor format.

- raw binary files. Associated metadata may be found in external files.

### Level 1 (L1)

**Description:** Raw data packaged with ancillary information and converted and standardized to an open convention and standard data formats. May be distributed as sets of individual converted files as originally segmented into arbitrary time ranges during sensor file creation or compiled into larger granules corresponding to logical deployment intervals.

- L1A: Raw L0 data converted to a standardized, open format with geographic coordinates (latitude & longitude) processed and included. Includes other ancillary information extracted from sensor-generated L0 data or other external sources. May include environmental information such as temperature, salinity and pressure. Use of the SONAR-netcDF4 v1 convention is strongly recommended.
- L1B: L1A data with quality-control steps applied, such as time-coordinate corrections that enforce strictly increasing, non-duplicate timestamps.

### Level 2 (L2)

**Description:** Calibrated acoustic quantities at raw data resolution, with spatial coordinates included (latitude, longitude and depth)

- L2A: Volume backscattering strength (`Sv`) with interpolated latitude, longitude and depth coordinates. May incorporate addition information, such as  split beam angle
- L2B: `Sv` L2A data with noise removal or other data filtering applied, including seafloor bottom removal.

### Level 3 (L3)

**Description:** Calibrated acoustic quantities regridded or aggregated to a common grid across channels. May include noise removal or other filtering.

- `Sv` resampled to a common, high-resolution grid across channels
- Mean Volume Backscattering Strength (`MVBS`)
- `Sv` frequency difference across two channels resampled to a common grid
- L3A: The above variables computed on L2A data
- L3B: The above variables computed on L2B (filtered) data

### Level 4 (L4)

**Description:** Acoustically derived biological features, involving further processing of L3 data that may include data reduction or incorporation of external sources of data.

- Nautical Area Backscattering Coefficients (`NASC`)
- Summary statistics of echogram features (center_of_mass, dispersion, etc)
- Taxon or species-level data labels (classification). May originate from a variety of methods, including frequency difference thresholds.
- Biomass estimation
