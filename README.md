# Parkplatz-Quest

Ein Lernspiel zum **Parkplatz-Schreiben** für die Grundschule (Klasse 3/4).
Die Kinder hören ein Wort, sehen die leeren Parkplätze und tippen das Wort ein.
Jeder Buchstabe springt dabei auf seinen Parkplatz.

## Level

| Level | Thema | Beispielwörter |
| --- | --- | --- |
| 1 | Silbenkönige: Wie viele Kronen? | Kürbis, Laterne, Spielkonsole |
| 2 | Einer-Parkplätze | Nebel, Monster, Roboter |
| 3 | Zweierkönige (au, ei, eu) und Ä, Ö, Ü | Eule, Feuer, Geister |
| 4 | Buchstaben-Teams (Sch, ch, Pf, St, Sp) | Schwert, Drache, Sturm |
| 5 | Doppelparkplatz | zocken, Spinne, Blätter |
| 6 | Thron, Freund und Zwilling (h, ie, Doppelvokal) | Zahn, Spiel, Tee |
| 7 | Nachbar am Ende (Auslautverhärtung) | Mond, Wald, Korb |
| Boss | alles gemischt | Gruselschloss, Zauberstab |

## Spielelemente

- Erfahrungspunkte (XP), Feuer-Serien, 3 Leben pro Level, bis zu 3 Sterne und ein Abzeichen pro Level
- Wörter werden vorgelesen (deutsche Stimme des Geräts nötig)
- Falsch besetzte Parkplätze werden rot markiert
- Tipp-Knopf zeigt Kronen und Silbenkönige
- Tasten für ä, ö, ü und ß
- „Lehrkraft: alle Level öffnen“ unten auf der Level-Karte

Der Fortschritt wird nur im Browser des jeweiligen Geräts gespeichert (localStorage).

## Online stellen mit GitHub Pages

1. Neues Repository auf GitHub anlegen, z. B. `parkplatz-quest`.
2. Die Dateien `index.html`, `README.md` und `.nojekyll` hochladen
   („Add file“ → „Upload files“).
3. Unter **Settings → Pages** bei „Source“ den Zweig `main` und den Ordner `/ (root)` wählen und speichern.
4. Nach etwa einer Minute ist das Spiel erreichbar unter
   `https://<dein-benutzername>.github.io/parkplatz-quest/`

## Wörter ändern

Alle Wörter stehen in `index.html` im Abschnitt `const LEVELS = [...]`.
Ein Eintrag sieht so aus:

```js
["Nebel", "b:N r:e | b:b r:e b:l", "🌫️"]
```

- Erstes Feld: das Wort
- Zweites Feld: die Parkplätze, durch Leerzeichen getrennt, `|` = Silbenende
- Drittes Feld: das Bild (Emoji)
- In Level 7 gibt es ein viertes Feld mit der Verlängerungsprobe, z. B. `"Mon-de"`

| Kürzel | Parkplatz |
| --- | --- |
| `r`, `b`, `g` | Einer-Parkplatz (`r` = Silbenkönig) |
| `r2` | Zweierkönig (au, ei, eu) |
| `g2` / `g3` | Zweier- / Dreier-Team (ch, Pf, St, Sp / Sch) |
| `bd`, `gd` | Doppelparkplatz |
| `bdf`, `gdf` | Doppelparkplatz mit Silbenende in der Mitte |
| `rl` | langer König mit Thron oder Freund (ah, ie …) |
| `rll` | langer König mit Zwilling (aa, ee, oo) |

Die Buchstaben `r`, `b` und `g` stammen aus der farbigen Version der Methode; im Spiel werden alle Parkplätze einfarbig gezeichnet. Wichtig: Die Buchstaben aller Parkplätze zusammen müssen genau das Wort ergeben.

## Grundlage

Parkplatzmethode nach Leo Schmitz („Auf dem Weg zur Schrift“) und die Parkplatzwörter-Hefte von Claudia Wahl.
