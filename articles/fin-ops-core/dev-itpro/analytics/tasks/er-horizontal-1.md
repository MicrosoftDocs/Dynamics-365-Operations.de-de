---
title: 'ER Horizontal erweiterbare Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten nutzen (Teil 1: Designformat)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Format (elektronische Berichterstellung) konfigurieren, um Berichte als Excel-Dateien (OPENXML-Arbeitsblätter) zu generieren. (Teil 1)
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab360c259af37ce3995d3cd2560bc2e765e0bceb
ms.sourcegitcommit: e3290eb58ae569a59d6ae2e6922e7d8be8f1980f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "7551775"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Horizontal erweiterbare Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten nutzen (Teil 1: Designformat)

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie einem Benutzer mit der Rolle Systemadministrator oder elektronischer Berichterstellungsentwickler ein Elektronische Berichterstellung-Format (ER) zur Generierung von Berichten als OPENXML-Arbeitsblätter (Excel) konfigurieren kann, in dem die erforderlichen Spalten als horizontal erweiterbare Bereiche erstellt werden können. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte ausgeführt, auszuführen, müssen Sie diese zuerst in diesen drei Aufgabenleitfäden ausführen:

„ER Konfigurationsanbieter erstellen und als aktiv markieren“

„ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 1: Datenmodell entwerfen)“

„ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 2: Modellzuordnung)“

Sie müssen auch eine lokale Kopie der Vorlage mit einem Beispielbericht herunterladen und speichern, die hier unter [Muster Finanzdimensions-Dienstleistungsbericht](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx) gefunden wird.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.

## <a name="create-a-new-report-configuration"></a>Erstellen einer neuen Berichtskonfiguration

1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Wählen Sie in der Struktur `Financial dimensions sample model` aus.
3. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
4. Geben Sie im Feld `Format based on data model Financial dimensions sample model` „Neu“ ein.
    * Verwenden Sie das Modell, die im Voraus als Datenquelle für den neuen Bericht erstellt wurde.  
5. Geben Sie im Feld „Name“ „`Sample report with horizontally expandable ranges`“ ein.
    * Beispielbericht mit horizontal erweiterbaren Bereichen  
6. Geben Sie im Feld „Beschreibung“ `To make Excel output with dynamically adding columns` ein.
    * Um Excel-Ausgaben mit dynamisch hinzugefügten Spalten zu erstellen  
7. Wählen Sie im Feld "Datenmodelldefinition" "Erfassung" aus.
8. Klicken Sie auf Konfiguration erstellen.

## <a name="design-the-report-format"></a>Entwerfen des Berichtsformats

1. Klicken Sie auf Designer.
2. Aktivieren Sie die Umschaltfläche `Show details`.
3. Klicken Sie im Aktivitätsbereich auf "Importieren".
4. Klicken Sie auf "Aus Excel importieren".
5. Klicken Sie auf Anhänge.
    * Importieren Sie die Vorlage des Berichts. Verwenden Sie hierzu die heruntergeladene Excel-Datei.  
6. Klicken Sie auf Neu.
7. Klicken Sie auf "Datei".
8. Schließen Sie die Seite.
9. Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die heruntergeladene Vorlage aus.  
10. Klicken Sie auf "OK".
    * Fügt einen neuen Bereich hinzu, um eine Excel-Ausgabe dynamisch mit so vielen Spalten zu erstellen wie Sie für Finanzdimensionen ausgewählt haben (im Benutzerdialogfeldformular). Jede Zelle für jede Spalte steht für den Namen einer einzelnen Finanzdimension.  
11. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
12. Wählen Sie in der Struktur `Excel\Range` aus.
13. Geben Sie im Feld „Excel-Bereich“ `DimNames` ein.
    * DimNames  
14. Wählen Sie im Feld „Replikationsrichtung“ `Horizontal` aus.
15. Klicken Sie auf "OK".
16. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` aus.
17. Klicken Sie auf "Nach oben verschieben".
18. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Cell<DimNames>` aus.
19. Klicken Sie auf Ausschneiden.
20. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` aus.
21. Klicken Sie auf Einfügen.
22. Erweitern Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
23. Erweitern Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
24. Erweitern Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
25. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` aus.
    * Fügt einen neuen Bereich hinzu, um eine Excel-Ausgabe dynamisch mit so vielen Spalten zu erstellen wie Sie für Finanzdimensionen ausgewählt haben (im Benutzerdialogfeldformular). Jede Zelle für jede Spalte steht einen einzelnen Finanzdimensionwert für jede Berichtstransaktion dar.  
26. Klicken Sie auf "Bereich hinzufügen".
27. Geben Sie im Feld „Excel-Bereich“ `DimValues` ein.
    * DimValues  
28. Wählen Sie im Feld „Replikationsrichtung“ `Horizontal` aus.
29. Klicken Sie auf "OK".
30. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>` aus.
31. Klicken Sie auf Ausschneiden.
32. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` aus.
33. Klicken Sie auf Einfügen.
34. Erweitern Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.

## <a name="map-format-elements-to-data-sources"></a>Zuweisen von Formatkomponenten zu Datenquellen

1. Klicken Sie auf die Registerkarte Zuordnung.
2. Erweitern Sie in der Struktur `model: Data model Financial dimensions sample model`.
3. Erweitern Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list`.
4. Erweitern Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
5. Erweitern Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
6. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>` aus.
7. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String` aus.
8. Klicken Sie auf Binden.
9. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` aus.
10. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list` aus.
11. Klicken Sie auf Binden.
12. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>` aus.
13. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real` aus.
14. Klicken Sie auf Binden.
15. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>` aus.
16. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real` aus.
17. Klicken Sie auf Binden.
18. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>` aus.
19. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String` aus.
20. Klicken Sie auf Binden.
21. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>` aus.
22. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date` aus.
23. Klicken Sie auf Binden.
24. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>` aus.
25. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String` aus.
26. Klicken Sie auf Binden.
27. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>` aus.
28. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String` aus.
29. Klicken Sie auf Binden.
30. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` aus.
31. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list` aus.
32. Klicken Sie auf Binden.
33. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>` aus.
34. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String` aus.
35. Klicken Sie auf Binden.
36. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical` aus.
37. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Journal: Record list` aus.
38. Klicken Sie auf Binden.
39. Erweitern Sie in der Struktur `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
40. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String` aus.
41. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>` aus.
42. Klicken Sie auf Binden.
43. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Dimensions setting: Record list` aus.
44. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` aus.
45. Klicken Sie auf Binden.
46. Wählen Sie in der Struktur `Excel = "SampleFinDimWsReport"\Cell<CompanyName>` aus.
47. Wählen Sie in der Struktur `model: Data model Financial dimensions sample model\Company: String` aus.
48. Klicken Sie auf Binden.
49. Klicken Sie auf Speichern.
50. Schließen Sie die Seite.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
