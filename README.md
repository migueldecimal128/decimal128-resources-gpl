# decimal128-resources-gpl

The GPL-licensed data assets of the decimal128 project, kept apart from
[decimal128-resources](https://github.com/migueldecimal128/decimal128-resources)
so that the library ports, which take that repository as a submodule, never
carry GPL material.

Its one consumer is
[decimal128-app-benchmark](https://github.com/migueldecimal128/decimal128-app-benchmark),
itself GPLv3, which mounts this repository as a submodule at `resources-gpl/`.

## Contents

```
UW-Madison/
  DFPBenchmarksv1.0.gz                  the suite as distributed (tar.gz)
  DFPBenchmarksv1.0/                    the suite, unpacked
    banking/  euro_conversion/  risk_management/  tax_preparation/  telco/
    decNumberLib/  IntelRDFPMathLib10U1/  nativeGccLib/
    README                              the suite's own README
  BenchmarksAndPerfAnalysisDFP-2007.pdf
  Performance_analysis_of_decimal_floating-point_lib-2009.pdf
```

This is the University of Wisconsin-Madison Decimal Floating-Point (DFP)
Benchmark suite, v1.0, described in

- Liang-Kai Wang, Charles Tsen, Ankit Jhalani, Michael J. Schulte,
  "Benchmarks and Performance Analysis of Decimal Floating-Point
  Applications," IEEE International Conference on Computer Design (ICCD),
  October 2007.
- Mike Anderson, Charles Tsen, Liang-Kai Wang, Katherine Compton,
  Michael J. Schulte, "Performance Analysis of Decimal Floating-Point
  Libraries and Its Impact on Decimal Hardware and Software Solutions,"
  IEEE ICCD, October 2009.

The files are byte-identical to `UW-Madison/` in decimal128-resources, from
which this repository was split with its history (the two commits that added
and renamed the directory).

## License

The suite's sources are licensed under the GNU General Public License,
version 3, as their headers state (for example `banking/arith.def` and
`tax_preparation/operator.h`); the tax preparation benchmark derives from
OpenTaxSolver, also GPL. The full license text is in [`COPYING`](COPYING).

Third-party parts bundled with the suite keep their own terms, given in
their files: `IntelRDFPMathLib10U1/` (Intel Decimal Floating-Point Math
Library) and `decNumberLib/` (IBM decNumber). The two PDFs are the papers
above, under their publisher's copyright.

## Line endings

This is a byte-exact data repository: `.gitattributes` sets `* -text`, so no
end-of-line conversion is ever applied.
