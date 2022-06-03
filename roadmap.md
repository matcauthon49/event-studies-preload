# Event Studies Roadmap

## Time Series Improvements

### First week (bug fixes and making sure current functionality works)

- Adding consistency checks: [Issue #29](https://github.com/xKDR/TSx.jl/issues/29)
- Adding ```Vector{Date}``` based subsetting: [Issue #19](https://github.com/xKDR/TSx.jl/issues/19)

### Second Week

- Addition of broadcasting mathematical operators ```(.+, .-, .*, ./)``` for TS objects with identical columns (can be done through ```Tables.jl``` interfaces)
- Addition of integer-based indexing

