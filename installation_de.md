# Installation (de) #

## Schritt 1: Kopieren ##
Kopieren Sie die Dateien aus dem Ordner `copy_this` in die jeweiligen Ordner Ihres OXID eShops. Der Inhalt des Ordners `your_template_folder` ist in den Ordner `tpl` des von Ihnen genutzten Shop-Templates einzufügen. Die folgende Abbildung erläutert diesen Schritt grafisch.

![http://semantox.bitsector.de/code_google/wiki/img/installation_copy_small.gif](http://semantox.bitsector.de/code_google/wiki/img/installation_copy_small.gif)


## Schritt 2: Aktivierung ##

Aktivieren Sie das Modul im Admin-Bereich Ihres OXID eShops, indem Sie unter `Stammdaten -> Grundeinstellungen -> System -> Module` die folgenden Zeilen einfügen:
```
oxutilsview => semantox/sox_oxutilsview
details => semantox/sox_details
content => semantox/sox_content
```

Wird die Klasse `oxutilsview`, `details` oder `content` bereits durch ein oder mehrere Module erweitert, so ergänzen Sie die jeweilige Zeile durch das Zeichen `&`, gefolgt von der dazugehörigen Semantox-Klasse. Ein Beispiel:
```
oxutilsview => ein_anderes/modul&semantox/sox_oxutilsview
```


## Schritt 3: Temporäre Dateien löschen ##
Löschen Sie den Inhalt (abgesehen von der Datei `.htaccess`) des Ordners `tmp`.

## Schritt 4: Konfiguration ##
Konfigurieren Sie das Modul im Admin-Bereich Ihres OXID eShops. Die Konfigurationsmöglichkeiten sind unter den folgenden Menüpunkten aufzufinden:
  * `Stammdaten -> Grundeinstellungen -> Semantox`
  * `Shopeinstellungen -> Zahlungsarten -> Semantox`
  * `Shopeinstellungen -> Versandarten -> Semantox`

Versuchen Sie zunächst unter `Shopeinstellungen -> Zahlungsarten -> Semantox` jeder Ihrer Zahlungsarten eine oder mehrere vordefinierte Zahlungsarten durch Auswahl der jeweiligen Checkboxen zuzuordnen. Dabei sollten die ausgewählten, vordefinierten Zahlungsarten möglichst exakt Ihren Zahlungsarten entsprechen. Wenn Sie für eine Ihrer Zahlungsarten kein passende, vordefinierte Zahlungsart finden, dann können Sie in diesem Fall von einer Zuordnung absehen.

Bitte gehen Sie bei der Zuordnung vordefinierter Versandarten unter dem Menüpunkt `Shopeinstellungen -> Versandarten -> Semantox` analog vor.

Unter `Stammdaten -> Grundeinstellungen -> Semantox` finden Sie die technische Konfiguration des Moduls sowie die Konfiguration von erweiterten Anbieterdaten und globalen Angebots- und Produktdaten. Die globalen Angebots- und Produktdaten werden allen im Shop enthaltenen Artikel zugewiesen. Ordnen Sie deshalb also nur diejenigen Eigenschaften zu, die auf alle Artikel zutreffen.

Eine präzisere Beschreibung der Konfiguration von Semantox finden Sie **[hier](configuration_de.md).**

## Schritt 5: Markup modifizieren (optional) ##
Damit auch nach der Integration von RDFa durch Semantox Ihr Online-Shop valides Markup aufweist, sollten Sie dessen Dokumenttypdefinition (DOCTYPE)  anpassen. Diese befindet sich in den ersten Zeilen eines jeden (X)HTML-Dokumentes. Eine Dokumenttypdefinition beginnt mit `<!DOCTYPE und endet mit >`. Ein Beispiel:
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
      "http://www.w3.org/TR/html4/loose.dtd">
```
Die Dokumenttypdefinition ist im Basic-Template des OXID eShops zu Beginn der Datei  `_header.tpl` unter `out -> basic -> tpl` zu finden. Im Azure-Template befindet sie sich in der Mitte der Datei `base.tpl` unter `out -> azure -> tpl -> layout`.
Wenn das Markup Ihres Shops auf HTML basiert, dann ersetzten Sie bitte die bisherige Dokumenttypdefinition bitte durch die folgende:
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01+RDFa 1.1//EN"
      "http://www.w3.org/MarkUp/DTD/html401-rdfa11-1.dtd">
```
Basiert das Markup auf XHTML, dann ersetzten Sie die Dokumenttypdefinition bitte durch diese:
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML+RDFa 1.0//EN"
      "http://www.w3.org/MarkUp/DTD/xhtml-rdfa-1.dtd">
```