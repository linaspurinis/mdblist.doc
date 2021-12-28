---
layout: page
title: Version History
nav_order: 2
---

# Version History

### 2020-12
- 28 - [Steven Lu Popular movies](https://github.com/sjlu/popular-movies) supported as [#externallists](external_lists)
- 16 - Static Lists - you can create a Static List and handpick movies and tv shows. Later you can use this static list as inclusion or exclusion filter.
- 14 - Support for nzbgeek.info RSS Feed added [#externallists](external_lists)
- 13 - Search Form Reset ratings icon added. You can reset ratings to default values with a single click.
- 12 - New feature - [**Import from Names**](import_from_names) is now available.
- 01 - Added watch provider icon for list view (You can turn off this feature in preferences). Only first (by priority) icon is displayed. Will use your Watch provider country selected in preferences.
- 01 - Added "Clone as Show Filter" for Movie lists and vice versa. You can save time by simply cloning your search.

### 2020-11
- 21 - Keywords pool has expanded to include additional keywords from IMDb https://www.imdb.com/title/{imdbid}/keywords.
- 21 - The tag icon <img src="/assets/images/icon_tag.png" alt="drawing" width="16"/> has been added to the list view. You no longer need to go into Movie/Show page to see if the item belong to a list.
- 15 - On the Movie/Show page, the yellow tag icon <img src="/assets/images/icon_tag.png" alt="drawing" width="16"/> will display Lists this movie/show belongs to.
- 14 - Support for external list Letterboxd *watchlist* and *watched* added [#externallists](external_lists)
- 07 - `dolby-vision-cp` data added from imdb.com "Technical Specifications" > "Cinematographic Process" for Movies with Dolby Vision
- 06 - `dolby-vision` data source is now https://www.blu-ray.com
- 06 - `dolby-atmos` data added from imdb.com "Technical Specifications" > "Sound Mix"
- 03 - Added option to randomly sort list on Trakt.tv.
- 03 - Using mdblist lists directly with Radarr, marks owners list active and prevents it's (free) account for being expired. [How to use mdblist.com lists directly with radarr](mdblist_to_radarr).
- 03 - Budget and Revenue filters added for Movies

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
- 07 - RSS Feeds for IFTTT. Lists now support RSS URLs for use with IFTTT or RSS readers. RSS will list the latest ~~200~~ 400 items added to your list and update on every list refresh
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
