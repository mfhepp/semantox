# Konfiguration (de) #

Auf dieser Wiki-Seite finden Sie eine detaillierte Anweisung zur Konfiguration von Semantox.


---

## Zahlungs- und Versandarten ##

Wählen Sie zur Konfiguration der Zahlungsarten den Menüpunkt "`Shopeinstellungen -> Zahlungsarten`". Wählen Sie anschließend eine Zahlungsart aus und öffnen Sie den Reiter "`Semantox`". Unter diesem Reiter finden Sie vordefinierte [Zahlungsarten des GoodRelations-Vokabulars](http://purl.org/goodrelations/v1#PaymentMethod). Die Zahlungsarten werden hier in allgemeine Zahlungsarten und Kreditkartenarten unterschieden. Markieren Sie von den vordefinierten Zahlungsarten nun diejenigen, die auf Ihre ausgewählte Zahlungsart zutreffen. Die folgende Abbildung zeigt diesen Schritt beispielhaft anhand der Zahlungsart `Kreditkarte`. Dieser Zahlungsart wurden die Kreditkartenarten `American Express`, `Diners Club`, `JCB`, `MasterCard` und `VISA` zugeordnet.

![http://semantox.bitsector.de/code_google/wiki/img/configuration_payment_de.gif](http://semantox.bitsector.de/code_google/wiki/img/configuration_payment_de.gif)

Bitte achten Sie grundsätzlich darauf, dass Sie Ihren Zahlungsarten nur die vordefinierten Zahlungsarten zuordnet, die mit ihnen übereinstimmen.

Gehen Sie zur Konfiguration der Zahlungsarten analog vor.


---

## Hauptkonfiguration ##

Die Hauptkonfiguration von Semantox können Sie unter dem Menüpunkt "`Stammdaten -> Grundeinstellungen`" im Reiter `Semantox` durchführen.

### Technische Einstellungen ###
Unter den technischen Einstellungen können Sie die automatische Einbettung der RDF-Daten steuern. Neben der Aktivierung der automatischen Einbindung können Sie zusätzlich auswählen, auf welchen Content-Seiten die RDF-Daten zu den Zahlungs- und Versandinformationen sowie die Anbieterdaten eingebettet werden sollen. Dazu gibt Semantox die Content-Seiten mit den folgenden `OXLOADIDs` vor:
  * oxagb
  * oxdeliveryinfo
  * oximpressum
  * oxrightofwithdrawal
Die RDF-Daten zu den Artikeln werden in die jeweiligen Detail-Seiten eingebettet und automatisch mit den Zahlungs- und Versandinformationen verknüpft.
NEUES BILD
![http://semantox.bitsector.de/code_google/wiki/img/configuration_shop_tech_de.gif](http://semantox.bitsector.de/code_google/wiki/img/configuration_shop_tech_de.gif)

### Anbieterdaten ###
Zur maschinenlesbaren Beschreibung der Anbieterdaten erweitert Semantox die Stammdaten um die folgenden Einträge:
  * Logo-URL (Logo des Anbieters)
  * Geo-Position (Längengrad und Breitengrad zur Lokalisierung des Anbieters)
  * GLN ([Global Location Number](http://www.gs1-germany.de/standards/identifikationssysteme/unternehmen_gln/gln/index_ger.html))
  * NAICS ([North American Industry Classification System](http://www.census.gov/eos/www/naics/))
  * ISIC ([International Standard Industrial Classification](http://unstats.un.org/unsd/cr/registry/regcst.asp?Cl=2))
  * D-U-N-S ([Data Universal Numbering System](http://www.dnbgermany.de/datenbank/duns_nummer.html))
Mit Hilfe dieser Angaben kann die Identifikation eines Anbieters optimiert werden. Die Angaben sind **optional**.

![http://semantox.bitsector.de/code_google/wiki/img/configuration_shop_offerer_de.gif](http://semantox.bitsector.de/code_google/wiki/img/configuration_shop_offerer_de.gif)

### Globale Angebotsdaten ###
Wie der Name dieses Konfigurationsabschnitts bereits vermuten lässt, sind die hier getroffenen Einstellungen für alle im Shop enthaltenen Artikel bzw. Angebote gültig. Bitte wählen Sie deshalb nur die Eigenschaften aus, die auf alle Artikel zutreffen. Die folgende Abbildung zeigt die Konfigurationsmöglichkeiten.

![http://semantox.bitsector.de/code_google/wiki/img/configuration_shop_globals_de.gif](http://semantox.bitsector.de/code_google/wiki/img/configuration_shop_globals_de.gif)

Mit den ersten beiden Auswahlmöglichkeiten können Sie bestimmen, ob die angezeigten Preise inkl. der gesetzlichen MwSt. sind und in welchem Zustand sich die angebotenen Artikel befinden.

Anschließend lässt sich die Funktion Ihrer Angebote festlegen. Bieten Sie in Ihrem Shop lediglich Ware zum Verkauf an, dann wählen Sie die Funktion `Verkauf`. Sollten Sie jedoch zusätzlich auch Reparaturleistungen anbieten, was der Funktion `Reparatur` entsprechen würde, dann müssten Sie die Auswahl `Keine/Mehrere der vorhandenen` treffen.

Neben der Funktion der Angebote können Sie zusätzlich auch die Konsumentengruppen, für die Ihre Angebote gültig sind, auswählen.

Abschließen lässt sich die Gültigkeitsdauer der Angebote und der Angebotspreise konfigurieren. Mit Einbindung der jeweiligen Gültigkeitsdauer wird z.B. Suchmaschinen signalisiert, ob und wie lange ein Angebot bzw. ein Angebotspreis gültig sind.