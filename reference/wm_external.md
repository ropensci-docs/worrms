# Get an external ID via an AphiaID

Get an external ID via an AphiaID

## Usage

``` r
wm_external(id, type = "tsn", ...)

wm_external_(id = NULL, name = NULL, type = "tsn", ...)
```

## Arguments

- id:

  (numeric/integer) an AphiaID. For `wm_external` it's required and must
  be `length(id) == 1`, for `wm_external_` it's optional and can be
  `length(id) >= 1`

- type:

  (character) the type of external id. one of: tsn, bold, dyntaxa, eol,
  fishbase, iucn, lsid, ncbi, gisd. default: tsn

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

- name:

  (character) one or more taxonomic names. optional

## Value

An integer that is the ID. When using underscore method, a list, named
by the input IDs

## Singular vs. plural

Of the two sister functions, the one without the underscore is the
original function that wraps the relavant WoRMS API method - and only
accepts one thing (i.e., name or AphiaID) per request.

The sister function with the underscore at the end is the plural
version, accepting more than one input. Internally this function loops
over the non-underscore method, and labels output (whether it's a list
or data.frame rows) with the input names or IDs so that you can easily
parse output by your inputs.

## Examples

``` r
if (FALSE) { # \dontrun{
# by default, get a TSN (an ITIS code)
wm_external(id = 1080)

## get many
wm_external_(id = c(1080, 126436))

# BOLD code
wm_external(id = 278468, type = "bold")

# NCBI code
wm_external(id = 278468, type = "ncbi")

# fishbase code
wm_external(id = 278468, type = "fishbase")

# curl options
library(crul)
wm_external(id = 105706, verbose = TRUE)
} # }
```
