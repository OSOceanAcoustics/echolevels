# Discussion 2022-07-12

## Based on proposal sketch

The sketch below was based on the [ideas laid out in the proposal](./from_proposal.md):

![data_processing_levels_old](https://user-images.githubusercontent.com/15334215/178650904-d2662ccb-3c37-40cd-8915-6ce8cb4e83b0.jpg)



## Revised version

The sketch below is revised during our discussion:

![data_processing_levels_new](https://user-images.githubusercontent.com/15334215/178650916-6bf133d4-8c10-49e7-a1d9-937fe4804f49.png)



Note that we now have a clear boundary between levels 2 and 3!

For level 3 and up, how to name these modules remain an open questions, but we have worked out a few groupings that makes sense:
- some functions are of "filtering" types that are based on the acoustic data itself: e.g., removal of noise estimated from the data, median filter, 2D convolution, etc.
- some functions are of "regridding" types that makes the data uniform in some way: e.g., compute mean volume backscattering strength (MVBS), actual regridding, etc.
- some functions rely on additional annotations or rule of thumb classification (in a way it is a type of filtering): e.g., removal of surface bubbles/transducer ringing down, removal of seafloor echoes, multi-frequency differencing, manual or automatic region annotations
