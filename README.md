# Cheatsheet for PHPStorm 

## PHPStorm Tools
- [Xdebug & Zend Debugger bookmarklets generator for PhpStorm](https://www.jetbrains.com/phpstorm/marklets/)
- [Browser Debugging Extensions](https://confluence.jetbrains.com/display/PhpStorm/Browser+Debugging+Extensions]) z.B. [Xdebug Helper - Chrome Extension](https://chrome.google.com/extensions/detail/eadndfjplgieldjbigjakmdgkmoaaaoc)
- [Chrome Extension](https://chrome.google.com/webstore/detail/jetbrains-ide-support/hmhgeddbohgjknpmjagkdomcpobmllji) für Javascript-Debugging

## Verschiedene Dokumentationen
- [Debugging with PhpStorm](https://confluence.jetbrains.com/display/PhpStorm/Debugging+with+PhpStorm)
- [Debugging with PhpStorm: Ultimate Guide](https://www.jetbrains.com/help/phpstorm/debugging-with-phpstorm-ultimate-guide.html)


## PHPDebugging
Eine kurze Übersicht über die Einstellungen für PHP-Debugging
![PHP Debug Konfiguration][php-debug]
- `Max. simultaneous connections`: Wenn mehrere Projekte gleichzeitig offen sind, dann kann hier die Anzahl erhöhrt werden und jedes Projekt kann debuggt werden ohne das es das andere blockiert.
- `Xdebug`: Der Port 9000 ist Standard. Kann aber mit `xdebug.remote_port` in der `php.ini` geändert werden. Oder aber auch über die `XDEBUG_CONFIG` > `XDEBUG_CONFIG=remote_host=192.168.99.1 remote_port=9001 remote_connect_back=0 idekey=PHPSTORM`



[php-debug]: local-apache/images/Debug-Config.png "PHP Debug Konfiguration"
