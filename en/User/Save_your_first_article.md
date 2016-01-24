---
language: English
currentMenu: save_article
subTitle: Save your first article
---

# Saving Your First Article

Articles in Wallabag can be saved in a variety of ways:

## From the Web Application

Find the **save a link** option in the Wallabag menu and enter the URL of the desired page. Click **Confirm** to store the contents of the article.

By default, only the text is saved. To save images, enable the setting *DOWNLOAD_PICTURES*. Read the chapter on hidden options for more information.

## From the bookmarklet

From [Wikipedia's definition](http://fr.wikipedia.org/wiki/Bookmarklet)

> A bookmarklet is a [bookmark](http://en.wikipedia.org/wiki/Internet_bookmark) stored in a [web browser](http://en.wikipedia.org/wiki/Web_browser) that contains [JavaScript](http://en.wikipedia.org/wiki/JavaScript)commands to extend the browser's functionality.

> Bookmarklets are unobtrusive scripts stored as the URL of a bookmark in a web browser or as a hyperlink on a web page.

> When clicked, a bookmarklet performs some function, one of a wide variety such as a search query or data extraction. Bookmarklets are usually [JavaScript programs](http://en.wikipedia.org/wiki/Computer_program).

This option provides a Bookmarklet in the Bookmarks bar of the user's web browser. Clicking the bookmarklet saves articles to the user's Wallabag account. Follow the steps to set this up:

1. Click **Config** in the Wallabag menu. 
2. Find the bookmarklet option (the `Bag it!` link) and drag & drop it into the web browser bookmarks bar.
3. Search for a website and click the bag it bookmarklet to save the article to the user's Wallabag account.

## From a smartphone

### Above all else

To use a smartphone application, RSS feeds must be enabled from the **Config** menu. Read the chapter on [RSS Feeds](RSS_feed.md) for more information.

### Android

#### Installation and configuration

The Android app can be downloaded from the [Google Play Store](https://play.google.com/store/apps/details?id=fr.gaulupeau.apps.InThePoche) and from [F-droid](https://f-droid.org/app/fr.gaulupeau.apps.InThePoche). The app is identical on either store.

Once installed, start the application by going to the **settings** menu and filling in the **URL (the  complete address of the Wallabag installation or  Framabag account)** and **User ID** fields. If multiple Wallabag accounts exist, The User Account and **Token** will need to be entered. (Enter all token letters as seen in the settings part of Wallabag).

#### Saving of an article

Once set up, articles can be shared from the phone web browser using the **Share** menn. A **Bag it!** entry in the share menu will save the article to Wallabag.

#### Reading

When opening the application, click on Synchronize: recently saved articles will be downloaded to the smartphone. This will allow for offline reading.

At the end of each article, a **Mark as read** button will archive it.

To date, the synchronisation occurs in one direction (from Wallabag to the application), meaning that articles read on the device will not be synchronized to the Wallabag account.

### iOS

#### Installation and configuration

The iOS application can be downloaded from the [AppStore](https://itunes.apple.com/app/id828331015).

Once installed, start the application by going to the **settings** menu and filling in the **URL (the  complete address of the Wallabag installation or  Framabag account)** and **User ID** fields. If multiple Wallabag accounts exist, The User Account and **Token** will need to be entered. (Enter all token letters as seen in the settings part of Wallabag).

#### Usage

If the app is configured correctly, it will automatically download the articles from the user's Wallabag account (use **pull-to-refresh** to trigger this update manually). This will allow for offline reading.

To date, the synchronisation occurs in one direction (from Wallabag to the application), meaning that articles read on the device will not be synchronized to the Wallabag account.

### Saving articles

When browsing a website simply tap the **Share**-button and select **Bag it!** (if the Wallabag icon is not available, click the **more** menu to find it). If everything is set up correctly, the article will be saved (a login process may be required occasionally).

###Windows Phone
####Installation and configuration

The Windows Phone application can be found in the [Windows Store](https://www.microsoft.com/en-us/store/apps/wallabag/9nblggh11646) or directly from the smartphone's Store.

Once installed, the application will show a notification on the first launch, asking for configuration of the Wallabag server. Go to the **Settings** part of the application by pressing the three dots menu at the bottom of the screen, then fill in the **URL (complete address of your wallabag installation or your Framabag account)** and **User ID (in most cases, you'll have to put 1)** fields.

If multiple Wallabag accounts exist, The User Account and **Token** will need to be entered. (Enter all token letters as seen in the settings part of Wallabag).

## From the web browser

### Firefox Classic Add-on

Download the Firefox add-on at [addons.mozilla.org](https://addons.mozilla.org/firefox/addon/wallabag/) and install it like any other Firefox add-on.

In the add-on's settings, fill the complete URL of your installation of wallabag or your Framabag account.

Personalize the Firefox toolbar to add the Wallabag (**W** icon). When saving an article, click on this icon: a new window will open to add the article and will close itself automatically.

### Firefox Social API Service

*Available from wallabag v1.9.1 only*

*You will need an https connection to use this. It's a Firefox [requirement](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Social_API/Manifest#Manifest_Contents), sorry*

With Firefox 29+ versions, your browser comes with an integrated interface to share things to multiple social services directly from your browser. In the Firefox interface, it is shown a paper plane-like icon that you will use to share a page, which means here, save an article.
You can add the service by going into the Config page of wallabag, then click on Mozilla Services Social API Extension. You must also accept to use Firefox Services.

### Chrome

Download the Chrome add-on [on the dedicated website](https://chrome.google.com/webstore/detail/wallabag/bepdcjnnkglfjehplaogpoonpffbdcdj) and install it like any other Chrome add-on.

In the add-on's settings, fill the complete URL of your installation of wallabag or your Framabag account.

During the addon's installation, a new icon appear in Chrome toolbar (a **W** icon). When saving an article, click on this icon: a new window will open to confirm the action.

### Opera

The recent versions of Opera (15+) allow to install add-ons compatible with Chrome.

First, install the add-on named [Download Chrome Extensions](https://addons.opera.com/en/extensions/details/download-chrome-extension-9/) which will allow you to install add-ons from the Chrome Web Store. Then, go [to to Google site](https://chrome.google.com/webstore/detail/wallabag/bepdcjnnkglfjehplaogpoonpffbdcdj) and get the Chrome add-on by clicking on *Add to Opera*. A message will invite you to confirm this action because this add-on is not coming from a certified source. The behavior will be the same as for Chrome (see above).
