---
title: Verwenden von Modellzuordnungskonfigurationen für aggregierte Berechnungen auf Datenbankebene
description: Diese Prozedur bietet Informationen darüber, wie eine neue Modellzuordnungskonfiguration für elektronische Berichterstellung (EB) entworfen wird und wie integrierte EB-Funktionen für effiziente Aggregationsberechnungen verwendet werden.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3084882dd4b51f067793b3a7999ce89cda1257d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184599"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Verwenden von Modellzuordnungskonfigurationen für aggregierte Berechnungen auf Datenbankebene

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur bietet Informationen darüber, wie eine neue Modellzuordnungskonfiguration für elektronische Berichterstellung (EB) entworfen wird und wie integrierte EB-Funktionen für effiziente Aggregationsberechnungen verwendet werden. In dieser Prozedur erstellen Sie eine Konfiguration für das Beispielunternehmen Litware, Inc. 

Diese Prozedur wird für Benutzer erstellt, die die Rolle des Systemadministrators oder des Entwicklers für elektronische Berichterstellung haben, die ihnen zugewiesen sind. Diese Schritte können mithilfe eines beliebigen Dataset abgeschlossen werden.

 Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in der Prozedur „EB verbessert die Effizienz von Aggregationsberechnungen, indem sie auf Datenbankebene ausgeführt werden (Teil 1: Konfigurationen vorbereiten)” abschließen.

1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie 'Intrastatmodell' in der Struktur.
3. Wählen Sie in der Struktur „Intrastat-Modell\Intrastat-Beispielzuordnung” aus.
4. Klicken Sie auf Designer.
5. Klicken Sie auf Designer.
6. Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabellendatensätze' aus.
7. Klicken Sie auf "Stamm hinzufügen".
    * Fügen Sie eine neue Datenquelle hinzu, die Datensätze darstellt, die Sie gruppieren möchten.  
8. Geben Sie im Feld "Name" 'Transactions' ein.
    * Buchungen  
9. Im Feld „Tabelle” geben Sie „Intrastat” ein.
    * Intrastat  
10. Klicken Sie auf "OK".
11. Wählen Sie in der Struktur "Funktionen\Gruppieren nach" aus.
    * Dieser Datenquellentyp wird verwendet, um eine neue Datenquelle zur Laufzeit einzuführen, um Datensätze zu gruppieren und erforderliche Aggregationen zu berechnen.  
12. Klicken Sie auf "Stamm hinzufügen".
13. Geben Sie im Feld „Name” die Bezeichnung „TransactionsGroups” ein.
    * TransactionsGroups  
14. Klicken Sie auf "Gruppe bearbeiten von".
15. Wählen Sie in der Struktur 'Transactions' aus.
    * Wählen Sie die hinzugefügte Datenquelle des Typs „Datensatzlisten” aus, die die Datensätze darstellt, die Sie gruppieren möchten.  
16. Klicken Sie auf "Feld hinzufügen zu".
17. Klicken Sie auf "Was gruppieren".
18. Erweitern Sie in der Struktur den Knoten 'Transactions'.
19. Wählen Sie in der Struktur „Transaktionen\Richtung” aus.
20. Klicken Sie auf "Feld hinzufügen zu".
21. Klicken Sie auf "Gruppierte Felder".
    * Wählen Sie das Feld aus, um die Gruppierungsebene anzugeben. Basierend auf dieser Auswahl gibt die Datenquelle zur Laufzeit so viele Buchungsgruppen zurück, wie es Richtungscodes gibt, die in der Intrastat-Tabelle auftauchen.  
22. Wählen Sie in der Struktur „Transaktionen\Rechnungsbetrag(AmountMST)” aus.
    * Wählen Sie das Feld aus, um die Quelle für die Aggregationsberechnung anzugeben.  
23. Klicken Sie auf "Feld hinzufügen zu".
24. Klicken Sie auf "Aggregationsfelder".
25. Markieren Sie in der Liste die ausgewählte Zeile.
26. Wählen Sie im Feld „Methode” die Option „Summe” aus.
    * Wählen Sie den Aggregationstyp aus.  
27. Geben Sie im Feld „Name” die Bezeichnung „SumOfAmountMST” ein.
    * Geben Sie den Namen der Aggregation in der konfigurierten Datenquelle an.  
28. Klicken Sie auf "Speichern".
    * Beachten Sie, dass das Feld „Ausführung bei” angibt, dass diese Gruppierung zur Laufzeit in der SQL-Datenbank ausgeführt wird.  
