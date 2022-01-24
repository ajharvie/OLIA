# Serial communication reference 
## List of serial commands

The below table lists the serial commands OLIA accepts. 

| Command | Description | Note |
| --- | --- | --- |
| `t` | Toggle synchronous filter | Default off |
| `r` | Toggle reference mode | Defaults to internal reference |
| `[x]` | Set internal reference frequency in Hz | e.g. send `200` to set reference frequency to 200 Hz |
| `g[n]` | Set input gain to n | e.g. send `g2` to set input gain to 2. Default 1 |
| `c` | Recalculate external reference frequency | Only for use with external reference |
| `e[x]` | Set exponential filter time constant to x seconds | e.g. send `e6` to set time constant to 6 s |
| `s[x]` | Set analogue output scale factor to x  | e.g. send `s10` to set output scale factor to 10  |
| `h[n]` | Set first "higher" harmonic number to calculate to n (see [Usage guide](https://github.com/ajharvie/OLIA/blob/main/doc/usageGuide.md))  | e.g. send `h2` to calculate from the 2nd harmonic|


Note: In above table, [x] represents floating point values and [n] represents integers. The square brackets should not be included in commands.

## Parsing OLIA's output

OLIA makes an output every 100 ms, consisting of a string of values separated by spaces, terminating in a carriage return and new line (".....\r\n"). These values are summarised in the table below, where the index represents each value's position in the output string.

| Index | Description | Type | Note |
| --- | --- | --- | --- |
| 0 | Clipping indicator  | Boolean | 1 (true) if clipping, 0 (false) otherwise |
| 1 | Analogue output scaling factor | Float | default 10 |
| 2 | Input preamp gain | Integer | Default 1, allowed values 0, 1, 2, 4, 8, 16, 32, 64 |
| 3 | Synchronous filter indicator | Boolean | Default 0 (false, exponential filter is in use), 1 if synchronous filter is in use |
| 4 | Reference mode indicator | Boolean | Default 0 (false, internal reference is in use), 1 if external reference is in use |
| 5 | Number of samples per reference signal period | Integer |  |
| 6 | True sample rate | Float | Units are Hz |
| 7 | Current reference signal frequency | Float | Units are Hz |
| 8 | Current exponential time constant | Float | Units are seconds |
| 9 | Undersampling | Integer | Degree of undersampling (for high frequency external reference signals only) e.g. if 1, there is no undersampling (64 samples per period) but if 2, this reduces to 32 samples per period |
| 10 | R | Float | Total recovered lock-in amplitude |
| 11 | ϕ | Float | Recovered phase in radians |
| 12 | Noise estimate | Float | Noise estimate based on the rooted variance of the quadrature signal |
| 13 | X(1) | Float | Recovered lock-in amplitude (In phase, fundamental) |
| 14 | Y(1) | Float | Recovered lock-in amplitude (quadrature, fundamental) |
| 15 | X(n) | Float | Recovered lock-in amplitude (In phase, nth harmonic). Here, n is the harmonic number of the first higher harmonic being calculated (default 2, reported later) |
| 16 | X(n+1) | Float | Recovered lock-in amplitude (In phase, n+1th harmonic) |
| 17 | X(n+2) | Float | Recovered lock-in amplitude (In phase, n+2th harmonic) |
| 18 | Y(n) | Float | Recovered lock-in amplitude (quadrature, nth harmonic) |
| 19 | Y(n+1) | Float | Recovered lock-in amplitude (quadrature, n+1th harmonic) |
| 20 | Y(n+2) | Float | Recovered lock-in amplitude (quadrature, n+2th harmonic) |
| 21 | n | Integer | Harmonic number n of first reported higher harmonic |


