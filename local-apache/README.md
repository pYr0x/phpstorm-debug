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

* Wird für das Projekt ein eigener VHost `C:\wamp64\bin\apache\apache2.4.23\conf\extra\httpd-vhosts.conf` und eine Umleitung in `C:\Windows\System32\drivers\etc\hosts` angelegt:
![V-Host][vhost]


* Wird kein VHost angelegt und das Projekt direkt unter dem Pfad betrieben, dann nur ein `localhost` angeben
![webserver][localhost]
Beim debuggen wird dann gefragt welches Projekt bei einer XDebug Anfrage debuggt werde soll
![incomming][incomming]
Soll dieses Fenster nicht mehr erscheinen, so muss der "Listener" in dem jeweiligen Projekten gestoppt werden 


[cli-i]: images/CLI-Interpreters.png "local cli interpreter"
[vhost]: images/Servers-vhost.png
[localhost]: images/Servers.png
[incomming]: images/incoming-connection-from-xdebug.png