---
language: English
currentMenu: sessions
subTitle: Sessions issues
---


#Session Issues:

If you end up disconnected even while checking the *Stay Signed In* checkbox, you can run the following commands as root (or with sudo):

* 
``` mkdir /var/lib/wallabag-sessions
chown www-data:www-data /var/lib/wallabag-sessions
```
*Note that if the www-data user does not exist you can use:* 
	```chown http:http /var/lib/wallabag-sessions```

* Using Apache add: `php_admin_value session.save_path /var/lib/wallabag-sessions` to your Apache vhost. For example: `wallabag-apache.conf`
Finally, restart apache, for instance like this : ```/etc/init.d/apache2 restart``` 

 If you're using nginx, add `php_admin_value[session.save_path] = /var/lib/wallabag-sessions` in your nginx configuration file.
Then, restart nginx : ```/etc/init.d/nginx restart```

*NOTE : If you're using systemd, you should do `systemctl restart apache2` (or nginx).*
