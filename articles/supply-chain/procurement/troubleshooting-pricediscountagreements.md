---
title: Problembehandlung bei Preisen, Ermäßigungen, Vereinbarungen und Rabatten
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Preisen, Ermäßigungen, Vereinbarungen und Rabatten auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b4349eeba285492202b5df8481b277a06708a4c8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429127"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Problembehandlung bei Preisen, Ermäßigungen, Vereinbarungen und Rabatten

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Preisen, Ermäßigungen, Vereinbarungen und Rabatten auftreten können.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Ich kann einen Kaufvertrag nicht mit einer Bestellposition verknüpfen, nachdem die Bestellung erstellt wurde.

Ein Kaufvertrag muss einer Bestellung zugewiesen werden, wenn die Bestellung erstellt wird. Andernfalls können Bestellpositionen nicht mit Kaufvertragspositionen verknüpft werden.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Welche Prüfung löst die Meldung „Manuell eingegebene Preise und Rabatte oder externes Dokument aktualisieren“ aus?

Wenn Sie das Versanddatum ändern, erhalten Sie möglicherweise die Meldung „Manuell eingegebene Preise und Rabatte oder externes Dokument aktualisieren“. Sie erhalten diese Nachricht, da bei einer Änderung des Versanddatums möglicherweise ein anderer Handels- oder Verkaufsvertrag ausgelöst wird und eine Preisänderung verursacht. Eine Änderung des Versanddatums kann sich auch auf Lagerpläne und andere verwandte Informationen auswirken.

Die Nachricht wird ausgelöst, wenn eine der Daten oder andere Parameter geändert werden. Der Zweck der Nachricht besteht darin, sicherzustellen, dass Sie über Preisänderungen informiert sind, die aufgrund dieser Änderungen auftreten können.

