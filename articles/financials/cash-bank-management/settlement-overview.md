---
title: Übersicht über Ausgleiche
description: Dieses Thema enthält allgemeine Informationen zum Ausgleichsprozess. Er beschreibt die Buchungstypen, die ausgeglichen werden können, wann und wie Buchungen ausgeglichen werden und die Ergebnisse des Ausgleichsprozesses.
author: kweekley
manager: AnnBe
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e13bdcdcf6dac68a95e6c2759a66bc59013464cb
ms.sourcegitcommit: fd3db9f2052c76a5d906b9ec23cb16222452a362
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "1539966"
---
# <a name="settlement-overview"></a>Übersicht über Ausgleiche

[!include [banner](../includes/banner.md)]

Dieses Thema enthält allgemeine Informationen zum Ausgleichsprozess. Er beschreibt die Buchungstypen, die ausgeglichen werden können, wann und wie Buchungen ausgeglichen werden und die Ergebnisse des Ausgleichsprozesses.

Während des Ausgleichs werden die Buchungen in einem Dokument für Buchungen in einem anderen Dokument übernommen, um den Saldo jedes Dokuments zu erhöhen oder zu verringern. Beispielsweise kann eine Zahlung einer Rechnung angewendet werden. Verschiedene Buchungsarten können, zu unterschiedlichen Zeiten und durch verschiedene Methoden ausgeglichen werden. Ausgleich kann auch veranlassen, dass neue Buchungen generiert werden.

## <a name="what-transactions-can-be-settled"></a>Welche Buchungen ausgeglichen werden können
Ausgleich innerhalb von Kreditoren und Debitoren kann zwischen allen Buchungsarten erfolgen, die sich auf den Kreditorensaldo oder Debitorensaldo auswirken, wie Rechnungen, Zahlungen, Gutschriften und Gebühren. Jede Buchungsart kann mit einer anderen Buchungsart ausgeglichen werden. So können Sie beispielsweise eine Zahlung mit einer Rechnung, eine Gutschrift mit einer Rechnung, eine Rechnung mit einer Rechnung und eine Zahlung mit einer Zahlung ausgleichen. Sie können Zahlungen mit einer Buchung mit derselben juristischen Person oder mit einer anderen juristischen Person ausgleichen. In Organisationen, die ein zentralisiertes Zahlungsmodell verwenden, können [zentralisierte Zahlungen](set-up-centralized-payments.md) den Zahlungsvorgang optimieren.

## <a name="when-to-settle-transactions"></a>Zeitpunkt für den Ausgleich von Buchungen
Buchungen können zum Zeitpunkt des Zahlungseintrags ausgeglichen werden. Wenn Sie beispielsweise eine Zahlung an einen Kreditor leisten, wählen Sie in der Regel die Rechnungen aus, die gezahlt werden sollen. Durch Auswahl von Rechnungen, aktivieren Sie ihn für Ausgleich für die Zahlung. Wenn Zahlungsbearbeiter des Debitoren eine Debitorenzahlung erfassen, können sie die entsprechenden Rechnungen für den Ausgleich basierend auf den Informationen markieren, die in der Zahlung des Debitors enthalten sind. Die Seite **Buchungen ausgleichen** wird verwendet, um Buchungen für den Ausgleich zu markieren. Diese Seite kann aus jeder ungebuchten Rechnung oder Zahlung geöffnet werden. Wenn die Transaktion gebucht wird, wird auch der Ausgleich gebucht. Buchungen können auch ausgeglichen werden, nachdem sie gebucht sind. Sie können eine Debitorenzahlung eingeben und buchen, ohne sie mit beliebigen Rechnungen auszugleichen. Allerdings müssen Sie möglicherweise erst entsprechende Informationen einholen, um sicherzustellen, dass die Zahlung für die richtige Rechnung ausgeglichen wird. Die Seite **Buchungen ausgleichen** kann über die Seite **Alle Debitoren** oder **Alle Kreditoren** bzw. die Seite **Buchungen** für jeden Debitor oder Kreditor geöffnet werden. Sie können gebuchte Vorauszahlungen auch für eine Rechnung reservieren, indem Sie die Zahlung für den Ausgleich mit einer Bestellung oder eines Auftrags markieren. In diesem Fall hat die Zahlung noch offene Saldo, er kann jedoch nicht mit einer anderen Rechnung ausgeglichen werden. Die Zahlung wird automatisch anhand die Rechnung ausgeglichen, die von der Bestellung oder dem Auftrag erstellt wird.

