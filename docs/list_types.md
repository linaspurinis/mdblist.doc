---
layout: page
title: List Types
nav_order: 4
---

# List Types

MDBList has several list types. The difference is mostly how the list is created and how items are updated.

## Dynamic Lists

Dynamic lists are created from the Search page.

You choose filters such as ratings, genres, years, keywords, streaming services, languages, runtime, certifications, and popular lists. MDBList saves those filters and refreshes the list automatically, so matching movies and shows can be added or removed as the source data changes.

Use dynamic lists when you want rules to decide what belongs on the list.

## AI Generated Lists

AI generated lists are created from an AI prompt.

You provide a prompt, and MDBList generates a movie or TV list from it. The list refreshes automatically from the saved prompt. You can edit the list name, prompt, and related options later from [My Lists](https://mdblist.com/mylists/#ai_lists).

Use AI lists when it is easier to describe the theme in natural language than to build it from filters.

## Static Lists

Static lists are manually curated lists.

You add, remove, and reorder items yourself. Static lists do not change because of Search filters or an AI prompt. You can create an empty static list, create one from an existing list, or append items from another list.

Use static lists when you want full manual control.

## Feed Lists

Feed lists automatically append newly discovered items from another source list during refresh.

A feed list has one source, such as a dynamic list, AI list, or external list. When MDBList refreshes the source, new matching items can be appended to the feed list. Feed lists are useful when you want to keep a running collection of new discoveries instead of replacing the list contents every refresh.

Feed lists are available to supporters.

## Linked Lists

Linked lists are lists from other MDBList users that you have linked to your account.

They appear in your My Lists page for quick access, but the original list still belongs to the other user. If the owner updates the list, you see the owner list's current contents.

Use linked lists when you want to follow or reuse another MDBList user's list without cloning it.

## External Lists

External lists are imported from outside MDBList.

Supported sources include Trakt, IMDb, Letterboxd, Rotten Tomatoes, JustWatch, Plex Watchlist, and other list or RSS sources. After import, the external list can be viewed in MDBList, used as a Search filter source, and used as a feed source. External lists update automatically on the schedule available for your account.

Read more: [External Lists](/docs/external_lists)

## Quick Comparison

Type | Created from | Updates automatically | Best for
--- | --- | --- | ---
Dynamic | Search filters | Yes | Rule-based lists
AI Generated | AI prompt | Yes | Natural-language themes
Static | Manual item selection | No | Hand-picked lists
Feed | Another source list | Yes, appends new source items | Running collections of discoveries
Linked | Another MDBList user's list | Follows the original list | Saving lists from other users
External | Outside sources | Yes | Importing lists from Trakt, IMDb, JustWatch, and similar sources
