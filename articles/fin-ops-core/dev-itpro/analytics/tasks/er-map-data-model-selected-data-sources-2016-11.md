---
title: Er-Datenmodell zu den ausgewählten Datenquellen zuordnen
description: In den folgenden Schritten wird erläutert, wie ein Benutzer in der Rolle „Systemadministrator” oder „Entwickler für elektronische Berichterstellung” ein Datenmodell der elektronischen Berichterstellung (EB) ausgewählten Datenquellen von Microsoft Dynamics 365 Finance, zuordnen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2d09370b0e08897799d40c41c20c21b58e885dc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684306"
---
# <a name="er-map-data-model-to-selected-data-sources"></a>Er-Datenmodell zu den ausgewählten Datenquellen zuordnen

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer in der Rolle „Systemadministrator” oder „Entwickler für elektronische Berichterstellung” ein Datenmodell der elektronischen Berichterstellung (EB) ausgewählten Datenquellen, zuordnen kann. Diese vorbildliche Zuordnung wird später als Datenquelle in einer Formatkonfiguration verwendet, die verwendet wird, um Dokumente für den elektronischen Zahlungsverkehr zu verwalten. In diesem Beispiel verknüpfen Sie ein Datenmodell für das Beispielunternehmen, Litware, Inc. mit Datenquellen. Um diese Schritte abzuschließen, die folgenden Schritte in der „Datenquellen für Modell-Zuordnung“ im Verfahren zuerst abschließen.


## <a name="open-er-configurations-tree"></a>Öffnen Sie ER-Konfigurationsstruktur
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Konfigurationen".

## <a name="select-created-model-mapping"></a>Wählen Sie erstellte Model-Zuordnung
1. Wählen Sie 'Zahlungen (vereinfachtes Modell)' in der Struktur aus.
    * Stellen Sie sicher, dass die Modellkonfiguration „Zahlungen (vereinfachtes Modell)“ im Voraus erstellt wurde. Andernfalls beenden Sie jetzt und kehren nach Abschluss des Aufgabenleitfadens „Erstellen einer neuer Konfiguration mit dem Datenmodell der ausgewählten Domäne“ zurück.  
2. Klicken Sie auf "Modelldesigner".
3. Klicken Sie auf "Modell der Datenquelle zuordnen".
4. Wählen Sie den "CT-Zuordnungs" Datensatz aus.
    * BÜ-Zuordnung  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Binden Sie erstellte Datenquellen an Datenmodell-Elemente
