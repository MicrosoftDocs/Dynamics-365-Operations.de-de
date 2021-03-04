---
title: 'ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 2: Konfigurieren von Berechnungen)'
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9314a8cd5838333a20dd59dfb52f80a43d89b8c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684690"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a>ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 2: Konfigurieren von Berechnungen)

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden „ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 1: Format erstellen)“ ausführen.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Erstellen einer Formatkonfiguration, um Inventarisierungs- und Zusammenfassungsdetails hinzuzufügen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Erweitern Sie 'Intrastatmodell' in der Struktur.
4. Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.
    * Angenommen, Sie müssen das Format anpassen, das von Microsoft bereitgestellten wird, indem Sie Positionen mit zusammengefassten Details am Ende des Intrastat-Berichts hinzufügen. Hierzu müssen Sie eine eigene Instanz der Intrastat-Konfiguration von der Microsoft-Instanz ableiten.  
5. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
6. Geben Sie im Feld "Neu" "Von Name ableiten: Intrastat (DE), Microsoft" ein.
7. Geben Sie im Feld Name "Intrastat (DE) mit Inventur und Zusammenfassung' ein.
8. Klicken Sie auf Konfiguration erstellen.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Konfigurieren Sie diesen Bericht, um eine Inventur und Zusammenfassung auf Basis der Ausgabedetails durchzuführen.
1. Klicken Sie auf Designer.
2. Wählen Sie die Option Ja im Feld "Ausgabendetails sammeln" aus.
    * Diese Markierung aktiviert zur Bearbeitungszeit die Sammlung von Ausgabeinformationen für die Generierung der Intrastatdatei.  
    * Sie müssen eine Inventur für Intrastat-Richtungen ausführen. Fügen Sie daher eine dedizierte Modellenumeration zur Liste der Datenquellen der Formatkonfiguration hinzu.  
3. Klicken Sie auf die Registerkarte Zuordnung.
4. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
5. Wählen Sie in der Strukturdarstellung "Data model\Enumeration" aus.
6. Geben Sie im Feld "Name" "Richtung" ein.
7. Geben Sie im Feld "Modellenumeration" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie den Wert Richtung aus.  
8. Klicken Sie auf "OK".
9. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
10. Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.
11. Geben Sie im Feld "Name" "$BlockName" ein.
12. Klicken Sie auf Formel bearbeiten.
13. Geben Sie im Feld 'Formel' "block" ein.
14. Klicken Sie auf "Speichern".
15. Schließen Sie die Seite.
16. Klicken Sie auf "OK".
17. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
18. Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.
19. Geben Sie im Feld Name "$RecName" ein.
20. Klicken Sie auf Formel bearbeiten.
21. Geben Sie im Feld 'Formel' "record" ein.
22. Klicken Sie auf "Speichern".
23. Schließen Sie die Seite.
24. Klicken Sie auf "OK".
25. Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.
26. Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.
27. Geben Sie im Feld "Name" '$InvName' ein.
28. Klicken Sie auf Formel bearbeiten.
29. Geben Sie im Feld 'Formel' "InvoicedAmountEUR" ein.
30. Klicken Sie auf "Speichern".
31. Schließen Sie die Seite.
32. Klicken Sie auf "OK".
33. Wählen Sie in der Struktur "Intrastat\Data" aus.
34. Klicken Sie auf die Schaltfläche „Bearbeiten“ für das Feld „Gesammelter Datenschlüsselname“.
35. Klicken Sie auf Datenquelle hinzufügen.
    * $BlockName  
36. Klicken Sie auf Speichern.
37. Schließen Sie die Seite.
38. Klicken Sie auf die Schaltfläche "Bearbeiten" für das Feld "Gesammelter Datenschlüsselwert".
39. Geben Sie im Feld Formel 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")' ein.
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Klicken Sie auf "Speichern".
41. Schließen Sie die Seite.
    * Positionen dieses Nummernkreises zählen. Die Ergebnisse werden mit dem Namen „block“ für unterschiedliche Richtungen separat verwendet. Der Wert „Import“ wird für beliebige Eingangs-Intrastat-Buchungen verwendet. Der Wert „Export“ wird für beliebige Abgangs-Intrastat-Buchungen verwendet. Nutzen Sie dies als virtuelles Excel-Arbeitsblatt. Für jede Buchung einer Zeile, in der die erste Spalte „block“ die Werte „Import“ und „Export“ hat.  
