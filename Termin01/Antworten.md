# Antworten #
## Popularität
- ### Was hat kde=1, zu bedeuten? Warum nicht einfach kde=True so wie bei dem histplot danach? ####

  - 1 ist dasselbe, wie True und kann auch als True Ersatz verwendet werden. 




-  ### Die x-Achsen sind in wissenschaftlicher Schreibweise → umwandeln in Dezimalschreibweise → siehe Vorlage ###

   - Warum jetzt x-Achse im Minus Bereich.


- ### stat=’count’ ist überflüssig, das ist der default. Man kann zwar auch defaults hinschreiben um es dem Leser einfacher zu machen, aber warum habt ihr das dann nicht auch bei dem histplot davor gemacht?

  - Gelöscht.
  
## Performance von Kanälen
Das Problem ist hier, dass ihr die mean-Views und mean-Likes separat berechnet. Laut Aufgabenstellung sollt ihr die Top 
10 Kanäle nach mean Views berechnen und dazu die entsprechenden mean-Likes, nicht insgesamt die Top 10 mean Likes. Dadurch habt ihr die extra Kanäle, weil die Top 10 mean Views ≠ Top 10 mean Likes. Lösung: Berechnung in einem groupby mit einem agg
Das ist kein Histogramm, da ihr keine Häufigkeiten zählt, sondern die durchschnittlichen Views und Likes anzeigt

- Geändert.
- Warum Y-Achse der Likes bei -200?
## Verteilung der Videolänge
Statt np.inf hätte man hier auch gaming_data[’duration’].max() nehmen können
- geändert. ABER `ValueError: Bin labels must be one fewer than the number of bin edges`

## Schnelligkeit des Trends
### Antwort auf die Frage “Warum ist der Titel "kaputt"?”: Dies geschieht durch mehrfaches Ausführen der Preprocessing Zellen am Anfang des Notebooks. Wenn ihr diese nur einmal ausführt bleibt der Titel intakt. Genauere Erklärung bei Interesse im nächsten Praktikum ###

### Wochentag der Veröffentlichung Beim ersten Diagramm stehen auf der x-Achse 0, 1, 2, … und nicht die richtigen Wochentage, beim 2. Diagramm schon. Warum? ###

- War bei beiden Wochentage, wahrscheinlich nur nicht ausgeführt nach dem Coden.