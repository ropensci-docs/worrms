# Changelog

## worrms 0.4.3

CRAN release: 2023-06-20

New maintainer: Bart Vanhoorne <bartv@vliz.be>

#### MINOR IMPROVEMENTS

- functions
  [`wm_records_names()`](https://docs.ropensci.org/worrms/reference/wm_records_names.md)
  and
  [`wm_records_taxamatch()`](https://docs.ropensci.org/worrms/reference/wm_records_taxamatch.md)
  now return always a list
  ([\#41](https://github.com/ropensci/worrms/issues/41))
- fix note on cran about LazyData (e5ba9f)

#### BUG FIXES

- fuzzy search option removed from
  [`wm_records_names()`](https://docs.ropensci.org/worrms/reference/wm_records_names.md)
  to stay on sync with the underlying web service
  ([\#26](https://github.com/ropensci/worrms/issues/26))

## worrms 0.4.2

CRAN release: 2020-07-08

#### MINOR IMPROVEMENTS

- fix a few failing tests on cran
  ([\#22](https://github.com/ropensci/worrms/issues/22))

## worrms 0.4.0

CRAN release: 2019-06-28

#### NEW FEATURES

- new functions
  [`wm_ranks_id()`](https://docs.ropensci.org/worrms/reference/wm_ranks.md)
  and
  [`wm_ranks_name()`](https://docs.ropensci.org/worrms/reference/wm_ranks.md)
  for getting taxonomic ranks by rank identifier or rank name
  ([\#20](https://github.com/ropensci/worrms/issues/20))
- new function
  [`wm_records_rank()`](https://docs.ropensci.org/worrms/reference/wm_records_rank.md)
  for getting AphiaRecords for a given rank id
  ([\#20](https://github.com/ropensci/worrms/issues/20))

#### MINOR IMPROVEMENTS

- [`wm_synonyms()`](https://docs.ropensci.org/worrms/reference/wm_synonyms.md)
  gains `offset` parameter to allow pagination
  ([\#20](https://github.com/ropensci/worrms/issues/20))
- [`tibble::as_data_frame()`](https://tibble.tidyverse.org/reference/deprecated.html)
  replaced with
  [`tibble::as_tibble()`](https://tibble.tidyverse.org/reference/as_tibble.html)

#### DEPRECATED AND DEFUNCT

- [`wm_record_()`](https://docs.ropensci.org/worrms/reference/wm_record.md)
  is deprecated;
  [`wm_record()`](https://docs.ropensci.org/worrms/reference/wm_record.md)
  now handles 1 or more AphiaID’s

#### BUG FIXES

- fix `wm_children` test that was failing on cran checks
  ([\#21](https://github.com/ropensci/worrms/issues/21))

## worrms 0.3.2

CRAN release: 2019-01-04

#### MINOR IMPROVEMENTS

- add link to taxize book in vignette and README
  ([\#12](https://github.com/ropensci/worrms/issues/12))

#### BUG FIXES

- fix bug in test regarding date
  ([\#19](https://github.com/ropensci/worrms/issues/19))

## worrms 0.3.0

CRAN release: 2018-11-07

#### MINOR IMPROVEMENTS

- fix to most functions throughout the package (those that have two
  versions, with and without an underscore): underscore versions of
  functions now do not error when an input is not found, but instead
  warn the user and move on - to facilitate working with many inputs.
  the non-underscore version of each function still only accepts 1 input
  and errors if you give more than 1
  ([\#14](https://github.com/ropensci/worrms/issues/14))
  ([\#18](https://github.com/ropensci/worrms/issues/18))

#### BUG FIXES

- make sure that functions that accept only 1 input for the first
  parameter error well with an informative message
  ([\#15](https://github.com/ropensci/worrms/issues/15))

## worrms 0.2.8

CRAN release: 2018-05-21

#### NEW FEATURES

- Integration with `vcr` and `webmockr` packages for unit test stubbing
- gains new functions for getting WORMS traits data (they call them
  “attributes”): `wm_attr_aphia`, `wm_attr_aphia_`, `wm_attr_category`,
  `wm_attr_category_`, `wm_attr_data`, `wm_attr_data_`, `wm_attr_def`,
  `wm_attr_def_` ([\#3](https://github.com/ropensci/worrms/issues/3))

## worrms 0.2.0

CRAN release: 2017-08-24

#### NEW FEATURES

- Added additional sister functions to most exported functions in the
  package, all with trailing underscore. For example, `wm_children` and
  `wm_children_`. These underscore methods take in many inputs,
  typically of a AphiaID or a taxonomic or vernacular name. We decided
  to make separate functions so that we minimize any disturbance to the
  existing package API.
  ([\#4](https://github.com/ropensci/worrms/issues/4))
  ([\#6](https://github.com/ropensci/worrms/issues/6))

#### MINOR IMPROVEMENTS

- Moved to using markdown docs
  ([\#5](https://github.com/ropensci/worrms/issues/5))
- All functions now state what they return
  ([\#9](https://github.com/ropensci/worrms/issues/9))

## worrms 0.1.0

CRAN release: 2017-01-14

#### NEW FEATURES

- Released to CRAN.
