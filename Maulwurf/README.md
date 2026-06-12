# 🐾 Projekt: Der Maulwurf (Toshiba Satellite C50-B-14E)

**Status:** Hardware-Final / Software: Alpha-Phase (Tüftelmodus)  
**Konzept:** Wall-Mounted Server, WLAN-Brücke und Netzwerk-Stabilisator.

---

## 📖 Die Geschichte: Der Remote-Spezialist

Der Maulwurf kam bereits zwei Monate nach dem "Einhorn" zu mir. Sein großer Auftritt kam erst vier Jahre später in der Logistik: Als dort die Hardware für das Personal knapp wurde, trat ich meinen offiziellen Dienst-Laptop ab und brachte den C50 als mein persönliches Arbeitsgerät mit.

Da die eigentliche Arbeit über **Remote Desktop** lief, spielte die schwache Eigenleistung keine Rolle – der C50 war das perfekte Werkzeug, um unbemerkt und effizient "an der Vordertür" der IT vorbei zu arbeiten.

---

### 🌐 Netzwerk-Infrastruktur & Die eiserne Einweg-Regel
* **Das Münchner Wetterradar-Drama (Die Vorgeschichte):** Das 5-GHz-WLAN verspricht theoretisch stolze 867 Mbits, kapituliert im Münchner Umland jedoch regelmäßig vor der gesetzlichen Lufthoheit des lokalen Wetterradars (DFS-Kanalwechsel). Da zudem eine komplette, leere Etage zwischen dem Dachgeschoss und dem Wohnzimmer unten liegt, stirbt jeder Versuch eines normalen WLAN-Uplinks den sofortigen Funktod.
* **Der Cat-8-Overkill (Die Infrastruktur):** Um dem Funktod zu entgehen, wurde die physische Verbindung gewählt. Das gesamte Haus – vom gigantischen Keller über das Wohnzimmer bis hoch ins Dachgeschoss – ist komplett mit **Cat-8-Kabeln** gepflastert. Braucht man das? Absolut nicht. Wird das jemals ausgelastet? Aktuell ganz und gar nicht. Warum macht man es trotzdem? Reine Langeweile und weil man es eben kann. 
* **Die LAN-Rettung & Das Einweg-Routing:** Auf dieser völlig überqualifizierten High-End-Kabelautobahn darf nun der Maulwurf mit seinem integrierten Fast-Ethernet-Anschluss glänzen und stabile 100 Mbits rennen lassen. Unter XFCE ist das System so abgeriegelt, dass es gar nicht erst versucht, sich in fremde WLAN-Netze einzuwählen. Es nimmt den Saft exklusiv vom Kabel und gibt das Internet per Funk nach oben weiter. Reine, eiserne Einweg-Diktatur.
* **Die Headless-Alibi-Stunde:** Die gesamte Funk-Kabel-Konstruktion ist als autonomer Systemdienst eingerichtet. Sie startet direkt beim Systemboot komplett ohne Benutzeranmeldung. Der Maulwurf arbeitet also schon heimlich im Verborgenen und stellt die Verbindung bereit, noch bevor überhaupt jemand den Desktop zu Gesicht bekommt. Nur fürs Alibi: Ich bin nicht heimlich im Netz! 😉

### 📊 Das Sabotage-Monitoring (Die O2 / Kabel Deutschland Chroniken)
* **Der „weiche“ Kabelbruch (Das Problem):** Die Zuleitung vom Wohnzimmer zum Siedlungsverteiler verläuft durch eine Hauswandhälfte. Irgendwo im Untergrund schlummert ein gemeiner, temperaturabhängiger „weicher“ Kabelbruch. Wird es im Herbst und Winter kalt, zieht sich das Material zusammen und die Verbindung bricht permanent weg.
* **Das Ticket-Schließ-Komplott (Der Feind):** Jedes Mal, wenn ein Support-Ticket beim Anbieter geöffnet wird, scannt dessen System die Leitung. Misst das System in einer Millisekunde zufällig ein Lebenszeichen, wird das Ticket vom Provider vollautomatisch als „gelöst“ geschlossen. 
* **Der 3-Sekunden-Paranoia-Ping (Die Lösung):** Um nicht für eine Leistung zu zahlen, die nur bruchstückhaft ankommt, läuft ein unbestechliches Hintergrundskript. Alle 3 Sekunden wird ein Google-Server angepingt. Jeder einzelne Verbindungsabbruch wird sekundengenau protokolliert. Das ist unser unumstößliches Beweismaterial für den nächsten Support-Krieg.
* **Schonwaschgang für sterbendes Silizium:** Um die betagte Festplatte durch das permanente Loggen im 3-Sekunden-Takt nicht vorzeitig ins Grab zu bringen, werden die Protokolldaten ausschließlich im flüchtigen Arbeitsspeicher (RAM) zwischengespeichert. Erst einmal pro Woche erbarmt sich ein Cronjob und schiebt den Datenberg gesammelt auf die HDD.

### 🔋 Energiemanagement (Die Rache der analogen Steckdose)
* **Verweigerung des Altersstarrsinns:** Eine moderne, intelligente Akku-Schonung (wie das Festlegen von Ladeschwellen bei 80%) wird vom nostalgischen Mainboard mit purem Ignorieren quittiert. Die Firmware kennt nur ein Ziel: Den Akku permanent bis zur absoluten Halskrause (100%) vollzuballern.
* **Das mechanische Workaround:** Da Software versagt, regiert hier nun die eiserne Faust einer externen, automatisierten Zeitschaltuhr. Sie kappt regelmäßig den Strom und zwingt das System zu künstlichen, materialschonenden Entladezyklen. Wenn das Board nicht mitdenkt, muss eben die Steckdose klüger sein.

### 🧮 Stabilitätstest (Cinebench R23 – Ein Trauerspiel in zwei Akten)
* **Das Multi-Core-Spektakel:** Das System absolvierte heldenhaft einen vollen 1-stündigen Dauertest im Cinebench R23 und erreichte stabile **~358 Punkte** im Multi-Core-Szenario. Die thermische Stabilität steht – die Leistung ist zumindest theoretisch anwesend. *(Bitte diesen Wert nicht mit Single-Core-Ergebnissen moderner CPUs verwechseln, sonst fängt der Prozessor an zu weinen!)*
* **Die Single-Core-Fantasie (Rein rechnerische Schätzung):** Ermittelt auf exakt **~170 Punkte**.
* **Ehrlicher Bastler-Disclaimer:** Ein realer Single-Core-Test wurde aus ethischen Gründen und zum Schutz der eigenen mentalen Gesundheit verweigert. Wenn zwei aktive Kerne schon eine Stunde für den Benchmark-Run benötigen, würde ein einzelner Kern knapp zwei Stunden lang an einem einzigen Bild herumklöppeln. Diese digitale Folter und die damit verbundene Lebenszeitverschwendung wird absolut niemandem empfohlen, der im Leben noch andere Hobbys hat. Die mathematische Herleitung (358 Punkte / 2 Kerne = 179 Punkte, abzüglich 9 Punkten Performance-Overhead) muss als rechtliche Absicherung reichen!
