---
language: English
currentMenu: theme
subTitle: Create new theme
---

# Creating a New Theme:

Themes are created using the [Twig](http://twig.sensiolabs.org/) template engine. Files are located in two different places depending on whether you're using *v1* or *v2* :

* With *v1*, you can find themes in the `themes/` folder.
* Starting from *v2*, you'll need to go to the `src/Wallabag/CoreBundle/Resources/views/themes/` folder to find the template files. These are grouped by category.

Assets (```imgs```, ```js```, ```css```, ```fonts```) can be found in the `public/` sub-folder.

All template files extend an unique file named `layout.html.twig`.
