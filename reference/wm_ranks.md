# Get taxonomic ranks by their identifier

Get taxonomic ranks by their identifier

## Usage

``` r
wm_ranks_id(rank_id, id = NULL, offset = 1, ...)

wm_ranks_name(rank_name, id = NULL, offset = 1, ...)
```

## Arguments

- rank_id:

  (numeric/integer) a rank identifier. length==1

- id:

  an AphiaID. length==1

- offset:

  (integer) record to start at. default: 1

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

- rank_name:

  (character) a rank name. length==1

## Value

A tibble/data.frame

## Examples

``` r
if (FALSE) { # \dontrun{
wm_ranks_id(220)
wm_ranks_id(180)
wm_ranks_id(180, id = 4)

wm_ranks_name("genus")
wm_ranks_name("genus", id = 4)
} # }
```
