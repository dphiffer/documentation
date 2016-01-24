---
language: English
currentMenu: site_config
subTitle: Write config files
---

# Write config files

Wallabag can use specific site config files to parse website articles. These files are stored in the [`inc/3rdparty/site_config/standard`](https://github.com/wallabag/wallabag/tree/master/inc/3rdparty/site_config/standard) folder.

The format used for these files is [XPath](http://www.w3.org/TR/xpath20/). Look at some examples in the folder.

## Automatic Config File Generation:

Fivefilters has created a [very useful tool](http://siteconfig.fivefilters.org/) to create config files. Just type in the address of the article to work with, and select the area containing the content wanted.

![siteconfig](https://lut.im/RNaO7gGe/l9vRnO1b)

Confirm this area by trying with other articles.  
Having gotten the right area, click on *Download Full-Text RSS site config* to download the file.

## Manual Config File Generation:

If the Fivefilters tool doesn't work correctly, take a look at the source (Ctrl + U on Firefox and Chromium). Search for your content and get the `class` or the `id` attribute of the area containing what you want.

Once you've gotten the id or class, you can write, for example, one or another of these lines:

```
body: //div[@class='myclass']
body: //div[@id='myid']
```

Then, test the file. If you have received the right content but you want to strip unnecessary parts, do:

```
strip: //div[@class='hidden']
```

You can look at other options for siteconfig files [here](http://help.fivefilters.org/customer/portal/articles/223153-site-patterns).