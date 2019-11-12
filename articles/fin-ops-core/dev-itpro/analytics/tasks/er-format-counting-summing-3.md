---
title: 'ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 3: Nutzen von Berechnungen für die Ausgabe)'
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbef7048488056f50ec8967a9af53d468666856
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550762"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 3: Nutzen von Berechnungen für die Ausgabe)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 2: Berechnungen konfigurieren)" ausführen.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Konfigurieren Sie diesen Bericht für Inventarisierungs- und Zusammenfassungsinformationen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Erweitern Sie 'Intrastatmodell' in der Struktur.
4. Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".
5. Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.
6. Klicken Sie auf Designer.
7. Klicken Sie auf die Registerkarte Zuordnung.
8. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
    * Fügen Sie eine neue Datenquelle hinzu, um die Liste der gemerkten Blöcken abzurufen.  
9. Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.
10. Geben Sie im Feld "Name" "$BlocksList" ein.
    * $BlocksList  
11. Klicken Sie auf Formel bearbeiten.
12. Wählen Sie in der Strukturdarstellung 'Data collection functions\COLLECTEDLIST'.
13. Klicken Sie auf Funktion hinzufügen.
14. Klicken Sie auf Datenquelle hinzufügen.
15. Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', ' ein.
    * COLLECTEDLIST('$BlockName',  
16. Geben Sie im Feld 'Formel' 'COLLECTEDLIST('$BlockName', "*")' ein.
    * COLLECTEDLIST('$BlockName', "*")  
17. Klicken Sie auf "Speichern".
    * Das Muster "*" bedeutet, dass alle Blöcke der Liste für diesen Datensatz enthalten sind.  
18. Schließen Sie die Seite.
19. Klicken Sie auf "OK".
20. Klicken Sie auf die Registerkarte 'Format'.
21. Wählen Sie in der Struktur "Intrastat\Data" aus.
22. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
23. Wählen Sie in der Struktur 'Text\Sequence'..
24. Geben Sie im Feld "Name" die Zeichenfolge "Summen nach Blöcken' ein.
    * Summen nach Blöcken  
25. Wählen Sie im Feld "Sonderzeichen" "Neue Zeile - Windows (CR LF)".
26. Klicken Sie auf "OK".
27. Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks'.
28. Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".
29. Wählen Sie in der Struktur 'Text\String' aus.
30. Geben Sie im Feld "Name" "Block code" ein.
    * Blockcode  
31. Klicken Sie auf "OK".
32. Klicken Sie auf "Zeichenfolge hinzufügen".
33. Geben Sie im Feld "Name" 'Lines counting' ein.
    * Inventarisierte Positionen  
34. Klicken Sie auf "OK".
35. Klicken Sie auf "Zeichenfolge hinzufügen".
36. Geben Sie im Feld Name "Total amount" ein.
    * Gesamtstundenzahl  
37. Klicken Sie auf "OK".
38. Klicken Sie auf die Registerkarte Zuordnung.
39. Wählen Sie in der Struktur '$BlocksList' aus.
40. Klicken Sie auf Binden.
    * Erstellen Sie eine Zusammenfassungsposition für jeden gemerkten Block.  
41. Klicken Sie auf die Registerkarte 'Format'.
42. Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Block code'.
43. Klicken Sie auf die Registerkarte Zuordnung.
44. Klicken Sie auf Formel bearbeiten.
45. Geben Sie im Feld 'Formel' '"Block id: " & ' ein.
    * "Block id: " &  
46. Erweitern Sie in der Struktur '$BlocksList'.
47. Wählen Sie in der Struktur '$BlocksList\Value'.
48. Klicken Sie auf Datenquelle hinzufügen.
49. Klicken Sie auf "Speichern".
50. Schließen Sie die Seite.
51. Klicken Sie auf die Registerkarte 'Format'.
52. Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Lines counting'.
53. Klicken Sie auf die Registerkarte Zuordnung.
54. Klicken Sie auf Formel bearbeiten.
    * Erstellen Sie eine Ausgabe für die Anzahl der Positionen für jeden Block in diesen Bericht.  
55. Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & ' ein.
    * "Anzahl der Positionen in diesem Block: " &  
56. Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT('.
    * "Anzahl der Positionen in diesem Block: " & TEXT(  
57. Wählen Sie in der Strukturdarstellung 'Data collection functions\COUNTIFS'.
58. Klicken Sie auf Funktion hinzufügen.
59. Klicken Sie auf Datenquelle hinzufügen.
60. Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '.
    * "Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName',  
61. Erweitern Sie in der Struktur '$BlocksList'.
62. Wählen Sie in der Struktur '$BlocksList\Value'.
63. Klicken Sie auf Datenquelle hinzufügen.
64. Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.
    * "Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Wählen Sie in der Struktur '$RecName' aus.
66. Klicken Sie auf Datenquelle hinzufügen.
67. Geben Sie im Feld Formel '"Anzahl Zeilen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.
    * "Anzahl der Positionen in diesem Block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Klicken Sie auf "Speichern".
69. Schließen Sie die Seite.
70. Klicken Sie auf die Registerkarte 'Format'.
71. Wählen Sie in der Struktur 'Intrastat\Data\Totals by blocks\Total amount'.
72. Klicken Sie auf die Registerkarte Zuordnung.
73. Klicken Sie auf Formel bearbeiten.
    * Erstellen Sie eine Ausgabe mit dem fakturierten Gesamtbetrag für jeden Block im Bericht.  
74. Geben Sie im Feld Formel '"Summe des berechneten Betrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.
    * "Summe des Rechnungsbetrags: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Klicken Sie auf "Speichern".
76. Schließen Sie die Seite.
77. Klicken Sie auf "Speichern".
78. Schließen Sie die Seite.

