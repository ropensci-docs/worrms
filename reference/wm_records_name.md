# Get records by single name, optional fuzzy matching

Get records by single name, optional fuzzy matching

## Usage

``` r
wm_records_name(name, fuzzy = TRUE, marine_only = TRUE, offset = 1, ...)
```

## Arguments

- name:

  (character) a taxonomic name, required.

- fuzzy:

  (logical) fuzzy search. default: `TRUE`

- marine_only:

  (logical) marine only or not. default: `TRUE`

- offset:

  (integer) record to start at. default: 1

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

## Value

A tibble/data.frame

## Note

there is no underscore method like other functions in this package as
there is already a plural version:
[`wm_records_names()`](https://docs.ropensci.org/worrms/reference/wm_records_names.md)

## Examples

``` r
if (FALSE) { # \dontrun{
wm_records_name(name = 'Leucophaeus')
wm_records_name(name = 'Leucophaeus', fuzzy = FALSE)
wm_records_name(name = 'Leucophaeus', marine_only = FALSE)
wm_records_name(name = 'Platanista', marine_only = FALSE)
wm_records_name(name = 'Platanista', marine_only = FALSE, offset = 5)
} # }
```
