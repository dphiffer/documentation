---
language: English
currentMenu: hidden
subTitle: Hidden options
---

# Hidden Options:

## Caution:

**Be careful**, this section is written for advanced users. It will involve modifying an important Wallabag configuration file:
`inc/poche/config.inc.php`. 

It is advised to do a backup of this file before proceeding.

**Any errors that occur during modification of a Wallabag file can result in malfunctions**.

This `config.inc.php` file is created when you install Wallabag.
Install Wallabag, do a backup copy of the file, then open it in your favorite text editor.

In this file, there are some options that are not, as of now, available in the **config** page of Wallabag.

## Modification of Advanced Options:

Options are defined as follows:

	@define ('OPTION_NAME', 'Value');

For each line, you can only modify the `Value` field.

Here is the list of each option you can change:

* `HTTP_PORT` (default: `80`) : The HTTP port of your web server. You may need to change it if your server is behind a proxy. Accepted values: number
* `SSL_PORT` (default: `443`) : The HTTP port of your web server. You may need to change it if your server uses SSLH. Accepted values: number
* `MODE_DEMO` (default : `FALSE)`: Used for setting up a demonstration server. Accepted values: `TRUE` or `FALSE`.
* `DEBUG_POCHE` (default: `FALSE`) : If you encounter some problems with Wallabag, we may ask you to active Debug mode.  Accepted values: `TRUE` or `FALSE`. Check the logs in `cache/log.txt` after activating.
* `ERROR_REPORTING` (default : `E_ALL & ~E_NOTICE`) : Set to `E_ALL` if needed to look for eventual PHP errors.
* `DOWNLOAD_PICTURES` (default: `FALSE`) : Allows Wallabag to fetch images from the articles you save on your server, instead of fetching only the text. We prefer to let you activate this option yourself. Accepted values: `TRUE` or `FALSE`.
* `REGENERATE_PICTURES_QUALITY` (default : `75`) : In order to avoid security problems, pictures are regenerated if you allow the download of pictures. This is the percentage of quality at which they are saved. Increase this number for better quality, lower for better performances.
* `SHARE_TWITTER` (default: `TRUE`) : enables Twitter sharing. Accepted values: `TRUE` or `FALSE`.
* `SHARE_MAIL` (default: `TRUE`) : enables mail sharing. Accepted values: `TRUE` or `FALSE`.
* `SHARE_EVERNOTE`(default : `FALSE`) : enables sharing with your Evernote account. Accepted values: `TRUE` or `FALSE`.
* `SHARE_DIASPORA` (default : `FALSE`) : enables sharing articles on your Diaspora account.
* `DIASPORA_URL` (default : `http://diasporapod.com`) : The URL of your Diaspora* pod
* `CARROT` (default : `FALSE`) : Like Flattr, it's a service to give small amounts of money to a web page. See http://carrot.org/
* `SHARE_SHAARLI` (default: `FALSE`) : enables sharing via your Shaarli installation (Shaarli is an open-source bookmark manager). Accepted values: `TRUE` or `FALSE`.
* `SHAARLI_URL` (default: `'http://myshaarliurl.com'`) : defines your Shaarli installation URL. Accepted values: an URL.
* `FLATTR` (default: `TRUE`) : enables the possibility to Flattr an article ([Flattr is a microdonation platform](http://en.wikipedia.org/wiki/Flattr)). If an article is Flattr-able, an icon will be displayed, allowing you to send a microdonation to the author. Accepted values: `TRUE` or `FALSE`.
* `SHOW_PRINTLINK` (default: `'1'`) : enables the Print button for articles. Accepted values: `'1'` to enable or `'0'` to disable.
* `SHOW_READPERCENT` (default: `'1'`) : enables the reading progress on articles (working on the `default`, `dark`, `dmagenta`, `solarized`, `solarized-dark` themes). Accepted values: `'1'` to enable or `'0'` to disable.
* `PAGINATION` (default: `'12'`) : defines the number of articles that are displayed on a list. Accepted values: number.
