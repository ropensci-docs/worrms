# Get records by date

Get records by date

## Usage

``` r
wm_records_date(
  start_date,
  end_date = NULL,
  marine_only = TRUE,
  offset = 1,
  ...
)
```

## Arguments

- start_date:

  (character) start date. required.

- end_date:

  (character) end date. optional

- marine_only:

  (logical) marine only or not. default: `TRUE`

- offset:

  (integer) record to start at. default: 1

- ...:

  named curl options. see
  [`curl::curl_options`](https://jeroen.r-universe.dev/curl/reference/curl_options.html)

## Value

A tibble/data.frame

## Examples

``` r
if (FALSE) { # \dontrun{
a_date <- format(Sys.Date() - 1, "%Y-%m-%dT%H:%M:%S+00:00")
wm_records_date(a_date)
} # }
```
