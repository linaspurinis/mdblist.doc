---
layout: page
title: API
#permalink: /api/
---

# API

API service allows you to access information about ratings, votes, streaming services and more

## Obtaining API Key

Generate your API key in [MDBList](https://mdblist.com) Preferences 

## Usage

Send your requests with GET to:

```
https://mdblist.com/api/?apikey=[yourkey]&
```

## Parameters


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

## Example

Get information about specific movie:

```
https://mdblist.com/api/?apikey=[yourkey]&i=tt0073195
```

Search for a movie or show:

```
https://mdblist.com/api/?apikey=[yourkey]&s=jaws
```
