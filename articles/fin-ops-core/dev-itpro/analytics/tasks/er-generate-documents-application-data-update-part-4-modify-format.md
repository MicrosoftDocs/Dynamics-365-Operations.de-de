---
title: Formate zum Generieren von Dokumenten verändern, die Anwendungsdaten haben
description: Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 3 - Ändern von Modell und Zuordnung)".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbed62c80c14e7cfe96d38d43a5db39b0469d939
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184921"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Formate zum Generieren von Dokumenten verändern, die Anwendungsdaten haben

[!include [task guide banner](../../includes/task-guide-banner.md)]

Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 3: Ändern von Modell und Zuordnung)".

Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren. In diesem Verfahren ändern Sie die ER-Konfigurationen, um sie derzeit nicht verwenden, um elektronische Dokumente zu erzeugen, wohingegen Anwendungsdaten auch zu aktualisieren. Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden.


## <a name="modify-format-to-collect-details-of-reporting"></a>Ändern Sie das Format, um Details zur Berichterstellung zu erfassen
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.
3. Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Format)" aus.
4. Klicken Sie auf Designer.
5. Erweitern Sie in der Struktur Datei.
6. Erweitern oder reduzieren Sie 'Datei\Erklärung
7. In der Struktur wählen Sie Datei\Erklärung\Daten'.
8. Wählen Sie im Vielfältigkeitsgebiet wählen Sie "viele" aus.
    * Konfigurieren Sie dieses Formatelement, um Details des Intrastat-Berichts-Prozesses zu archivieren. Dieser Artikel stellt den Archivheaderdatensatz dar.  
9. Erweitern oder reduzieren Sie Datei\Erklärung\Daten.
10. Wählen Sie in der Struktur Erklärung\Daten\Elemente'.
11. Wählen Sie im Vielfältigkeitsgebiet wählen Sie "Null viele" aus.
    * Konfigurieren Sie dieses Formatelement, um Details des Intrastat-Berichts-Prozesses zu archivieren. Dieser Artikel enthält die Liste von archivierten Positionen.  
12. Erweitern oder reduzieren Sie Datei\Erklärung\Daten\Elemente.
13. Wählen Sie in der Struktur Datei\Erklärung\Daten\ElementeDim1.
14. Wählen Sie "Ja" im Feld "Ausgenommene Felder" aus.
    * Sie werden diese Daten nicht archivieren, sodass Sie dieses Formatelement aus der Datenquelle aus Intrastat-Berichts-Details ausschließen.  
15. Erweitern oder reduzieren Sie Datei\Erklärung\Daten\ElementeDim1.
16. Wählen Sie in der Struktur Datei\Erklärung\Daten\Elemente\Dim1\Eigenschaft.
17. Wählen Sie "Ja" im Feld "Ausgenommene Felder" aus.
18. Wählen Sie in der Struktur Datei<\Erklärung\Daten\Elemente\Dim1Datum.
19. Wählen Sie "Ja" im Feld "Ausgenommene Felder" aus.
20. Wählen Sie in der Struktur Datei\Erklärung\Daten\Elemente\Dim2.
21. Wählen Sie "Ja" im Feld "Ausgenommene Felder" aus.
22. Erweitern oder reduzieren Sie Datei\Erklärung\Daten\Elemente\Dim2.
23. Wählen Sie in der Struktur Datei\Erklärung\Daten\Elemente\Dim2\Eigenschaft.
24. Wählen Sie "Ja" im Feld "Ausgenommene Felder" aus.
25. Wählen Sie in der Struktur Datei\Erklärung\Daten\Elemente\Dim2\Code.
26. Wählen Sie "Ja" im Feld "Ausgenommene Felder" aus.
27. Wählen Sie in der Struktur Datei\Erklärung\Daten\Elemente\Dim3.
    * Einige Formatelemente können denselben Namen haben. Zum Beispiel Dim. Sie können dies nicht explizit ermitteln, wenn Sie dieses Format als Datenquelle für das Archivieren von Intrastat-Berichts-Details verwenden, sondern Sie müssen lediglich die alternativen Namen für diese Formatelemente festlegen.   
28. Geben Sie im Feld Namen "Amount" ein.
    * Dauer  
29. Wählen Sie im Vielfältigkeitsgebiet wählen Sie "Genau eines" aus.
30. Wählen Sie in der Struktur Datei\Erklärung\Daten\Elemente\Dim4.
31. Geben Sie im Feld Name "Item" ein.
    * Artikel  
32. Wählen Sie im Vielfältigkeitsgebiet wählen Sie "Genau eines" aus.
    * Neben den Designformatelementen müssen die folgenden Intrastat-Berichts-Details archiviert werden: Eindeutige Datensatzkennung jedes gemeldeten Warenartikels und der Name der generiren Datei. Da diese Daten nicht in den Intrastat-Bericht ausgefüllt werden, müssen die Verpackungseinheiten das Format hinzufügen, die auf diese Detailelementen als Datenquellenartikel zugeordnet ist.  
33. In der Struktur wählen Sie Datei\Erklärung\Daten'.
34. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
35. Wählen Sie in der Struktur Datenquelle\Elemente.
36. Geben Sie im Feld "Name" "Dateiname" ein.
    * Dateiname  
37. Wählen Sie im Feld Datententyp, Zeichenfolge aus.
38. Klicken Sie auf "OK".
39. Wählen Sie in der Struktur Erklärung\Daten\Elemente'.
40. Klicken Sie auf Artikel hinzufügen.
41. Geben Sie im Feld Typ Waren Rec ID ein.
    * Warendatensatz-ID  
