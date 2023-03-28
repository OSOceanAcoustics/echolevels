# Data processing levels: inputs-outputs by echopype function

- N.P.L.: No Processing Level attached to output (typically because latitude & longitude are not found in the output)
- L0: Level 0, raw file


input (with input id) -> function -> output (with output id) |
--------- |
L0 (with lat-lon) -> `open_raw` -> L1A [1]
L0 (without lat-lon) -> `open_raw` -> N.P.L. [2] -> `update_platform` -> L1A [3]
[1,3] -> `calibrate.compute_Sv` -> N.P.L. [4] -> `consolidate.add_latlon` -> L2A [5]
[1,3] -> `calibrate.compute_TS` -> N.P.L. [6]
[5] -> `clean.remove_noise` -> L2B [7]
[5] -> `mask.frequency_differencing` -> N.P.L. [8]
[7] -> `mask.frequency_differencing` -> N.P.L. [9]
[5] + [8] -> `mask.apply_mask` -> L3A [10]
[7] + [9] -> `mask.apply_mask` -> L3B [11]
[4,5,7,10,11] -> `commongrid.compute_MVBS` -> N.P.L. [12]
[4,5,7,10,11] -> `commongrid.compute_MVBS_index_binning` -> N.P.L. [13]
[4,5,7,10,11] -> `commongrid.compute_NASC` -> N.P.L. [14]

Not included: `qc.coerce_increasing_time`, `consolidate.swap_dims_channel_frequency`, `consolidate.add_depth`, `consolidate.add_splitbeam_angle`
