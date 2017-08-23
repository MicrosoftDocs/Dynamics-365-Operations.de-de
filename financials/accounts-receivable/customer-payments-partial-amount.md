---
title: "Debitorenzahlungen für einen Teilbetrag"
description: "Es kann vorkommen, dass Debitoren eine Zahlung leisten, die geringer als der in der Rechnung gestellte Betrag ist. In diesem Artikel werden die verschiedenen Möglichkeiten der Vorgehensweise in einer solchen Situation beschrieben. Die zur Verfügung stehenden Optionen sind von den jeweiligen Geschäftsanforderungen und der Konfiguration abhängig."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1982e495f740d6061b9574aa9f40f38180e8d110
ms.openlocfilehash: ebfa8aaed6f82e9c3142540d0850c59d49328d59
ms.contentlocale: de-de
ms.lasthandoff: 08/03/2017

---

# <a name="customer-payments-for-a-partial-amount"></a>Debitorenzahlungen für einen Teilbetrag

[!include[banner](../includes/banner.md)]


Es kann vorkommen, dass Debitoren eine Zahlung leisten, die geringer als der in der Rechnung gestellte Betrag ist. In diesem Artikel werden die verschiedenen Möglichkeiten der Vorgehensweise in einer solchen Situation beschrieben. Die zur Verfügung stehenden Optionen sind von den jeweiligen Geschäftsanforderungen und der Konfiguration abhängig.

<a name="partial-payment-with-no-discount"></a>Teilzahlung ohne Rabatte
--------------------------------

Debitoren könnten eine Teilzahlung leisten, da sie derzeit nicht genügend Bargeld haben, um die Rechnung vollständig zu bezahlen, oder weil es eine Streitigkeit zu einem Rechnungsposten gibt. In diesem Fall kann die Rechnung mit der Zahlung teilweise ausgeglichen werden. Die Rechnung bleibt offen und zeigt einen offenen Saldo.

## <a name="discount-amounts"></a>Rabattbeträge
Sie können Debitoren ein Skonto für die Zahlung einer Rechnung vor dem Fälligkeitsdatum anbieten. Beispielsweise geben Sie eine Rechnung für 100,00 ein, die einen Skonto in Höhe von 2 % angibt, wenn die Rechnung innerhalb von 10 Tagen bezahlt wird. Die Fälligkeitsdatumsbedingungen sind 30 Tage. Wenn Sie eine Zahlung von 98,00 innerhalb von 10 Tagen empfangen, geben Sie die Zahlung für 98,00 ein. Wird die Rechnung für den Ausgleich markiert wurde, wird das Skonto automatisch übernommen.

## <a name="partial-payments-with-cash-discounts"></a>Teilzahlungen mit Skonti
Wenn Debitoren eine Teilzahlung leisten, planen sie möglicherweise, eine weitere Teilzahlung zu leisten, um die Rechnung vollständig zu begleichen. Um ein Skonto für eine Teilzahlung in Anspruch zu nehmen, müssen Sie die Option **Skonti für Teilzahlungen berechnen** auf **Ja** auf der Seite **Debitorenparameter** festlegen. 

Es kann beispielsweise sein, dass Sie ein Skonto in Höhe von 2 % gewährt wird, wenn die Rechnung innerhalb von 10 Tagen nach ihrer Ausstellung bezahlt wird. Es wird eine Rechnung über 100,00 Euro gebucht. Wenn Sie innerhalb von 10 Tagen eine Zahlung in Höhe von 49,00 Euro empfangen, geben Sie in die Zahlungserfassung einen Habenbetrag von 49,00 Euro ein. Wenn Sie die Teilzahlung auf der Seite **Bankbuchungen** ausgleichen, wird im Feld **Zu verwendender Skontobetrag** der Betrag **1,00** angezeigt. Der Skontobetrag wird auf ein Skontokonto gebucht. 

> [!NOTE] 
> Hinweis: Wenn Sie eine Teilzahlung eingeben und im Feld **Auszugleichender Betrag** den vollständigen Rechnungsbetrag beibehalten, wird das Feld **Zu verwendender Rabattbetrag** beim Buchen automatisch neu berechnet.

## <a name="credit-notes-with-discounts"></a>Gutschriften mit Rabatten
Es kann auch vorkommen, dass Debitoren einige in einer Rechnung enthaltenen Artikel zurückgeben und dafür eine Gutschrift erhalten. Wenn ein Skonto in der ursprünglichen Rechnung stammt, sollte die Gutschrift für den Debitor ein Teil des Skontos sein, das vom Debitor in Anspruch genommen wurde. Wenn die Option **Skonti für Gutschriften berechnen** auf **Ja** auf der Seite **Debitorenkontenparameter** festgelegt ist, wird der Rabatt für die Gutschrift automatisch berechnet. 

Es kann beispielsweise sein, dass Sie in den Zahlungsbedingungen einen Rabatt in Höhe von 2 % gewährt haben, wenn die Rechnung innerhalb von 10 Tagen nach der Ausstellung beglichen wird. Eine Rechnung über 100,00 wurde gebucht, und der Debitor hat das Skonto in Anspruch genommen. Wenn der Debitor die Waren zurückgibt und Sie eine Gutschrift ausstellen, können Sie die Gutschrift von -100,00 Euro eingeben. Wenn Sie die Gutschrift auf der Seite **Offene Buchungen ausgleichen** anzeigen, wird im Feld **Auszugleichender Betrag****98,00** angezeigt, und **-2,00** wird im Feld **Skontobetrag** angezeigt. Der Skontobetrag wird auf ein Skontokonto gebucht.

## <a name="overpaymentunderpayment-amounts"></a>Überzahlungs-/Unterzahlungsbeträge
Wenn Kunden eine Zahlung leisten, muss möglicherweise ein sehr kleiner Betrag noch ausgeglichen werden. Beispiel: Sie stellen dem Debitor eine Rechnung über 1.000,00 Euro aus, und der Debitor bezahlt davon 999,90 Euro. Falls der verbleibende Betrag niedriger als der Betrag ist, der für Überzahlungen oder Unterzahlungen auf der Seite **Debitorenparameter** angegeben ist, wird die Differenz automatisch zu einem Sachkonto für Über-/Unterzahlungen gebucht.

## <a name="full-settlement"></a>Vollständiger Ausgleich
Debitoren machen möglicherweise eine Teilzahlung, in der der verbleibende Betrag nicht bezahlt wird, jedoch größer ist als der Unterzahlungsbetrag, der auf der **Kreditorenparameter**-Seite angegeben wird. Wenn Sie die Rechnung markieren möchten, z. B. vollständig ausgeglichen, können Sie die **Vollständigen Ausgleich**-Option auf der Seite **Bankbuchung** verwenden. (Sie können die vollständigen Ausgleich aktivieren, indem Sie einen Konfigurationsschlüssel verwendet wird). Beispielsweise wird eine Rechnung über 1.000,00 gebucht, und der Debitor leistet eine Zahlung in Höhe von 990,00. Sie sind damit einverstanden, dass der Debitor die verbleibenden 10.00 nicht zahlen muss. Nachdem Sie die Rechnung für den Ausgleich markieren, können Sie auch **Kein vollständiger Ausgleich** markieren. Die Rechnung dann wird dann als vollständig ausgeglichen angesehen. Die Differenz von 10,00 Euro wird als zusätzlicher Skontobetrag auf ein Skontokonto gebucht.


Weitere Informationen finden Sie unter [Überfällige Debitorenzahlungen](tasks/deposit-customer-payments.md).

