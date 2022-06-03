# Event Studies Roadmap

## Time Series Improvements

### First week (bug fixes and making sure current functionality works)

- Adding consistency checks: [Issue #29](https://github.com/xKDR/TSx.jl/issues/29)
- Adding ```Vector{Date}``` based subsetting: [Issue #19](https://github.com/xKDR/TSx.jl/issues/19)
- Assessing how well `Statistics.jl` is currently integrated with `TSx.jl`

### Second Week

- Addition of broadcasting mathematical operators ```(.+, .-, .*, ./)``` for TS objects with identical columns (can be done through ```Tables.jl``` interfaces)
- Addition of integer-based indexing

## Event Studies Design

### Models

As per the information given in [MacKinlay: Event Studies in Economics and Finance](https://www.jstor.org/stable/2729691), the following return models should be paramount for calculating abnormal returns $X_\tau$:

$$AR_{i\tau} = R_{i\tau} - E(R_{i\tau}\mod X_\tau)$$

- Constant Mean Return Model:
    - Let $\mu_i$ be the mean return. Then the constant mean return model is
    $$R_{it} = \mu_i + \zeta_{it}$$
- Market Model

The user should be allowed to select the window over which the normal returns calculation will take place.