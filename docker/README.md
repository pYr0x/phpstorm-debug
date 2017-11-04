## PHPStorm Hilfe
[Docker Dokumentation](https://www.jetbrains.com/help/phpstorm/docker.html)

## Xdebug Konfiguration
Die Konfiguration von Xdebug auf der Docker Maschine kann unterschiedlich erfolgen.
Entweder:
- in der `php.ini`
- mittels `environment` [Variabel](https://docs.docker.com/compose/environment-variables/) z.B. `XDEBUG_CONFIG=remote_host=192.168.99.1 remote_port=9001 remote_connect_back=0 idekey=PHPSTORM`

## Docker PHP Interpreter konfigurieren
Zuerst muss der Docker-Daemon ohne TLS gestartet werden.

![Windows Docker][win-docker]

Danach muss unter `Settings` > `Build, Execution, Deployment` > `Docker` eine Docker Instanz angelegt werden.

Danach muss unter `Settings` > `Languages & Frameworks` > `PHP` der PHP Interpreter aus dem Docker-Container angelegt werden. Dazu:
1. Docker Container starten `docker-compose up`
2. Danach schauen wie der `Image-ID` lautet auf dem PHP und Xdebug läuft. 
![PHP Docker Image ID][docker-image]
3. `Remote CLI` from Docker hinzufügen.
4. Radio-Button `Docker` auswählen und das Image das bei (2) gefunden wurde, auswählen.
5. `OK` und kurz warten, danach sollte PHP, Xdebug von der Docker Maschine erkannt worden sein.

![CLI][cli]


## Webserver einrichten



[win-docker]: images/Windows-Docker.png "Window Docker"
[docker-image]: images/PHP-Docker-Image.png "PHP Docker Image"
[remote-cli]: images/Configure-Remote-PHP-Interpreter.png "Remote Docker CLI"
[cli]: images/CLI-Interpreters.png "CLI"