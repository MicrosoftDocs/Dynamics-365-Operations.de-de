---
title: Übersicht über Ausgleiche
description: Dieses Thema enthält allgemeine Informationen zum Ausgleichsprozess. Es beschreibt, welche Transaktionstypen ausgeglichen werden können und wann und wie diese ausgeglichen werden. Es beschreibt auch die Ergebnisse des Ausgleichsprozesses.
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 650b0ef0123cf9acf42c2e7460693b555897744f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443562"
---
# <a name="settlement-overview"></a>Übersicht über Ausgleiche

[!include [banner](../includes/banner.md)]

Dieses Thema enthält allgemeine Informationen zum Ausgleichsprozess. Es beschreibt, welche Transaktionstypen ausgeglichen werden können und wann und wie diese ausgeglichen werden. Es beschreibt auch die Ergebnisse des Ausgleichsprozesses.

Während des Ausgleichs werden die Buchungen in einem Dokument für Buchungen in einem anderen Dokument übernommen, um den Saldo jedes Dokuments zu erhöhen oder zu verringern. Beispielsweise kann eine Zahlung einer Rechnung angewendet werden. Verschiedene Transaktionstypen können, zu unterschiedlichen Zeiten und durch verschiedene Methoden ausgeglichen werden. Der Ausgleichsprozess kann auch neue Transaktionen generieren.

## <a name="what-transactions-can-be-settled"></a>Welche Buchungen ausgeglichen werden können

In Kreditorenkonten und Debitoren kann der Ausgleich zwischen allen Transaktionstypen erfolgen, die sich auf den Kreditorensaldo oder Debitorensaldo auswirken. Diese Transaktionstypen können Rechnungen, Zahlungen, Gutschriften und Gebühren umfassen. Jede Buchungsart kann mit einer anderen Buchungsart ausgeglichen werden. So können Sie beispielsweise eine Zahlung mit einer Rechnung, eine Gutschrift mit einer Rechnung, eine Rechnung mit einer anderen Rechnung und eine Zahlung mit einer anderen Zahlung ausgleichen.

Sie können Zahlungen mit einer Buchung mit derselben juristischen Person oder mit einer anderen juristischen Person ausgleichen. In Organisationen, die ein zentralisiertes Zahlungsmodell verwenden, können [zentralisierte Zahlungen](set-up-centralized-payments.md) den Zahlungsvorgang optimieren.

## <a name="when-to-settle-transactions"></a>Zeitpunkt für den Ausgleich von Buchungen

Transaktionen können bei Eingabe von Zahlungen ausgeglichen werden. Wenn Sie beispielsweise eine Zahlung an einen Kreditor leisten, wählen Sie in der Regel aus, welche Rechnungen bezahlt werden sollen. Durch Auswahl von Rechnungen, aktivieren Sie ihn für Ausgleich für die Zahlung. Wenn Sachbearbeiter für Debitorenzahlungen Kundenzahlungen erfassen, können sie die entsprechenden Rechnungen für den Ausgleich basierend auf den Informationen markieren, die in der Zahlung jedes Debitors enthalten sind. Sie verwenden die Seite **Transaktionen ausgleichen**, um Transaktionen für den Ausgleich zu markieren. Sie können diese Seite von jeder ungebuchten Rechnung oder Zahlung aus öffnen. Wenn die Transaktion gebucht wird, wird auch der Ausgleich gebucht. 

Buchungen können auch ausgeglichen werden, nachdem sie gebucht sind. Sie können eine Debitorenzahlung eingeben und buchen, ohne sie mit beliebigen Rechnungen auszugleichen. Allerdings möchten Sie möglicherweise erst sicherstellen, dass die Zahlung für die korrekte Rechnung beglichen ist, bevor Sie den Ausgleich buchen. Die Seite **Buchungen ausgleichen** kann über die Seite **Alle Debitoren** oder **Alle Kreditoren** bzw. die Seite **Buchungen** für jeden Debitor oder Kreditor geöffnet werden.

Sie können gebuchte Vorauszahlungen auch für eine Rechnung reservieren, indem Sie die Zahlung für den Ausgleich mit einer Bestellung oder eines Auftrags markieren. In diesem Fall hat die Zahlung noch offene Saldo, er kann jedoch nicht mit einer anderen Rechnung ausgeglichen werden. Die Zahlung wird automatisch anhand die Rechnung ausgeglichen, die von der Bestellung oder dem Auftrag erstellt wird.

## <a name="how-to-settle-transactions"></a>Verfahrensweise für den Ausgleich von Buchungen

Buchungen können manuell oder automatisch oder mit einer Kombination aus beiden Methoden ausgeglichen werden. Die Wahl einer Ausgleichsmethode hängt von Ihren Geschäftsprozessen ab. Auf den Seiten **Kreditorenparameter** und **Debitorenparameter** können Sie den Ausgleichsprozess konfigurieren, so dass er an diesen Geschäftsprozessen ausgerichtet ist.

