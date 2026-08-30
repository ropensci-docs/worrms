# Get records for one or more taxonomic name(s)

Get records for one or more taxonomic name(s)

## Usage

``` r
wm_records_names(name, marine_only = TRUE, ...)
```

## Arguments

- name:

  (character) start date. required.

- marine_only:

  (logical) marine only or not. default: `TRUE`

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

## Value

A list of tibble's/data.frame's, one for each of the input names

## Note

there is no underscore method like other functions in this package as
this is the plural version for
[`wm_records_name()`](https://docs.ropensci.org/worrms/reference/wm_records_name.md)

## Examples

``` r
if (FALSE) { # \dontrun{
wm_records_names(name = 'Leucophaeus scoresbii')
wm_records_names(name = c('Leucophaeus scoresbii', 'Coryphaena'))
} # }
```
