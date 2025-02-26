---
layout: page
title: Plex Trakt Scrobbler
nav_order: 4
parent: How-To
---

# Plex Trakt Scrobbler
{: .d-inline-block }
Supporter
{: .label .label-yellow }
The Plex Trakt Scrobbler uses [Plex Pass](https://www.plex.tv/plex-pass/) webhooks to automatically scrobble what you’re watching, rating, and collecting from Plex to Trakt. Once set up, everything runs automatically in the background.

# What is scrobbling?
Scrobbling simply means automatically tracking what you’re watching. Instead of checking in from your phone of the website, this plugin runs in the background and automatically scrobbles back to Trakt while you enjoy watching your media.

# How to enable the Plex Trakt Scrobbler

Go to [Preferences](https://mdblist.com/preferences/) page, generate and copy Webhook URL.

![](/assets/images/plex_scrobbler.png)

Sign in to your Plex Media Server and go to the Webhooks settings. Click **Add Webhook**, paste in the URL, and click **Save Changes**.
![](/assets/images/plex_webhook.png)

Still in your Plex Media Server settings, we need to make sure a few notification options are enabled.

Go to **General**, and make sure **Push Notifications** are enabled.
![](/assets/images/plex_push.jpg)

Go to **Network**, and make sure **Webhooks** are enabled.
![](/assets/images/plex_webhooks.jpg)

Note: Plex Pass webhooks only allow you to get new data from Plex, its not possible to send any data to Plex or sync your past history.