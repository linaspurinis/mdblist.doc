---
layout: default
title: Kometa
parent: Third-party support
nav_order: 2
---
<img src="/assets/images/kometa.webp" alt="Kometa integration" width="400"/>

# Kometa

Kometa (formerly known as Plex Meta Manager) is a powerful tool designed to give you complete control over your media libraries. With Kometa, you can take your customization to the next level, with granular control over metadata, collections, overlays, and much more.

## Kometa integration

```
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

```
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