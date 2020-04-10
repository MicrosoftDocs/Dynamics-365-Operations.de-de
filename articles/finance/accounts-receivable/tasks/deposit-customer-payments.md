---
title: Debitorenzahlungen empfangen
description: Zahlen Sie Debitorenzahlungen ein.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140178"
---
# <a name="deposit-customer-payments"></a>Debitorenzahlungen empfangen

[!include [banner](../../includes/banner.md)]

Zahlen Sie Debitorenzahlungen ein. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Navigationsbereich > Module > Debitorenkonten > Zahlungen > Zahlungserfassung**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Name** **CustPay** im Dropdownmenü aus.
4. Wählen Sie **Positionen** aus.
5. Wählen Sie im Feld **Konto** den Debitor aus, für den Sie die Zahlung erfassen.
6. Geben Sie im Feld **Gutschrift** den Betrag der Zahlung ein. Falls gewünscht, können Sie den Betrag leer lassen und dessen Berechnung dem System überlassen, indem Sie die Rechnungen auswählen, die bezahlt wurden.  
7. Geben Sie im Feld **Zahlungsreferenz** einen Wert ein. Die Zahlungsreferenz kann die Schecknummer für die Zahlung sein, die Sie eingeben. Die Zahlungsreferenz ist erforderlich, um die Zahlung auf einem Einzahlungsbeleg einzubeziehen.  
8. Markieren Sie das Feld "Einzahlungsbeleg verwenden". Wenn die Zahlung in der Einzahlung enthalten sein soll, ändern Sie diese Einstellung auf "Ja".  
9. Wählen Sie **Neu** aus.
10. Wählen Sie im Feld **Konto** den Debitoren für die nächste Zahlung aus.
11. Geben Sie im Feld **Gutschrift** den Zahlungsbetrag ein.
12. Geben Sie im Feld **Zahlungsreferenz** einen Wert ein.
13. Markieren Sie das Feld **Einzahlungsbeleg verwenden**.
14. Wählen Sie **Buchen** aus. Zahlungen müssen gebucht werden, bevor der Einzahlungsbeleg generiert werden kann. Damit soll sichergestellt werden, dass die Zahlungen sich nicht ändern, nachdem der Einzahlungsbeleg generiert wurde.  
15. Wählen Sie **Funktionen** aus.
16. Wählen Sie **Einzahlungsbeleg** aus.
17. Wählen Sie **OK**. Die erste Seite wird verwendet, um den Einzahlungsbeleg zu erstellen.  
18. Wählen Sie **OK**. Der zweite Schritt ist, den Einzahlungsbeleg zu drucken, aber dieser Schritt ist nicht erforderlich.  

