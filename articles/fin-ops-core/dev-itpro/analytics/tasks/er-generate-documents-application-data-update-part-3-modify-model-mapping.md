---
title: Modelle und Zuordnungen ändern, um Dokumente zu generieren, die Anwendungsdaten haben
description: Dieses Thema zeigt, wie Sie Berichtskonfigurationen entwerfen, um ein elektronisches Dokument zu generieren und Anwendungsdaten zu aktualisieren. (Teil 2 – Dokumente generieren).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64bcf885fe2f5fca6b91589171b5e539eff2c3e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567091"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>Modelle und Zuordnungen ändern, um Dokumente zu generieren, die Anwendungsdaten haben

[!include [banner](../../includes/banner.md)]

Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, „ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 2 - Dokumente erstellen)“. 

Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren. In diesem Verfahren ändern Sie die ER-Konfigurationen, um sie derzeit nicht verwenden, um elektronische Dokumente zu erzeugen, wohingegen Anwendungsdaten auch zu aktualisieren. Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden.


## <a name="modify-data-model"></a>Datenmodell ändern
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie 'Intrastatmodell' in der Struktur (Modell).
    * Erweitern Sie das Datenmodell nach Bedarf. Neben der Verwendung als Datenquelle, um den Intrastat-Bericht zu generieren, wird das Datenmodell verwendet, um Details zum Intrastat-Berichts-Prozess zu erfassen. Die Details werden dann verwendet, um Anwendungsdaten zu aktualisieren.   
3. Klicken Sie auf Designer.
4. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
5. Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.
6. Geben Sie im Feld Typ Für Bewertungsdatenaktualisierung.
    * Aktualisierung der Anwendungsdaten  
7. Klicken Sie auf Hinzufügen.
8. Wählen Sie in der Strukturdarstellung "für Bewerbungsdatenenaktualisierung " aus.
    * Dieser neue Stammartikel wird hinzugefügt, um dem Datenfluss zum Bewegen von Daten vom Intrastat-Bericht (Als Datenquelle verwendet) für die Bewerbungstabellen (das Aktualisierungsziel) zu definieren. Beachten Sie, dass verschiedene Stammartikel zum Abrufen von Daten verwendet werden müssen für die ausgehenden Dokumente und zum Abrufen von Daten vom Dokuments, das verwendet wird, um Anwendungsdaten zu aktualisieren.   
9. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
10. Geben Sie im Feld Typ Archivkopfzeile ein.
    * Archivkopfzeile  
11. Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.
12. Klicken Sie auf Hinzufügen.
    * Da ein Datensatz für jeden Intrastat-Bericht erstellt wird,, der erzeugt werden soll, müssen Sie einen neuen Artikel dafür erstellen.  
13. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
14. Geben Sie im Feld "Name" "Dateiname" ein.
    * Dateiname  
15. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
16. Klicken Sie auf Hinzufügen.
17. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
18. Geben Sie im Feld Name die Anzahl Zeilen ein.
    * Anzahl Positionen  
19. Wählen Sie im Artikelfeld Integer aus.
20. Klicken Sie auf Hinzufügen.
    * Fügen Sie diesen Artikel hinzu, um die Anzahl von Intrastat-Buchungen anzugeben, die während der aktuellen Generierung eines Berichts gemeldet werden.  
21. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
22. Geben Sie im Feld Typ Archivzeilen ein.
    * Archivieren von Positionen  
23. Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.
24. Klicken Sie auf Hinzufügen.
    * Fügen Sie diesen Artikel hinzu, um die Anzahl von Intrastat-Buchungen anzugeben, die während der aktuellen Generierung eines Berichts gemeldet werden.  
25. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
26. Geben Sie im Feld Namen "Amount" ein.
    * Dauer  
27. Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.
28. Klicken Sie auf Hinzufügen.
29. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
30. Geben Sie im Feld Typ Waren Rec ID ein.
    * Warendatensatz-ID  
31. Wählen Sie im Feld "Artikeltyp" 'Int64 aus.
32. Klicken Sie auf Hinzufügen.
33. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
34. Geben Sie im Feld Typ Artikelnummer ein.
    * Artikelnummer  
35. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
36. Klicken Sie auf Hinzufügen.
37. Klicken Sie auf "Speichern".
38. Schließen Sie die Seite.

## <a name="modify-model-mapping"></a>Modellzuordnung ändern
1. Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.
2. Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Zuordnung)" aus.
    * Ändern Sie die bestehende Zuordnung, um die Bewerbungsdatenenaktualisierung zu starten und Intrastat-Berichts-Details zu archivieren.  
3. Klicken Sie auf Designer.
4. Klicken Sie auf "Neu".
5. Geben Sie im Feld Typ Archiv aktualisieren ein.
    * Archiv aktualisieren  
6. Wählen Sie im Feld Richtung Destination nach aus.
7. Klicken Sie auf "Speichern".
    * Dieser neue Zuordung definiert den Datenfluss zum Bewegen von Daten (Intrastat-Bericht) vom Datenmodell zur Bewerbungstabelle (das Aktualisierungsziel). Beachten Sie, dass Stammartikel des anderen Modells verwendet werden müssen, um Daten aus der Anwendung für den Berichterstellungsprozess und die Daten vom Datenmodell Sie anschließend die Möglichkeit für die Bewerbungsdatenenaktualisierung abzurufen.   
