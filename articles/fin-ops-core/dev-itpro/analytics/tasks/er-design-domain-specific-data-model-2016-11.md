---
title: ER Domänenspezifisches Datenmodell entwerfen
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268f661079b80551b36ad2e1877615d878350051
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681948"
---
# <a name="er-design-domain-specific-data-model"></a>ER Domänenspezifisches Datenmodell entwerfen

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält. Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie das Format der Zahlungsdokumente erstellen.

In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationen unter Unternehmen geteilt werden. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.

1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.

    Wählen Sie den Konfigurationsanbieter für das Beispielunternehmen 'Litware, Inc.' Sollten Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.  
    
2. Klicken Sie auf "Berichterstellungskonfigurationen".

    Sie erstellen eine Konfiguration, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält. Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie das Format der Zahlungsdokumente erstellen.  

## <a name="create-a-new-data-model-configuration"></a>Neue Datenmodellkonfiguration erstellen
1. Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.
2. Geben Sie im Feld "Name" "Zahlungen (vereinfachtes Modell)" ein.
3. Geben Sie im Feld "Beschreibung" "Zahlungsmodellkonfiguration" ein.

    Der aktive Konfigurationsanbieter wird automatisch hier eingegeben. Dieser Anbieter ist in der Lage, diese Konfiguration verwalten. Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.  

4. Klicken Sie auf die Schaltfläche „Konfiguration erstellen“, um die Konfigurationserstellungsaufgabe abzuschließen

## <a name="create-a-data-model"></a>Datenmodell erstellen
Sie erstellen ein neues Datenmodell für die ausgewählte Konfiguration. Diese Konfigurationsversion hat den Status "Entwurf".  
1. Klicken Sie auf Designer.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Definieren der Struktur einer Partei, die an einem Zahlungsprozess teilnimmt
1. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
2. Geben sie im Feld „Name” das Wort „Partei” ein.
3. Klicken Sie auf Hinzufügen.
4. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
5. Geben Sie im Feld "Name" "Name" ein.
6. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
7. Klicken Sie auf Hinzufügen.
8. Geben sie im Feld „Suchen” das Wort „Partei” ein.
9. Klicken Sie auf „Vorheriges suchen”.

## <a name="define-the-bank-structure-for-this-model"></a>Definieren Sie die Bankstruktur für dieses Modell
1. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
2. Geben Sie im Feld "Name" "Agent" ein.
3. Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.
4. Klicken Sie auf Hinzufügen.
5. Geben Sie im Feld „Beschreibung” die Bezeichnung „Finanzinstitut (z. B. eine Bank) ein, das ein Konto für die Partei (Debitor/Kreditor) verwaltet.”.

    Finanzinstitut (z. B. eine Bank), das ein Konto für die Partei (Debitor/Kreditor) verwaltet.  

6. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
7. Geben Sie im Feld "Name" "Name" ein. 
8. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
9. Klicken Sie auf Hinzufügen.
10. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
11. Geben Sie im Feld "Name" "SWIFT" ein.
12. Klicken Sie auf Hinzufügen.
13. Geben Sie im Feld „Beschreibung” die Bezeichnung „Bankidentifizierungscode” ein. 
14. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
15. Geben Sie im Feld "Name" "RoutingNumber" ein.
16. Klicken Sie auf Hinzufügen.
17. Geben Sie im Feld „Beschreibung” die Bezeichnung „Routingnummer” ein.
18. Klicken Sie auf „Vorheriges suchen”.

## <a name="define-the-bank-account-structure-for-this-model"></a>Definieren Sie die Kontostruktur für dieses Modell
1. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
2. Geben Sie im Feld "Name" "Konto" ein. 
3. Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.
4. Klicken Sie auf Hinzufügen.
5. Geben Sie im Feld „Beschreibung” die Bezeichnung „Kennung eines Kontos einer Partei in einem Finanzinstitut (beispielsweise eine Bank).” ein.

    Kennung eines Kontos einer Partei in einem Finanzinstitut (beispielsweise eine Bank).  

6. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
7. Geben Sie im Feld "Name" 'Währung' ein. 
8. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
9. Klicken Sie auf Hinzufügen.
10. Geben Sie im Feld „Beschreibung” die Bezeichnung „Währungscode” ein.
11. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
12. Geben Sie im Feld "Name" "Nummer" ein. 
13. Klicken Sie auf Hinzufügen.
14. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
15. Geben Sie im Feld "Name" "IBAN" ein. 
16. Klicken Sie auf Hinzufügen.
17. Geben Sie im Feld „Beschreibung” die „Internationale Bankkontonummer” ein.

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Definieren der Zahlungsmeldungsstruktur für Kreditübertragungs-Zahlungstyp.
1. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
2. Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.
3. Geben Sie im Feld "Name" "CustomerCreditTransferInitiation".
4. Klicken Sie auf Hinzufügen.
5. Geben Sie im Feld „Suchen” die Bezeichnung „CustomerCreditTransferInitiation” ein. 
6. Klicken Sie auf „Vorheriges suchen”.
7. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
8. Geben Sie im Feld "Name" 'MessageIdentification' ein. 
9. Klicken Sie auf Hinzufügen.
10. Geben Sie im Feld „Beschreibung” die Bezeichnung „Die Punkt-zu-Punkt-Referenz, die von der Anweisungspartei zugewiesen wird (und an die nächste Partei gesendet wird), um die Nachricht zu identifizieren” ein.

    Die Punkt-zu-Punkt-Referenz, die von der Anweisungspartei zugewiesen (und an die nächste Partei gesendet wird), um die Nachricht zu identifizieren.  

11. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
12. Geben Sie im Feld "Name" 'ProcessingDateTime' ein.
13. Wählen Sie im Feld "Artikeltyp" 'DateTime' aus.
14. Klicken Sie auf Hinzufügen.
15. Geben Sie im Feld „Beschreibung” die Bezeichnung „Das Datum und die Uhrzeit der Erstellung der Zahlungsnachricht.” ein. 
16. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.

    Definieren Sie die Zahlungsbuchungsstruktur für dieses Modell.  

17. Geben Sie im Feld "Name" "Zahlungen" ein.
18. Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.
19. Klicken Sie auf Hinzufügen.
20. Geben Sie im Feld "Beschreibung" "Zahlungspositionen der aktuellen Nachricht" ein.
21. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
22. Geben Sie im Feld "Name" 'Kreditor' ein. 
23. Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.
24. Klicken Sie auf Hinzufügen.
25. Geben Sie im Feld „Beschreibung” die „Bezeichnung Partei, für die ein Geldbetrag fällig ist” ein. 
26. Klicken Sie auf „Artikelreferenz wechseln”.
27. Geben sie im Feld „Suchen” das Wort „Partei” ein.
28. Klicken Sie auf „Weitersuchen”.
29. Klicken Sie auf "OK".
30. Geben Sie im Feld „Suchen” die Bezeichnung „Zahlungen” ein.
31. Klicken Sie auf „Weitersuchen”.
32. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
33. Geben Sie im Feld "Name" "Zahlungspflichtiger" ein. 
34. Klicken Sie auf Hinzufügen.
35. Geben Sie im Feld „Beschreibung” „Partei, die dem (letztendlichen) Kreditor einen Geldbetrag schuldet.” ein.
36. Klicken Sie auf „Artikelreferenz wechseln”.
37. Geben sie im Feld „Suchen” das Wort „Partei” ein.
38. Klicken Sie auf „Weitersuchen”.
39. Klicken Sie auf "OK".
40. Klicken Sie auf „Weitersuchen”.
41. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
42. Geben Sie im Feld "Name" "Beschreibung" ein.
43. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
44. Klicken Sie auf Hinzufügen.
45. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
46. Geben Sie im Feld "Name" 'Währung' ein.
47. Klicken Sie auf Hinzufügen.
48. Geben Sie im Feld „Beschreibung” die Bezeichnung „Währungscode” ein.
49. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
50. Geben Sie im Feld "Name" 'TransactionDate' ein. 
51. Wählen Sie im Feld "Artikeltyp" 'Datum' aus.
52. Klicken Sie auf Hinzufügen.
53. Geben Sie im Feld „Beschreibung” das „Transaktionsdatum” ein. 
54. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
55. Geben Sie im Feld "Name" 'InstructedAmount' ein.  
56. Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.
57. Klicken Sie auf Hinzufügen.
58. Geben Sie im Feld „Beschreibung” „Der zwischen Debitor und Kreditor vor Abzug von Gebühren zu transferierende Geldbetrag, vor Abzug von Gebühren”. Der Betrag sollte in der Währung gezahlt werden, wie ursprünglich von der initiierenden Partei gestellt.'

    Zwischen Debitor und Kreditor vor Abzug von Gebühren transferierter Geldbetrag. Der Betrag sollte in der Währung gezahlt werden, wie ursprünglich von der initiierenden Partei gestellt.  

59. Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.
60. Geben Sie im Feld "Name" 'End2EndID' ein. 
61. Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.
62. Klicken Sie auf Hinzufügen.
63. Geben Sie im Feld „Beschreibung” „Die eindeutige Kennung, die von der initiierenden Partei zugewiesen wird” ein. Diese Kennung wird unverändert in der gesamten End-to-End-Kette übergeben' ein. 
64. Geben Sie im Feld "Name" "PaymentModel" ein.

    Der PaymentModel-Name wird an vordefinierten Schnittstellen von Zahlungsformularen ausgerichtet.  

65. Klicken Sie auf "Speichern".
66. Schließen Sie die Seite.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]