---
layout: page
title: MDBList API
permalink: /api/
---

# API service allows you to access information about ratings, votes, streaming services and more

### Obtaining API Key

Generate your API key in [MDBList](https://mdblist.com) Preferences 

### Usage

Send your requests with GET to:

```
https://mdblist.com/api/?apikey=[yourkey]&
```

### Parameters


| Parameter       | Description               | Options           | Default Value  |
|-----------------|:--------------------------|:------------------|:---------------|
| i               | A valid IMDb ID           |                   |                |
| t               | A valid Trakt ID          |                   |                |
|-----------------+---------------------------+-------------------+----------------|
| tm              | A valid TMDb ID           |                   |                |
| m               | Media type                | movie, show       | movie          |
|-----------------+---------------------------+-------------------+----------------|
| s               | Title to search for       | Any string        |                |
| y               | Year to limit title search| Valid year YYYY   |                |
{: .custom-class #custom-id}

### Example

Get information about specific movie:

```
https://mdblist.com/api/?apikey=[yourkey]&i=tt0073195
```

Search for a movie or show:

```
https://mdblist.com/api/?apikey=[yourkey]&s=jaws
```
