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

## Lists JSON

Every lists can be accessed as JSON, by adding /json after lists URL

```yaml
https://mdblist.com/lists/linaspurinis/top-10-pirated-movies-of-the-week-50/json
```
Response
```json
[
    {
        "id": 693134,
        "rank": 1,
        "adult": 0,
        "title": "Dune: Part Two",
        "tvdbid": 0,
        "imdb_id": "tt15239678",
        "mediatype": "movie",
        "release_year": 2024,
    },
    ...
    {
        "id": 1011985,
        "rank": 8,
        "adult": 0,
        "title": "Kung Fu Panda 4",
        "tvdbid": 0,
        "imdb_id": "tt21692408",
        "mediatype": "movie",
        "release_year": 2024,
    }
]
```

You can also add Genres by using **append_to_response**

```yaml
https://mdblist.com/lists/linaspurinis/top-10-pirated-movies-of-the-week-50/json?append_to_response=genre
```
Response
```json
[
    {
        "id": 693134,
        "rank": 1,
        "adult": 0,
        "genre": [
            "action",
            "science-fiction",
            "adventure",
            "romance",
            "drama",
        ],
        "title": "Dune: Part Two",
        "tvdbid": 0,
        "imdb_id": "tt15239678",
        "mediatype": "movie",
        "release_year": 2024,
    },
        ...
    {
        "id": 1011985,
        "rank": 8,
        "adult": 0,
        "genre": [
            "animation",
            "action",
            "adventure",
            "comedy",
            "family",
            "fantasy",
        ],
        "title": "Kung Fu Panda 4",
        "tvdbid": 0,
        "imdb_id": "tt21692408",
        "mediatype": "movie",
        "release_year": 2024,
    }
]
```


You can also limit the output returned using **limit** and **offset**

```yaml
https://mdblist.com/lists/linaspurinis/top-10-pirated-movies-of-the-week-50/json?limit=5&offset=2
```

## Movies API

Movies API service allows you to access information about ratings, votes, streaming services and more

### Usage

Send your requests with GET to:

```
https://mdblist.com/api/?apikey=[yourkey]&
```

### Parameters

| Parameter       | Description                                          | Options           | Default Value    |
|:----------------|:-----------------------------------------------------|:------------------|:-----------------|
| i               | A valid IMDb ID                                      |                   |                  |
| t               | A valid Trakt ID                                     |                   |                  |
| tm              | A valid TMDb ID                                      |                   |                  |
| tv              | A valid TVDB ID                                      |                   | Defaults to show |
| mal             | A valid MAL ID                                       |                   | Ignores mediatype|
| m               | Media type                                           | movie, show       | movie            |

| Parameter       | Description                                          | Options           | Default Value    |
|:----------------|:-----------------------------------------------------|:------------------|:-----------------|
| s               | Title to search for                                  | Any string        |                  |
| sc              | Limit results by score                               | From 0 to 100     |                  |
| o               | Order results by score                               | match             |                  |
| y               | Year to limit title search                           | Valid year YYYY   |                  |
| l               | Limits results returned                              | From 1 to 100     | 50               |

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
        "language":"en",
        "spoken_language":"en",
    },
    {
        "id":361743,
        "rank":2,
        "adult":0,
        "title":"Top Gun: Maverick",
        "imdb_id":"tt1745960",
        "mediatype":"movie",
        "release_year":2022,
        "language":"en",
        "spoken_language":"en",
    },
]
```

You can also limit the output returned using **limit** and **offset**

```yaml
GET https://mdblist.com/api/lists/{id}/items?apikey={api_key}&limit=5&offset=2
```


## Add Items to Static List
{: .d-inline-block }
Supporter
{: .label .label-yellow }

Add one or more items to a static list. Items can be movies or shows, no more, than 10 movies and 10 shows per request.
```yaml
POST https://mdblist.com/api/lists/{listid}/items/add?apikey={api_key}
```
Payload
```json
{
 "movies": [
    {
     "tmdb": 630,
     "imdb": "tt0032138"
    },
    {
     "tmdb": 238
    }     
 ],
 "shows": [
    {
     "imdb": "tt0417299"
    },
    {
     "tmdb": 1396
    }
   ]
}
You can provide following ID's: ['tmdb','imdb','trakt','tvdb']
```
Response
```json
{
    "response": true,
    "added": {
        "movies": 0,
        "shows": 0
    },
    "existing": {
        "movies": 1,
        "shows": 2
    },
    "not_found": {
        "movies": 1,
        "shows": 0
    }
}
```


## Remove Items from Static List
{: .d-inline-block }
Supporter
{: .label .label-yellow }

Remove one or more items from a static list. Items can be movies or shows, no more, than 10 movies and 10 shows per request.
```yaml
POST https://mdblist.com/api/lists/{listid}/items/remove?apikey={api_key}
```
Payload
```json
{
 "movies": [
    {
     "tmdb": 630,
     "imdb": "tt0032138"
    },
    {
     "tmdb": 238
    }     
 ],
 "shows": [
    {
     "imdb": "tt0417299"
    },
    {
     "tmdb": 1396
    }
   ]
}
You can provide following ID's: ['tmdb','imdb','trakt','tvdb']
```
Response
```json
{
    "response": true,
    "deleted": {
        "movies": 2,
        "shows": 2
    },
    "not_found": {
        "movies": 1,
        "shows": 0
    }
}
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
                'audience', 'metacritic', 'rogerebert', 'mal', 'score', 'score_average']
```
Payload
```json
{
    "ids": 
        [923, 990, 545611],
    "provider": "tmdb"
}
ids: List of mediatype IDs by type {provider}
provider: ['tmdb','imdb']
```
Response
```json
{
    "rating": {"923": 4.0, "990": 4.0, "545611": 4.5}, 
    "rating_type": "letterboxd", 
    "mediatype": "movie",
    "provider": "tmdb"
}
```