Mithilfe eines Zahlungsvorschlags können Sie Kreditorenzahlungen und Kunden-Lastschriftzahlungen erstellen. Ein Zahlungsvorschlag wird verwendet, um zu zahlende Rechnungen auszuwählen. Der Zahlungsvorschlag wird manuell gestartet, und das System markiert dann automatisch die ausgewählten Rechnungen zum Ausgleich, wenn die Zahlungen erstellt werden.

Wenn Zahlungen manuell erstellt werden, können Sie die Seite **Buchungen ausgleichen** verwenden, um Rechnungen für den Ausgleich auszuwählen. Sie können die Rechnungen manuell auswählen oder die Option **Nach Priorität markieren** verwenden, um die Rechnungen automatisch für den Ausgleich zu markieren. Die Option **Nach Priorität markieren** steht nur für Debitoren zur Verfügung. Sie können diese Option auf der Registerkarte **Ausgleichspriorität** der Seite **Debitorenparameter** aktivieren.

Wenn ein Zahlungsbearbeiter eine Zahlung eingibt, aber diese Zahlung nicht ausgleicht, bevor sie gebucht ist, dann kann die Zahlung automatisch ausgeglichen werden. Sie können den automatischen Ausgleich auf den Seiten **Debitorenparameter** und **Kreditorenparameter** aktivieren. Durch den automatischen Ausgleich werden Transaktionen nur in derselben juristischen Person ausgeglichen. Transaktionen zwischen mehreren juristischen Personen werden nicht ausgeglichen.

Wenn Sie den automatischen Ausgleich verwenden, können Sie die vordefinierte Ausgleichspriorität verwenden, oder Sie können Ihre eigene Ausgleichspriorität auf der Seite **Debitorenparameter** definieren. Diese Funktion steht nur für Debitoren zur Verfügung.

## <a name="results-of-settlement"></a>Ergebnisse des Ausgleichs

Wenn Buchungen ausgeglichen werden, wird der offene Saldo jeder Buchung je nach Bedarf erhöht oder verringert. Gewöhnlich, wenn eine Rechnung und eine Zahlung ausgeglichen werden, wird der Status und der Saldo jeder Buchung gemäß den folgenden Regeln aktualisiert:

- Ist der Zahlungsbetrag höher als der Rechnungsbetrag ist, wird der Rechnungssaldo bis 0,00 verringert, und die Rechnung wird geschlossen. Die Zahlung bleibt offen, und der Saldo ist die Differenz z wischen dem Zahlungsbetrag und dem Rechnungsbetrag.
- Ist der Zahlungsbetrag niedriger als der Rechnungsbetrag ist, wird der Zahlungssaldo bis 0,00 verringert, und die Zahlung wird geschlossen. Die Rechnung bleibt offen, und der Saldo ist die Differenz zwischen dem Rechnungsbetrag und dem Zahlungsbetrag.
- Entspricht der Zahlungsbetrag dem Rechnungsbetrag, werden sowohl die Zahlung als auch die Rechnung geschlossen, und der Saldo von beiden verringert sich auf 0,00.

Wenn der [Zahlungsbetrag geringer als der Rechnungsbetrag ist](../accounts-payable/vendor-payments-partial-amount.md) wegen eines Skontos, einer Abschreibung oder Unterzahlung, werden die Rechnung und Zahlung möglicherweise trotzdem geschlossen, abhängig davon, wie Ausgleiche auf den Seiten **Kreditorenparameter** und **Debitorenparameter** definiert sind.

Ausgleiche können auch Buchungen generieren. Beispielsweise erzeugt der Ausgleich einer Rechnung und einer Zahlung möglicherweise ein Skonto, einen realisierten Gewinn oder Verlust, Mehrwertsteueranpassungen, Abschreibungen oder Centdifferenzen.

## <a name="identifying-marked-transactions-during-settlement"></a>Identifizieren markierter Transaktionen während des Ausgleichs

Wenn Sie versuchen, eine Transaktion auszugleichen, wird möglicherweise ein Symbol angezeigt, das angibt, dass die Transaktion an einem anderen Ort markiert ist. In diesem Fall können Sie die Transaktion auf der Seite **Transaktionen ausgleichen** auswählen, und dann **Abfrage \> Ausgleich aus dem Ausgleichsfenster** auswählen. In der Ansicht für diese Abfrage werden Erfassungen, Aufträge, Rechnungen, Zahlungsvorschläge und Kundenstandorte angezeigt, die möglicherweise den Ausgleich der Transaktion verhindern. Um das Problem zu beheben, können Sie den Link auswählen, um direkt von der Abfrage zum gesperrten Standort zu gelangen. Anschließend können Sie das Dokument mit den Anpassungen aktualisieren, die für den Ausgleich erforderlich sind. Sie können auch den Indikator **Markiert** zur Identifizierung anderer Dokumente verwenden, die am selben Sperrstandort enthalten sind.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Rest ausgleichen](settle-remainder.md)
