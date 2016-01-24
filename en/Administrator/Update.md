---
language: English
currentMenu: upgrade
subTitle: Update wallabag
---

# Updating Wallabag:
## Updating an Existing Wallabag Installation:

 In order to update your installation: 
 
 Download and unzip the archive into your installation folder. For example on Ubuntu/Debian:

    wget http://wllbg.org/latest
    unzip latest
    rsync -ur wallabag-version-number/* /var/www/html/wallabag/
*Note: This could be another location such as ```/srv/html```, ```/usr/share/nginx/html```, etc.*

Then, connect to Wallabag in your browser and follow the instructions to finish the update.

You can verify at the bottom of the configuration page if you're running the latest version.

**If it fails**, delete the `install` folder and clear the cache:

    cd /var/www/html/wallabag/
    rm -r cache/* install/

Clearing the cache is also possible in the configuration page by clicking on the `Delete Cache` link.
