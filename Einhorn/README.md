🦄 Projekt: Das Einhorn (Toshiba Satellite C660-2N3)
​Status: Aktive Prototyping-Phase (Hardware-Labor-Setup)
Konzept: Experimentelle Workstation & Test-Plattform für Thermal-Grenzwerte.
​📊 Performance-Vergleich (Cinebench R23)
​Original (Intel i5-2450M): ca. 1.4xx Punkte
​Mod (Intel i7-2720QM): 2.238 Punkte
​Erkenntnis: Trotz der boardseitigen 38W-Limitierung wurde die Multi-Core-Leistung fast verdoppelt. Im Alltag (Programmstarts, Multitasking) ist der Performance-Gewinn massiv, da die CPU hier ihre volle Boost-Power ausspielen kann.
​📖 Die Geschichte hinter dem Projekt
​Der Ursprung: Ein wirtschaftlicher Totalschaden
​Das Einhorn kam als defekter Ersatzteilspender zu mir. Gehäusebrüche, kein Display, keine Speichermedien – eigentlich reif für die Tonne. Doch ich entschied mich gegen das Ausschlachten und stellte das Board erst mal in die Ecke.
​Die Rettung: Der Huckepack-Einsatz
​Der Wendepunkt kam, als mein eigentlicher PC plötzlich komplett abgeschmiert ist und ich sofort Ersatz brauchte. Da ich keine Zeit für eine aufwendige Reparatur des Rechners hatte, schnappte ich mir den Toshiba, stellte ihn kurzerhand oben auf das defekte PC-Gehäuse und steckte einfach alle Kabel um. Aus diesem "Huckepack-Provisorium" wurde eine treue Notlösung, die über ein Jahr lang zuverlässig ihren Dienst verrichtete.
​Die Vision: Das experimentelle Board
​Aus diesem verlässlichen Wegbegleiter wurde schließlich mein persönliches Testlabor. Mich hat der Reiz gepackt, ein System zu haben, an dem ich ohne Rücksicht auf Konventionen experimentieren kann. Der Kern des Projekts: "Kann man eine 45W High-End-CPU zwingend in ein 35W-Laptop-Design quetschen?" Das Einhorn beweist: Ja, es geht absolut. Solange man das Lastprofil versteht, liefert die CPU genau dann die nötige Power, wenn sie gebraucht wird, ohne die Hardware zu gefährden.
​🛠️ Technische Modifikationen & Hardware-Hacks
​CPU-Upgrade: Austausch des Dual-Core i5 gegen einen Intel Core i7-2720QM (4 Kerne / 8 Threads).
​Custom Power-Supply: Einbau eines Step-Down-Wandlers (19\text{V} \rightarrow 5\text{V} / 5\text{A}), um die USB-Schiene stabil zu versorgen.
​Konnektivität-Hub: mPCI-e Slot Modifikation für 4x USB 3.0. Ein Port ist fest für einen Gigabit-LAN-Adapter reserviert (Kabel-Verbindung hat Vorrang).
​Aktueller Aufbau: Das System liegt derzeit offen auf einer Erhöhung. Dies schützt die Bauteile und gewährleistet die optimale Höhe für Anschlüsse, solange die BIOS-Eingriffe laufen. Das finale Gehäuse ist bereits in Planung.
​🚧 Roadmap: BIOS-Hacking
​BIOS-Force-Aktivierung: Da kein internes Display verbaut ist, wird das BIOS via Hardware-Programmer (ASProgrammer) so modifiziert, dass das Bildsignal sofort auf die externen Ausgänge (VGA/HDMI) gezwungen wird.
​Power-Table Tuning: Feinjustierung der Power-Limits (PL1/PL2) innerhalb der stabilen 38W-Grenze.
​Hardware-Schutz: Die Beibehaltung des 38W-Limits dient als bewusster Schutz für die VRMs (Spannungswandler).
​⚖️ Fazit des Experiments
​Das Einhorn beweist, dass Hardware flexibler ist als ihre Spezifikationen. Mit technischem Gespür und Mut zum Experiment lässt sich ein "wirtschaftlicher Totalschaden" in eine voll einsatzfähige, individuelle Workstation verwandeln.
