Ich habe das Spiel mit einem generierten Prompt aus und mit deepseek generiert:

Rolle: Erstelle eine einzelne HTML-Datei mit eingebettetem CSS und JavaScript für ein Lernspiel für Kleinkinder (3–5 Jahre). Kein Build-Tool, keine Frameworks außer Bootstrap 5 (per CDN). Die Datei muss direkt im Browser auf einem Tablet lauffähig sein.

Spielkonzept:
Ein Buchstabe wird groß in der Mitte des Bildschirms angezeigt. Darunter erscheinen mehrere Buchstaben-Buttons zur Auswahl. Das Kind muss den Button antippen, der dem groß dargestellten Buchstaben entspricht.

Zielgruppe: Kinder von 3 bis 5 Jahren, gespielt auf einem Tablet (Touch). Große Tap-Flächen, klare Kontraste, keine Texte, die gelesen werden müssen (außer optional kleine Labels im Einstellungsmenü für Erwachsene).

Bildschirme:

1. Start-/Einstellungsbildschirm
Vor Spielbeginn erscheint ein Einstellungsmenü mit drei Einstellungen. Jede Einstellung wird durch eine Reihe von Sternen dargestellt (1–5 bzw. 1–3 bzw. 1–4 Sterne). Mehr Sterne = schwieriger. Das Antippen eines Sterns setzt den Wert.

Buchstabenmenge (1–5 Sterne)

1 = wenige, sehr einfache Buchstaben

5 = alle Buchstaben des Alphabets

Groß-/Kleinschreibung (1–3 Sterne)

1 = nur Großbuchstaben

2 = nur Kleinbuchstaben

3 = gemischt (Groß- und Kleinbuchstaben gemischt)

Auswahlanzahl (1–4 Sterne)

1 = 2 Auswahlmöglichkeiten

2 = 3 Auswahlmöglichkeiten

3 = 4 Auswahlmöglichkeiten

4 = 5 Auswahlmöglichkeiten

Unter den Sternen jeweils ein kleines, für Erwachsene lesbares Label. Ein großer Start-Button (z. B. „Los" oder ein Play-Symbol) startet das Spiel.

2. Spielbildschirm
Großes Buchstaben-Display mittig oben (sehr groß, z. B. 30–40 % der Bildschirmhöhe).

Darunter eine Reihe von großen, runden oder abgerundeten Auswahl-Buttons mit je einem Buchstaben.

Oben links oder oben rechts ein kleiner „Zurück"-Button (z. B. Haus-Icon oder Pfeil), der zurück zum Einstellungsbildschirm führt.

Endlos: Es gibt kein Ende, keinen Fortschrittsbalken, keine Punkteanzeige.

Feedback:

Richtig: Der angetippte Button und/oder der große Buchstabe reagieren mit einer freundlichen Animation (z. B. sanftes Aufleuchten, kurzes Hüpfen, Farbwechsel zu Grün) und einem angenehmen, kurzen Ton (kein schriller Sound). Danach erscheint nach kurzer Pause (ca. 0,6–1 s) der nächste Buchstabe mit neuer Auswahl.

Falsch: Der angetippte Button wackelt sanft hin und her (Shake-Animation) und wird kurz leicht rötlich/gedimmt. Kein „Falsch"-Ton, kein Bestrafen. Die Aufgabe bleibt bestehen, das Kind kann erneut wählen.

Buchstabenlogik:

Buchstaben werden nicht alphabetisch eingeführt, sondern nach visueller Einfachheit sortiert. Beispielreihenfolge (von einfach zu komplex): O, I, L, T, S, A, M, E, F, H, X, U, V, W, C, G, J, P, R, B, D, K, N, Y, Z, Q.

Bei „Buchstabenmenge = 1" nur die ersten wenigen dieser Liste verwenden; bei 5 die gesamte Liste.

Bei „gemischt" (Groß-/Kleinschreibung) wird pro Runde zufällig entschieden, ob der gesuchte Buchstabe groß oder klein dargestellt wird. Die Auswahl-Buttons enthalten dann gemischte Fälle – aber jede Option in einem konsistenten Stil pro Durchgang, sodass das Kind nicht durch Stilwechsel verwirrt wird. Der gesuchte Buchstabe und die Auswahl sollten denselben Fall-Regeln folgen.

Der gesuchte Buchstabe bleibt permanent sichtbar, während die Auswahl darunter angezeigt wird.

Kein Buchstabe erscheint zweimal direkt hintereinander als gesuchter Buchstabe.

Die richtige Antwort darf nicht immer an derselben Position stehen (Position zufällig, aber bei 2 Optionen abwechselnd links/rechts).

Visuelles Design:

Pastellfarben.

Angenehmer grüner Hintergrund als sanfter Gradient (z. B. von einem hellen Pastellgrün zu einem etwas kräftigeren Grün, vertikal oder diagonal).

Große, runde Buttons mit weichen Schatten und abgerundeten Ecken.

Große, gut lesbare, kindgerechte serifenlose Schrift (z. B. „Comic Sans MS" als Fallback oder eine freundliche Systemschrift).

Keine blinkenden oder überladenen Elemente. Ruhige, freundliche Atmosphäre.

Ausreichend Kontrast für Lesbarkeit, aber keine grellen Farben.

Layout muss sich an verschiedene Tablet-Größen anpassen (responsive, Bootstrap-Grid oder Flexbox).

Barrierefreiheit:

Große Tap-Flächen (mindestens 80×80 px, besser mehr).

Keine Abhängigkeit von Farbe allein (Feedback auch durch Animation/Bewegung).

Keine Texte, die das Kind lesen müsste.

Ton optional – falls Ton verwendet wird, nur kurze, weiche, angenehme Klänge (z. B. mit Web Audio API erzeugte sanfte Töne, kein externes Audio nötig).

Technische Vorgaben:

Eine einzige HTML-Datei.

Bootstrap 5 per CDN einbinden.

Vanilla JavaScript (kein jQuery, keine weiteren Libraries).

Kein Server, keine externen Assets (keine Bilder, keine Audiodateien) – alles inline oder per CSS/Web Audio.

Responsive, primär für Tablet-Hochformat optimiert, aber auch im Querformat nutzbar.

Sauber kommentierter Code, damit die Einstellungen später leicht angepasst werden können (z. B. Buchstabenliste, Farben, Animationsdauern als Konstanten am Anfang des Skripts).

Ausgabe: Bitte die komplette HTML-Datei in einem Codeblock ausgeben, ohne zusätzliche Erklärungen.
