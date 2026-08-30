# Get records for one or more taxonomic name(s) using the TAXAMATCH fuzzy matching algorithm

Get records for one or more taxonomic name(s) using the TAXAMATCH fuzzy
matching algorithm

## Usage

``` r
wm_records_taxamatch(name, marine_only = TRUE, ...)
```

## Arguments

- name:

  (character) taxon name. required.

- marine_only:

  (logical) marine only or not. default: `TRUE`

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

## Value

A list of tibble's/data.frame's, one for each of the input names

## Note

there is no underscore method like other functions in this package as
this function already accepts many names

## Examples

``` r
if (FALSE) { # \dontrun{
wm_records_taxamatch(name = 'Leucophaeus')
wm_records_taxamatch(name = c('Leucophaeus', 'Coryphaena'))
} # }
```
