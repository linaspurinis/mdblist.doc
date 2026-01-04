---
layout: page
title: External Lists
nav_order: 6
#permalink: /external_lists/
---

# External Lists

You can import lists into mdblist.com for external sources. After import, they are available in the Popular lists dropdown and can be used in a search.

## Supported External Lists

### IMDb

Type | URL
--- | ---
IMDb List | https://www.imdb.com/list/**list-id**
IMDb Search | https://www.imdb.com/search/**list-type**?**search-params**
IMDb Chart | https://www.imdb.com/chart/**chart-name**
IMDb Watchlist | https://www.imdb.com/user/**user**/watchlist
IMDb Ratings | https://www.imdb.com/user/**user**/ratings
IMDb Coming Soon | https://www.imdb.com/movies-coming-soon
IMDb Calendar | https://www.imdb.com/calendar

### Trakt

Type | URL
--- | ---
Trakt List | https://trakt.tv/users/**user**/lists/**list-name**
Trakt Official List | https://trakt.tv/lists/official/**list-name**
Trakt Collection | https://trakt.tv/users/**user**/collection
Trakt Favorites | https://trakt.tv/users/**user**/favorites

### Letterboxd

Type | URL
--- | ---
Letterboxd List | https://letterboxd.com/**user**/list/**list-name**
Letterboxd Watchlist | https://letterboxd.com/**user**/watchlist
Letterboxd Watched | https://letterboxd.com/**user**/films

### Rotten Tomatoes

Type | URL
--- | ---
RottenTomatoes Editorial | https://editorial.rottentomatoes.com/guide/**list-name**
RottenTomatoes Top | https://www.rottentomatoes.com/top/bestofrt/**list-name**
RottenTomatoes Browse | https://www.rottentomatoes.com/browse/[**tv_series_browse**, **movies_at_home**, **movies_in_theaters**, **movies_coming_soon**]/**parameters**

### Streaming Services

Type | URL
--- | ---
JustWatch Provider | https://justwatch.com/**country**/provider/**provider-name**
JustWatch Charts | https://justwatch.com/**country**/streaming-charts
Plex Watchlist | https://rss.plex.tv/**{uuid}**
UnoGS (Netflix) | https://unogs.com/search/?**query-params**
Flixpatrol | https://flixpatrol.com/[**popular**, **demographics**, **top10**, **streaming-services**]/**parameters**

### Other Lists

Source | URL
--- | ---
[A Good Movie to Watch](https://agoodmovietowatch.com) | https://agoodmovietowatch.com/**genre**\|**mood**/**list-type**
[BestSimilar](https://bestsimilar.com) | https://bestsimilar.com/tag/**tag-name**
[Steven Lu Popular movies](https://github.com/sjlu/popular-movies) | https://popular-movies-data.stevenlu.com/**list-name**.json
[MUBI](https://mubi.com/lists/) | https://mubi.com/lists/**list-name**
[NZBgeek](https://nzbgeek.info) RSS Feed | https://api.nzbgeek.info/**params**
[omgwtfnzbs](https://omgwtfnzbs.me) RSS Feed | https://rss.omgwtfnzbs.me/**params**
[rlsbb.cc](https://rlsbb.cc) Movies RSS | https://rlsbb.cc/category/movies/**category-name**/feed

*To use your own Trakt Watchlist as a filtering option, enable "Trakt Library Sync" and use "Hide Trakt Library Items" with "In Watchlist" and or "Not in Watchlist" options.*
*List of all Trakt Official lists [https://trakt.tv/search/lists/?types=official](https://trakt.tv/search/lists/?types=official)
Found an interesting list not listed here? Send me an [email](mailto:linas@mdblist.com).

## Prepopulated Popular List

Read more about already prepopulated popular lists: [Popular Lists](popular_lists)
