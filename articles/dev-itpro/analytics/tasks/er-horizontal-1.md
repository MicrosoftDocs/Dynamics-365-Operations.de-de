--- 
title: "Ein Format zur Verwendung von horizontal erweiterbaren Bereichen zum dynamischen Hinzufügen von Spalten in Excel-Berichten entwerfen"
description: "In den folgenden Schritten wird erläutert, wie einem Benutzer mit der Rolle Systemadministrator oder elektronischer Berichterstellungsentwickler ein Elektronische Berichterstellung-Format (ER) zur Generierung von Berichten als OPENXML-Arbeitsblätter (Excel) konfigurieren kann, in dem die erforderlichen Spalten als horizontal erweiterbare Bereiche erstellt werden können."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9c3cf17cd406a50a9f92e78991289f9139d7c73
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a>Ein Format zur Verwendung von horizontal erweiterbaren Bereichen zum dynamischen Hinzufügen von Spalten in Excel-Berichten entwerfen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie einem Benutzer mit der Rolle Systemadministrator oder elektronischer Berichterstellungsentwickler ein Elektronische Berichterstellung-Format (ER) zur Generierung von Berichten als OPENXML-Arbeitsblätter (Excel) konfigurieren kann, in dem die erforderlichen Spalten als horizontal erweiterbare Bereiche erstellt werden können. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte ausgeführt, auszuführen, müssen Sie diese zuerst in diesen drei Aufgabenleitfäden ausführen: 

"ER Konfigurationsanbieter erstellen und als aktiv markieren"

"ER - Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Designdatenmodell)"

"ER - Verwendung von Finanzdimensionen als Datenquelle (Teil 2: Modellzuordnung)"

Sie müssen auch eine lokale Kopie der Vorlage mit einen Beispielbericht herunterladen und speichern, den Sie hier finden [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266). 


Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


## <a name="create-a-new-report-configuration"></a>Erstellen einer neuen Berichtskonfiguration
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".
3. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
4. Geben Sie im Feld "Neu" "Format basierend auf Finandimensions-Beispieldatenmodell" ein.
    * Verwenden Sie das Modell, die im Voraus als Datenquelle für den neuen Bericht erstellt wurde.  
5. Geben Sie im Feld "Name" "Beispielbericht mit horizontal erweiterbaren Bereichen" ein.
    * Beispielbericht mit horizontal erweiterbaren Bereichen  
6. Geben Sie im Feld "Beschreibung" "Für Excel-Ausgaben mit dynamisch hinzugefügten Spalten" ein.
    * Um Excel-Ausgaben mit dynamisch hinzugefügten Spalten zu erstellen  
7. Wählen Sie im Feld "Datenmodelldefinition" "Erfassung" aus.
8. Klicken Sie auf Konfiguration erstellen.

## <a name="design-the-report-format"></a>Entwerfen des Berichtsformats
1. Klicken Sie auf Designer.
2. Aktivieren Sie die Umschaltfläche "Detaildaten anzeigen".
3. Klicken Sie im Aktivitätsbereich auf "Importieren".
4. Klicken Sie auf "Aus Excel importieren".
5. Klicken Sie auf Anhänge.
    * Importieren Sie die Vorlage des Berichts. Verwenden Sie hierzu die heruntergeladene Excel-Datei.  
6. Klicken Sie auf "Neu".
7. Klicken Sie auf "Datei".
8. Schließen Sie die Seite.
9. Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die heruntergeladene Vorlage aus.  
10. Klicken Sie auf "OK".
    * Fügt einen neuen Bereich hinzu, um eine Excel-Ausgabe dynamisch mit so vielen Spalten zu erstellen wie Sie für Finanzdimensionen ausgewählt haben (im Benutzerdialogfeldformular). Jede Zelle für jede Spalte steht für den Namen einer einzelnen Finanzdimension.  
11. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
12. Wählen Sie in der Struktur 'Excel\Bereich' aus.
13. Im Feld "Excel-Bereich" geben Sie "DimNames" ein.
    * DimNames  
