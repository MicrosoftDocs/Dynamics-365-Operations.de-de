---
title: Händlerzahlungen für einen Teilbetrag
description: Es kann vorkommen, dass Sie eine Zahlung an einen Kreditor leisten, die geringer als der in der Rechnung angegebene Betrag ist. In diesem Artikel werden die verschiedenen Möglichkeiten der Vorgehensweise in einer solchen Situation beschrieben.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ee17aeb75e2bdc3b9c36d50914c24aa9d6218b7
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189516"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Kreditorenzahlungen für einen Teilbetrag

[!include [banner](../includes/banner.md)]

Es kann vorkommen, dass Sie eine Zahlung an einen Kreditor leisten, die geringer als der in der Rechnung angegebene Betrag ist. In diesem Artikel werden die verschiedenen Möglichkeiten der Vorgehensweise in einer solchen Situation beschrieben. Die zur Verfügung stehenden Optionen sind von den jeweiligen Geschäftsanforderungen und der Konfiguration abhängig. 

## <a name="cash-discount-amounts"></a>Skontobeträge

Ein Händler kann Ihnen einen Skonto für die Zahlung einer Rechnung vor dem Fälligkeitsdatum anbieten. Beispielsweise geben Sie eine Rechnung für 100.00 ein, die einen Skonto in Höhe von 2 % angibt, wenn die Rechnung innerhalb von 10 Tagen bezahlt wird. Die Fälligkeitsdatumsbedingungen sind 30 Tage. Wenn ein Zahlungsvorschlag das Skonto als Kriterium zum Auswählen einer Rechnung verwendet und der Vorschlag am oder vor dem Skontodatum erfolgt, wird die Rechnung zur Zahlung ausgewählt und die Zahlung über einen Betrag von 98,00 erstellt. Ein Skonto kann auch für eine Einmalzahlung verwendet werden, die manuell erstellt wurde.

## <a name="partial-payments-with-cash-discounts"></a>Teilzahlungen mit Skonti
Wenn Sie eine Teilzahlung leisten, planen Sie möglicherweise, eine weitere Teilzahlung zu leisten, um die Rechnung vollständig zu begleichen. Um ein Skonto für eine Teilzahlung in Anspruch zu nehmen, müssen Sie die Option **Skonti für Teilzahlungen berechnen** auf **Ja** auf der Seite **Kreditorenparameter** festlegen. 

Es kann beispielsweise sein, dass Ihnen ein Skonto in Höhe von 2 % gewährt wird, wenn die Rechnung innerhalb von 10 Tagen nach ihrer Ausstellung bezahlt wird. Es wird eine Rechnung über 100,00 Euro gebucht. Wenn Sie innerhalb von 10 Tagen eine Zahlung in Höhe von 49,00 Euro leisten, geben Sie in die Zahlungserfassung einen Sollbetrag von 49,00 Euro ein. Wenn Sie die Teilzahlung auf der Seite **Offene Buchungen ausgleichen** ausgleichen, wird im Feld **Zu verwendender Skontobetrag** der Betrag **1,00** angezeigt. 

> [!NOTE] 
> Hinweis: Wenn Sie eine Teilzahlung eingeben und im Feld **Auszugleichender Betrag** den vollständigen Rechnungsbetrag beibehalten, wird das Feld **Zu verwendender Rabattbetrag** beim Buchen automatisch neu berechnet.

## <a name="credit-notes-with-cash-discounts"></a>Gutschriften mit Skonti
Es kann auch vorkommen, dass Sie einige in einer Rechnung enthaltene Artikel zurückgeben und dafür eine Gutschrift erhalten. Falls ein Skonto für die ursprüngliche Rechnung in Anspruch genommen wurde, können Sie den Wert des Rabatts subtrahieren, um eine Rückerstattung über den korrekten Betrag zu erhalten. Wenn die Option **Skonti für Gutschriften berechnen** auf **Ja** auf der Seite **Kreditorenkontenparameter** festgelegt ist, wird der Rabatt für die Gutschrift automatisch berechnet. 

Es kann beispielsweise sein, dass Ihnen ein Skonto in Höhe von 2 % gewährt wird, wenn die Rechnung innerhalb von 10 Tagen nach ihrer Ausstellung bezahlt wird. Es wird eine Rechnung über 100,00 Euro gebucht. Falls Sie die Waren zurückgeben und eine Gutschrift erhalten, können Sie die Gutschrift für den Gesamtbetrag der Originalrechnung, 100,00, zusammen mit den 2 % Skonto eingeben, das ebenfalls in der Gutschrift definiert wird.  Wenn Sie die Gutschrift auf der Seite **Buchungen ausgleichen** anzeigen, wird im Feld **Auszugleichender Betrag** **98,00** angezeigt. **-2,00** wird im Feld **Skontobetrag** angezeigt. Der Skontobetrag wird auf ein Skontokonto gebucht.

## <a name="overpaymentunderpayment-amounts"></a>Überzahlungs-/Unterzahlungsbeträge
Es kann vorkommen, dass Sie eine Teilzahlung ausführen, wobei der Betrag, der noch ausgeglichen werden muss, sehr gering ist. Beispielsweise ist die Kreditorenrechnung für 1.000,00 und Sie zahlen 999.90. Falls der verbleibende Betrag niedriger als der Betrag ist, der für Überzahlungen oder Unterzahlungen auf der Seite **Kreditorenparameter** angegeben ist, wird die Differenz automatisch zu einem Sachkonto für Über-/Unterzahlungen gebucht.


Weitere Informationen finden Sie unter [Kreditorenzahlungsübersicht](../cash-bank-management/tasks/vendor-payment-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]