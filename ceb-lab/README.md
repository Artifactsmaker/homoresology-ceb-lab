# Convergent Equivalence Benchmark Lab

**CEB-Lab** is a static research-artifact web application for exploring Convergent Equivalence: the measurable behavior of different expressions that converge to the same Target Solution.

The default benchmark studies the Equivalence Class around `S = 5`, comparing each Equivalent Expression by Solution Preservation, Transformation Cost, Convergence Stability, Interpretability Score, Compression Gain, and Reusability Score.

## Run locally

Open `index.html` in a modern browser. No server, package installation, backend, account, or build step is required.

Chart.js is loaded from a CDN. If the page is opened without an internet connection and Chart.js has not previously been cached, the benchmark, table, metrics, and exports still work; only chart rendering is unavailable.

For GitHub Pages, publish the repository root and use `index.html` as the entry point.

## Benchmark metrics

- **Solution Preservation (`S_P`)** — whether an expression evaluates to the Target Solution.
- **Transformation Cost (`C_T`)** — structural complexity; lower is better.
- **Convergence Stability (`C_S`)** — numerical proximity to the Target Solution.
- **Interpretability Score (`I_S`)** — estimated human readability.
- **Compression Gain (`C_G`)** — compactness of the representation.
- **Reusability Score (`R_S`)** — estimated generalizability of the expression pattern.
- **Equivalence Density (`E_D`)** — convergent expressions divided by all benchmark expressions.
- **Global Convergence Score (`GS`)** — weighted aggregate of the benchmark profile.

All heuristics are transparent in `index.html` and should be treated as benchmark instrumentation, not as mathematical proof.

## Controlled expression language

CEB-Lab supports decimal and integer numbers, parentheses, `+`, `-`, `*`, `/`, `^`, `sqrt(x)`, `abs(x)`, and `factorial(x)`. A purpose-built parser is used; arbitrary JavaScript execution is not permitted.

## Folder structure

```text
index.html
README.md
user-guide.md
benchmark/
  sample-report.md
  sample-report.json
  sample-report.csv
screenshots/
```

## Exported reports

The app exports a current Equivalence Benchmark Report as Markdown, JSON, or CSV. Reports contain expression-level measurements, aggregate metrics, interpretation, limitations, timestamp, and version metadata.

## Citation placeholder

> [Author]. (2026). *Convergent Equivalence Benchmark Lab (CEB-Lab), version 1.0.0*. [Repository / DOI].

## License placeholder

No license has been selected. Add a `LICENSE` file before public redistribution.

