# System-Programmierung
## Hands-on zu Lektion 3
Für Slides und Code Beispiele, siehe [Lektion 3](../../../fhnw-syspr/blob/master/03/README.md)

> *Achtung: Arbeiten Sie nicht direkt auf diesem Repository.*<br/>
> *[Prüfen Sie die vorhandenen Forks, um das Repository für Ihre Klasse zu finden.](../../network/members)*

### a) TLPI Beispiele builden, 15'
* [TLPI](http://www.man7.org/tlpi/) Beispielcode Setup auf dem Raspberry Pi:<pre>
    $ cd ~
    $ wget http://man7.org/tlpi/code/download/tlpi-180725-book.tar.gz
    $ tar xfzmv tlpi-180725-book.tar.gz
    $ cd tlpi-book
    $ sudo apt-get install libcap-dev
    $ sudo apt-get install libacl1-dev
    $ make</pre>

### b) File I/O, 30'
* Schreiben Sie ein Programm *my_cpu_temp.c*, dass die CPU Temperatur in ein File *./temp.txt* schreibt.
* Hinweis für Raspberry Pi, Wert durch 1000 teilen:<pre>
    $ cat -v /sys/class/thermal/thermal_zone0/temp</pre>
* Erweitern Sie das Programm, dass es alle 3 Sekunden einen neuen Messwert anhängt, im [CSV](https://tools.ietf.org/html/rfc4180) Format.
* Hinweis: Die [sleep](http://man7.org/linux/man-pages/man3/sleep.3.html) Funktion ermöglicht Pausen.

### Abgabe (optional)
* Lokale Änderungen [committen und pushen](#git).
* GitHub [Issue erstellen](../../issues/new) mit "Bitte um Review, @tamberg".
* Offene Fragen ausformulieren, was geht nicht, was haben Sie versucht.
* GitHub mailt mir (@tamberg) automatisch, ich versuche in weniger als 24h zu antworten :)

## Tools
### Git
Auf Ihrem Computer
* Zu Beginn jeder Lektion wird ein Hands-on Repository Link freigeschaltet
* Nachdem Sie das "Assessment" annehmen, bekommen Sie per Email ein Repository
* Die REPO_URL enthält Ihren GitHub Account USER_NAME und Ihre Klasse 3ia oder 3ib, z.B.<br/>
            https://github.com/fhnw-syspr-3ia/fhnw-syspr-work-03-tamberg

Auf dem Raspberry Pi
* Repository klonen<pre>
    $ cd ~
    $ git clone REPO_URL</pre>
* Neue Datei kreieren<pre>
    $ git add FILE</pre>
* Änderungen committen<pre>
    $ git commit FILE -m "Fixed all bugs"</pre>
* Änderungen hochladen<pre>
    $ git push</pre>

### Nano
Auf dem Raspberry Pi
* Neue oder bestehende Datei öffnen mit $ nano FILE
* Editieren (Achtung, nano hat kein Undo)
* Speichern mit `CRTL-X` `Y` `RETURN`

### SSH
Auf Ihrem Computer
* Terminal öffnen (Mac) oder `WINDOWS` `R` cmd `RETURN` (Windows)
* SSH Session starten mit<pre>
    $ ssh pi@raspberrypi.local</pre>

## Support
- [FHNW Syspr Slack](https://fhnw-syspr.slack.com/)