42. Erweitern Sie 'Intrastat\Data: Sequence' in der Struktur.
43. Wählen Sie 'Intrastat\Data: Sequence\Arrivals?'.
44. Klicken Sie auf die Schaltfläche „Bearbeiten“ für das Feld „Gesammelter Datenschlüsselname“.
    * Positionen dieses Nummernkreises zählen. Die Ergebnisse werden unter dem Namen „Record“ gespeichert.  
45. Wählen Sie in der Struktur '$RecName' aus.
46. Klicken Sie auf Datenquelle hinzufügen.
47. Klicken Sie auf Speichern.
48. Schließen Sie die Seite.
49. Klicken Sie auf die Schaltfläche „Bearbeiten“ für das Feld „Gesammelter Datenschlüsselwert“.
50. Geben Sie im Feld Formel "Intrastat.CommodityRecord.CommodityCode" ein.
51. Klicken Sie auf "Speichern".
52. Schließen Sie die Seite.
    * Positionen dieses Nummernkreises zählen. Die Ergebnisse werden mit dem Namen „record“ für unterschiedliche Warencodes separat verwendet. Nutzen Sie dies als virtuelles Excel-Arbeitsblatt. Für jede Buchung wird eine Zeile ausgefüllt, in der die erste Spalte „block“ mit den Werten „Import“ und „Export“ und der zweite und Block „record“ mit dem Warencodewert ausgefüllt wird.  
53. Wählen Sie in der Struktur "Intrastat\Data: Sequence\Dispatches?' aus.
54. Klicken Sie auf die Schaltfläche „Bearbeiten“ für das Feld „Gesammelter Datenschlüsselname“.
55. Wählen Sie in der Struktur '$RecName' aus.
56. Klicken Sie auf Datenquelle hinzufügen.
57. Klicken Sie auf Speichern.
58. Schließen Sie die Seite.
59. Klicken Sie auf die Schaltfläche „Bearbeiten“ für das Feld „Gesammelter Datenschlüsselwert“.
60. Geben Sie im Feld Formel "Intrastat.CommodityRecord.CommodityCode" ein.
61. Klicken Sie auf Speichern.
62. Schließen Sie die Seite.
63. Erweitern Sie 'Intrastat\Data: Sequence\Dispatches: Sequence?' in der Struktur.
64. Erweitern Sie 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord'' in der Struktur.
65. Klicken Sie auf die Registerkarte 'Format'.
66. Wählen Sie in der Strukturdarstellung 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.
67. Klicken Sie auf die Registerkarte Zuordnung.
68. Klicken Sie auf die Schaltfläche „Bearbeiten“ für das Feld „Gesammelter Datenschlüsselname“.
69. Wählen Sie in der Struktur '$InvName' aus.
70. Klicken Sie auf Datenquelle hinzufügen.
71. Klicken Sie auf "Speichern".
72. Schließen Sie die Seite.
    * Zusammenfassen des fakturierten Betrags für Positionen dieser Sequenz Die Ergebnisse werden mit dem Namen „InvoicedAmountEUR“ für unterschiedliche Intrastat-Richtungen und Warencodes separat verwendet. Nutzen Sie dies als virtuelles Excel-Arbeitsblatt. Für jede Buchung einer Zeile, in der die erste Spalte „block“ die Werte „Import“ und „Export“ hat. Der zweite Block „record“ wird mit dem Warencodewert ausgefüllt, und die dritte Spalte „InvoicedAmountEUR“ wird mit dem Rechnungsbetrag ausgefüllt.  
73. Erweitern Sie 'Intrastat\Data\Arrivals?' in der Struktur.
74. Erweitern Sie 'Intrastat\Data: Arrivals?\Record = Intrastat.CommodityRecord'' in der Struktur.
75. Klicken Sie auf die Registerkarte 'Format'.
76. Wählen Sie in der Strukturdarstellung 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.
77. Klicken Sie auf die Registerkarte Zuordnung.
78. Klicken Sie auf die Schaltfläche „Bearbeiten“ für das Feld „Gesammelter Datenschlüsselname“.
79. Wählen Sie in der Struktur '$InvName' aus.
80. Klicken Sie auf Datenquelle hinzufügen.
81. Klicken Sie auf "Speichern".
82. Schließen Sie die Seite.
83. Klicken Sie auf "Speichern".
84. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]