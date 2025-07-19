# Custom Pseudorandom Number Generator (PRNG) Analysis
 Overview

This project implements a **custom pseudorandom number generator (PRNG)** using the **Linear Congruential Generator (LCG)** method. It analyses the generated data for:

- **Uniformity** using histograms
- **Dependency** using scatter plots

Algorithm Details

The PRNG is based on the formula:

[X_{n+1} = (aX_n + c) \mod m]

where:

- `a = 1103515245`
- `c = 12345`
- `m = 2^31`
- `seed` is user-defined

The output is normalized to the range [0,1).

Files Generated

- `myprng_dependency.pdf`: Scatter plot to check dependency and correlations.
- `myprng_uniformity.pdf`: Histograms of X and Y outputs to check uniformity.


Summary Statistics

Example output (your actual results may slightly vary):

=== Custom PRNG Summary ===
Mean X: 0.4961, Std X: 0.2887
Mean Y: 0.4650, Std Y: 0.2887


How to Run

 Install required libraries:

   pip install numpy matplotlib
Run the script:

python your_script_name.py
Check the generated plots (.pdf files) for analysis.
Interpretation
Uniformity: Histograms should ideally be flat across the range if the PRNG is unbiased.

Dependency: Scatter plot should appear random without visible patterns. Structured patterns indicate dependency weaknesses (common in LCGs).

Applications
Random sampling for simulations

Cryptography (note: LCG is not cryptographically secure)

Testing randomness algorithms in coursework or research

