# Get records by vernacular name, optional fuzzy matching

Get records by vernacular name, optional fuzzy matching

## Usage

``` r
wm_records_common(name, fuzzy = FALSE, offset = 1, ...)

wm_records_common_(name, fuzzy = FALSE, offset = 1, ...)
```

## Arguments

- name:

  (character) a species common name. required. For `wm_records_common`
  must be `length(name) == 1`; for `wm_records_common_` can be
  `length(name) >= 1`

- fuzzy:

  (logical) fuzzy search. default: `FALSE`

- offset:

  (integer) record to start at. default: 1

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

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
wm_records_common(name = 'dolphin')
wm_records_common(name = 'clam')

wm_records_common_(name = c('dolphin', 'clam'))

wm_records_common(name = 'dolphin', fuzzy = TRUE)
wm_records_common(name = 'clam', fuzzy = TRUE, offset = 5)
} # }
```
