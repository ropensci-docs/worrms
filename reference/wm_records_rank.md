# Get AphiaRecords for a given taxonRankID

Get AphiaRecords for a given taxonRankID

## Usage

``` r
wm_records_rank(rank_id, id = NULL, offset = 1, ...)
```

## Arguments

- rank_id:

  (numeric/integer) a rank id

- id:

  (character) a single AphiaID

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
wm_records_rank(rank_id = 180, id = 106776)
wm_records_rank(rank_id = 180, id = 106776, offset = 50)
} # }
```
