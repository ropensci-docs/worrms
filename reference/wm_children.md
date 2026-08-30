# Get children for an AphiaID

Get children for an AphiaID

## Usage

``` r
wm_children(id, marine_only = TRUE, offset = 1, ...)

wm_children_(id = NULL, name = NULL, marine_only = TRUE, offset = 1, ...)
```

## Arguments

- id:

  (numeric/integer) an AphiaID. For `wm_children` it's required and must
  be `length(id) == 1`, for `wm_children_` it's optional and can be
  `length(id) >= 1`

- marine_only:

  (logical) marine only or not. default: `TRUE`

- offset:

  (integer) record to start at. default: 1

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
wm_children(343613)
wm_children(id = 105706)
wm_children(id = 105706, FALSE)
wm_children(id = 105706, offset = 5)

# plural version, via id or name
wm_children_(id = c(105706, 343613))
wm_children_(name = c('Mesodesma', 'Leucophaeus'))
} # }
```
