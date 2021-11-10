---
layout: default
title: New Movies to Discord using Zapier
parent: RSS Feed
nav_order: 1
---

# Discords integration with Zapier
{: .d-inline-block }
Supporter
{: .label .label-yellow }

Here is an automation example on how to get new Movies added to the list automatically generate a post on Discord.


## Getting list RSS URL

From your list view [My Lists](https://mdblist.com/mylists/) click on RSS icon (Copy RSS URL).

## Zapier integration

- Click "Create Zap"  
- Search for RSS and select “RSS by Zapier”
- For “Trigger event” select “New Item in Feed” and click Continue.
- Enter Feed URL and click Continue. 
![Zapier step 1](/assets/images/rss_zapier_rss.png)
- Click “Test Trigger”. You will see some RSS data parsed by Zapier, click Continue.

- For Action search and select Discord.
- Choose “Send Channel Message” as Action Event and click Continue.
- Select your Discord account or add a new one, click Continue.
- On the next step, Select a Channel, fill message text as in the screenshot example below and click Continue to Test your created action. 
![My helpful screenshot](/assets/images/rss_zapier_discord.png)

Final result
![My helpful screenshot](/assets/images/rss_discord.jpg)
