# Get AphiaID from a taxonomic name

Get AphiaID from a taxonomic name

## Usage

``` r
wm_name2id(name, ...)

wm_name2id_(name, ...)
```

## Arguments

- name:

  (character) a taxonomic name, required. For `wm_name2id` must be
  `length(name) == 1`, but for `wm_name2id_` can be `length(name) >= 1`

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

## Value

An integer that is the AphiaID. When using underscore method, a list,
named by the input names

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
wm_name2id(name = "Rhincodon")
wm_name2id_(name = c("Rhincodon", "Gadus morhua"))
} # }
```
