# Das LOD-Pilotprojekt "Berner Ortsgeschichten" 
Das LOD-Pilotprojekt "Berner Ortsgeschichten" ist eine Zusammenarbeit zwischen Digital Scholarship und dem ZHB (Zentrum für Historische Bestände), beide Teil der Universitätsbibliothek Bern. Während Digital Scholarship nach geeigneten Daten suchte, um erste Erfahrungen mit einem Linked Data-Projekt zu sammeln, hatte das ZHB das Ziel, die Daten der Bibliographie der Berner Geschichte (BBG) besser zugänglich zu machen. Da der Datensatz dieser Bibliographie jedoch mehr als 30.000 Datensätze umfasst, wurde beschlossen, zunächst den Fokus auf die rund 600 Berner Ortsgeschichten zu legen, die sich auf bestimmte Dörfer und Städte beziehen.
Da diese Texte die Geschichte eines bestimmten Ortes erzählen, sollten sie nicht nur mit externen Links anhand der GND-Identifikatoren (GND-IDs) der Orte, die aus dem Bibliothekskatalog (Alma) stammen, angereichert werden, sondern auch georeferenziert und auf einer Karte zugänglich sein.
Im ersten Schritt wurden etwa 40 Berner Ortsgeschichten aus dem 19. Jahrhundert ausgewählt, die vollständig digitalisiert und auf DigiBern verfügbar sind. Die entsprechenden Metadaten, die aus dem Katalog extrahiert wurden, wurden angereichert und auf einer Karte georeferenziert.
Es gab viele Herausforderungen zu bewältigen: Erstens können GND-IDs nicht einfach aus Alma abgerufen werden. Die vollständigen Metadaten mussten über die SRU-Schnittstelle extrahiert werden, und dann wurden die GND-IDs mit Python extrahiert. Zweitens verweisen die GND-IDs nicht direkt auf die gewünschten Linked Data. Mit Hilfe von muenzfunde.ch konnten jedoch viele der gewünschten Links zu Wikidata (Q-IDs), dem Historischen Lexikon der Schweiz (HLS-DHS) und ortsnamen.ch ermittelt werden. Schließlich hatte die IT-Abteilung keine Zeit, die Daten auf einer Karte anzuzeigen, daher wurde Google My Maps als Workaround gewählt, obwohl es stark eingeschränkte Funktionalitäten bietet. Dennoch zeigen die über 8.400 Aufrufe der Karte "Berner Ortsgeschichten aus dem 19. Jahrhundert" auf DigiBern ein erhebliches Interesse an dieser Art von Ressource.
Das Python-Skript wurde dann für den größeren Datensatz von Berner Ortsgeschichten aus den Jahren 1975 und später (500+) angepasst. Darüber hinaus wurde eine separate Datentabelle als Konkordanz erstellt, die die Tabelle von muenzfunde.ch ersetzte, die für die 40 Ortsgeschichten des 19. Jahrhunderts verwendet wurde.
Dank der während dieses Prozesses hinzugefügten Q-IDs können Links zu den Wappen von Dörfern/Städten und zu den offiziellen Websites der Gemeinden sowie andere gewünschte Links nun zuverlässig mit wenigen Zeilen Python aus Wikidata extrahiert werden, zusammen mit den geografischen Koordinaten. Die IT-Abteilung konnte ein Proof-of-Concept für die Karte erstellen, die über das Universitätsnetzwerk (Citrix) zugänglich ist. Automatische Aktualisierungen der Daten aus dem Katalog sind geplant, aber unwahrscheinlich, dass sie in diesem Jahr durchgeführt werden.
Weitere geplante Schritte umfassen die kontinuierliche Erweiterung der Berner Ortsdatentabelle (BEOT), die die Q-IDs, Links zu HLS-DHS und ortsnamen.ch sowie die GND-IDs enthält, sowie die direkte Anreicherung der GND-Datensätze mit den Q-IDs. Darüber hinaus gibt es Pläne, die Standortdaten in Wikidata zu ergänzen/korrigieren und die Projektdaten auf GitHub verfügbar zu machen.
