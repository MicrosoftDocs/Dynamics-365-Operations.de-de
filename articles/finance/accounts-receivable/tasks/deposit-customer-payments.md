---
title: Debitorenzahlungen empfangen
description: Zahlen Sie Debitorenzahlungen ein.
author: ShivamPandey-msft
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ed692d9c82fd496e31258a70415db1838d99313
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714032"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
