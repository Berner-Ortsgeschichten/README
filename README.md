# README
Das LOD-Pilotprojekt "Berner Ortsgeschichten" ist eine Zusammenarbeit zwischen Digital Scholarship und dem ZHB (Zentrum für Historische Bestände) der Universitätsbibliothek Bern. Während Digital Scholarship nach geeigneten Daten suchte, um erste Erfahrungen mit einem Linked Data Projekt zu sammeln, hatte das ZHB das Ziel, die Daten der Bibliographie der Berner Geschichte (BBG) besser zugänglich zu machen. Da der Datensatz dieser Bibliographie jedoch mehr als 30.000 Datensätze umfasst, wurde beschlossen, zunächst den Fokus auf die rund 600 Berner Ortsgeschichten zu legen, die sich auf bestimmte Dörfer und Städte beziehen.

Da diese Texte die Geschichte eines bestimmten Ortes erzählen, sollten sie nicht nur mit externen Links anhand der GND-Identifikatoren (GND-IDs) der Orte aus dem Bibliothekskatalog (Alma) angereichert werden, sondern auch georeferenziert und auf einer Karte zugänglich sein.

Siehe auch: https://www.ub.unibe.ch/service/digital_scholarship/lod_und_datenanreicherung/index_ger.html

Auf dieser GitHub-Seite sind verschiedene Ressourcen zum Projekt verfügbar:
- Projekt "Berner Ortsgeschichten"
- BEOT: Die BErnerOrtsTabelle enthält für Berner Ortschaften aus den Berner Ortsgeschichten die IDs für Wikidata, das Historisches Lexikon der Schweiz, ortsnamen.ch und die GND-ID.
- BEOG_Pythonscript: Dieses Script lädt über eine SRU-Abfrage aus Alma die Metadaten (MARCXML) der Titel herunter, welche mit "bbggr" kodiert sind. Danach extrahiert es die Titeldaten und die GND-ID für den Ort, welcher in der Ortsgeschichte beschrieben wird. Über die BEOT werden die Q-IDs hinzugefügt, mit welchen danach aus Wikidata die gewünschten Daten (Koordinaten, Wappen und Webseite der Gemeinde, Wikipedia- und geo.admin.ch-Link) heruntergeladen werden.
- Linked-Data-Modell-BEOG: Beschreibung des Datasets der "Berner Ortsgeschichten ab 1975" als Linked Data Modell in RDF-Turtle.
