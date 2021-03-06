
<!-- TODO: name file README.Rmd -->

<!-- Copyright Notice: Sample Package README forked from `rtweet` repo -->

# rtweet <img src="figures/logo.png" width="160px" align="right" />

[![Build
Status](https://travis-ci.org/ropensci/rtweet.svg?branch=master)](https://travis-ci.org/ropensci/rtweet)
[![CRAN
status](https://www.r-pkg.org/badges/version/rtweet)](https://cran.r-project.org/package=rtweet)
[![Coverage
Status](https://codecov.io/gh/ropensci/rtweet/branch/master/graph/badge.svg)](https://codecov.io/gh/ropensci/rtweet?branch=master)
[![DOI](https://zenodo.org/badge/64161359.svg)](https://zenodo.org/badge/latestdoi/64161359)
[![](https://badges.ropensci.org/302_status.svg)](https://github.com/ropensci/software-review/issues/302)
[![Project Status: Active – The project has reached a stable, usable
state and is being actively
developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
![Downloads](https://cranlogs.r-pkg.org/badges/rtweet)
![Downloads](https://cranlogs.r-pkg.org/badges/grand-total/rtweet)
[![lifecycle](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
[![DOI](https://joss.theoj.org/papers/10.21105/joss.01829/status.svg)](https://doi.org/10.21105/joss.01829)

R client for accessing Twitter’s REST and stream APIs. Check out the
[rtweet package documentation website](https://rtweet.info).

### Package Functionality

There are several R packages for interacting with Twitter’s APIs. See
how {rtweet} compares to these others in the chart below.

| Task                        | [rtweet](https://github.com/ropensci/rtweet) | [twitteR](https://github.com/geoffjentry/twitteR) | [streamR](https://github.com/pablobarbera/streamR) | [RTwitterAPI](https://github.com/joyofdata/RTwitterAPI) |
| --------------------------- | -------------------------------------------- | ------------------------------------------------- | -------------------------------------------------- | ------------------------------------------------------- |
| Available on CRAN           | ✅                                            | ✅                                                 | ✅                                                  | ❌                                                       |
| Updated since 2016          | ✅                                            | ❌                                                 | ✅                                                  | ❌                                                       |
| Non-‘developer’ access      | ✅                                            | ❌                                                 | ❌                                                  | ❌                                                       |
| Extended tweets (280 chars) | ✅                                            | ❌                                                 | ✅                                                  | ❌                                                       |
| Parses JSON data            | ✅                                            | ✅                                                 | ✅                                                  | ❌                                                       |
| Converts to data frames     | ✅                                            | ✅                                                 | ✅                                                  | ❌                                                       |
| Automated pagination        | ✅                                            | ❌                                                 | ❌                                                  | ❌                                                       |
| Search tweets               | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Search users                | ✅                                            | ❌                                                 | ❌                                                  | ❓                                                       |
| Stream sample               | ✅                                            | ❌                                                 | ✅                                                  | ❌                                                       |
| Stream keywords             | ✅                                            | ❌                                                 | ✅                                                  | ❌                                                       |
| Stream users                | ✅                                            | ❌                                                 | ✅                                                  | ❌                                                       |
| Get friends                 | ✅                                            | ✅                                                 | ❌                                                  | ✅                                                       |
| Get timelines               | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Get mentions                | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Get favorites               | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Get trends                  | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Get list members            | ✅                                            | ❌                                                 | ❌                                                  | ❓                                                       |
| Get list memberships        | ✅                                            | ❌                                                 | ❌                                                  | ❓                                                       |
| Get list statuses           | ✅                                            | ❌                                                 | ❌                                                  | ❓                                                       |
| Get list subscribers        | ✅                                            | ❌                                                 | ❌                                                  | ❓                                                       |
| Get list subscriptions      | ✅                                            | ❌                                                 | ❌                                                  | ❓                                                       |
| Get list users              | ✅                                            | ❌                                                 | ❌                                                  | ❓                                                       |
| Lookup collections          | ✅                                            | ❌                                                 | ❌                                                  | ❓                                                       |
| Lookup friendships          | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Lookup statuses             | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Lookup users                | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Get retweeters              | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Get retweets                | ✅                                            | ✅                                                 | ❌                                                  | ❓                                                       |
| Post tweets                 | ✅                                            | ✅                                                 | ❌                                                  | ❌                                                       |
| Post favorite               | ✅                                            | ❌                                                 | ❌                                                  | ❌                                                       |
| Post follow                 | ✅                                            | ❌                                                 | ❌                                                  | ❌                                                       |
| Post messsage               | ✅                                            | ✅                                                 | ❌                                                  | ❌                                                       |
| Post mute                   | ✅                                            | ❌                                                 | ❌                                                  | ❌                                                       |
| Premium 30 day              | ✅                                            | ❌                                                 | ❌                                                  | ❌                                                       |
| Premium full archive        | ✅                                            | ❌                                                 | ❌                                                  | ❌                                                       |
| Run package tests           | ✅                                            | ❌                                                 | ❌                                                  | ❌                                                       |

## Responsible use

**{{rtweet}}** should be used in strict accordance with Twitter’s
[developer
terms](https://developer.twitter.com/en/developer-terms/more-on-restricted-use-cases).

## Installation

To get the current released version from CRAN:

``` r
## install rtweet from CRAN
install.packages("rtweet")

## load rtweet package
library(rtweet)
```

To get the current development version from Github:

``` r
## install remotes package if it's not already
if (!requireNamespace("remotes", quietly = TRUE)) {
  install.packages("remotes")
}

## install dev version of rtweet from github
remotes::install_github("ropensci/rtweet")

## load rtweet package
library(rtweet)
```

## Usage

All you need is a **Twitter account** (user name and password) and you
can be up in running in minutes\!

Simply send a request to Twitter’s API (with a function like
`search_tweets()`, `get_timeline()`, `get_followers()`,
`get_favorites()`, etc.) during an interactive session of R, authorize
the embedded **`rstats2twitter`** app (approve the browser popup), and
your token will be created and saved/stored (for future sessions) for
you\!

[![ropensci\_footer](https://ropensci.org/public_images/ropensci_footer.png)](https://ropensci.org)
