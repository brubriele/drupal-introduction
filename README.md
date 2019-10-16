# Drupal Introduction
A simple introduction to Drupal 8.

## Development environment:
First you need to install:

* [Visual Studio 2012 VC 11 x64][vcredist]
* [WampServer 3 x64][wampserver3]
* [Composer][composer]

## Configuring environment:

Add the PHP and MySQL paths on the environment variables like as:

![Environment variables](https://i.imgur.com/zPKJvNm.png)

At the terminal check if everything is ok:

![PHP](https://i.imgur.com/Rvq81Y1.png)

![MySQL](https://i.imgur.com/Edj9M60.png)

Enable this module/extension and restart the WampServer:

* modrewrite (Apache)
* OPcache (PHP).

VirtualHost configuration example:
```
<VirtualHost *:80>
  ServerName drupal.local
  ServerAlias drupal.local
  DocumentRoot "${INSTALL_DIR}/www/drupal"
  <Directory "${INSTALL_DIR}/www/drupal">
    Options +Indexes +Includes +FollowSymLinks +MultiViews
    AllowOverride All
    Require local
  </Directory>
</VirtualHost>
```

~~Sorry by my english, I'm practicing yet.~~

[vcredist]: <http://www.microsoft.com/en-us/download/details.aspx?id=30679>
[wampserver3]: <https://sourceforge.net/projects/wampserver/files/WampServer%203/WampServer%203.0.0/wampserver3.1.9_x64.exe/download>
[composer]: <https://getcomposer.org/Composer-Setup.exe>
