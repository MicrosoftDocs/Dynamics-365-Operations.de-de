--- 
title: "Zuordnen von Modellen zum Verwenden von Finanzdimensionen als Datenquelle für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bbc7401284146c2ab4fdfe325cfefb95d1eefb81
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Zuordnen von Modellen zum Verwenden von Finanzdimensionen als Datenquelle für elektronische Berichterstellung

[!include[task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann. Diese Schritte können in jedem Unternehmen ausgeführt werden.

Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren "ER - Finanzdimensionen als Datenquelle nutzen (Teil 1: Design des Datenmodells)" ausführen.


## <a name="add-required-data-sources-to-model-mapping"></a>Hinzufügen von erforderlichen Datenquellen zur Modellzuordnung
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell".
3. Klicken Sie auf Designer.
4. Klicken Sie auf "Modell der Datenquelle zuordnen".
5. Klicken Sie auf "Neu".
6. Wählen Sie im Feld "Definition" "Erfassung" aus.
7. Geben Sie im Feld "Name" "Dimensionsdatenzuordnung" ein.
8. Geben Sie im Feld "Beschreibung" "Dimensionsdatenzuordnung" ein.
9. Klicken Sie auf "Speichern".
10. Klicken Sie auf Designer.
11. Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabelle" aus.
12. Klicken Sie auf "Stamm hinzufügen".
13. Geben Sie im Feld Name "Firma" ein.
14. Im Tabellenfeld geben Sie "CompanyInfo" ein.
15. Klicken Sie auf "OK".
16. Wählen Sie in der Struktur "Funktionen\Finanzdimensionsdetails".
17. Klicken Sie auf "Stamm hinzufügen".
    * Diese Datenquelle gibt an, wie der Bereich der Finanzdimensionen für einen Bericht definiert wird, der dieses Modell als Datenquelle verwendet.  
18. Geben Sie im Feld "Name" einen Wert ein.
19. Wählen Sie "Ja" im Feld "Dimensionen anfordern".
    * Wählen Sie die Option Ja aus, um dem Benutzer die Auswahl zur Laufzeit zu ermöglichen. Bei "Neun" werden standardmäßig alle Finanzdimensionen der aktuellen Instanz verwendet.  
20. Wählen Sie im Feld Finanzdimensionen "Juristische Person" aus.
    * Wählen Sie "Alle" aus, um dem Benutzer die Auswahl der gewünschten Dimensionen für die aktuelle Instanz zu ermöglichen.  Wählen Sie "Juristische Person" aus, um dem Benutzer die Auswahl der Dimensionen für das Unternehmen zu ermöglichen.  Wählen Sie "Dimension" aus, um dem Benutzer die Auswahl von Dimensionen über einen einzelnen Dimensionssatzes zu ermöglichen.  
21. Wählen Sie "Ja" im Feld "Hauptkonto anfordern".
    * Legen Sie "Hauptkonto anfordern" auf "Ja" fest, um Benutzern zu ermöglichen, das Hauptkonto als Teil der Liste mit den Dimensionen auszuwählen.   Bei "Nein" wird das Hauptkonto nicht in der Liste mit den Dimensionen aufgenommen und die Option "Hauptkonto erforderlich" ist aktiviert. Wenn "Hauptkonto erforderlich" auf Ja festgelegt ist, wird das Hauptkonto unabhängig von der Auswahl des Benutzers in der Liste mit den Dimensionen festgelegt.  
22. Klicken Sie auf "OK".
23. Wählen Sie in der Strukturdarstellung "Dynamics 365 for Operations \Tabellendatensätze" aus.
24. Klicken Sie auf "Stamm hinzufügen".
25. Geben Sie im Feld "Name" "LedgerJournal" ein.
26. Wählen Sie "Ja" im Feld "Ask for query".
27. Im Tabellenfeld geben Sie "LedgerJournalTable" ein.
28. Klicken Sie auf "OK".

## <a name="map-data-model-elements-to-added-data-sources"></a>Zuordnen von Datenmodell-Elementen zu hinzugefügten Datenquellen
1. Erweitern Sie in der Struktur 'Erfassung'.
2. Erweitern Sie in der Struktur 'Erfassung\Buchung'.
3. Erweitern Sie in der Struktur 'Erfassung\Buchung\Dimensionsdaten'.
4. Erweitern Sie 'Dimensionseinstellung' in der Struktur.
5. Erweitern Sie in der Struktur "LedgerJournal".
6. Erweitern Sie 'LedgerJournal\\<Relations' in der Struktur.
7. Erweitern Sie 'LedgerJournal\<Relations\LedgerJournalTrans' in der Struktur.
8. Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher' in der Struktur.
9. Wählen Sie in der Struktur 'Erfassung\Buchung\Beleg'.
10. Klicken Sie auf Binden.
11. Wählen Sie in der Strukturdarstellung 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.
    * Beachten Sie, dass für jede Referenz zu Finanzdimensionen, die beispielsweise auf LedgerDimension festgelegt ist, ein entsprechender Datenquellenartikel verfügbar ist (LedgerDimension.Dimension). Dieser Datenquellenartikel bietet die Finanzdimensionen des Dimensionssatzes als Liste des Datensatzes.  
12. Erweitern Sie in der Strukturdarstellung 'LedgerJournal\\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.
13. Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.
14. Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.
15. Erweitern Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Definitionen'.
16. Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Definitionen\Name'.
17. Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Name'.
18. Klicken Sie auf Binden.
19. Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.
20. Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Description'.
21. Klicken Sie auf Binden.
22. Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.
23. Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data\Code'.
24. Klicken Sie auf Binden.
25. Wählen Sie in der Struktur 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.
26. Wählen Sie in der Struktur 'Journal\Transaction\Dimensions data'.
27. Klicken Sie auf Binden.
28. Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.
29. Wählen Sie in der Struktur 'Erfassung\Buchung\Debit'.
30. Klicken Sie auf Binden.
31. Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.
32. Wählen Sie in der Struktur 'Erfassung\Buchung\Date'.
33. Klicken Sie auf Binden.
34. Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.
35. Wählen Sie in der Struktur 'Journal\Transaction\Currency'.
36. Klicken Sie auf Binden.
37. Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.
38. Wählen Sie in der Struktur 'Journal\Transaction\Credit'.
39. Klicken Sie auf Binden.
40. Wählen Sie 'LedgerJournal\<Relations\LedgerJournalTrans' in der Struktur.
41. Wählen Sie in der Struktur 'Journal\Transaction'.
42. Klicken Sie auf Binden.
43. In der Struktur ausgewählte 'LedgerJournal\Journal batch number(JournalNum)'.
44. Wählen Sie in der Struktur 'Journal\Batch'.
45. Klicken Sie auf Binden.
46. Wählen Sie in der Struktur 'LedgerJournal' aus.
47. Wählen Sie in der Struktur 'Journal' aus.
48. Klicken Sie auf Binden.
49. Erweitern Sie in der Struktur 'Dimensions'.
50. In der Struktur erweitern Sie 'Dimensions\Main account and dimensions'.
51. In der Struktur erweitern Sie 'Dimensions\Main account and dimensions\Definition'.
52. In der Struktur wählen Sie 'Dimensions\Main account and dimensions\Name'.
53. Wählen Sie 'Dimensionseinstellung\Code' in der Struktur.
54. Klicken Sie auf Binden.
55. In der Struktur wählen Sie 'Dimensions\Main account and dimensions\Definition\Report column name'.
56. Wählen Sie 'Dimensionseinstellung\Name' in der Struktur.
57. Klicken Sie auf Binden.
58. In der Struktur wählen Sie 'Dimensions\Main account and dimensions'.
59. Wählen Sie 'Dimensions setting' in der Struktur.
60. Klicken Sie auf Binden.
61. Wählen Sie in der Struktur 'Company' aus.
62. Klicken Sie auf "Bearbeiten".
63. Geben Sie im Feld "expressionAsStringText" 'Company.'find()'.'name()'' ein.
    * Company.'find()'.'name()'  
64. Klicken Sie auf "Speichern".
65. Schließen Sie die Seite.
66. Klicken Sie auf "Speichern".
67. Schließen Sie die Seite.

## <a name="complete-this-draft-models-version"></a>Abschließen dieser Version dieses Entwurfsmodells
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Klicken Sie auf "Status ändern".
4. Klicken Sie auf "Abgeschlossen".
5. Klicken Sie auf "OK".


