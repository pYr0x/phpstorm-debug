## Lokale Xdebug Konfiguration 
Die lokale Konfiguration in der `php.ini` könnte so aussehen:
```
; XDEBUG Extension
[xdebug]
zend_extension ="c:/wamp64/bin/php/php7.0.10/zend_ext/php_xdebug-2.4.1-7.0-vc14-x86_64.dll"

xdebug.remote_enable = on
xdebug.profiler_enable = off
xdebug.profiler_enable_trigger = Off
xdebug.profiler_output_name = cachegrind.out.%t.%p
xdebug.profiler_output_dir ="c:/wamp64/tmp"
xdebug.show_local_vars=0
```

## Lokaler PHP Interpreter konfigurieren
Unter `Settings` > `Languages & Frameworks` > `PHP` können neue oder alte PHP Interpreter erstellt bzw. bearbeitet werden.
Eine Konfugiration könnte so aussehen:

![cli interpreter][cli-i]

PHPStorm erkennt die Version und Xdebug automatisch.

Wenn der Haken `Visible only for this Project` nicht gesetzt ist, können auch andere Projekte diesen CLI Interpreter nutzen.

## Lokalen Webserver einrichten
Unter `Settings` > `Languages & Frameworks` > `PHP` > `Servers` muss ein Webserver eingerichtet werden.
Eine Konfugiration könnte so aussehen:

![localhost][webserver]

Das `path mapping` folgt dann in [php](php/README.md) oder in [php-rewrite](php-rewrite/README.md)
- `Max. simultaneous connections`: Wenn mehrere Projekte gleichzeitig offen sind, dann kann hier die Anzahl erhöhrt werden und jedes Projekt kann debuggt werden ohne das es das andere blockiert.
- `Xdebug`: Der Port 9000 ist Standard. Kann aber mit `xdebug.remote_port` in der `php.ini` geändert werden. Oder aber auch über die `XDEBUG_CONFIG` > `XDEBUG_CONFIG=remote_host=192.168.99.1 remote_port=9001 remote_connect_back=0 idekey=PHPSTORM`



[cli-i]: images/CLI-Interpreters.png "local cli interpreter"
[webserver]: images/Servers.png.png "local webserver"