1. Klicken Sie auf Designer.
2. In der Struktur wählen Sie Datums und Zeit (ProcessingDateTime) aus.
3. In der Struktur wählen Sie "Datum" (ProcessingDateTime)".
4. Klicken Sie auf Binden.
5. Wählen Sie in der Strukturdarstellung "Zahlungsnachrichtenkennung (MessageIdentification )" aus.
6. Erweitern Sie in der Struktur den Knoten 'Transactions'.
7. In der Struktur ausgewählte "Buchungs- \ Erfassungsstapelnummer (JournalNum)".
8. Klicken Sie auf Binden.
9. Wählen Sie in der Struktur 'Zahlungen' aus.
10. Wählen Sie in der Struktur 'Transactions' aus.
11. Klicken Sie auf Binden.
12. Erweitern Sie 'Payments= Transactions' in der Struktur.
13. Erweitern Sie 'Payments= Transactions\Creditor' in der Struktur.
14. Erweitern Sie 'Payments= Transactions\Creditor\Account' in der Struktur.
15. In der Struktur ausgewählte "Payments=-Buchungen\Kreditgeber\Konto\Währungscode (Währung)".
16. In der Struktur erweitern Sie "Transactions\vendBankAccountInTransactionCompany()".
17. In der Struktur ausgewählte "Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)".
18. Klicken Sie auf Binden.
19. In der Struktur ausgewählte "Payments=-Buchungen\Kreditgeber\Konto\IBAN code(IBAN)".
20. In der Struktur wählen Sie aus "Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)".
21. Klicken Sie auf Binden.
22. Wählen Sie 'Payments= Transactions\Creditor\Account\Number' in der Struktur aus.
23. In der Struktur ausgewählte "Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)".
24. Klicken Sie auf Binden.
25. Erweitern Sie 'Payments= Transactions\Creditor\Agent' in der Struktur.
26. Wählen Sie 'Payments= Transactions\Creditor\Account\Agent\Name' in der Struktur aus.
27. In der Struktur wählen Sie "Transactions\vendBankAccountInTransactionCompany()\Name" aus.
28. Klicken Sie auf Binden.
29. Wählen Sie 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)' in der Struktur aus.
30. In der Struktur ausgewählte "Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)".
31. Klicken Sie auf Binden.
32. In der Struktur ausgewählte "Payments=-Buchungen\Kreditgeber\Agent\SWIFT code(SWIFT)".
33. In der Struktur ausgewählte "Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)".
34. Klicken Sie auf Binden.
35. Wählen Sie 'Payments= Transactions\Creditor\Account\Name' in der Struktur aus.
36. Erweitern Sie 'Transactions\findVendTable()' in der Struktur.
37. In der Struktur wählen Sie Transactions\findVendTable()\name()'.
38. Klicken Sie auf Binden.
39. In der Struktur ausgewählte "Payments=-Buchungen\Währungscode (Währung)".
40. Erweitern Sie 'Transactions\>Relations' in der Struktur.
41. In der Struktur erweitern Sie "Buchungen\>Geschäftsbeziehung \ Währungstabelle (Währung)".
42. Wählen Sie in der Strukturdarstellung "Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)".
43. Klicken Sie auf Binden.
44. Erweitern Sie 'Payments= Transactions\Debtor' in der Struktur.
45. Erweitern Sie 'Payments= Transactions\Debtor\Account' in der Struktur.
46. In der Struktur ausgewählte "Payments=-Buchungen\Debtor\Konto\Währungscode (Währung)".
47. Wählen Sie in der Struktur 'Bank Account(BankAccount)' aus.
48. Erweitern Sie in der Struktur 'Bank Account(BankAccount)'.
49. In der Struktur ausgewählte "Bank Account(BankAccount)\Currency(CurrencyCode)".
50. Klicken Sie auf Binden.
51. Wählen Sie in der Struktur 'Bank Account(BankAccount)\IBAN' aus.
52. In der Struktur ausgewählte "Payments=-Buchungen\Debtor\Konto\IBAN code(IBAN)".
53. Klicken Sie auf Binden.
54. Wählen Sie 'Payments= Transactions\Debtor\Account\Number' in der Struktur aus.
55. In Struktur, auswählen "Bank Account(BankAccount)\Bank account number(AccountNum)".
56. Klicken Sie auf Binden.
57. Erweitern Sie 'Payments= Transactions\Debtor\Agent' in der Struktur.
58. Wählen Sie 'Payments= Transactions\Debtor\Account\Agent\Name' in der Struktur aus.
59. Wählen Sie in der Struktur 'Bank Account(BankAccount)\Name' aus.
60. Klicken Sie auf Binden.
61. Wählen Sie 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)' in der Struktur aus.
62. In Struktur, auswählen "Bank Account(BankAccount)\Routing number(RegistrationNum)".
63. Klicken Sie auf Binden.
64. In der Struktur ausgewählte "Payments=-Buchungen\Debtor\Agent\SWIFT code(SWIFT)".
65. In der Struktur ausgewählte "Bank Account(BankAccount)\SWIFT code(SWIFTNo)".
66. Klicken Sie auf Binden.
67. Wählen Sie 'Payments= Transactions\Debtor\Account\Name' in der Struktur aus.
68. Wählen Sie in der Strukturdarstellung "Unternehmensdaten (Unternehmen") aus.
69. Erweitern Sie in der Strukturdarstellung "Unternehmensdaten (Unternehmen)".
70. Wählen Sie in der Strukturdarstellung "Unternehmensdaten (Unternehmen)\Name" aus.
71. Klicken Sie auf Binden.
72. Wählen Sie 'Payments= Transactions\Description' in der Struktur aus.
73. Wählen Sie 'Transactions\Description(Txt)' in der Struktur aus.
74. Klicken Sie auf Binden.
75. In der Struktur ausgewählte "Payments= Transactions\End to end identification code(End2EndID)".
76. Wählen Sie in der Struktur\$TransactionsEndToEndID' aus.
77. Klicken Sie auf Binden.
78. In der Struktur wählen Sie "Payments=-Buchungen \ Betrag (InstructedAmount)" aus.
79. Wählen Sie in der Struktur 'Transaktion\$Betrag' aus.
80. Klicken Sie auf Binden.
81. Wählen Sie in der Strukturdarstellung "Payments= Transactions\Transaction date(TransactionDate)" aus.
82. Wählen Sie 'Transactions\Date(TransDate)' in der Struktur aus.
83. Klicken Sie auf Binden.

## <a name="validate-created-mapping"></a>Erstellte Zuordnung validieren
1. Klicken Sie auf "Überprüfen".
    * Überprüft die neue Zuordnung, um sicherzustellen, dass alle Bindungen in Ordnung sind.  
2. Klicken Sie zum Erweitern oder Reduzieren des Abschnitts Fehlerliste auf den Pfeil.
3. Klicken Sie auf "Speichern".
4. Schließen Sie die Seite.
5. Schließen Sie die Seite.
6. Schließen Sie die Seite.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Ändern Sie den Status der aktuellen Version der Modellkonfiguration
1. Klicken Sie auf "Status ändern".
    * Ändern Sie den Status der entworfenen Modellkonfiguration – von „Entwurf” zu „Abgeschlossen”, um es für die Generierung des Zahlungsformatdesigns verfügbar zu machen.  
2. Klicken Sie auf "Abgeschlossen".
    * Wählen Sie „Abgeschlossen” aus.  
3. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Beispielsweise „Version 1”.  
4. Klicken Sie auf "OK".
5. Wählen Sie die abgeschlossene Version der aktuellen Konfiguration aus.
    * Beachten Sie, dass die erstellte Konfiguration als abgeschlossene Version 1 gespeichert wird.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]