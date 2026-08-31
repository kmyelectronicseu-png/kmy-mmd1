# Benutzerhandbuch für den KMY MMD-1 Schaltungsanalysator und Fehlerortungsgerät

Der KMY MMD-1 ist ein professionelles Test- und Fehlerdiagnosegerät, das es ermöglicht, defekte Bauteile auf elektronischen Leiterplatten zu lokalisieren, ohne die Platine unter Spannung zu setzen. Wenn zwei Prüfspitzen mit den Anschlüssen der verdächtigen Komponente in Kontakt gebracht werden, legt das Gerät ein schwaches Testsignal an die Komponente an und stellt die dynamische Beziehung zwischen Spannung und Strom grafisch auf dem Bildschirm dar. Die resultierende charakteristische Kurve wird als der elektrische „Fingerabdruck“ des Bauteils betrachtet. Anhand der Form dieser Kurve kann sofort bestimmt werden, ob es sich bei dem Bauteil um einen Widerstand, einen Kondensator oder eine defekte Diode handelt. Ein Oszilloskop und ein zweikanaliges Voltmeter sind ebenfalls fest in das System integriert.

Das Gerät kann über ein USB-Kabel an einen Windows-PC angeschlossen oder drahtlos betrieben werden. Darüber hinaus ist die Steuerungssoftware vollständig kompatibel mit Smartphones und Tablets unter dem Android-Betriebssystem.

*(Hinweis: Das englische Benutzerhandbuch [user-guide-en.md](user-guide-en.md) ist derzeit veraltet. Bis diese englische Version aktualisiert wird, dienen die technischen Informationen in diesem aktualisierten Handbuch als primäre Referenz.)*

---

## Inhaltsverzeichnis

