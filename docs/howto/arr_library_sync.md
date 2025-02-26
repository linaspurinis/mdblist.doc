---
layout: page  
title: Radarr Sonarr Library Sync  
nav_order: 5  
parent: How-To  
---

# Radarr/Sonarr Library Sync

## Full Library Sync (Requires Local Client)

To perform a full library sync, you'll need a local client set up. Here are two options:

### MDBListarr
- **Description**: A tool to sync your movie and show libraries with Radarr and Sonarr.  
- **Docker**: Create a Docker container using the image below:  
  - Docker Hub: [https://hub.docker.com/r/linaspurinis/mdblistarr](https://hub.docker.com/r/linaspurinis/mdblistarr)  
  - GitHub: [https://github.com/linaspurinis/mdblistarr](https://github.com/linaspurinis/mdblistarr)  

### Notifiarr
- **Description**: Another option for syncing and managing notifications with Radarr/Sonarr.  
- **GitHub**: [https://github.com/Notifiarr/notifiarr](https://github.com/Notifiarr/notifiarr)  

Once your local client is configured, you can add movies to Radarr and shows to Sonarr directly from MDBList.  
![MDBList Integration](/assets/images/mdblist-integration.png "Integration"){:width="600px"}

## Sync Only Changes

To sync library changes, follow these steps:

1. **Radarr Configuration**:  
   - Navigate to **Settings > Connect** in Radarr.  
   - Set up a webhook (see image below).  
   ![Radarr Webhook](/assets/images/radarr-webhook.png "Radarr Webhook"){:width="600px"}

2. **Get Webhook URL**:  
   - Visit the [Preferences](https://mdblist.com/preferences/) page on MDBList.  
   - Copy the **Webhook URL** provided there.  
   ![MDBList Webhook](/assets/images/mdblist-webhook.png "Radarr/Sonarr Webhook"){:width="600px"}

3. **Filter Using Your Library**:  
   - With the webhook set up, you can now filter content using your library on MDBList.  
   ![MDBList Library Filter](/assets/images/mdblist-library.png "Filter"){:width="600px"}