29. Schließen Sie die Seite.
30. Klicken Sie auf "OK".
31. Erweitern Sie in der Struktur die Option „Summen”.
32. In der Struktur erweitern Sie „TransactionsGroups”.
33. In der Struktur erweitern Sie „TransactionsGroups\aggregiert”.
34. Wählen Sie „TransactionsGroups\aggregiert\SumOfAmountMST” in der Struktur aus.
35. Wählen Sie „Summen\Gesamtrechnungswert(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')” in der Struktur aus.
36. Klicken Sie auf Binden.
    * Basierend auf dieser Einstellung berechnet diese Datenquelle die Summe der Werte des Felds „AmountMST” für alle einzelnen Gruppen von Buchungen. Diese Aggregationsberechnung ist als TransactionsGroups.aggregated.TotalAmount-Artikel verfügbar.  
37. In der Struktur erweitern Sie „TransactionsGroups”.
38. Wählen Sie in der Struktur „TransactionsGroups” aus.
39. Klicken Sie auf "Bearbeiten".
40. Klicken Sie auf "Gruppe bearbeiten von".
41. Erweitern Sie in der Struktur den Knoten 'Transactions'.
42. Wählen Sie in der Struktur „Transaktionen\Rechnungsbetrag(AmountMST)” aus.
43. Klicken Sie auf "Feld hinzufügen zu".
44. Klicken Sie auf "Aggregationsfelder".
45. Markieren Sie in der Liste die ausgewählte Zeile.
46. Wählen Sie im Feld „Methode” die Option „Max.” aus.
47. Geben Sie im Feld „Name” die Bezeichnung „MaxOfAmountMST” ein.
48. Klicken Sie auf "Speichern".
    * Aktuell kann die Ausführung von GROUPBY-Datenquellen mit einigen Einschränkungen in die SQL-Datenbankebene übersetzt werden. Übersetzung kann entweder für Datenquellen des Typs „Datensatzliste” durchgeführt werden oder für Datenquellen, die als ein Ausdruck mithilfe der FILTER-Funktion dargestellt werden. Sie kann auch erfolgen, wenn die einzige Aggregation für ein einzelnes Feld der Gruppierungsdatensätze konfiguriert wird.  
    * Beachten Sie, dass, obwohl mehr als eine Aggregation für das Feld „AmountMST” konfiguriert wurde, das Feld „Ausführung bei” immer noch angibt, dass diese Gruppierung zur Laufzeit in der SQL-Datenbank ausgeführt wird. Dies liegt daran, dass nur eine Aggregation an den Datenmodellartikel gebunden ist und zur Laufzeit verwendet wird, um Daten aus dieser Datenquelle zu ziehen.  
49. Schließen Sie die Seite.
50. Klicken Sie auf "OK".
51. In der Struktur erweitern Sie „TransactionsGroups”.
52. In der Struktur erweitern Sie „TransactionsGroups\aggregiert”.
53. Wählen Sie „TransactionsGroups\aggregiert\MaxOfAmountMST” in der Struktur aus.
54. Wählen Sie „Summen\Gesamter statistischer Wert(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')” in der Struktur aus.
55. Klicken Sie auf Binden.
56. In der Struktur erweitern Sie „TransactionsGroups”.
57. Wählen Sie in der Struktur „TransactionsGroups” aus.
58. Klicken Sie auf "Bearbeiten".
59. Klicken Sie auf "Gruppe bearbeiten von".
    * Beachten Sie, dass das Feld „Ausführung bei” angibt, dass diese Gruppierung zur Laufzeit im Arbeitsspeicher ausgeführt wird, da beide Aggregationen desselben Felds an die Datenmodellartikel gebunden sind.   
60. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
61. Klicken Sie auf Löschen.
62. Klicken Sie auf "Ja".
63. Klicken Sie auf Löschen.
64. Klicken Sie auf "Ja".
65. Klicken Sie auf "Feld hinzufügen zu".
66. Klicken Sie auf "Was gruppieren".
67. Erweitern Sie „Warendatensatz(Intrastat)” in der Struktur.
68. Klicken Sie auf "Speichern".
    * Beachten Sie, dass das Feld „Ausführung bei” angibt, dass diese Gruppierung zur Laufzeit im Arbeitsspeicher ausgeführt wird, obwohl keine Aggregationen definiert sind und die ausgewählte Datenquelle vom Typ „Tabellendatensätze” sich auf dieselbe „Intrastat”-Tabelle bezieht. Dies ist erforderlich, weil in der Datenquelle einige berechneten Felder enthält, die noch nicht zur SQL-Datenbankebene übersetzt werden können.  

