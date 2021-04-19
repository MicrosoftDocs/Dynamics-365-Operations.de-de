---
title: EB-Modellzuordnungen definieren und Datenquellen für sie auswählen
description: In diesem Thema wird beschrieben, wie ein Systemadministrator oder ein Entwickler für elektronische Berichterstellung Datenquellen für ein Datenmodell der elektronischen Berichterstellung auswählen kann.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d88aaa24d61d6768801a84c81002d7a6ab2f316
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755081"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>EB-Modellzuordnungen definieren und Datenquellen für sie auswählen

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" zugewiesen ist, ein Modell der elektronischen Berichterstellung (ER) auswählen kann. Die Datenquellen werden einzelnen Komponenten des ausgewählten Datenmodells zur Entwurfszeit und Daten zu diesem Datenmodell zur Laufzeit aufzufüllen verbunden. In diesem Beispiel wählen Sie Datenquellen für ein bestehendes Datenmodell, das für das Beispielunternehmen Litware, Inc. erstellt wurde. Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte in der Prozedur „Erstellen eines neuen Datenmodells abschließen“.


## <a name="open-the-electronic-reporting-configurations-tree"></a>Die Konfigurationsstruktur „Elektronische Berichterstellung” öffnen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Berichterstellungskonfigurationen".

## <a name="insert-a-new-model-mapping"></a>Hinzufügen einer Zuordnung des neuen Modells
1. Wählen Sie 'Zahlungen (vereinfachtes Modell)' in der Struktur aus.
2. Klicken Sie auf Designer.
3. Klicken Sie auf "Modell der Datenquelle zuordnen".
4. Klicken Sie auf "Neu".
    * Dieses erstellt einen neuen Datensatzes, der das Datenmodell Datenquellen zuordnet. In diesem Beispiel ordnen Sie das Datenmodell Datenquellen für den gewünschten Zahlungstyp zu: Banküberweisung.     Es ist möglich, mehr als eine Zuordnung für ein bestimmtes Datenmodell zu entwerfen. So können Sie beispielsweise eine Zuordnung für unterschiedliche Arten von Zahlungen, wie für Direktbelastung oder für Banküberweisungen erstellen. In diesem Beispiel erstellen Sie eine Verknüpfung für Banküberweisungen.  
5. Geben Sie im Feld "Name" "CT mapping" ein.
    * BÜ-Zuordnung  
6. Geben Sie im Feld "Beschreibung" "Payment model mapping CT" ein.
    * Zahlungsmodell zuordnen BÜ  
7. Geben Sie im Feld „Definition” die Bezeichnung „CustomerCreditTransferInitiation” ein.
    * CustomerCreditTransferInitiation  
8. ResolveChanges die Definition.
9. Klicken Sie auf "Speichern".

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Benötigte Datenquellen für die Strommodellzuordnung definieren
1. Klicken Sie auf Designer.
2. Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabellendatensätze' aus.
3. Klicken Sie auf "Stamm hinzufügen".
    * Geben Sie diese Datenquelle ein, um Zahlungsbuchungen zuzugreifen.  
4. Geben Sie im Feld "Name" 'Transactions' ein.
    * Buchungen  
5. Geben Sie im Feld Beschreibung "Transactions" ein.
    * Buchungen  
6. Geben Sie ins Feld Hilfe "Sachkontenerfassungs-Positionen" ein.
    * Sachkontoerfassungspositionen  
7. Wählen Sie "Ja" im Feld "Ask for query".
    * Wählen Sie Ja aus.  
8. Im Tabellenfeld geben Sie "LedgerJournalTrans" ein.
    * LedgerJournalTrans  
9. Klicken Sie auf "OK".
    * Wählen Sie die Tabelle "LedgerJournalTrans" als Datenquelle für das Modell der aktuellen Daten aus.  
10. Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.
11. Klicken Sie auf Hinzufügen.
    * Klicken Sie auf Hinzufügen, um ein neues berechnetes Feld hinzuzufügen.  
12. Geben Sie im Feld "Name" '$EndToEndID' ein.
    * $EndToEndID  
13. Klicken Sie auf Formel bearbeiten.
14. Wählen Sie in der Struktur 'String\CONCATENATE' aus.
15. Klicken Sie auf Funktion hinzufügen.
16. Erweitern Sie in der Struktur den Knoten 'Transactions'.
17. Wählen Sie in der Struktur 'Transactions\Voucher' aus.
18. Klicken Sie auf Datenquelle hinzufügen.
19. Im Feld „Formel” geben Sie „CONCATENATE(Transactions.Voucher, „-", „ ein.
    * Geben Sie [ , „-“, ] am Ende der Formel ein.  
20. Wählen Sie in der Struktur den Knoten 'String\TEXT'.
21. Klicken Sie auf Funktion hinzufügen.
22. Wählen Sie in der Strukturdarstellung "Transactions\Record-ID (RecId)" aus.
23. Klicken Sie auf Datenquelle hinzufügen.
24. Im Feld „Formel” geben Sie „CONCATENATE(Transactions.Voucher, „-", TEXT(Transactions.RecId))” ein.
    * Geben Sie [))] am Ende der Formel ein.  
