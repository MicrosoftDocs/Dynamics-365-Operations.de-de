---
title: Häufig gestellte Fragen zur Beschaffung
description: Dieser Artikel bietet Antworten auf häufig gestellte Fragen (FAQs) zur Beschaffungsfunktionalität von Supply Chain Management
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 6e710b254638b255ce4aa3e0adde0dd23bf60f64
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869574"
---
# <a name="procurement-faq"></a>Häufig gestellte Fragen zur Beschaffung

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet Antworten auf häufig gestellte Fragen (FAQs) zur Beschaffungsfunktionalität von Supply Chain Management.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kann ich nur Bestellungen anzeigen, die ich erstellt habe?

Diese Funktionalität ist derzeit nicht verfügbar.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kann ich Bestand reservieren und Transaktionen mit dem registrierten Bestand einer Bestellung erstellen?

### <a name="issue-description"></a>Problembeschreibung

Auch wenn Artikel in einem *Erfasst*-Zustand auf einer Bestellung sind, können Sie den Bestand trotzdem reservieren. Mit anderen Worten, Sie können Transaktionen für den registrierten Bestand erstellen.

### <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Erstellen einer Bestellung.
2. Registrieren Sie die Bestellposition.
3. Beachten Sie, dass Sie Reservierungen oder Transaktionen für den registrierten Bestand generieren können.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt. Es wird erwartet, dass die registrierten Artikel physisch im Lagerort oder im Bestand angekommen sind und daher für eine Reservierung verfügbar sind.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kann ich den Benutzer finden, der eine Bestellung storniert hat?

Diese Information wird nur verfolgt, wenn die Bestellung der Änderungsverwaltung unterliegt. Wenn Sie die Änderungsverwaltung verwenden, können Sie sehen, wer die Änderung (die Stornierung) eingereicht hat und wer sie genehmigt hat.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Warum kann ich einen Kaufvertrag nicht mit einer bestehenden Bestellung verknüpfen?

Ein Kaufvertrag muss einer Bestellung zugewiesen werden, wenn die Bestellung erstellt wird. Andernfalls können Bestellpositionen nicht mit Kaufvertragspositionen verknüpft werden.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Welche Prüfung löst die Meldung „Manuell eingegebene Preise und Rabatte oder externes Dokument aktualisieren“ aus?

Wenn Sie das Versanddatum ändern, erhalten Sie möglicherweise die Meldung „Manuell eingegebene Preise und Rabatte oder externes Dokument aktualisieren“. Sie erhalten diese Nachricht, da bei einer Änderung des Versanddatums möglicherweise ein anderer Handels- oder Verkaufsvertrag ausgelöst wird und eine Preisänderung verursacht. Eine Änderung des Versanddatums kann sich auch auf Lagerpläne und andere verwandte Informationen auswirken.

Die Nachricht wird ausgelöst, wenn eine der Daten oder andere Parameter geändert werden. Der Zweck der Nachricht besteht darin, sicherzustellen, dass Sie über Preisänderungen informiert sind, die aufgrund dieser Änderungen auftreten können.

Die Nachricht ist die Eingabeaufforderung zur Bewertung des Handelsabkommens (TAE). Eine vollständige Beschreibung finden Sie unter [Bewertungsrichtlinien für Handelsabkommen](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Warum kann ich nicht mehr als eine Rechnung für eine Bestellposition mit kategorienbasierten Artikeln buchen?

Eine Menge ist obligatorisch, wenn Sie Rechnungen buchen möchten. Wenn die gesamte Menge einer Position nur für einen Teilbetrag in Rechnung gestellt wurde, können Sie den verbleibenden Betrag nicht auf einer anderen Rechnung in Rechnung stellen.