* **A. Einführung**
  1. [Was leistet dieses Gerät?](#1-was-leistet-dieses-gerat)
  2. [Das Gerät im Überblick](#2-das-gerat-im-uberblick)
  3. [Anforderungen und Vorbereitung](#3-anforderungen-und-vorbereitung)
* **B. Installation und Erstverbindung**
  4. [Softwareinstallation](#4-softwareinstallation)
  5. [Erstverbindung mit dem Gerät](#5-erstverbindung-mit-dem-gerat)
  6. [Die erste Messung](#6-die-erste-messung)
* **C. Kennlinienschreiber (V-I-Analysator)**
  7. [Funktionsprinzip der Kennlinienprüfung](#7-funktionsprinzip-der-kennlinienprufung)
  8. [Grundlegende Messeinstellungen](#8-grundlegende-messeinstellungen)
  9. [Kurveninterpretation: Bauteilsignaturen-Galerie](#9-kurveninterpretation-bauteilsignaturen-galerie)
  10. [Erweiterte Messeinstellungen](#10-erweiterte-messeinstellungen)
  11. [Zwei-Prüfspitzen-Betrieb und Synchronmodus](#11-zwei-prufspitzen-betrieb-und-synchronmodus)
* **D. Vergleichsmodus und Platinentest**
  12. [Vergleichsfunktionen](#12-vergleichsfunktionen)
  13. [Platinenaufzeichnung und Platinentestsystem](#13-platinenaufzeichnung-und-platinentestsystem)
* **E. Weitere Hilfswerkzeuge**
  14. [Oszilloskop-Modus](#14-oszilloskop-modus)
  15. [Multimeter-Modus](#15-multimeter-modus)
* **F. Systemeinstellungen, Kalibrierung und Verbindung**
  16. [Systemeinstellungen](#16-systemeinstellungen)
  17. [Kalibrierungsassistent](#17-kalibrierungsassistent)
  18. [Drahtlose Nutzung und Wi-Fi-Einrichtung](#18-drahtlose-nutzung-und-wi-fi-einrichtung)
  19. [Verwendung auf Mobilgeräten (Smartphone/Tablet)](#19-verwendung-auf-mobilgeraten-smartphonetablet)
  20. [Software-Updates](#20-software-updates)
* **G. Referenzinformationen**
  21. [Technische Grenzwerte und Parameter](#21-technische-grenzwerte-und-parameter)
  22. [Fehlerbehebung und Lösungen](#22-fehlerbehebung-und-losungen)
  23. [Technischer Support und Kontakt](#23-technischer-support-und-kontakt)

---

## Abschnitt A — Einführung

### 1. Was leistet dieses Gerät?

Beim Testen einer defekten elektronischen Leiterplatte ist das direkte Anlegen von Spannung ein weit verbreitetes Verfahren. Dieser Vorgang führt jedoch häufig zu dauerhaften Schäden an anderen intakten Bauteilen auf der Platine. Der KMY MMD-1 wurde speziell entwickelt, um diese Risiken zu eliminieren. Mit dem Gerät kann der Zustand der Komponenten sicher analysiert werden, indem sie einzeln kontaktiert werden, ohne die Platine unter Spannung zu setzen.

Das Gerät führt diese Erkennung mit drei verschiedenen Methoden durch:

* **Kennlinienprüfung (V-I-Analyse):** Legt ein schwaches Testsignal an das Bauteil an, um dessen Strom-Spannungs-Kurve zu ermitteln. In den meisten Fällen erkennt das System den Typ und den Wert des Bauteils automatisch. Jede Bauteilklasse wie Widerstand, Kondensator, Spule, Diode und Zenerdiode zeichnet eine einzigartige Kurve. Diese Kurven können anhand realer Beispiele in Abschnitt 9 untersucht werden.
* **Platinenaufzeichnung und Platinentest:** Diese Methode wurde speziell für Serienfertiger oder technisches Personal entwickelt, das wiederkehrende Arbeiten an demselben Platinenmodell durchführt. Die Testpunkte auf einer freigegebenen Referenzplatine werden einmalig im System aufgezeichnet. Anschließend werden die fehlerverdächtigen Platinen automatisch mit diesen aufgezeichneten Daten verglichen. Das Gerät meldet dem Anwender übersichtlich die von den Referenzwerten abweichenden Punkte.
* **Oszilloskop und Multimeter:** Nach dem Einschalten der Platine können dieselben Prüfspitzen und dieselbe Softwareschnittstelle verwendet werden, um Live-Signale zu überwachen oder präzise Spannungsmessungen durchzuführen.

Zusammenfassend ist der KMY MMD-1 ein professionelles Hilfsgerät für technisches Personal im Bereich Elektronikentwicklung, Fehlerdiagnose und Reparatur sowie für Hersteller, die eine schnelle Validierung in Serienproduktionslinien durchführen möchten.

### 2. Das Gerät im Überblick

Auf der Vorderseite des Geräts befinden sich 4 Anschlüsse für 4-mm-Bananenstecker. Die Anschlüsse ganz links und ganz rechts sind aktive Prüfspitzen (Sonde 1 und Sonde 2). Kennlinienprüfungen, Oszilloskop- und Multimeter-Messungen werden alle über diese beiden aktiven Eingänge durchgeführt. Die beiden mittleren Buchsen sind Masseanschlüsse (GND).

Bei der Messung eines Bauteils muss ein Anschluss des Bauteils mit der aktiven Prüfspitze (Sonde 1 oder Sonde 2) und der andere Anschluss mit der benachbarten GND-Buchse verbunden werden. Beim Testen eines zweipoligen Widerstands oder einer Diode wird beispielsweise ein Pin an die Sonde 1 und der andere Pin an die benachbarte Masseleitung (GND) angeschlossen.

![Geräteübersicht](images/shared/device-overview.svg)


Auf der Rückseite des Geräts befinden sich zwei Anschlüsse:
* **USB-C-Eingang (Rechts):** Ermöglicht die Verbindung mit dem PC und die Datenübertragung. Über diesen Anschluss bezieht das Gerät auch die für den Betrieb erforderliche Energie.
* **Externer Netzeingang (Links):** Reserviert für alternative Stromversorgungsanforderungen.


Es befinden sich keine physischen Tasten oder Benachrichtigungs-LEDs am Gerätegehäuse. Statusinformationen, Verbindung und die aktiven Betriebsmodi des Geräts müssen stets über den Softwarebildschirm am PC oder Mobilgerät überwacht werden.

### 3. Anforderungen und Vorbereitung

Für den Betrieb des Systems sind das KMY MMD-1-Gerät, ein USB-Kabel und ein Computer mit einem 64-Bit-Windows 10- oder Windows 11-Betriebssystem ausreichend. Bei drahtloser Nutzung kann ein Smartphone oder Tablet mit Android 7.0 und höher verwendet werden. Die Installation ist stark vereinfacht und die Software kann unter Windows ohne Administratorrechte installiert werden.

⚠️ **Wichtiger Sicherheitshinweis:** Vor dem Kontaktieren der Platine mit den Prüfspitzen muss absolut sichergestellt sein, dass die zu testende Platine **vollständig stromlos** ist und alle **Kondensatoren darauf vollständig entladen** sind. Während der Kennlinienschreiber aktiv ist, legt er über die Prüfspitzen sein eigenes Testsignal an. Ein unter Spannung stehender Schaltkreis verzerrt dieses Signal und kann sowohl die Platine als auch das KMY MMD-1-Gerät dauerhaft beschädigen.

---

## Abschnitt B — Installation und Erstverbindung

### 4. Softwareinstallation

#### Installationsschritte unter Windows
1. Besuchen Sie die offizielle GitHub-Release-Seite: [https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest](https://github.com/kmyelectronicseu-png/kmy-mmd1/releases/latest)
2. Laden Sie die aktuelle Datei **KMY-MMD-1-Kurulum.exe** herunter und führen Sie sie aus.
3. Zu Beginn der Installation wird ein Sprachauswahlfenster angezeigt. Diese Auswahl betrifft nur die Installationsschritte; die Sprache der Benutzeroberfläche der Anwendung selbst kann jederzeit im Menü „Einstellungen“ geändert werden.
4. Folgen Sie den Schritten im Installationsassistenten. Um Administratorbarrieren im System zu vermeiden, wird das Programm direkt in das Benutzerverzeichnis statt unter „Programme“ installiert (`%LocalAppData%\Programs\KMY MMD-1`). Auf diese Weise wird die Installation auch ohne Administratorrechte auf dem Computer erfolgreich abgeschlossen.

Alle vom Gerät und der Software benötigten Komponenten und Firmware-Versionen sind in dieser einzigen Installationsdatei enthalten; es sind keine zusätzlichen Downloads erforderlich. Die Datei mit der Endung `.imza` auf der Download-Seite dient der Sicherheitsüberprüfung der Installation. Die Anwendung prüft zukünftige Updates automatisch anhand dieser Signaturdatei; es ist kein manueller Eingriff erforderlich.

*Hinweis: Auch wenn die Anwendung vom System deinstalliert wird, bleiben die erstellten Platinenprojekte, Kalibrierungsprofile und exportierten Testberichte sicher im Ordner **Dokumente** gespeichert. Lediglich Benutzereinstellungen wie die Sprachauswahl werden bei der Deinstallation zurückgesetzt.*

#### Installationsschritte unter Android
1. Laden Sie die Datei **KMY-MMD-1-Mobil.apk** von der entsprechenden Release-Seite auf das Mobilgerät herunter und öffnen Sie sie.
2. Das Android-Betriebssystem fordert aufgrund von Sicherheitsprotokollen die Erlaubnis zur Installation aus Quellen außerhalb des offiziellen Stores an. Nachdem die Option „Installation aus dieser Quelle zulassen“ aktiviert wurde, wird die Installation automatisch abgeschlossen.
3. Die mobile Anwendung läuft problemlos auf allen 64-Bit-ARM-Architekturgeräten mit Android 7.0 und höher.

*Wichtiger Hinweis: Die mobile Anwendung kann nur drahtlos über Wi-Fi mit dem Gerät verbunden werden. Eine direkte USB-Verbindung wird auf Mobilgeräten nicht unterstützt. Der einzige praktische Unterschied besteht darin, dass die Geräte-Firmware nicht über das Mobilgerät aktualisiert werden kann. In Bezug auf Mess-, Analyse- und Testfunktionen gibt es keinen funktionellen Unterschied zwischen der mobilen Version und der Desktop-Version. Detaillierte Informationen finden Sie im Abschnitt [Verwendung auf Mobilgeräten](#19-verwendung-auf-mobilgeraten-smartphonetablet).*

### 5. Erstverbindung mit dem Gerät

Führen Sie nach dem Anschließen des USB-Kabels an den Computer die Anwendung **KMY MMD-1** aus. Ihr Gerät wird in der Liste der verfügbaren Geräte oben auf dem Bildschirm angezeigt; klicken Sie auf die Schaltfläche **Verbinden**, um die Verbindung herzustellen.

Um die Messgenauigkeit zu gewährleisten, kalibriert sich das Gerät bei jedem Start automatisch anhand interner Referenzspannungen (Selbstkalibrierung). Dieser Vorgang dauert **ca. 13-15 Sekunden**. Während dieses kritischen Prozesses sind die Steuerelemente der Software vorübergehend gesperrt; der Ausgang kann nicht aktiviert und die Betriebsmodi können nicht ausgewählt werden. Während dieser Zeit muss gewartet werden, bis das Gerät die Vorbereitung abgeschlossen hat. Wenn die Verbindungsstatusanzeige grün leuchtet, ist das Gerät einsatzbereit.

> 🖼️ **[BILD-PLATZHALTER - DIESER BLOCK MUSS NACH DEM HINZUFÜGEN DES BILDES VOLLSTÄNDIG GELÖSCHT WERDEN]**
> **Bildbeschreibung:** Screenshot des Hauptfensters der KMY MMD-1-Software während der Kalibrierungsphase beim Start. Die Verbindungsliste muss oben sichtbar sein und das Gerät als „Kalibrierung...“ oder „Verbindung herstellen...“ anzeigen, wobei alle Steuerelemente mit einer Countdown-Anzeige von 13-15 Sekunden ausgegraut/gesperrt sind.
> **Dateinamenvorschlag:** `software-connection.png`
> **Nutzungshinweis:** Nach dem Platzieren des Bildes an dieser Stelle muss dieses Beschreibungsfeld (Platzhalter) vollständig gelöscht werden.

*Falls direkt nach dem Anschließen des Kabels beim Klicken auf die Schaltfläche „Verbinden“ ein Fehler auftritt, hat die Hardware ihre Startroutine möglicherweise noch nicht abgeschlossen. Es wird empfohlen, den Vorgang nach einigen Sekunden Wartezeit zu wiederholen.*

### 6. Die erste Messung

Um das Gerät zu testen, verwenden Sie einen Standardwiderstand mit bekanntem Wert. Obwohl der Wert nicht kritisch ist, eignet sich jeder Widerstand **zwischen 100 Ω und 10 kΩ** hervorragend für den ersten Test.

1. Verbinden Sie ein Ende des Widerstands mit dem als **Sonde 1** gekennzeichneten aktiven Eingang und das andere Ende mit der benachbarten **GND**-Buchse.
2. Belassen Sie die Parameter im linken Bedienfeld auf ihren Standardwerten. Die Anfangseinstellungen von **Spannung: Niedrig** und **Strombereich: Mittel** reichen aus, um einen Widerstand zu messen.
3. Klicken Sie auf die Schaltfläche **Ausgang: Aus** in der linken unteren Ecke des Bildschirms, um den Status auf **Ausgang: Ein** zu ändern.
4. In der Mitte des Bildschirms erscheint eine schräge, gewinkelte Linie. Diese gerade Linie ist die elektrische „Signatur“ des Widerstands. Der berechnete Wert des Widerstands wird in der Infokarte direkt unter der Grafik angezeigt.
5. Um den Test zu beenden, drücken Sie die Schaltfläche **Ausgang** erneut, um den Ausgang auszuschalten, oder trennen Sie den Widerstand vom Anschluss.

> 🖼️ **[BILD-PLATZHALTER - DIESER BLOCK MUSS NACH DEM HINZUFÜGEN DES BILDES VOLLSTÄNDIG GELÖSCHT WERDEN]**
> **Bildbeschreibung:** Screenshot des ersten Messbildschirms in der Software. Eine perfekte schräge lineare Kurve eines Standardwiderstands muss auf dem Gitter angezeigt werden, und die untere Ergebniskarte muss „WIDERSTAND“ und den berechneten Wert (z. B. 1,0 kΩ) mit hoher Genauigkeit anzeigen.
> **Dateinamenvorschlag:** `first-measurement-resistor.png`
> **Nutzungshinweis:** Nach dem Platzieren des Bildes an dieser Stelle muss dieses Beschreibungsfeld (Platzhalter) vollständig gelöscht werden.

In Abschnitt 9 werden die charakteristischen Signaturen aller anderen Bauteile auf dem Bildschirm im Detail untersucht. Vorerst wurde beobachtet, wie praktisch und schnell das System arbeitet.

---

## Abschnitt C — Kennlinienschreiber (V-I-Analysator)

### 7. Funktionsprinzip der Kennlinienprüfung

![Hauptfenster](images/shared/main-window.png)

In der Softwareschnittstelle befinden sich die Testparameter auf der linken Seite, das Diagrammfenster in der Mitte und die Registerkarten Vergleich, Platinenaufzeichnung und Platinentest am rechten Rand.

Bei der Kennlinienprüfung legt das Gerät eine Wechselspannung (AC) in Form einer Sinuswelle an das gemessene Bauteil an. Während dieser Zeit zeichnet es die den Bauteil durchfließende Stromstärke gleichzeitig im Verhältnis zur angelegten Spannung auf der Grafik auf.

* **Widerstand:** Da sich Strom und Spannung völlig synchron ändern, entsteht eine gerade, gewinkelte Linie auf dem Bildschirm.
* **Kondensator:** Da der Strom seinen Spitzenwert vor der Spannung erreicht, wird eine elliptische Form auf dem Bildschirm gezeichnet.
* **Diode:** Da sie den Strom nur in einer Richtung durchlässt, tritt ein scharfer Knick (Knie) auf dem Bildschirm auf.

Jede Bauteilfamilie zeichnet je nach ihrem physikalischen Aufbau eine einzigartige Grafik. Diese Grafik stellt eine Identitätskarte für dieses Bauteil dar. Das Gerät verfügt über zwei unabhängige Prüfspitzen; diese können je nach Bedarf einzeln oder gleichzeitig (Synchronmodus) verwendet werden (Details finden Sie in Abschnitt 11).

### 8. Grundlegende Messeinstellungen

Der Ansichtsmodus **Einfach** im linken Bedienfeld bietet die drei wichtigsten Grundeinstellungen für Messungen. In diesem Modus werden aus Gründen der Benutzerfreundlichkeit statt komplexer technischer Zahlen klare Pegelbezeichnungen wie **Niedrig, Mittel-1, Mittel-2, Hoch** bevorzugt. Sowohl die Spannungs- als auch die Frequenzparameter nutzen diese vier Stufen.

Die tatsächlichen technischen Werte, die diesen Stufen entsprechen, sind wie folgt:

| Stufenname | Spannung (Spitzenwert) | Frequenz |
| :--- | :---: | :---: |
| **Niedrig** | 2,5 V | 10 Hz |
| **Mittel-1** | 5 V | 50 Hz |
| **Mittel-2** | 10 V | 100 Hz |
| **Hoch** | 15 V | 1000 Hz |

* **Spannung:** Der maximale (Spitzen-)Spannungspegel, der an das Bauteil angelegt wird. Beim Messen eines fehlerverdächtigen Bauteils unbekannten Typs muss immer mit der niedrigsten Stufe begonnen werden. Bleibt die Linie auf dem Bildschirm horizontal und flach, muss der Spannungspegel schrittweise erhöht werden. Halbleiter wie Dioden- und Transistorübergänge benötigen eine bestimmte Schwellenspannung, um in den leitenden Zustand überzugehen; passive Komponenten wie Widerstände und Kondensatoren benötigen einen solchen Schwellenwert nicht.
* **Frequenz:** Der wichtigste Parameter, um frequenzabhängige (reaktive) Bauteile wie Kondensatoren und Spulen von Widerständen zu unterscheiden. Die vom Widerstand gezeichnete gerade Linie wird durch Frequenzänderungen nicht beeinflusst. Andererseits erscheint beispielsweise ein 100-nF-Kondensator bei 10 Hz als dünne und geschlossene Linie, während er sich bei einer Erhöhung der Frequenz auf 1000 Hz zu einer perfekten Ellipse öffnet. Der schnellste Weg, um zu überprüfen, ob es sich um einen Kondensator handelt, besteht darin, die Breite der Ellipse auf dem Bildschirm durch Ändern der Frequenz zu beobachten.
* **Strombereich:** Bestimmt, mit welcher Stromempfindlichkeit das Gerät während der Messung arbeitet.

| Bereich | Idealer Einsatzbereich |
| :--- | :--- |
| **Empfindlich** | Kondensatoren, hochohmige Widerstände und alle empfindlichen Bauteile, die einen sehr geringen Strom aufnehmen. |
| **Mittel** | Ein sicherer Ausgangspunkt für unbekannte Bauteile. |
| **Grob** | Niederohmige Widerstände, leitende Dioden und robuste Teile mit hoher Stromaufnahme. |

*Wenn die oberen Teile der Kurve auf dem Bildschirm abgeflacht (abgeschnitten) erscheinen oder die Software eine Signalbereichswarnung ausgibt, verringern Sie die Prüfspannung oder wechseln Sie in einen höheren (gröberen) Strombereich. Wenn ein empfindliches Bauteil mit sehr geringer Stromaufnahme im Strombereich „Grob“ gemessen wird, kann sich die Kurve auf dem Bildschirm in eine völlig horizontale Linie verwandeln, was fälschlicherweise als Unterbrechung (Open Circuit) interpretiert werden kann. Wiederholen Sie in solchen Zweifelsfällen die Messung, indem Sie den Strombereich auf „Empfindlich“ einstellen.*

### 9. Kurveninterpretation: Bauteilsignaturen-Galerie

Die Ergebniskarte direkt unter dem Grafikbildschirm benennt das vom Gerät erkannte Bauteil, berechnet dessen Wert und liefert eine Konfidenzrate, die angibt, wie sicher diese Erkennung ist. Die 12 unten aufgeführten grundlegenden Bauteilbeispiele wurden im Einklang mit dem realen elektrischen Verhalten ermittelt, und die Bezeichnungen auf der Ergebniskarte entsprechen exakt den Texten, die auf dem Gerätebildschirm angezeigt werden.

⚠️ **Wichtiger Hardware-Hinweis:** Der KMY MMD-1 ist ein zweipoliger (Prüfspitzen) Kennlinienschreiber; daher kann er dreipolige Bauteilklassen wie „MOSFET“ oder „Transistor“ softwareseitig nicht eigenständig identifizieren. Der Anwender muss wissen, welche zwei Anschlüsse der dreipoligen Elemente gemessen werden. Das Gerät interpretiert das elektrische Verhalten zwischen den beiden kontaktierten Anschlüssen. Daher werden die Transistor- und MOSFET-Beispiele im Handbuch basierend auf dem „vom Gerät erkannten Verhalten“ und den tatsächlichen Ergebnistexten auf dem Bildschirm erklärt.

#### Widerstand
Eine gerade, schräge Linie, die den Grafikbildschirm genau in der Mitte kreuzt. Wenn der Widerstandswert sinkt, nimmt die Linie einen Winkel nahe der Vertikalen an; steigt der Widerstand, flacht die Linie horizontal ab. Bei Frequenzänderungen ändert sich der Winkel dieser Linie nie. Dies ist das klarste Merkmal, das den Widerstand von allen anderen Bauteilen unterscheidet.

![Widerstandskurve](images/shared/curve-resistor.png)


#### Kondensator
Bildet eine deutliche Ellipse auf dem Bildschirm. Bei Erhöhung der Frequenz öffnet sich das Innere der Ellipse und wird deutlich sichtbar, während es sich bei Verringerung der Frequenz zu einer dünnen Linie schließt.

![Kondensatorkurve](images/shared/curve-capacitor.png)


#### Spule (Induktivität)
Das genaue Spiegelbild des Kondensators. Sie zeichnet ebenfalls eine Ellipse, aber ihre Reaktion verläuft in die entgegengesetzte Richtung: Bei Erhöhung der Frequenz verengt sich die Ellipse, während sie sich bei Verringerung der Frequenz erweitert.

![Spulenkurve](images/shared/curve-inductor.png)


#### Kondensator + ESR (Äquivalenter Serienwiderstand)
Die charakteristische Ellipse eines Kondensators, die jedoch auf der Grafik leicht nach rechts oder links gekippt ist. Der Serienwiderstand (ESR) verursacht diese Schrägstellung der Ellipse. Der Kapazitätswert des Kondensators und die Parallel-/Serienwiderstandswerte werden separat auf der Ergebniskarte ausgewiesen.

![Kondensator + ESR Kurve](images/shared/curve-capacitor-esr.png)


#### Diode
Bildet in einer Richtung eine flache Linie (Sperrbereich) und in der anderen Richtung eine ausgeprägte Knickform (Leitbereich). Die Position dieses Knickpunkts auf der Spannungsachse ist die Schwellenspannung (Durchlassspannung) der Diode. Während dieser Schwellenwert bei Siliziumdioden bei ca. 0,6 V - 0,7 V liegt, liegt er bei Schottky-Dioden weiter links (bei niedrigerer Spannung) und bei LEDs deutlich weiter rechts (bei höherer Spannung).

![Diodenkurve](images/shared/curve-diode.png)


#### Zenerdiode
Knie-Abbrüche sind in beiden Richtungen des Diagramms zu beobachten. Der Knick auf der rechten Seite zeigt die normale Durchlassschwelle der Diode, der Knick auf der linken Seite die Zener-Durchbruchspannung ($V_z$). Zenerdioden bis 15 V können mit diesem Gerät problemlos analysiert werden; für Zenerdioden mit höherer Spannung reicht die Prüfspannungsgrenze des Geräts nicht aus.

![Zenerkurve](images/shared/curve-zener.png)


#### TVS-Diode (Transientenspannungsableiter)
Eine unidirektionale TVS-Diode weist elektrisch genau die gleichen Eigenschaften wie eine Zenerdiode auf. Das Gerät stuft sie ebenfalls automatisch als **ZENER** ein (es gibt keine separate „TVS“-Kennzeichnung auf der Ergebniskarte). Der symmetrische Durchbruch bidirektionaler TVS-Dioden in beide Richtungen passt nicht perfekt in eine der Standard-Bauteilklassen. Bei der Messung wird sie auf der Karte möglicherweise als **|Z|** oder **Undefiniert** ausgegeben.

![Bidirektionale TVS-Kurve](images/shared/curve-tvs-bidirectional.png)


#### MOSFET — Gate-Source-Anschlüsse
Der Gate-Anschluss von MOSFETs verhält sich wie ein sehr kleiner Kondensator, der vom Gehäuse isoliert ist, sodass praktisch kein Strom durch ihn fließt. Bei Kleinsignal-MOSFETs ist dieser Kapazitätswert so gering (einige Pikofarad), dass der fließende Strom unter der Erkennungsgrenze des Geräts bleibt und die Ergebniskarte **UNTERBRECHUNG** (Open Circuit) anzeigt. Dies ist kein Fehler, sondern der natürliche Zustand des Gates. Bei leistungsstärkeren Leistungs-MOSFETs (mit einer Kapazität von einigen Nanofarad) kann eine dünne **Kondensator**-Ellipse beobachtet werden.

![MOSFET Gate-Source Kurve](images/shared/curve-mosfet-gs.png)


#### MOSFET — Drain-Source-Anschlüsse
Jeder MOSFET verfügt herstellungsbedingt über eine integrierte Inversdiode (Body-Diode). Wenn das Gate unbeschaltet oder mit der Source verbunden ist und Drain-Source kontaktiert wird, fließt der Strom durch diese Body-Diode und nicht durch den Kanal. Das Gerät erkennt sie direkt als Standard-**DIODE**, meist mit einer geringfügig höheren Durchlassspannung ($V_f$) im Vergleich zu Signaldioden.

![MOSFET Drain-Source Kurve](images/shared/curve-mosfet-ds.png)


#### Transistor — Basis-Emitter-Übergang
Der Basis-Emitter-Übergang ist elektrisch eine Diode. Das Gerät gibt auf dem Bildschirm **DIODE** aus, und die Durchlassspannung ($V_f$) wird typischerweise zwischen 0,65 V und 0,70 V gemessen.

![Transistor Basis-Emitter Kurve](images/shared/curve-transistor-be.png)


#### Transistor — Basis-Kollektor-Übergang
Der Basis-Kollektor-Übergang ist ebenfalls eine Diode. Da dieser Übergang jedoch physisch über eine größere Fläche verteilt ist, fällt seine Schwellenspannung in der Regel etwas niedriger aus als die des Basis-Emitter-Übergangs. Auf der Ergebniskarte wird **DIODE** angezeigt.

![Transistor Basis-Kollektor Kurve](images/shared/curve-transistor-bc.png)


#### Transistor — Kollektor-Emitter-Anschlüsse

![Transistor Kollektor-Emitter Kurve](images/shared/curve-transistor-ce.png)
Wird Kollektor-Emitter gemessen, ohne die Basis zu kontaktieren, bleiben beide internen Übergänge gesperrt, und das Gerät erkennt eine **UNTERBRECHUNG** (Open Circuit). Dies ist kein Fehler, sondern der natürliche Zustand des Transistors. Da eine Basissteuerung erforderlich ist, damit der Transistor leitet, wird unter diesen Testbedingungen im Normalfall ein isolierender Zustand erwartet.

*Wichtiger Schaltungshinweis:* Beim Messen eines Bauteils direkt auf einer Platine ohne Auslöten entspricht die beobachtete Kurve nicht der Kurve dieses Bauteils allein; sie ist die Summe der elektrischen Reaktionen aller anderen Pfade und Elemente, die parallel dazu geschaltet sind. Im Zweifelsfall liefert das Ablöten eines einzelnen Pins des Bauteils von der Platine mit einem Lötkolben und das Wiederholen der Messung das zuverlässigste Ergebnis.

### 10. Erweiterte Messeinstellungen

![Erweitertes Panel](images/shared/advanced-panel.png)

Beim Wechsel in die **Erweiterte** Ansicht der Benutzeroberfläche werden die drei Parameter im einfachen Bedienfeld nicht mehr stufenbasiert gesteuert, sondern können über präzise Schieberegler millimetergenau eingestellt werden (Spannung 0,1 - 15 V, Frequenz 1 - 1000 Hz). In diesem Modus stehen zusätzlich folgende erweiterte Funktionen zur Verfügung:

* **Wellenform:** Es können die Wellenformen Sinus, Dreieck, Rechteck, Sägezahn und Gleichspannung (DC) ausgewählt werden. Der Standard für die Kennlinienanalyse ist immer die Sinuswelle. Die Option DC legt eine konstante Gleichspannung an das Bauteil an.
* **Manueller Bias (Offset):** Ermöglicht das Verschieben des Mittelpunkts (Offsets) des Testsignals über oder unter den Nullpegel. Zur Einstellung werden anstelle eines klassischen Scrollbalkens Richtungstasten (Pfeiltasten) verwendet, die bei gedrückter Taste eine kontinuierliche Erhöhung/Verringerung bewirken. Die Schrittweite kann auf 10 mV, 100 mV oder 1 V eingestellt werden, und eine Ein-Klick-Schaltfläche **Zurücksetzen** ist vorhanden. Diese Funktion ist standardmäßig deaktiviert und sollte für fast alle Standardtests deaktiviert bleiben.
* **Strombereich:** Im Gegensatz zum einfachen Modus kann dieser Parameter für Sonde 1 und Sonde 2 völlig unabhängig voneinander eingestellt werden. Wenn zwei Prüfspitzen miteinander verglichen werden sollen, müssen die Strombereiche beider Sonden identisch eingestellt sein; zwei Kurven in unterschiedlichen Bereichen stimmen niemals überein, selbst wenn exakt dieselben Komponenten gemessen werden.

Die meisten Änderungen werden automatisch an das Gerät übertragen, sobald die Interaktion mit den Einstellreglern oder Tasten beendet wird. Die Schaltfläche **Übernehmen** wird verwendet, um das Senden der Einstellungen an die Hardware sofort zu erzwingen, ohne diese automatische Wartezeit abzuwarten.

Am unteren Rand des linken Bedienfelds befinden sich drei intelligente Funktionen, die die Messung erleichtern:

* **Auto-Erkennung:** Wenn diese Option aktiv ist, erkennt das Gerät den Bauteiltyp, sobald er mit der Prüfspitze berührt wird, und wechselt automatisch in die optimale Kombination aus Spannung, Frequenz und Strombereich zur optimalen Darstellung. Um fehlerhafte Übergänge zu vermeiden, ändert das System die Einstellungen erst, wenn dasselbe Ergebnis mindestens dreimal hintereinander bestätigt wurde. Bei unruhiger Handführung springen die Bildschirmeinstellungen somit nicht ständig hin und her.
* **Auto-Optimierung:** Führt bei Betätigung eine einmalige Suche nach den idealen Parametern für das aktuell an der Prüfspitze befindliche Bauteil durch; es wendet die optimalen Einstellungen an, wenn ein sinnvolles Ergebnis gefunden wird, und belässt die Einstellungen andernfalls unverändert.
* **Suchlaufmodus (Sweep):** Durchläuft automatisch Schritt für Schritt einen ausgewählten Bereich für einen der Parameter Spannung, Frequenz oder Strombereich, bis der Suchlauf gestoppt wird; die anderen beiden Parameter bleiben konstant. Wenn die Identität einer Komponente unbekannt ist, stellt der Frequenz-Suchlauf eine hervorragende Methode dar: Ändert sich die Kurve mit der Frequenz, handelt es sich um ein reaktives Bauteil (Kondensator/Spule); bleibt sie unverändert, ist es ein ohmsches Bauteil (Widerstand).

**Registerkarte Sichtbarkeit:**
* **Referenz:** Blendet eine zuvor aufgezeichnete Referenzkurve als Schablone über die aktuelle Live-Messung ein.
* **Ersatzschaltbild:** Zeichnet unter der Ergebniskarte dynamisch das vom Gerät ermittelte vereinfachte Ersatzschaltbild.
* **Einfrieren:** Friert die aktuelle Kurve auf dem Bildschirm zur genaueren Untersuchung ein.

### 11. Zwei-Prüfspitzen-Betrieb und Synchronmodus

Normalerweise treiben die Modi **Sonde 1** und **Sonde 2** jeweils nur eine Prüfspitze gleichzeitig an. Der **Synchronmodus** treibt beide Sonden gleichzeitig aus derselben Signalquelle an. Dies ist der praktische Weg, um zwei Komponenten nebeneinander in einem einzigen Durchlauf zu vergleichen.

Im Synchronmodus überwacht das Gerät kontinuierlich das elektrische Lastgleichgewicht an beiden Prüfspitzen und zeigt gelbe Warnfenster auf dem Bildschirm an, wenn ein Ungleichgewicht festgestellt wird:

* *„Die Lasten an den Prüfspitzen sind sehr unterschiedlich; die Ableseempfindlichkeit kann im Synchronmodus abweichen. Verwenden Sie den Einzelprüfspitzenmodus für präzise Messungen.“*
* *„Anschluss P1 ist offen (schwebend); die Messung an P2 kann während der synchronen Messung um ~1 % abweichen.“* *(Die symmetrische Warnung wird für P1 angezeigt, wenn P2 offen ist.)*

Das Anzeigen dieser Warnungen bedeutet nicht, dass die Messung völlig falsch ist. Es erinnert lediglich daran, dass bei sehr großen Lastunterschieden an den beiden Prüfspitzen die Messung im Synchronmodus systembedingt leicht abweichen kann. Für Vergleiche, die eine millimetergenaue Präzision erfordern, ist der Wechsel in den Einzelprüfspitzenmodus (Sonde 1 oder Sonde 2) die sicherste Methode.

---

## Abschnitt D — Vergleichsmodus und Platinentest

### 12. Vergleichsfunktionen

![Vergleichspanel](images/shared/compare-panel.png)

Die Registerkarte **Vergleich** am rechten Rand öffnet ein praktisches Seitenmenü. Drei Betriebsmodi stehen zur Verfügung:

* **Aus:** Deaktiviert den Vergleichsmodus.
* **Echtzeit ↔ Referenz:** Vergleicht das aktuell von der Prüfspitze berührte aktive Bauteil mit einer zuvor aufgezeichneten Referenzkurve. Durch Klicken auf die Schaltfläche **Referenz erfassen** wird die aktuelle Kurve auf dem Bildschirm als Benchmark gespeichert; sie kann in einer Datei gespeichert und später wieder geladen werden.
* **Sonde 1 ↔ Sonde 2:** Vergleicht die beiden Prüfspitzen direkt miteinander. Eine als gut bekannte Komponente wird als Referenz an eine Sonde angeschlossen, die verdächtige Komponente an die andere. Diese Methode ist wesentlich sicherer, da beide Messungen völlig zeitgleich, bei gleicher Temperatur und unter identischen elektrischen Bedingungen durchgeführt werden.

Die Entscheidung basiert auf einem Prozentsatz der Ähnlichkeit im Verhältnis zu einem vom Anwender definierten Schwellenwert. Liegt die Ähnlichkeit über dem Schwellenwert, wird **ÜBEREINSTIMMUNG** (Grün) angezeigt; andernfalls erscheint **KEINE ÜBEREINSTIMMUNG** (Rot). Der werkseitige Schwellenwert liegt bei 90 %. Die Option **Empfindlichkeit im kritischen Bereich** (Aus, Normal, Hoch) verschärft den Vergleich in den Biege- und Knickbereichen der Kurve, da die wahre elektrische Identität des Bauteils primär dort verborgen liegt.

Wenn keine der beiden Prüfspitzen einen messbaren Strom zieht, gibt das Gerät keine fälschliche Übereinstimmung durch den Vergleich des schwebenden Hintergrundrauschens aus. Stattdessen wird die Meldung **KEINE MESSUNG** ausgegeben. Diese Warnung weist darauf hin, dass entweder kein Kontakt besteht oder der Strombereich für dieses Bauteil zu grob (hoch) gewählt ist.

Durch Aktivieren der Funktion **Akustisches Signal** muss der Bildschirm nicht ständig im Auge behalten werden; das System gibt nur dann ein akustisches Signal ab, wenn sich die Vergleichsentscheidung (Bestanden/Fehlgeschlagen) ändert.

### 13. Platinenaufzeichnung und Platinentestsystem

Dies ist die ideale Methode zum Testen spezifischer Platinenmodelle, die wiederkehrend repariert oder validiert werden sollen: Zeichnen Sie jeden Testpunkt einmal auf und scannen Sie anschließend alle verdächtigen Platinen schnell mit dieser Referenzdatenbank ab.

#### Schritt-für-Schritt-Aufzeichnung einer Platinenreferenz:

![Platinenaufzeichnung-Oberfläche](images/shared/board-record-interface.png)
1. **Projektordner erstellen:** Wählen Sie einen Arbeitsordner. Das Bild der Platine und alle Testpunkte werden in diesem einzigen Ordner gespeichert; der Projektordner kann als Ganzes auf einen anderen Computer kopiert und übertragen werden.
2. **Platinenbild hinzufügen:** Laden Sie eine klare, schattenfreie Fotografie der Platine hoch, die direkt von oben aufgenommen wurde. Eine gleichmäßige Beleuchtung erleichtert das präzise Positionieren der Testpunkte auf dem Bild.
3. **Punkte definieren:** Kontaktieren Sie den Testpunkt auf der physischen Platine mit der Prüfspitze. Klicken Sie gleichzeitig auf diese Stelle auf dem Platinenfoto im Softwarebildschirm. Vergeben Sie einen beschreibenden Namen für den Punkt (es wird empfohlen, die Originalbezeichnungen der Platine zu verwenden: R14, C7, U3-1) und klicken Sie auf **Punkt speichern**.
4. **Reihenfolge anordnen:** Die gespeicherten Punkte können per Drag-and-Drop in die gewünschte Testreihenfolge gebracht werden.

* **Mehrstufige Signatur (Multi-Stage Signature):** Wenn diese Option aktiv ist, wird jeder Testpunkt nicht nur bei einer einzigen Einstellung, sondern bei 3-4 verschiedenen Spannungs- und Frequenzstufen aufgezeichnet. Der Aufzeichnungsprozess dauert geringfügig länger, aber es ist weitaus schwieriger für ein fehlerhaftes Bauteil, einen auf diese Weise aufgezeichneten Punkt unbemerkt zu passieren.

#### Testen einer aufgezeichneten Platine:
Klicken Sie auf die Schaltfläche **Test starten** und steuern Sie die Punkte nacheinander an. Jeder Punkt wird gemessen, mit seiner Referenz verglichen und als bestanden oder fehlgeschlagen markiert. Nicht übereinstimmende Punkte werden auf dem Platinenfoto in **Rot** hervorgehoben. Statt einer unübersichtlichen Textliste erhalten Sie eine visuelle Fehlerkarte. Sie können den Test anhalten, Punkte überspringen und nach Abschluss über die Option **Restliche testen** nur zu den unvollständigen Punkten zurückkehren.

![Platinentest-Oberfläche](images/shared/board-test-interface.png)


* **Auto-Modus:** Wechselt automatisch zum nächsten Punkt, sobald die Messung erfolgreich übereinstimmt. Aktivieren Sie diese Option, wenn Sie sich beim Halten der Prüfspitzen auf die physische Platine statt auf den Bildschirm konzentrieren möchten.
* **Excel-Bericht erstellen:** Nach Abschluss des Tests wird durch Klicken auf diese Schaltfläche ein detaillierter dreiseitiger Excel-Bericht generiert: Punkt-für-Punkt-Details, eine Übersichtstabelle und eine visuelle Bestanden/Fehlgeschlagen-Karte der Platine.

---

## Abschnitt E — Weitere Hilfswerkzeuge

### 14. Oszilloskop-Modus

Beim Wechsel in den Oszilloskop-Modus wird der Signalausgang des Geräts vollständig deaktiviert, und die Prüfspitzen wechseln in einen passiven Hörmodus, um externe Signale zu überwachen. Die Eingangskanäle können Spannungen bis zu **50 V** sicher messen.

🎨 **Wichtiger Hinweis zum Farbschema der Kanäle:** Auf dem Oszilloskopbildschirm wird Kanal 1 in **Gelb** und Kanal 2 in **Cyan** dargestellt. Dieses Farbschema ist das genaue Gegenteil von Sonde 1 (Cyan) und Sonde 2 (Gelb) auf dem Kennlinienschreiber-Bildschirm. Die Farben der beiden Modi sind bewusst unterschiedlich gestaltet, um Verwechslungen zu vermeiden; lassen Sie sich von diesem Farbunterschied beim Wechsel zwischen den Modi nicht irritieren.

Das Gerät tastet aufgrund von Hardwarebeschränkungen immer mit einer festen Rate von **5,5 kS/s** (5500 Abtastungen pro Sekunde) ab. Das Ändern der Zeitbasis (Timebase) im Programm ändert diese Abtastrate nicht; es ändert lediglich das auf dem Bildschirm angezeigte Zeitfenster. Das praktische Ergebnis davon ist, dass der KMY MMD-1 als **Niederfrequenz-Oszilloskop** eingestuft wird. Es eignet sich hervorragend für Netzteil-Restwelligkeit, Motorsteuerungen und Signale unterhalb des Audiobands; oberhalb von 1 kHz wird die Formtreue der Welle jedoch unzuverlässig.

![Oszilloskop-Modus](images/shared/oscilloscope-mode.png)


* **AUTO:** Analysiert das eingehende Signal und stellt Zeitbasis, vertikale Spannungsskalierung und Triggerpegel automatisch für Sie ein. Wird kein aussagekräftiges Signal erkannt, bleiben die vorherigen Einstellungen erhalten.
* **Trigger-Modi:**
  * *Auto:* Aktualisiert den Bildschirm kontinuierlich, auch wenn keine Triggerbedingung erfüllt ist.
  * *Normal:* Aktualisiert den Bildschirm nur, wenn die konfigurierte Triggerbedingung eintritt.
  * *Single:* Erfasst das Signal einmalig, wenn die Triggerbedingung erfüllt ist, und friert den Bildschirm ein.

Die Referenzpegelpfeile und der Triggerpegelpfeil an den Bildschirmrändern können direkt mit der Maus verschoben werden. Dies ist der schnellste Weg, um schnelle Anpassungen vorzunehmen, ohne Werte in Nummernfelder eingeben zu müssen. Die Schaltfläche **Prüfen** ermöglicht es, den Live-Stream anzuhalten und durch die **letzten 20 Sekunden der aufgezeichneten Historie** zu navigieren. Da die Aufzeichnung im Hintergrund fortgesetzt wird, während Sie den Live-Bildschirm betrachten, wird das Ereignis dennoch erfasst, wenn Sie eine plötzliche Schwankung bemerken.

Vier Messungen werden sofort in der unteren Informationsleiste angezeigt: **Vpp** (Spitze-Spitze-Spannung), **Avg** (Mittelwert der Spannung), **Vrms** (Effektivspannung) und **Frequenz**. Die Datenbank enthält insgesamt 11 Messparameter; Sie können dieser Leiste beliebige Parameter hinzufügen oder daraus entfernen.

### 15. Multimeter-Modus

In diesem Modus können beide Prüfspitzen unabhängig voneinander und gleichzeitig Spannung messen. Es gibt keine Tasten zur manuellen Bereichs- oder Funktionsauswahl (AC/DC). Der KMY MMD-1 analysiert das eingehende Signal, um selbstständig zu entscheiden, ob es als Gleichspannung (DC) oder Wechselspannung (AC) gemessen werden soll.

* **REL (Relativmessung):** Nimmt den aktuell gelesenen Wert als Nullreferenz und zeigt nachfolgende Änderungen relativ zu diesem Wert an (+/-).
* **MIN/MAX:** Erfasst den niedrigsten und höchsten gemessenen Spannungswert seit Beginn der Messung und listet sie auf dem Bildschirm auf.
* **HOLD:** Friert den aktuellen Messwert auf dem Bildschirm ein.

Auch in diesem Modus ist der aktive Testsignalausgang vollständig ausgeschaltet. Vergessen Sie nicht, den Kanal der Prüfspitze, die Sie verwenden möchten, geöffnet zu lassen. Wenn die Prüfspitze eines inaktiven Kanals offen in der Luft gelassen wird, entspricht der auf dem Bildschirm angezeigte Wert keiner realen Spannung, sondern elektromagnetischem Rauschen, das über das Kabel eingekoppelt wird.

---

## Abschnitt F — Systemeinstellungen, Kalibrierung und Verbindung

### 16. Systemeinstellungen

![Einstellungen](images/shared/settings-device.png)

Durch Klicken auf das Zahnradsymbol in der oberen Leiste wird das allgemeine Einstellungsfenster geöffnet. Es besteht aus zwei grundlegenden Registerkarten: **Gerät** und **Kalibrierung**. Beide Registerkarten verfügen oben über eine schnelle Sprachauswahloption (Türkisch / Englisch).

#### Inhalt der Registerkarte Gerät:
Dieser Abschnitt enthält die Softwareversion, die eindeutige Gerätenummer, Wi-Fi-Verbindungseinrichtungstools und eine integrierte Schaltfläche **Aktualisieren**. Die Schaltfläche Aktualisieren prüft und aktualisiert sowohl die PC-Software als auch die Geräte-Firmware mit einem einzigen Klick.

Zusätzlich befindet sich unter der Überschrift „Service / Diagnose“ ein Notfallwerkzeug, mit dem das Gerät im Falle eines Problems während eines Firmware-Updates auf eine stabile ältere Firmware-Version zurückgesetzt werden kann. Dies ist kein Bereich, auf den im täglichen Gebrauch zugegriffen werden muss; er ist ausschließlich für technische Support-Szenarien reserviert.

### 17. Kalibrierungsassistent

![Kalibrierung Einstieg](images/shared/calibration-intro.png)

Die Kalibrierungsdaten des KMY MMD-1 werden **direkt im internen nichtflüchtigen Speicher des Geräts (EEPROM/Flash)** gespeichert, nicht auf dem Computer. Die Software liest diese Kalibrierungstabelle bei jedem Start aus dem Gerät selbst aus. Auf diese Weise kann das Gerät unabhängig vom angeschlossenen PC oder Telefon direkt im kalibrierten Zustand verwendet werden, ohne dass der Kalibrierungsprozess wiederholt werden muss.

#### Anforderungen für die Kalibrierung:
* Zwei Standardwiderstände mit bekanntem Wert (Toleranz von 1% oder besser, **zwischen 300 Ω und 1000 Ω**; einer für jede Prüfspitze, beide müssen während des gesamten Kalibrierungsprozesses gleichzeitig angeschlossen bleiben).
* Ein Digitalmultimeter für präzise Messungen.
* Der Kalibrierungsprozess dauert **ca. 15 Minuten** und umfasst 5 grundlegende Phasen.

#### Kalibrierungsschritte im Detail:
1. **Offener Schaltkreis (Ca. 30 Sek.):** Beide Prüfspitzen müssen vollständig schwebend sein und dürfen nichts berühren. In dieser Phase werden die Nullpunkte der Stromkanäle und die Referenzlinie des Oszilloskops kalibriert.
2. **Widerstandsmessung an S1:** *“Schließen Sie einen bekannten Widerstand an BEIDE Prüfspitzen an; in diesem Schritt wird nur Sonde 1 gemessen.”* Beide Widerstände bleiben in ihren Steckplätzen, aber das Gerät analysiert nur den Kanal der Sonde 1. Geben Sie nach Abschluss der Messung den mit Ihrem Multimeter gemessenen **tatsächlichen Widerstandswert** auf dem Bildschirm ein, anstatt sich an den Farbcodes des Bauteils zu orientieren.
3. **Widerstandsmessung an S2:** *“Lassen Sie beide Widerstände ANGESCHLOSSEN.”* Dieselben Widerstände bleiben an Ort und Stelle; dieses Mal wird Sonde 2 gemessen.

Auf die ersten drei Phasen der Kalibrierung folgt ein einziges Bestätigungsfenster: **Speichern und Fortfahren**. Die Speicherung im Flash-Speicher wird an dieser Stelle konsolidiert.

4. **Spannungsmessung (Multimeter):** Trennen Sie die Prüfspitzen von ihren Anschlüssen und lassen Sie sie vollständig frei hängen. Das Gerät erzeugt nacheinander Testspannungen von $-12	ext{ V}$, $-5	ext{ V}$, $+5	ext{ V}$ und $+12	ext{ V}$. Messen Sie auf jeder Stufe die Spannung an der Sonde-1-Klemme physisch mit Ihrem externen Multimeter und geben Sie den gemessenen Wert in die Software ein.
5. **Gleichspannungskalibrierung des Ausgangs (DAC) (Ca. 45 Sek.):** Das Gerät durchläuft automatisch den Bereich von $-15	ext{ V}$ bis $+15	ext{ V}$ in Schritten von 1 V und korrigiert sich selbst basierend auf den im vorherigen Schritt eingegebenen Spannungsmessungen. Unmittelbar danach misst und kompensiert das Gerät bei noch schwebenden Prüfspitzen automatisch die AC-Treiberamplitude und den Mittelpunktoffset. Es ist keine Aktion Ihrerseits erforderlich; der Prozess dauert nur etwas länger.

* **Optionale 6. Phase (Oszilloskop-Kalibrierung):** Am Ende der vorherigen Schritte wird eine optionale Phase zur Feineinstellung der Oszilloskop-Messwerte angeboten. Da das Gerät im Oszilloskop-Modus kein eigenes Signal erzeugen kann, werden Sie aufgefordert, eine externe Spannungs- oder Signalquelle bekannter Genauigkeit zu verwenden. Wenn Sie nicht über eine solche Quelle verfügen, können Sie diesen Schritt sicher überspringen; alle anderen Bereiche außer dem Oszilloskop bleiben vollständig kalibriert.

*Software-Funktionen:* Jeder Bestätigungsbildschirm ermöglicht es Ihnen, die vorherige Phase zu wiederholen, wenn Sie glauben, einen Fehler gemacht zu haben. In den ersten drei Phasen können Sie, wenn bereits eine gültige Kalibrierung auf dem Gerät vorhanden ist, diesen Schritt überspringen und die vorherigen Werte beibehalten. Der Schreibvorgang in den Flash-Speicher des Geräts wird verschoben, bis alle Schritte erfolgreich abgeschlossen sind. Wenn Sie den Assistenten vorzeitig schließen, bleiben die vorherigen Kalibrierungsdaten auf dem Gerät intakt.

*Wie oft sollte kalibriert werden?* Es wird empfohlen, die Kalibrierung zu erneuern, wenn Sie feststellen, dass die Messwerte spürbar von einem zuverlässigen externen Multimeter abweichen oder wenn die Software meldet, dass die Referenzlinie eine Drift aufweist. Andernfalls ist der Zugriff auf das Kalibrierungsmenü unter normalen Betriebsbedingungen nicht erforderlich.

### 18. Drahtlose Nutzung und Wi-Fi-Einrichtung

![Wi-Fi-Einrichtung](images/shared/wifi-setup.png)

Der KMY MMD-1 unterstützt die drahtlose Netzwerkverbindung in zwei verschiedenen Modi:

1. **Stationsmodus (Station):** Wenn in Ihrem Labor oder Ihrer Werkstatt ein Wi-Fi-Netzwerk aktiv ist, verbindet sich das Gerät mit diesem. Auf diese Weise können Ihr Computer oder Ihr Mobiltelefon über das lokale Netzwerk mit dem Gerät kommunizieren.
2. **Access-Point-Modus (AP):** Wenn Sie im Außendienst arbeiten oder in der Umgebung kein Wi-Fi-Netzwerk vorhanden ist, sendet das Gerät sein eigenes drahtloses Signal aus. Sie können Ihren Computer oder Ihr Mobiltelefon direkt mit dem Gerät verbinden.

#### Wi-Fi-Einrichtung über die Anwendung:
Öffnen Sie bei über USB angeschlossenem Gerät das Menü **Einstellungen → Wi-Fi-Einrichtung**, wählen Sie den gewünschten Verbindungsmodus, geben Sie den Netzwerknamen (SSID) und das Passwort ein und senden Sie die Daten an das Gerät.

#### Wi-Fi-Einrichtung über den Browser (Web-Interface):
Trennen Sie das USB-Kabel. Ab Werk sendet der KMY MMD-1 ein ungesichertes drahtloses Netzwerk namens **KMY MMD-1** aus. Wenn Sie Ihr Telefon oder Notebook mit diesem Netzwerk verbinden, öffnet sich die Einrichtungsseite automatisch; andernfalls geben Sie **192.168.4.1** in die Adresszeile Ihres Browsers ein. Erweiterte Netzwerkoptionen wie die Zuweisung einer statischen IP werden ausschließlich über dieses Web-Interface verwaltet.

#### Wenn das Gerät nicht in der Liste angezeigt wird (Manuelle Verbindung):
Wenn Sie sicher sind, dass das Gerät mit dem Netzwerk verbunden ist, es aber nicht in der Softwareliste angezeigt wird, können Sie auf das Symbol **„Geräteadresse manuell eingeben“** neben der Wi-Fi-Auswahl klicken und seine IP-Adresse manuell eingeben. Dies kann erforderlich sein, da die automatische Erkennung auf Broadcast-Paketen basiert, die das Gerät sekündlich aussendet, und einige Router diese Pakete an drahtlose Clients blockieren. Sie können die IP-Adresse in der Liste der verbundenen Clients Ihres Routers oder auf der Web-Einrichtungsseite des Geräts ermitteln. Diese manuelle IP-Option ist ebenfalls im Verbindungsbildschirm der Android-App verfügbar.

*Wichtige Details zur Beachtung:*
* Die KMY MMD-1-Hardware unterstützt jeweils nur eine einzige aktive Verbindung; ein in Verwendung befindliches Gerät wird in der Liste als **BELEGT** angezeigt.
* Die Option **Netzwerkeinstellungen zurücksetzen** setzt die drahtlose Netzwerkkonfiguration jederzeit auf den werkseitigen Standardzustand zurück.

### 19. Verwendung auf Mobilgeräten (Smartphone/Tablet)

Die gleiche unter Windows verwendete Anwendung läuft auch unter Android, ohne Funktionseinschränkungen bei Analyse und Messung. Das Layout wurde für schmale Mobilbildschirme optimiert: Am oberen und unteren Rand des Grafikbereichs befinden sich permanente Steuerleisten.

![Mobile Oberfläche](images/shared/mobile-interface.png)


* **Herunterziehen der oberen Statusleiste:** Durch Herunterstreichen dieser Leiste wird das Statusfeld geöffnet. Es enthält den Verbindungsstatus, Fehlermeldungen oder Sperrgründe (falls vorhanden) sowie drei Schnellbereiche: **Werkzeuge**, **Einstellungen** und **Verbinden/Trennen**. Bei relevanten Warnungen oder Fehlern wird dieses Feld automatisch ausgeklappt.
* **Hochziehen der unteren Steuerleiste:** Durch Hochstreichen dieser Leiste wird das vollständige Steuerfeld geöffnet. Es stoppt auf der Höhe, auf der Sie den Finger vom Bildschirm nehmen, ohne vollständig geöffnet oder geschlossen sein zu müssen. Es enthält exakt die gleichen Einstellungen wie die Desktop-Version. Die Leiste zeigt jederzeit die Direktzugriffe auf Kennlinienprüfung, Oszilloskop und Multimeter sowie Verknüpfungen für Spannung, Frequenz und Strombereich.
* **Zugriff auf Funktionen:** Die Optionen **Vergleich, Platinenaufzeichnung und Platinentest** werden über den Bereich *Werkzeuge* verwaltet. **Allgemeine Einstellungen und Kalibrierung** werden über den Bereich *Einstellungen* verwaltet. Beide Optionen sind identisch mit den Fenstern auf dem Desktop, mit einer für den Mobilbildschirm angepassten Skalierung.
* **Verbindungsfeld:** Der Bereich *Verbinden* bietet die Suchliste der Geräte, eine Backup-Taste zum direkten Verbinden mit dem Netzwerk des Geräts und ein Feld für die manuelle IP-Eingabe.

*Einschränkung bei Firmware-Updates auf Mobilgeräten:* Die Geräte-Firmware kann nicht über Mobilgeräte aktualisiert werden, da der Vorgang das sichere USB-Protokoll erfordert und eine direkte USB-Verbindung auf Mobilgeräten nicht unterstützt wird. Updates der mobilen Anwendung selbst werden jedoch auf dem Telefon installiert: Wenn Sie auf **Aktualisieren** klicken, lädt die Anwendung die neue Version herunter, validiert deren Signatur und öffnet den nativen Android-Installationsbildschirm. Der Vorgang wird mit einer einzigen Bestätigung abgeschlossen, ohne dass ein Webbrowser erforderlich ist.

### 20. Software-Updates

Das Aufrufen von **Einstellungen → Aktualisieren** überprüft sowohl die Anwendungsversion als auch die Geräte-Firmware und installiert die veralteten Elemente. Ihre Kalibrierungsdaten werden dabei nicht verändert.

Zu Beginn der Installation eines Updates wird folgende Meldung auf dem Bildschirm angezeigt: *“Installation wird gestartet, die Anwendung wird nun geschlossen und mit der neuen Version neu gestartet.”* Es ist völlig normal, dass sich das Fenster abrupt schließt und nach einigen Sekunden wieder öffnet; dies ist kein Fehler des Programms.

*Details zu Updates:*
* Anwendungsupdates werden unabhängig davon durchgeführt, ob das Gerät angeschlossen ist oder nicht.
* Die Geräte-Firmware kann nur über eine **physische USB-Verbindung** aktualisiert werden. Ein Update über das Netzwerk oder vom Mobiltelefon aus ist nicht möglich; die Firmware ist im Installationsprogramm der Desktop-Anwendung enthalten.
* Falls keine Internetverbindung besteht, informiert die Update-Prüfung den Anwender; die aktuellen Daten und Einstellungen gehen nicht verloren und werden nicht beschädigt.

---

## Abschnitt G — Referenzinformationen

### 21. Technische Grenzwerte und Parameter

| Parameter | Technischer Grenzwert und Wert |
| :--- | :--- |
| **Prüfspannung** | $\pm 15	ext{ V}$ Spitze |
| **Prüffrequenz** | $1	ext{ Hz} - 1000	ext{ Hz}$ |
| **Eingangsgrenze Oszilloskop / Voltmeter** | Maximal $50	ext{ V}$ |
| **Abtastrate des Oszilloskops** | $5,5	ext{ kS/s}$ (Hardwareseitig fest) |
| **Aufzeichnungstiefe des Oszilloskops** | Letzte $20	ext{ Sekunden}$ kontinuierlich |
| **Stromversorgung** | Über den USB-Anschluss |

* **Grundlegende Sicherheits- und Betriebsregeln:**
  * Testen Sie Platinen immer im stromlosen Zustand und bei vollständig entladenen Kondensatoren.
  * Der KMY MMD-1 erzeugt nur im Modus **Kennlinienprüfung** ein Signal. In den Modi Oszilloskop und Multimeter bleibt der Ausgang deaktiviert und die Prüfspitzen arbeiten ausschließlich im passiven Hörmodus.
  * Die rote **Not-Aus-Taste** unterbricht den Signalausgang sofort. Sie funktioniert jederzeit, solange das Gerät an den Computer angeschlossen ist, auch wenn keine Kalibrierung vorliegt.
  * Der Signalausgang wird erst aktiviert, wenn das Gerät seine Startroutine abgeschlossen und das Vorhandensein einer gültigen Kalibrierung in seinem Speicher verifiziert hat.
  * ⚠️ **Hochspannungswarnung:** Keine der Komponenten dieses Geräts ist für den Betrieb unter Netzspannung ($220	ext{ V AC}$) ausgelegt. Bringen Sie die Prüfspitzen unter keinen Umständen mit Steckdosen oder Hochspannungsleitungen in Kontakt.

### 22. Fehlerbehebung und Lösungen

* **Das Gerät wird nicht in der Liste angezeigt:**
  Überprüfen Sie den Zustand des physischen USB-Kabels und den USB-Anschluss des Computers. Wenn es mit dem lokalen Netzwerk verbunden ist und immer noch nicht angezeigt wird, versuchen Sie die Methode der [manuellen IP-Eingabe](#18-drahtlose-nutzung-und-wi-fi-einrichtung).
* **Die Steuerelemente sind sofort nach dem Verbinden gesperrt:**
  Dieses Verhalten stellt keinen Fehler dar. Das Gerät führt eine interne Kalibrierung durch, um seine Hardware auszubalancieren. Dies dauert etwa 13 bis 15 Sekunden und endet automatisch.
* **Der Ausgang kann nicht aktiviert werden (Ausgang lässt sich nicht einschalten):**
  Das Gerät befindet sich noch im Startvorgang oder verfügt über keine im internen Speicher abgelegte Kalibrierung. Rufen Sie **Einstellungen → Kalibrierung** auf, um den Status zu überprüfen.
* **Die Kurve ist flach und horizontal:**
  Die Prüfspitzen kontaktieren kein Bauteil (offener Schaltkreis) oder die Prüfspannung liegt unter der Durchlassschwelle des Halbleiterbauteils. Erhöhen Sie den Spannungspegel oder wechseln Sie in einen Strombereich mit höherer Empfindlichkeit.
* **Im Synchronmodus wird eine gelbe Warnleiste auf dem Bildschirm angezeigt:**
  Die den Prüfspitzen zugeordneten elektrischen Lasten weichen erheblich voneinander ab oder eine der Sonden ist offen in der Luft. Wechseln Sie für präzise Messungen in den Einzelprüfspitzenmodus (Details in Abschnitt 11).
* **Das Vergleichsfenster zeigt kontinuierlich „KEINE MESSUNG“ an:**
  Keine der Prüfspitzen zieht einen messbaren Strom. Überprüfen Sie den physischen Kontakt der Sonden und wechseln Sie beim Messen hochohmiger Komponenten in den Bereich **Empfindlich**.
* **Das Gerät wird in der Liste als „BELEGT“ angezeigt:**
  Eine andere Verbindung (ein PC oder ein Mobilgerät) verwendet das Gerät aktiv über das lokale Netzwerk. Schließen Sie die Anwendung auf dem anderen Gerät zuerst.
* **Messwerte und Diagramme weisen Abweichungen auf:**
  Schalten Sie das Gerät aus und wieder ein; die Selbstkalibrierung beim Start behebt die meisten Abweichungen. Wenn die Software meldet, dass die Referenzlinie eine Drift aufweist, wiederholen Sie den Kalibrierungsprozess.
* **Die Wellenform wird im Oszilloskop-Modus verzerrt oder unvollständig dargestellt:**
  Überprüfen Sie die Frequenz des zu testenden Signals. Mit einer Abtastrate von 5,5 kS/s können Sie die Wellenform von Signalen oberhalb von 1 kHz nicht zuverlässig darstellen.
* **Die mobile Anwendung findet das Gerät nicht im drahtlosen Netzwerk:**
  Stellen Sie sicher, dass sowohl Ihr Mobiltelefon als auch das Gerät mit demselben Wi-Fi-Netzwerk verbunden sind. Wenn das Gerät sein eigenes Signal sendet (Access-Point-Modus), bestätigen Sie, dass das Mobiltelefon direkt mit dem Netzwerk **KMY MMD-1** verbunden ist.

### 23. Technischer Support und Kontakt

Für alle technischen Fragen, Unterstützungsanfragen oder Support im Zusammenhang mit dem KMY MMD-1 können Sie sich an unsere offizielle GitHub-Seite wenden oder uns per E-Mail kontaktieren:

* **Offizielle GitHub-Seite:** [https://github.com/kmyelectronicseu-png/kmy-mmd1](https://github.com/kmyelectronicseu-png/kmy-mmd1)
* **Direkter E-Mail-Support:** [kmyelectronics.eu@gmail.com](mailto:kmyelectronics.eu@gmail.com)

Um die Unterstützung zu beschleunigen, empfehlen wir Ihnen, die eindeutige Nummer Ihres Geräts zu notieren, bevor Sie sich an das Support-Team wenden. Sie finden Ihre Gerätenummer unter dem Pfad **Einstellungen → Gerät → Gerätenummer** in der Softwareschnittstelle.