25. Klicken Sie auf "Speichern".
    * Stellen Sie sicher, dass keine Fehler für die erstellte Formel ermittelt worden sind. Sehen Sie sich die Registerkarte FEHLER unter dem Formeleditorsteuerelement an.  
26. Schließen Sie die Seite.
27. Klicken Sie auf "OK".
    * Fügen Sie das berechnete Feld dieser Datenquelle hinzu.  
28. Klicken Sie auf Hinzufügen.
    * Klicken Sie auf Hinzufügen, um ein neues berechnetes Feld hinzuzufügen.  
29. Geben Sie im Feld Namen $Amount ein.
    * $Amount  
30. Klicken Sie auf Formel bearbeiten.
31. Erweitern Sie in der Struktur den Knoten 'Transactions'.
32. Wählen Sie in der Strukturdarstellung "Transactions\Debit(AmountCurDebit)" aus.
33. Klicken Sie auf Datenquelle hinzufügen.
34. Im Feld „Formel” geben Sie „Transactions.AmountCurDebit - „ ein.
    * Geben Sie [ - ] am Ende der Formel ein.  
35. Wählen Sie in der Strukturdarstellung "Transactions\Credit(AmountCurCredit)" aus.
36. Klicken Sie auf Datenquelle hinzufügen.
37. Klicken Sie auf "Speichern".
38. Schließen Sie die Seite.
39. Klicken Sie auf "OK".
    * Hierdurch wird das $Amount-berechnete Feld der ausgewählten Datenquelle für das Modell der aktuellen Daten hinzugefügt.  
40. Wählen Sie in der Struktur 'Transaktion\$Betrag' aus.
41. Erweitern Sie in der Struktur den Knoten 'Transactions'.
42. In der Struktur erweitern oder reduzieren Sie „Buchungen\$Betrag”.
43. Erweitern oder reduzieren Sie „Buchungen” in der Struktur.
44. Wählen Sie in der Struktur 'Dynamics 365 for Operations\Tabellendatensätze' aus.
45. Klicken Sie auf "Stamm hinzufügen".
    * Geben Sie diese Datenquelle ein, um auf die Bankkontodetails des Unternehmens zuzugreifen.  
46. Geben Sie im Feld "Name" "BankAccount" ein.
    * BankAccount  
47. Geben Sie im Feld Beschreibung "Bank Account" ein.
    * Bankkonto  
48. Geben Sie im Feld Hilfe "Bank Account" ein.
    * Bankkonto  
49. Wählen Sie "Ja" im Feld "Ask for query".
    * Wählen Sie Ja aus.  
50. Im Tabellenfeld geben Sie "BankAccountTable" ein.
    * BankAccountTable  
51. Klicken Sie auf "OK".
    * Wählen Sie die Tabelle "BankAccountTable" als Datenquelle für das Modell der aktuellen Daten aus.  
52. Klicken Sie auf "Stamm hinzufügen".
    * Geben Sie diese Datenquelle ein, um auf die Anforderungen des Unternehmens zuzugreifen.  
53. Geben Sie im Feld Name "Firma" ein.
    * Firma  
54. Geben Sie im Feld Beschreibung einen Wert ein.
    * Unternehmensdaten  
55. Geben Sie im Feld Hilfe "Company information" ein.
    * Unternehmensdaten  
56. Wählen Sie "Ja" im Feld "Ask for query".
    * Wählen Sie Ja aus.  
57. Im Tabellenfeld geben Sie "CompanyInfo" ein.
    * CompanyInfo  
58. Klicken Sie auf "OK".
    * Wählen Sie die Tabelle "CompanyInfo" als Datenquelle für das Modell der aktuellen Daten aus.  
59. Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.
60. Klicken Sie auf "Stamm hinzufügen".
    * Fügen Sie ein berechnetes Feld als neue Datenquelle ein.  
61. Geben Sie im Feld "Name" 'ProcessingDateTime' ein.
    * ProcessingDateTime  
62. Im Feld Beschriftung geben Sie "Verarbeiten von Datum und Zeit" ein.
    * Datum und Uhrzeit der Verarbeitung  
63. Klicken Sie auf Formel bearbeiten.
64. In der Struktur wählen Sie „Datum/Uhrzeit\SESSIONNOW” aus.
65. Klicken Sie auf Funktion hinzufügen.
66. Klicken Sie auf "Speichern".
67. Schließen Sie die Seite.
68. Klicken Sie auf "OK".
    * Fügen Sie das ProcessingDateTime-berechnete Feld als Datenquelle für das Modell der aktuellen Daten.  
69. Klicken Sie auf "Speichern".
70. Schließen Sie die Seite.
71. Schließen Sie die Seite.
72. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]