14. Wählen Sie im Feld "Replikationsrichtung" "Horizontal" aus.
15. Klicken Sie auf "OK".
16. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<DimNames>: Horizontal' aus.
17. Klicken Sie auf "Nach oben verschieben".
18. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Zelle<DimNames>' aus.
19. Klicken Sie auf Ausschneiden.
20. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<DimNames>: Horizontal' aus.
21. Klicken Sie auf Einfügen.
22. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<DimNames>: Horizontal' aus.
23. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>: Vertikal' aus.
24. Erweitern Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\BEreich<TransactionLine>: Vertikal'.
25. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal'.
    * Fügt einen neuen Bereich hinzu, um eine Excel-Ausgabe dynamisch mit so vielen Spalten zu erstellen wie Sie für Finanzdimensionen ausgewählt haben (im Benutzerdialogfeldformular). Jede Zelle für jede Spalte steht einen einzelnen Finanzdimensionwert für jede Berichtstransaktion dar.  
26. Klicken Sie auf "Bereich hinzufügen".
27. Im Feld "Excel-Bereich" geben Sie "DimValues" ein.
    * DimValues  
28. Wählen Sie im Feld "Replikationsrichtung" "Horizontal" aus.
29. Klicken Sie auf "OK".
30. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Zell<DimValues>
31. Klicken Sie auf Ausschneiden.
32. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Bereich\Horizontal<DimValues>
33. Klicken Sie auf Einfügen.
34. Erweitern Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Bereich\Horizontal<DimValues>

## <a name="map-format-elements-to-data-sources"></a>Zuweisen von Formatkomponenten zu Datenquellen
1. Klicken Sie auf die Registerkarte Zuordnung.
2. In der Struktur erweitern Sie "Modell: Datenmodell-Finanzdimensionsbeispielmodell".
3. In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.
4. In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.
5. In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.
6. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReportBereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Bereich<DimValues>\Horizontal\Zelle<DimValues>.
7. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste\Code: String'.
8. Klicken Sie auf Binden.
9. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Bereich\Horizontal<DimValues>
10. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Dimensionsdaten: Datensatzliste'.
11. Klicken Sie auf Binden.
12. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Zell<Credit>
13. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Haben: Gleitkommazahl'.
14. Klicken Sie auf Binden.
15. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Zell<Debit>
16. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Soll: Gleitkommazahl'.
17. Klicken Sie auf Binden.
18. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Zell<Currency>
19. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Währung: String'.
20. Klicken Sie auf Binden.
21. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Zell<TransDate>
22. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Datum: Datum'.
23. Klicken Sie auf Binden.
24. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Zell<TransVoucher>
25. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste\Beleg: String'.
26. Klicken Sie auf Binden.
27. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal\Zell<TransBatch>
28. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste\Charge: String'.
29. Klicken Sie auf Binden.
30. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Bereich<TransactionLine>: Vertikal'.
31. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Transaktion: Datensatzliste'.
32. Klicken Sie auf Binden.
33. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal\Zelle<Batch>.
34. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste\Charge: String'.
35. Klicken Sie auf Binden.
36. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<JournalLine>Vertikal.
37. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Erfassung: Datensatzliste'.
38. Klicken Sie auf Binden.
39. In der Struktur erweitern Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Dimensionseinstellung: Datensatzliste'.
40. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Dimensionseinstellung: Datensatzliste\Code: String'.
41. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<DimNames> Horizontal\Zelle<DimNames>aus.
42. Klicken Sie auf Binden.
43. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Dimensionseinstellung: Datensatzliste'.
44. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Bereich<DimNames>: Horizontal' aus.
45. Klicken Sie auf Binden.
46. Wählen Sie in der Struktur 'Excel = "SampleFinDimWsReport"\Zelle<CompanyName>' aus.
47. In der Struktur wählen Sie 'Modell: Datenmodell Finanzdimensionen-Beispielmodell\Unternehmen: String'.
48. Klicken Sie auf Binden.
49. Klicken Sie auf "Speichern".
50. Schließen Sie die Seite.


