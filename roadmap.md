# Event Studies Roadmap

## Time Series Improvements

### First week (bug fixes and making sure current functionality works)

- Adding consistency checks: [Issue #29](https://github.com/xKDR/TSx.jl/issues/29)
- Adding ```Vector{Date}``` based subsetting: [Issue #19](https://github.com/xKDR/TSx.jl/issues/19)
- Assessing how well `Statistics.jl` is currently integrated with `TSx.jl`

### Second Week

- Addition of broadcasting mathematical operators ```(.+, .-, .*, ./)``` for TS objects with identical columns (can be done through ```Tables.jl``` interfaces)
- Addition of integer-based indexing (through integration with `GLM.jl`)

## Event Studies Design

### Models

As per the information given in [MacKinlay: Event Studies in Economics and Finance](https://www.jstor.org/stable/2729691), the following return models should be paramount for calculating abnormal returns $X_\tau$, listed along with `TSx` requirements

$$AR_{i\tau} = R_{i\tau} - E(R_{i\tau}\mid X_\tau)$$

- Constant Mean Return Model
    - Efficient calculation of arithmetic/logarithmic returns (to be added to `TSx` via broadcasting)
    - To be used for calculation of Normal Returns and Market Returns
- Market Model
    - Efficient calculation of arithmetic/logarithmic returns
    - Efficient linear regression between stock and market returns
- Models based on CAPM

The user should be allowed to select the window over which the normal returns calculation will take place. Other statistical/economic models can be implemented, for example those given in [Event Studies for Financial Research](https://link.springer.com/book/10.1057/9781137368799). 
