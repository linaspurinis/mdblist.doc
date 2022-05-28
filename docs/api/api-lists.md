---
layout: default
title: Lists
parent: API
nav_order: 2
---

# Lists API

LIsts API service allows you to access lists information

## Obtaining API Key

Generate your API key in [MDBList](https://mdblist.com) Preferences 

## Usage

Send your requests with GET to:

```yaml
GET https://mdblist.com/api/endpoint/?apikey=[yourkey]&
```

## Endpoints

### My lists

Returns all lists
```yaml
GET https://mdblist.com/api/lists/user/
```

### User lists

Returns list of User Lists
```yaml
GET https://mdblist.com/api/lists/user/id/
id: user id
```

### List information

Returns information about a list
```yaml
GET https://mdblist.com/api/lists/id/
id: list id
```

### List items

Returns list items
```yaml
GET https://mdblist.com/api/lists/id/items/
id: list id
```

### TOP lists

Returns top-100 lists by likes
```yaml
GET https://mdblist.com/api/lists/top/
```

### Lists search

Search public lists by title
```yaml
GET https://mdblist.com/api/lists/search/?s=query
s: query, the title to search
```