8. Klicken Sie auf Designer.
9. Wählen Sie in der Strukturdarstellung Datenmodell\Datenmodell aus.
    * Die erforderliche Datenquelle hinzufügen. Dies ist das Datenmodell, das Details der gemeldeten Intrastat-Buchungen enthält, die archiviert werden müssen.  
10. Klicken Sie auf "Stamm hinzufügen".
11. Geben Sie im Feld Namen die Modelart ein.
    * Modell  
12. Wählen Sie im Definitionsfeld den Wert Für Anwendungsdatenaktualisierung aus oder geben Sie diesen ein.
    * Aktualisierung der Anwendungsdaten  
13. Klicken Sie auf "OK".
14. Erweitern Sie in der -Struktur den Knoten 'Modell'.
15. Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.
16. Wählen Sie in der Struktur Modell\Archivkopfzeile aus.
17. Klicken Sie auf Hinzufügen.
    * Da Sie Intrastat-Buchungen für das gemeldete Chargenattribut archivieren möchten, muss die entsprechende Datenquelle hinzugefügt werden.  
18. Geben Sie im Feld Name den Typ Auzählungszeile ein.
    * Aufgezählte Positionen  
19. Klicken Sie auf Formel bearbeiten.
20. Wählen Sie in der Struktur Liste\AUFZÄHLUNG aus.
21. Klicken Sie auf Funktion hinzufügen.
22. Erweitern Sie in der -Struktur den Knoten 'Modell'.
23. Wählen Sie in der Struktur Modell\Archivkopfzeile aus.
24. Wählen Sie in der Struktur Modell\ArchivkopfzeileArchivzeilen aus.
25. Klicken Sie auf Datenquelle hinzufügen.
26. Im Formelfeld bestimmt geben Sie "AUFZÄHLUNG (Modell Archivkopfzeile, Archivzeilen) ein.
    * AUFZÄHLEN (Modell. Archivpositionen, Archivzeilen)  
27. Klicken Sie auf "Speichern".
28. Schließen Sie die Seite.
29. Klicken Sie auf "OK".
30. Klicken Sie Destination hinzfügen aus.
    * Fügen Sie der Bewerbungstabellen nach Bedarf hinzu, die Aktualisierungen benötigen, u, Details der gemeldeten Intrastat-Buchungen zu archivieren.  
31. Geben Sie im Feld den Archivtyp ein..
    * Archiv  
32. Geben Sie im Feld Tabelle den Typ IntrastatArchiveGeneral ein.
    * Formular "IntrastatArchiveGeneral"  
    * Behalten Sie die Belegaktion „Einfügen“, sodass Sie Datensätze für das Detailarchivierens jedes Intrastat-Berichts-Prozesses hinzufügen können.  
33. Wählen Sie "Ja" im Feld Beleg-Infoprotokoll.
    * Wählen Sie die Option Ja aus, um Informationen zu Problemen mit der Bewerbungsdatenenaktualisierung abzurufen.  
34. Wählen Sie Ja im Feld Belegaktionsüberprüfungsfeld aus.
    * Wählen Sie die Option „Ja“ aus, um leere Prüfungsfehler zum Feld „Intrastat-Archiv ID“ zu unterdrücken. Dieses erfolgt, nachdem Datensätze hinzugefügt wurden, basierend auf den Einstellungen der Nummernkreise, die für diese Tabelle in der Außenhandelparameterform konfiguriert werden.  
35. Klicken Sie auf "OK".
    * Binden Sie Elemente der hinzugefügten Datenquelle (das gefilterte Modell auf Basis des ausgewählten Stammartikel) mit Elementen des hinzugefügten Ziels.  
36. In der Struktur erweitern Sie Archiv.
37. In der Struktur erweitern Sie Archiv\<Beziehungen.
38. In der Struktur erweitern Sie Archiv\<BeziehungenIntrastatArchiveDetail.
39. Wählen Sie in der Struktur Archiv\<BeziehungenIntrastat\ArchiveDetail\Betrag (AmountMST).
40. Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen.
41. Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert.
42. Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Betrag.
43. Klicken Sie auf Binden.
44. Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetail\Waren(IntrastatCommodity).
45. Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Waren Rec.-ID.
46. Klicken Sie auf Binden.
47. Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetai\lArtikelzahl (ItemId).
48. Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Artikelnummer.
49. Klicken Sie auf Binden.
50. Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetail\Artikelzahl (LineNumber) aus.
51. Wählen Sie in der Struktur Modell\Archivkopfzeile\Zeilen\Anzahl aus.
52. Klicken Sie auf Binden.
53. In der Struktur wählen Sie Archiv\<Beziehungen\Intrastat\ArchiveDetail.
54. Wählen Sie in der Struktur Modell\Archivkopfzeile\Anzahl Zeilen aus.
55. Klicken Sie auf Binden.
56. Wählen Sie in der Struktur Archive\Dateinamen (FileName) aus.
57. Wählen Sie in der Struktur Modell\Archivkopfzeile\Dateien aus.
58. Klicken Sie auf Binden.
59. Wählen Sie in der Strukturdarstellung Archiv\Anzahl Zeilen(NumberOfLines) aus.
60. Wählen Sie in der Struktur Modell\Archivkopfzeile\Anzahl Zeilen aus.
61. Klicken Sie auf Binden.
62. Wählen Sie in der Struktur Archiv aus.
63. Wählen Sie in der Struktur Modell\Archivkopfzeile aus.
64. Klicken Sie auf Binden.
65. Klicken Sie auf "Speichern".
66. Schließen Sie die Seite.
67. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]