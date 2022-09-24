
<!-- README.md is generated from README.Rmd. Please edit that file -->

# geojsonio

<!-- badges: start -->

[![R-CMD-check](https://github.com/ropensci/geojsonio/workflows/R-CMD-check/badge.svg)](https://github.com/ropensci/geojsonio/actions?query=workflow%3AR-CMD-check)
[![cran
checks](https://cranchecks.info/badges/worst/geojsonio)](https://cranchecks.info/pkgs/geojsonio)
[![codecov.io](https://codecov.io/github/ropensci/geojsonio/coverage.svg?branch=main)](https://codecov.io/github/ropensci/geojsonio?branch=main)
[![rstudio mirror
downloads](https://cranlogs.r-pkg.org/badges/geojsonio)](https://github.com/r-hub/cranlogs.app)
[![cran
version](https://www.r-pkg.org/badges/version/geojsonio)](https://cran.r-project.org/package=geojsonio)
<!-- badges: end -->

**Convert various data formats to GeoJSON or TopoJSON**

This package is a utility to convert geographic data to GeoJSON and
TopoJSON formats. Nothing else. We hope to do this one job very well,
and handle all reasonable use cases.

Functions in this package are organized first around what you’re working
with or want to get, GeoJSON or TopoJSON, then convert to or read from
various formats:

-   `geojson_list()`/`topojson_list()` - convert to GeoJSON/TopoJSON as
    R list format
-   `geojson_json()`/`topojson_json()` - convert to GeoJSON/TopoJSON as
    JSON
-   `geojson_sp()` - convert output of `geojson_list()` or
    `geojson_json()` to `sp` spatial objects
-   `geojson_sf()` - convert output of `geojson_list()` or
    `geojson_json()` to `sf` objects
-   `geojson_read()`/`topojson_read()` - read a GeoJSON/TopoJSON file
    from file path or URL
-   `geojson_write()`/`topojson_write()` - write a GeoJSON/TopoJSON file
    locally

Each of the above functions have methods for various objects/classes,
including `numeric`, `data.frame`, `list`, `SpatialPolygons`,
`SpatialLines`, `SpatialPoints`, etc.

Additional functions:

-   `map_gist()` - push up a GeoJSON or topojson file as a GitHub gist
    (renders as an interactive map)
-   `map_leaf()` - create a local interactive map using the `leaflet`
    package

## \*json Info

-   GeoJSON - [spec](https://tools.ietf.org/html/rfc7946)
-   [GeoJSON lint](https://geojsonlint.com/)
-   TopoJSON -
    [spec](https://github.com/topojson/topojson-specification/blob/master/README.md)

## Install

A note about installing `rgeos` - built on top of C libraries, and
installation often causes trouble for Linux users because no binaries
are provided on CRAN for those platforms. Other dependencies in
`geojsonio` should install easily automatically when you install
`geojsonio`.

*Mac*

Install `GDAL` on the command line first, e.g., using `homebrew`

    brew install gdal

Then install `rgeos`

``` r
install.packages("rgeos", type = "source")
```

*Linux*

Get deps first

    sudo apt-get install libgdal1-dev libgdal-dev libgeos-c1 libproj-dev

> Note: if you have trouble installing rgeos, try installing
> `libgeos++-dev`

Then install `rgeos`

``` r
install.packages("rgeos", type = "source")
```

**Install geojsonio**

Stable version from CRAN

``` r
install.packages("geojsonio")
```

Or development version from GitHub

``` r
install.packages("remotes")
remotes::install_github("ropensci/geojsonio")
```

``` r
library("geojsonio")
```

## Meta

-   Please [report any issues or
    bugs](https://github.com/ropensci/geojsonio/issues).
-   License: MIT
-   Get citation information for `geojsonio` in R doing
    `citation(package = 'geojsonio')`
-   Please note that this package is released with a [Contributor Code
    of Conduct](https://ropensci.org/code-of-conduct/). By contributing
    to this project, you agree to abide by its terms.
