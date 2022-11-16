---
layout: default
---

This page descries the strategy we are applying to manage the urispace to identify all possible required elements in this space published at

baseuri == `https://data.ocean-sampling-day.org`

# concepts

| entity type                     | path-pattern                                           | description                                                                              | example                          |
| ------------------------------- | ------------------------------------------------------ | ---------------------------------------------------------------------------------------- | -------------------------------- |
| root / space                    | /                                                      | the root of this URIspace doubles as the "space" that contains and identifies everything |                                  |
| data-package                    | /{repository-name}/                                    | identifier for the RO-crate                                                              | `/OSD2018/`                      |
| year                            | /year/{yyyy}/                                          | everything from OSD related to a certain year                                            | `/year/2014/`                    |
| station                         | /station/{stationcode}/                                | coded locations where samples are taken                                                  | `/station/OSD19/`                |
| sampling-protocol               | /protocol/{protocol}                                   | standard, agreed, conform way of taking the physical sample                              | `/protocol/NPL02`                |
| replicate (aka material sample) | /sample/{stationcode}-{yyyy}-{protocol}-{replicate_nr} | actual container (testtube) containing retrieved material samples                        | `/sample/OSD100_2014-03_NPL02_1` |
| processing-level                | /level/{levelcode}                                     | meaningful internal term for `raw` or `processed` level of the data                      | `/level/raw`                     |
| ontology                        | /ns/ontology                                           | specific space to describe additional internal concepts for OSD                          | `/ns/ontology`                   |

# contents

| entity type  | path-pattern                | description                                                                              | example |
| ------------ | --------------------------- | ---------------------------------------------------------------------------------------- | ------- |
| file-content | /{repository-name}/{path}   | download point to get actual content of a file in the specified package                  |
| file-preview | /{repository-name}#./{path} | preview location to get a human readable view of a certain file in the specified package |

# fragments

| entity type | path-pattern | description | example |
| ----------- | ------------ | ----------- | ------- |

| no actul fragmentations have been defined at the moment, but we could consider: species (ncbi or aphia), combo year-station, combo year-protocol, ...

## Glossary

- We decided to avoid using the possiby ambiguous word `dataset` but rather either:
  - `datapackage` --> to refer to our beloved ro-crates
  - `datafile` --> to refer ro one particular file (e.g. csv) inside a package

## Note

- rows in csv files should introduce identifiers to the conceptual type of things they represent. Unclear now if we might also want to introduce an identifier to the rows (as being data-lines)
