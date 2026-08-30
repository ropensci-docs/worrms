# Get taxonomic name for an AphiaID

Get taxonomic name for an AphiaID

## Usage

``` r
wm_id2name(id, ...)

wm_id2name_(id, ...)
```

## Arguments

- id:

  (numeric/integer) an AphiaID, required. For `wm_id2name` must be
  `length(id) == 1`, but for `wm_id2name_` can be `length(id) >= 1`

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

## Value

An character string that is the taxnomic name. When using underscore
method, a list, named by the input IDs

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
wm_id2name(id = 105706)
wm_id2name_(id = c(105706, 126436))
} # }
```