## <a name="how-to-settle-transactions"></a>Verfahrensweise für den Ausgleich von Buchungen
Buchungen können manuell oder automatisch oder mit einer Kombination aus beiden Methoden ausgeglichen werden. Die Auswahl einer Zahlungsmethode hängt von Geschäftsprozessen ab, die durch die Einrichtung des Ausgleichs in den Kreditorenparametern und Debitorenparametern implementiert werden. Sie können Kreditorenzahlungen und Debitorendirektbelastungszahlungen erstellen, indem Sie einen Zahlungsvorschlag verwenden, der verwendet wird, um Rechnungen auszuwählen, die gezahlt werden sollen. Der Zahlungsvorschlag wird manuell initiiert, Dynamics 365 for Finance and Operations und markiert automatisch die ausgewählten Rechnungen zum Ausgleich, wenn die Zahlungen erstellt werden. Wenn Zahlungen manuell erstellt werden, können Sie die Seite **Buchungen ausgleichen** verwenden, um Rechnungen für den Ausgleich auszuwählen. Sie können die Rechnungen manuell auswählen oder die Option **Nach Priorität markieren** verwenden, um die Rechnungen automatisch für den Ausgleich zu markieren. Die Option **Nach Priorität markieren** steht nur für Debitoren zur Verfügung. Um diese Option zu aktivieren, verwenden Sie die Seite **Ausgleichspriorität** in den Debitorenparametern. Wenn ein Zahlungsbearbeiter eine Zahlung eingibt, aber diese Zahlung nicht ausgleicht, bevor sie gebucht ist, kann die Zahlung automatisch ausgeglichen werden. Sie können den automatischen Ausgleich in den Debitorparametern und in den Kreditorparametern aktivieren. Der automatische Ausgleich gleicht Buchungen innerhalb derselben juristischen Person und nicht in mehreren juristischen Personen aus. Wenn Sie ein automatischer Ausgleich verwenden, können Sie den vordefinierten Ausgleichsauftrag verwenden, oder Sie können eigene Ausgleichsprioritätenauftrag in den Debitorparametern definieren. Diese Funktion steht nur für Debitoren zur Verfügung.

## <a name="results-of-settlement"></a>Ergebnisse des Ausgleichs
Wenn Buchungen ausgeglichen werden, wird der offene Saldo jeder Buchung bei Bedarf erhöht oder verringert. In einem typischen Szenario, in dem eine Rechnung und eine Zahlung ausgeglichen werden, wird der Status und der Saldo jeder Buchung gemäß den folgenden Regeln aktualisiert:

-   Ist der Zahlungsbetrag höher als der Rechnungsbetrag ist, wird der Rechnungssaldo bis 0,00 verringert, und die Rechnung wird geschlossen. Die Zahlung bleibt offen, und der Saldo ist der Betrag, um den die Zahlung den Rechnungsbetrag übersteigt.
-   Ist der Zahlungsbetrag niedriger als der Rechnungsbetrag ist, wird der Zahlungssaldo bis 0,00 verringert, und die Zahlung wird geschlossen. Die Rechnung bleibt offen, und der Saldo ist der Unterzahlungsbetrag, um den die Zahlung den Rechnungsbetrag untersteigt.
-   Entspricht der Zahlungsbetrag dem Rechnungsbetrag, werden die Zahlung und die Rechnung geschlossen, und der Saldo von beiden ist 0,00.

Wenn aufgrund eines Skontos, einer Abschreibung oder Unterzahlung die [Zahlung geringer als der Rechnungsbetrag ist](../accounts-payable/vendor-payments-partial-amount.md), werden Rechnung und Zahlung je nach Einstellungen des Ausgleichs in den Kreditorenparametern und den Debitorenparametern noch abgeschlossen. Ausgleich kann auch Buchungen generieren. Beispielsweise erzeugt der Ausgleich einer Rechnung und Zahlung ein Skonto, einen realisierten Gewinn oder Verlust, Mehrwertsteueranpassungen, Abschreibungen oder Centdifferenzen.


## <a name="additional-resources"></a>Zusätzliche Ressourcen
- [Rest ausgleichen](settle-remainder.md)

