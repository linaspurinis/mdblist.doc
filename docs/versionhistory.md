---
layout: page
title: Version History
nav_order: 1
---

# Version History

### 2020-11
{: .d-inline-block }

Comming soon
{: .label .label-yellow }

- Using mdblist lists directly with Radarr, marks owners list active and prevents it's (free) account for being expired. [How to use mdblist.com lists directly with radarr](mdblist_to_radarr).
- Budget and Revenue filters added for Movies

### 2020-10
- 29 - Telegram Notification can be turned ON or OFF on a list basis. Previously you could turn notification ON or OFF for all lists only. [#supporter](supporter)
- 28 - Added keywords `one-actor`, `two-actors`, `three-actors` for Movies where cast size is one, two or three actors.
- 26 - [Original Language] option has been added for Language dropdown to allow filtering by Original Movie Language (by default, all spoken languages are filtered).
- 25 - **dolby-vision** keyword has been added to filter movies with Dolby Vision. [#keywords](keywords)
- 21 - `fix` Marking as *watched* didn't work for items without correct imdbid.
- 19 - `fix` Trakt library *watched* status incorrectly filtered items with any trakt library status.
- 16 - "Top Rated Movies - 250" list from https://www.imdb.com/chart/top/ added to "Popular Lists"
- 15 - Trakt.tv lists sorting is now back, but only for lists with less than 4000 items
- 15 - Fomantic-UI updated from version 2.8.6 to version 2.8.8
- 15 - RSS Feeds image changed from poster to backdrop, added links to score providers and trailer
- 14 - Keyword added - *has-trailer*
- 07 - RSS Feeds for IFTTT. Lists now support RSS URLs for use with IFTTT or RSS readers. RSS will list the latest 200 items added to your list and update on every list refresh
- 07 - 'England' renamed to 'United Kingdom' according to iso_3166_1 country code

### 2020-09
- 29 - "Save Filter" option is available alongside "Create Trakt List". Your saved filter is available from the Lists menu.
- 27 - You can use mdblist lists directly in Radarr. Instructions avalable [here](mdblist_to_radarr).
- 26 - Ability to rate movies and tv shows without leaving mdblist.com site.
- 24 - "In Theaters" dropdown added to select countries where the movie is in theaters right now.
- 20 - Watch providers replaced the Streaming option. Data is gathered via tmdb API and provided by JustWatch.
- 20 - Your lists are now included in the "Popular lists" section and are available for filtering.
- 06 - Changed inactivity for nonsupporters. After 90 days of inactivity, a list will continue to refresh, but /inactive/ will be added to the list name. Lists will stop refreshing after 120 days of inactivity.
- 01 - Roger Ebert ratings added
- 01 - Share lists directly from mdblist.com even with your rated ratings (from preferences turn on "Show personal Trakt.tv ratings on public list page")

### 2020-08
- 26 - Mixed lists. You can create mixed Trakt lists containing Movies and Shows.
- 24 - Popular lists to exclude. Now you can use popular lists as exclude Filter
- 23 - API options added: tm - a valid TMDb ID, y - year to limit title search (would also include previous and next year movies)
- 20 - Popular movies lists: Top Netflix and Top Disney movies added
- 19 - Added tags anime-dubbed for anime movies
- 18 - Anime provider changed to myanimelist.net
- 10 - Language Filter expanded to include Spoken language data
- 09 - Label for external lists with usage information
