# Discussion 2022-07-12

## Based on proposal sketch

The sketch below was based on the [ideas laid out in the proposal](./from_proposal.md):


## Revised version

The sketch below is revised during our discussion:



Note that we now have a clear boundary between levels 2 and 3!

For level 3 and up, how to name these modules remain an open questions, but we have worked out a few groupings that makes sense:
- some functions are of "filtering" types that are based on the acoustic data itself: e.g., removal of noise estimated from the data, median filter, 2D convolution, etc.
- some functions are of "regridding" types that makes the data uniform in some way: e.g., compute mean volume backscattering strength (MVBS), actual regridding, etc.
- some functions rely on additional annotations or rule of thumb classification (in a way it is a type of filtering): e.g., removal of surface bubbles/transducer ringing down, removal of seafloor echoes, multi-frequency differencing, manual or automatic region annotations
