# Versioning

This is copied almost directly from Yihui Xie, from here: <https://yihui.org/en/2013/06/r-package-versioning/>.
It is some of the clearest guidance available for software versioning, and can just as easily apply to anything else (e.g., a research compendium or parameter set).

1. a version number is of the form major.minor.patch (x.y.z), e.g., 0.1.7
2. only the version x.y is released to CRAN
3. x.y.z is always the development version, and each time a new feature or a bug fix or a change is introduced, bump the patch version, e.g., from 0.1.3 to 0.1.4
4. when one feels it is time to release to CRAN, bump the minor version, e.g., from 0.1 to 0.2
5. when a change is crazy enough that many users are presumably going to yell at you (see the illustration above), it is time to bump the major version, e.g., from 0.18 to 1.0
6. the version 1.0 does not imply maturity; it is just because it is potentially very different from 0.x (such as API changes); same thing applies to 2.0 vs 1.0
