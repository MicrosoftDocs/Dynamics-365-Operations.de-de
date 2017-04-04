---
title: "Händlerzahlungen für einen Teilbetrag"
description: "Es kann vorkommen, dass Sie eine Zahlung an einen Kreditor leisten, die geringer als der in der Rechnung angegebene Betrag ist. In diesem Artikel werden die verschiedenen Möglichkeiten der Vorgehensweise in einer solchen Situation beschrieben. Die zur Verfügung stehenden Optionen sind von den jeweiligen Geschäftsanforderungen und der Konfiguration abhängig."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Händlerzahlungen für einen Teilbetrag

Es kann vorkommen, dass Sie eine Zahlung an einen Kreditor leisten, die geringer als der in der Rechnung angegebene Betrag ist. In diesem Artikel werden die verschiedenen Möglichkeiten der Vorgehensweise in einer solchen Situation beschrieben. Die zur Verfügung stehenden Optionen sind von den jeweiligen Geschäftsanforderungen und der Konfiguration abhängig. 

<a name="cash-discount-amounts"></a>Skontobeträge
---------------------

Ein Händler kann Ihnen einen Skonto für die Zahlung einer Rechnung vor dem Fälligkeitsdatum anbieten. Beispielsweise geben Sie eine Rechnung für 100.00 ein, die einen Skonto in Höhe von 2 % angibt, wenn die Rechnung innerhalb von 10 Tagen bezahlt wird. Die Fälligkeitsdatumsbedingungen sind 30 Tage. Wenn ein Zahlungsvorschlag das Skonto als Kriterium zum Auswählen einer Rechnung verwendet und der Vorschlag am oder vor dem Skontodatum erfolgt, wird die Rechnung für Zahlung ausgewählt, und die Zahlung wird für 98,00. Ein Skonto kann für eine einmalige Zahlung auch stammen, die manuell erstellt wurde.

## <a name="partial-payments-with-cash-discounts"></a>Teilzahlungen mit Skonti
Wenn Sie eine Teilzahlung leisten, planen Sie möglicherweise, eine weitere Teilzahlung zu leisten, um die Rechnung vollständig zu begleichen. Um ein Skontosatz für eine Teilzahlung zu ergreifen, müssen Sie berechnen die ** Sie Skonti für Teilzahlungen ** ** Option Ja festlegen ** auf der Kreditorenparameter ** ** Seite. 

Es kann beispielsweise sein, dass Ihnen ein Skonto in Höhe von 2 % gewährt wird, wenn die Rechnung innerhalb von 10 Tagen nach ihrer Ausstellung bezahlt wird. Es wird eine Rechnung über 100,00 Euro gebucht. Wenn Sie eine Zahlung in Höhe von 49,00 in 10 Tagen leisten, geben Sie einen Sollbetrag von 49,00 in eine Zahlungserfassung ein. Wenn Sie die Teilzahlung im ** der Offene Buchungen ausgleichen ** Seite ausgleichen, ** 1,00 **wird im ** der Skontobetrag zu ergreifen ** Feld. 

> [!NOTE] 
> Wenn Sie eine Teilzahlung eingeben und im Feld den vollständigen Rechnungsbetrag ** auszugleichenden Betrag ** Feld beibehalten, wird das der Skontobetrag ** zu ergreifen ** Feld automatisch neu berechnet, wenn Sie die Buchungen.

## <a name="credit-notes-with-cash-discounts"></a>Gutschriften mit Skonti
Es kann auch vorkommen, dass Sie einige in einer Rechnung enthaltene Artikel zurückgeben und dafür eine Gutschrift erhalten. Falls ein Skonto für die ursprüngliche Rechnung in Anspruch genommen wurde, können Sie den Wert des Rabatts subtrahieren, um eine Rückerstattung über den korrekten Betrag zu erhalten. ** Wenn die Berechnung von Skonti für Gutschriften ** Option auf Ja ** ** auf die ** Kreditorenkontenparameter ** Seite festgelegt ist, wird der Skontobetrag für die Gutschrift automatisch berechnet. 

Es kann beispielsweise sein, dass Ihnen ein Skonto in Höhe von 2 % gewährt wird, wenn die Rechnung innerhalb von 10 Tagen nach ihrer Ausstellung bezahlt wird. Es wird eine Rechnung über 100,00 Euro gebucht. Falls Sie die Waren zurückgeben und eine Gutschrift erhalten, können Sie die Gutschrift für den Gesamtbetrag der Originalrechnung, 100,00, zusammen mit dem 2 -Prozent-Skonto eingeben, das ebenfalls in der Gutschrift definiert wird.  Wenn Sie die Gutschrift zur ** Bankbuchungen ** Seite anzeigen, ** 98,00 **wird im ** auszugleichenden Betrag ** Feld und ** - 2,00 **wird in ** Skontobetrag ** Feld. Der Skontobetrag wird auf ein Skontokonto gebucht.

## <a name="overpaymentunderpayment-amounts"></a>Überzahlungs-/Unterzahlungsbeträge
Es kann vorkommen, dass Sie eine Teilzahlung ausführen, wobei der Betrag, der noch ausgeglichen werden muss, sehr gering ist. Beispielsweise ist die Kreditorenrechnung für 1.000,00 und Sie zahlen 999.90. Falls der verbleibende Betrag niedriger als der Betrag ist, der für Überzahlungen oder Unterzahlungen auf der Seite **Kreditorenparameter** angegeben ist, wird die Differenz automatisch zu einem Sachkonto für Über-/Unterzahlungen gebucht.