42. Wählen Sie im Feld Datentyp Int64 aus.
43. Klicken Sie auf "OK".
44. Klicken Sie auf die Registerkarte Zuordnung.
45. Wählen Sie in der Struktur Datei\Erklärung\Daten\Dateiname aus.
46. Klicken Sie auf Binden.
47. Erweitern Sie in der -Struktur den Knoten 'Modell'.
48. Erweitern Sie in der Struktur 'Modell\Transaktionen.
49. Wählen Sie in der Strukturdarstellung Daten\Erklärung\Daten\Element = \ModelltransaktionenCommodity rec id.
50. Wählen Sie in der Strukturdarstellung Modell\Transaktionen\Commodity rec id.
51. Klicken Sie auf Binden.
52. Klicken Sie auf "Speichern".

## <a name="modify-format-to-memorize-details-of-reporting"></a>Ändern Sie das Format, um Details zur Berichterstellung zu speichern
1. Klicken Sie auf „Format zu Modell zuordnen”.
2. Klicken Sie auf "Neu".
3. Wählen Sie im Definitionsfeld den Wert Für Anwendungsdatenaktualisierung Wurzelelement aus oder geben Sie diesen ein.
    * Aktualisierung der Anwendungsdaten  
4. Geben Sie im Feld Typ Zuordnung zu Aktualisierungstaten.
    * Zuordnung, um die Daten zu aktualisieren  
5. Klicken Sie auf "Speichern".
    * Diese Zuordnung definiert, wie die Details des Intrastat-Berichts gesammelt und im Datenmodell erfasst werden, deren Struktur beim ausgewählten Stammartikel "Für Anwendungsdatenaktualisierungen" angegeben wird. Diese Details, die Modellzuordnung mit demselben Stammartikel "Für Anwendungsdatenaktualisierungen" und die Richtung "Zum Ziel "werden für die Datenaktualisierung verwendet. Die Anwendungsdatenaktualiserung beginnt direkt nachdem der ausgehenden Intrastat-Bericht generiert wurde. Beachten Sie, dass die Anwendungsdatenenaktualisierung zur Laufzeit übersprungen werden kann, aber dass das Datenmodell leer sein muss (mit leeren Datensatzbeleglist).   
6. Klicken Sie auf Designer.
    * Beachten Sie, dass das ausgehende Intrastat-Berichts-Format standardmäßig als Datenquelle für diese Modellzuordnung hinzugefügt wird.  
    * Binden Sie die Elemente des Berichts (stellt Datenquelle dar) an die Elemente des Datenmodells, das auf Basis des ausgewählten Stammartikel des Modells gefiltert wird.  
7. Wählen Sie in der Struktur Archivkopfzeile erweitern.
8. Wählen Sie in der Struktur Archivkopfzeile\Archivzeilen erweitern.
9. Erweitern Sie in der Struktur Format.
10. In der Struktur erweitern Sie Format\Erklärung: XML Element (Erklärung).
11. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten).
12. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten)\Artikel: XML Element 0..* (Artikel).
13. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten)\Artikel: XML. Element 0..* (Artikel)\Dim3: XML Element 1..1 (Betrag).
14. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten)\Artikel: XML. Element 0..* (Artikel)\Dim4: XML Element 1..1 (Artikel).
15. Wählen Sie in der Struktur Archivkopfzeile\Anzahl Zeilen aus.
16. Klicken Sie auf "Bearbeiten".
17. Wählen Sie in der Liste\COUNT aus.
18. Klicken Sie auf Funktion hinzufügen.
19. Erweitern Sie in der Struktur Format.
20. In der Struktur erweitern Sie Format\Erklärung: XML Element (Erklärung).
21. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten).
22. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten)\Element: XML Element 0..* (Element).
23. Klicken Sie auf Datenquelle hinzufügen.
24. Auf Formelfeld bestimmt geben Sie " ANZAHL (format.Declaration.Data.Item)" ein.
    * ANZAHL (format.Declaration.Data.Item)  
25. Klicken Sie auf "Speichern".
26. Schließen Sie die Seite.
27. Wählen Sie in der Struktur Archivkopfzeile\Dateiname aus.
28. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten)\Dateiname: Element:Zeichenfolge(Dateiname).
29. Klicken Sie auf Binden.
30. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten)\Artikel: XML. Element 0.. * (Artikel)\Dim4: XML Element 1..1 (Element)\Anzahl: Zeichenfolge(Anzahl).
31. Wählen Sie in der Struktur Archivkopfzeile\Archivzeilen\Elementzahl aus.
32. Klicken Sie auf Binden.
33. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten:\XML Element 1..*(Daten)\Artikel: XML. Element 0..* (Artikel)\Dim3: XML Element 1..1 (Betrag)\Wert: Numerisch (Wert).
34. Wählen Sie in der Struktur Archivkopfzeile\Archivzeilen\Betrag aus.
35. Klicken Sie auf Binden.
36. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML Element (Erklärung)\Daten: XML-Element 1..* (Daten)\Element: XML Element 0...* (Artikel)\Waren Rec. ID. Element Int64(Waren rec-ID).
37. Wählen Sie in der Struktur Archivkopfzeile\Archivzeilen\Waren rec id aus.
38. Klicken Sie auf Binden.
39. Wählen Sie in der Struktur Archivkopfzeile\Archivzeilen aus.
40. Wählen Sie in der Strukturdarstellung Format\Erklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten)\Element: XML Element 0..* (Element).
41. Klicken Sie auf Binden.
42. Wählen Sie in der Struktur Archivkopfzeile.
43. Wählen Sie in der Strukturdarstellung formatErklärung: XML-Element (Erklärung)\Daten: XML Element 1..*(Daten).
44. Klicken Sie auf Binden.
45. Klicken Sie auf "Speichern".
46. Schließen Sie die Seite.
47. Schließen Sie die Seite.
48. Schließen Sie die Seite.

