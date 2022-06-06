---
layout: page
title: API
nav_order: 17
permalink: /docs/api
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

# API

API service allows you to access information about ratings, votes, streaming services and more

## Obtaining API Key

Generate your API key in [MDBList](https://mdblist.com/preferences) Preferences 

# Endpoints

## Movies API

Movies API service allows you to access information about ratings, votes, streaming services and more

### Usage

Send your requests with GET to:

```
https://mdblist.com/api/?apikey=[yourkey]&
```

### Parameters


| Parameter       | Description               | Options           | Default Value    |
|:----------------|:--------------------------|:------------------|:-----------------|
| i               | A valid IMDb ID           |                   |                  |
| t               | A valid Trakt ID          |                   |                  |
| tm              | A valid TMDb ID           |                   |                  |
| tv              | A valid TVDB ID           |                   | Defaults to show |
| m               | Media type                | movie, show       | movie            |
| s               | Title to search for       | Any string        |                  |
| sc              | Limit results by score    | From 0 to 100     |                  |
| y               | Year to limit title search| Valid year YYYY   |                  |

### Example

Get information about specific movie:

```
https://mdblist.com/api/?apikey=[yourkey]&i=tt0073195
```

Search for a movie or show:

```
https://mdblist.com/api/?apikey=[yourkey]&s=jaws
```

## My Limits
Returns list of User Lists
```yaml
GET https://mdblist.com/api/user/
```
Response
```json
{
    "limits":{
        "supporter":true,
        "rating_ids":100,
        "api_requests":25000,
    }
}
```

## My lists
Returns all lists
```yaml
GET https://mdblist.com/api/lists/user/
```
Response
```json
[
    {
        "id":13,
        "name":"Top Watched Movies of The Week for KiDS",
        "slug":"top-watched-movies-of-the-week-for-kids",
        "items":13,
        "likes":50,
        "private":false,
        "mediatype":"movie",
        "description":"",
    },
    {
        "id":14,
        "name":"Top Watched Movies of The Week / >60",
        "slug":"top-watched-movies-of-the-week",
        "items":72,
        "likes":244,
        "private":false,
        "mediatype":"movie",
        "description":"",
    }
]
```

## User lists

Returns list of User Lists
```yaml
GET https://mdblist.com/api/lists/user/{id}/
id: user id
```
Response
```json
[
    {
        "id":13,
        "name":"Top Watched Movies of The Week for KiDS",
        "slug":"top-watched-movies-of-the-week-for-kids",
        "items":13,
        "likes":50,
        "mediatype":"movie",
        "description":"",
    },
    {
        "id":14,
        "name":"Top Watched Movies of The Week / >60",
        "slug":"top-watched-movies-of-the-week",
        "items":72,
        "likes":244,
        "mediatype":"movie",
        "description":"",
    }
]
```

## List information

Returns information about a list
```yaml
GET https://mdblist.com/api/lists/{id}?apikey={api_key}
id: list id
```
Response
```json
[
    {
        "id":14,
        "name":"Top Watched Movies of The Week / >60",
        "slug":"top-watched-movies-of-the-week",
        "items":72,
        "likes":244,
        "user_id":3,
        "mediatype":"movie",
        "user_name":"linaspurinis",
        "description":"",
    }
]
```

## List items

Returns list items
```yaml
GET https://mdblist.com/api/lists/{id}/items?apikey={api_key}
id: list id
```
Response
```json
[
    {
        "id":496243,
        "rank":1,
        "adult":0,
        "title":"Parasite",
        "imdb_id":"tt6751668",
        "mediatype":"movie",
        "release_year":2019,
    },
    {
        "id":361743,
        "rank":2,
        "adult":0,
        "title":"Top Gun: Maverick",
        "imdb_id":"tt1745960",
        "mediatype":"movie",
        "release_year":2022,
    },
]
```

## TOP lists

Returns top-100 lists by likes
```yaml
GET https://mdblist.com/api/lists/top?apikey={api_key}
```
Response
```json
[
    {
        "id":2194,
        "name":"Latest TV Shows",
        "slug":"latest-tv-shows",
        "items":200,
        "likes":473,
        "user_id":1230,
        "mediatype":"show",
        "user_name":"garycrawfordgc",
        "description":"",
    },
    {
        "id":14,
        "name":"Top Watched Movies of The Week / >60",
        "slug":"top-watched-movies-of-the-week",
        "items":72,
        "likes":244,
        "user_id":3,
        "mediatype":"movie",
        "user_name":"linaspurinis",
        "description":"",
    },
}
```

## Lists search

Search public lists by title
```yaml
GET https://mdblist.com/api/lists/search?s={query}&apikey={api_key}
query: List Title to search
```
Response
```json
[
    {
        "id":14,
        "name":"Top Watched Movies of The Week / >60",
        "slug":"top-watched-movies-of-the-week",
        "items":72,
        "likes":244,
        "user_id":3,
        "mediatype":"movie",
        "user_name":"linaspurinis",
        "description":"",
    },
]
```

## Ratings
Bulk rating request. Provide list if tmdb ids with media_type and return_rating
```yaml
POST https://mdblist.com/api/rating/{media_type}/{return_rating}?apikey={api_key}
media_type: ['movie','show']
return_rating: ['trakt', 'imdb', 'tmdb', 'letterboxd', 'tomatoes', 
                'audience', 'metacritic', 'rogerebert', 'mal']
```
Payload
```json
{"ids": 
    [923, 990, 545611]
}
```
Response
```json
{
    "rating": {"923": 4.0, "990": 4.0, "545611": 4.5}, 
    "rating_type": "letterboxd", 
    "mediatype": "movie"
}
```
