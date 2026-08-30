# Get record by external ID

Get record by external ID

## Usage

``` r
wm_record_by_external(id, type = "tsn", ...)

wm_record_by_external_(id = NULL, name = NULL, type = "tsn", ...)
```

## Arguments

- id:

  (numeric/integer) an AphiaID. For `wm_record_by_external` it's
  required and must be `length(id) == 1`, for `wm_record_by_external_`
  it's optional and can be `length(id) >= 1`

- type:

  (character) the type of external id. one of: tsn, bold, dyntaxa, eol,
  fishbase, iucn, lsid, ncbi, gisd. default: tsn

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

- name:

  (character) one or more taxonomic names. optional

## Value

A named list. When using underscore method, each output is named by the
input ID, and can be separated by the list names

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
wm_record_by_external(id = 85257)
wm_record_by_external(id = 159854)

wm_record_by_external_(id = c(85257, 159854))
} # }
```
