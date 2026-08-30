# Get attribute data by AphiaID

Get attribute data by AphiaID

## Usage

``` r
wm_attr_data(id, include_inherited = FALSE, ...)

wm_attr_data_(id = NULL, name = NULL, ...)
```

## Arguments

- id:

  (numeric/integer) an AphiaID. For `wm_attr_data` it's required and
  must be `length(id) == 1`, for `wm_attr_data_` it's optional and can
  be `length(id) >= 1`

- include_inherited:

  (logical) Include attributes inherited from its parent taxon. Default:
  `FALSE`

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

- name:

  (character) one or more taxonomic names. optional

## Value

A tibble/data.frame. when using underscore method, outputs from each
input are binded together, but can be split by `id` column

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
wm_attr_data(id = 127160)
wm_attr_data(id = 126436)

wm_attr_data_(id = c(127160, 126436))
} # }
```
