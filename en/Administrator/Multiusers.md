---
language: English
currentMenu: multiusers
subTitle: Multi users
---

# Multi-Users

## Creating a new account:

### Administrator mode:

If you want to share Wallabag with several people, you can create new accounts from the configuration page.

At the bottom of this page there is a form where you can input a username and password.

It is now possible to login to this account from the login page of Wallabag.

No information is shared amongst the accounts.

### Open registration mode:

Starting from version 1.9, the administrator can let users register by themselves. This is done by changing the following lines in the configuration file:

    // registration
    @define ('ALLOW_REGISTER', FALSE);
    @define ('SEND_CONFIRMATION_EMAIL', FALSE);

A user is then able to enter their username and password to create their own account. Depending on the configuration, a confimation email will be sent to users who give an email address.

## Removing an account:

It is possible to remove your own account from the configuration page. You simply have to enter your password and ask for its removal.

Of course, when there is only one account, it is impossible to remove it.
