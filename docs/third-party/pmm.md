---
layout: default
title: Plex Media Manager
parent: Third-party support
nav_order: 2
---

# Plex Media Manager

Plex Meta Manager is an open source Python 3 project that has been designed to ease the creation and maintenance of metadata, collections, and playlists within a Plex Media Server. The script is designed to be run continuously and be able to update information based on sources outside your plex environment. Plex Meta Manager supports Movie/TV/Music libraries and Playlists.

## Plex Media Manager integration


```json
libraries:
  Movies:
    operations:
      mass_audience_rating_update: mdb
      mass_content_rating_update: mdb_commonsense
mdblist:
  apikey: *************************
  cache_expiration: 60
  ```
- apikey: mdblist.com API key

```json
collections:
  Best New Movies:
    mdblist_list:
      url: https://mdblist.com/lists/linaspurinis/new-movies
      limit: 100
      sort_by: score
  Most Popular Movies:
          mdblist_list: https://www.mdblist.com/lists/linaspurinis/most-popular-movies-top-20
```

- url: mdblist.com list URL
- limit: limit the number of items
- sort_by: ["score", "released", "imdbrating", "imdbvotes", "imdbpopular", "tmdbpopular", "rogerebert", "budget", "revenue", "added"]