Die Nachricht ist die Eingabeaufforderung zur Bewertung des Handelsabkommens (TAE). Eine vollständige Beschreibung finden Sie unter [Bewertungsrichtlinien für Handelsabkommen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Ein Bestellungsbeleg enthält nicht alle Gebühren.

### <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Stellen Sie auf der **Beschaffungs- und Ursprungsparameter**-Seite auf der Registerkarte **Lieferung** sicher, dass die **Auf Produktbeleg Gebühren generieren**-Option auf *Ja* festgelegt ist.
1. Erstellen einer Bestellung, die Gebühren enthält.
1. Bestätigen Sie die Bestellung.
1. Erhalten Sie die Bestellung.
1. Sehen Sie sich die Quittungssumme an und vergleichen Sie sie mit der erwarteten Gesamtsumme.
1. Beachten Sie, dass nicht alle Gebühren auf dem Bestellbeleg enthalten sind.

### <a name="issue-resolution"></a>Problemlösung

Die Auflösung hängt davon ab, wie die verschiedenen Gebühren eingerichtet wurden. Informationen zum Einrichten verschiedener Gebühren zur Erfüllung Ihrer Anforderungen finden Sie im folgenden Blogbeitrag: [Sonstiges Gebühren zum Zeitpunkt des Produkteingangs buchen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Preise und Rabatte für Handelsabkommen gelten nicht für Verkaufs- oder Bestellpositionen, die über die Datenverwaltung importiert werden.

### <a name="issue-description"></a>Problembeschreibung

Handelsabkommen, die für Verkaufs- oder Bestellpositionen gelten, werden nicht auf Positionen angewendet, die über die Datenverwaltung importiert werden. Dieselben Handelsabkommen gelten jedoch für manuell erstellte Verkaufs- oder Bestellpositionen.

### <a name="reason-for-the-issue"></a>Grund für das Problem

Wenn Bestellpositionen, die über die Datenverwaltung importiert werden, bereits Preisinformationen enthalten, wird das Handelsabkommen für diese Positionen nicht neu bewertet. Wenn zum Beispiel **Positionsrabatt in Prozent** oder einer der Preis- und Rabattwerte für eine Position festgelegt ist, werden Handelsabkommen für diese Position nicht nachgeschlagen.

### <a name="issue-workaround"></a>Problemumgehung

Dieses Verhalten wird erwartet und ist sowohl für Aufträge als auch für Bestellungen ähnlich.

Importieren Sie zur Umgehung dieses Problems die Bestellpositionen, ohne Preisinformationen festzulegen. Die Handelsabkommen werden dann angewendet und die Bestellpositionen werden basierend auf den definierten Handelsabkommen aktualisiert.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Ein Lieferantenrabatt wird nicht auf der Grundlage von Rechnungen kumuliert.

### <a name="issue-description"></a>Problembeschreibung

Wenn gebuchte Rechnungen unterschiedliche Fälligkeitstermine haben, werden diese Rechnungen nicht in Lieferantenrabatten berücksichtigt, die daraus generiert werden.

### <a name="issue-resolution"></a>Problemlösung

Das Fälligkeitsdatum wird bei der Berechnung des Lieferantenrabattes nicht berücksichtigt. Ziehen Sie in Betracht, das System so anzupassen, dass das Fälligkeitsdatum und die Beziehung zur Rechnung in Bezug auf den tatsächlichen Lieferantenrabatt deutlicher werden.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Stückpreise auf Bestellungen werden nicht basierend auf der Stückumrechnung berechnet.

### <a name="issue-description"></a>Problembeschreibung

Wenn eine Einheit in einer Bestellung geändert wird, werden die Handelsvertragspreise nicht gemäß den Definitionen der Einheitenumrechnung neu berechnet.

### <a name="issue-resolution"></a>Problemlösung

Die Preise werden immer aus Handelsabkommen (oder anderen Preiseinstellungen im System, wie z. B. Verkaufsvereinbarungen oder Artikelpreisen) ermittelt und für eine Einheit festgelegt.

Wenn die Einheit in einer Bestellposition geändert wird, sucht das System nach einem Preis für die neue Einheit und wendet diesen Preis an. Wenn für das Gerät kein Preis gefunden wird, wendet das System keinen Preis an. Die Einheitenumrechnung kann nicht verwendet werden, um den Preis in eine andere Einheit umzurechnen. Theoretisch entspricht der Preis für eine Schachtel mit zehn Stück möglicherweise nicht dem Zehnfachen des Preises einer Schachtel.

### <a name="issue-workaround"></a>Problemumgehung

Eine Möglichkeit, dieses Problem zu umgehen, besteht darin, sicherzustellen, dass Handelsabkommen für die Einheiten bestehen, von denen Sie erwarten, dass sie in den Bestellpositionen für den Artikel verwendet werden.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Währungsumrechnungsprobleme treten bei Handelsabkommen auf.

Preise von Handelsabkommen werden nicht nach der Währung neu berechnet, wenn die Währung in einer Bestellung abweicht.

Mit der Funktion *Allgemeine Währung* können Sie Preise und Rabatte in nur einer Währung definieren. Sie können dann nach Bedarf in andere Währungen umrechnen. Darüber hinaus kann die Funktion nach Abschluss der Umrechnung automatisch eine intelligente Rundung anwenden.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Wenn ich die Seite „Kaufvertrag“ in einem Positionsansichtsmodus öffne, kann ich die Seite nicht personalisieren, indem ich das Feld „Preiseinheit“ in der Übersicht der Position hinzufüge.

Einige gemeinsam genutzte Felder im Vereinbarungsframework können nicht in Personalisierungen einbezogen werden. Diese Einschränkung tritt aufgrund des implementierten Datenmodells auf. Daher können Sie das **Preiseinheit**-Feld nicht personalisieren.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Das maximale Limit aus einem Kaufvertrag gilt nicht für eine Bestellanforderung.

### <a name="issue-description"></a>Problembeschreibung

Wenn eine Bestellanforderung mit einem Kaufvertrag verknüpft ist, gilt das maximale Limit aus dem Kaufvertrag nicht für die Bestellanforderung. Die Standardpreisinformationen werden korrekt eingegeben, es kann jedoch mehr als das maximale Limit aus dem Kaufvertrag in der Bestellanforderung bestellt werden.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten wird erwartet. Da Anforderungen nicht immer genehmigt werden, sollte eine Menge oder ein Betrag nicht im Kaufvertrag reserviert werden. Daher werden Sie das Höchstlimit aus dem Kaufvertrag nicht erreichen.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Handelsabkommen können aus abgelehnten Angebotsanforderungen erstellt werden. Daher verhindert das System nicht, dass Handelsabkommensjournale erstellt werden, wenn die Angebotsanforderungen-Position nicht akzeptiert wurde.

Sie können Handelsabkommen für alle Antworten auf eine Angebotsanforderungen (RFQ) erstellen, unabhängig davon, ob sie akzeptiert oder abgelehnt wurden. Weitere Informationen finden Sie unter [ÜBersicht der Angebotsanforderungen (RFQs)](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]