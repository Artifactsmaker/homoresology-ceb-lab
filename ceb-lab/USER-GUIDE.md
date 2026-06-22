# CEB-Lab User Guide

## 1. Set the Target Solution

Enter a finite number in the **Target Solution** field. This value is the benchmark endpoint, written as `S`.

## 2. Add or remove expressions

Each input in the Equivalent Expression panel is a candidate Transformation Path.

- Select **Add Transformation Path** to add an expression.
- Select the `×` button beside an expression to remove it.
- Supported syntax: `+`, `-`, `*`, `/`, `^`, parentheses, `sqrt(x)`, `abs(x)`, and `factorial(x)`.
- Press Enter in any expression field to run the benchmark.

Unsupported names, characters, malformed expressions, division by zero, and invalid function domains are reported as invalid. CEB-Lab never uses unrestricted `eval`.

## 3. Run the benchmark

Select **Run benchmark**. The dashboard, charts, benchmark table, and generated interpretation update immediately. All processing stays in the browser.

Use **Reset** to restore the default Equivalence Class around `S = 5`. Use **Theme** to switch between dark and light modes.

## 4. Interpret the metrics

- **Solution Preservation (`S_P`)**: `100` if the expression converges to `S`; otherwise `0`.
- **Transformation Cost (`C_T`)**: counts operators, functions, parenthesis depth, and a token penalty. Lower values indicate a shorter or simpler Transformation Path.
- **Convergence Stability (`C_S`)**: `100 / (1 + |result − S|)`. Exact convergence scores `100`.
- **Interpretability Score (`I_S`)**: starts at `100` and decreases with operators, advanced functions, and nesting.
- **Compression Gain (`C_G`)**: rewards shorter expressions.
- **Reusability Score (`R_S`)**: a heuristic estimate based on arithmetic and function patterns.
- **Equivalence Density (`E_D`)**: the percentage of all entered expressions that validly converge to `S`.
- **Global Convergence Score (`GS`)**: a weighted aggregate using the published default weights, including a normalized Transformation Cost penalty.

The chart views compare expressions, summarize the average profile, and show convergent versus non-convergent paths.

## 5. Export reports

Choose **Export .MD**, **Export .JSON**, or **Export .CSV** below the benchmark table.

- Markdown is intended for manuscripts, repositories, and human review.
- JSON preserves metadata, metric symbols, detailed rows, and aggregate values.
- CSV contains one row per Equivalent Expression for spreadsheet or statistical analysis.

## Limitation

This benchmark evaluates computational convergence behavior within a controlled expression environment. It does not claim to exhaust all mathematical equivalences or prove general equivalence theory.

