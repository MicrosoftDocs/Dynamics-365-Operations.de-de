---
title: Buchung von Standardkostenabweichungen
description: In diesem Artikel finden Sie Informationen über die Einrichtung von Buchungsprofilen für die Nachkalkulation.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: e7b2d04f32b75dbd1354b3ef74a41ea1b6469c8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894876"
---
# <a name="standard-cost-variance-posting"></a>Buchung von Standardkostenabweichungen

Wenn Sie die Nachkalkulation für ein oder mehrere Produkte in Ihrem Unternehmen verwenden, müssen Sie die [Voraussetzungen für die Nachkalkulation](/supply-chain/cost-management/prerequisites-standard-costs.md) konfigurieren. Dieser Artikel erklärt die Buchungskonten, die für Schritt 3 der Voraussetzungen, „Sachkonten den Artikelbuchungen zuordnen, die sich auf Standardkostenabweichungen beziehen.“, erforderlich sind.

Bei Käufen und Produktionsaufträgen können unterschiedliche Arten von Abweichungen auftreten. Beispiele für Produktionsabweichungen finden Sie unter [Gängige Quellen für Produktionsabweichungen](/supply-chain/cost-management/common-sources-of-production-variances.md). Preisabweichungen bei Bestellungen treten auf, wenn Sie Standardkosten für einen gekauften Artikel verwenden und es eine Differenz zwischen den Standardkosten des Produkts und dem Rechnungsbetrag auf der Bestellung gibt.

## <a name="sample-posting-profile-configuration"></a>Beispiel für die Konfiguration eines Buchungsprofils

In der folgenden Tabelle finden Sie Beispiele für die Standardbuchungsarten. Es enthält Beispiele für Hauptkonten und Beschreibungen.

- Die „Soll/Haben?“ Die Spalte „Soll“ gibt an, ob es sich bei der Transaktion typischerweise um eine Belastung oder eine Gutschrift handelt. In manchen Fällen kann die Transaktion entweder Soll oder Haben buchen.
- Die Spalte „Verrechnungskonto“ zeigt an, dass die Buchungsart ein Verrechnungskonto ist. Mit anderen Worten: Der Betrag, der auf diesem Konto gebucht wird, wird automatisch storniert, wenn eine spätere Transaktion gebucht wird.
- Die Spalte „P/F“ zeigt die Art der Buchung an. „P“ steht für die physische Buchung und „F“ für die finanzielle Buchung.
- Die Spalte „Folgen“ zeigt an, ob das Hauptkonto für die Buchungsart in der Regel dasselbe ist wie das Hauptkonto für eine andere Buchungsart. Er gibt insbesondere die Buchungsart an, die normalerweise verwendet wird.

> [!NOTE]
> Die Hauptkonten und die Namen der Hauptkonten in der Tabelle sind Vorschläge. Wir empfehlen Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um die beste Konfiguration für Ihre geschäftlichen Anforderungen zu ermitteln.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | P/F | Folgen | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Einkaufspreisabweichung | 510310 | Einkaufspreisabweichung | Ausgaben | Entweder | Nein | Fr | Nicht zutreffend | Dieses Konto wird verwendet, wenn es eine Abweichung zwischen dem Einkaufspreis und den Standardkosten auf einer Bestellung gibt. |
| Neubewertung der Lagerkosten | 510330 | Neubewertung der Lagerkosten | Ausgaben | Entweder | Nein | Fr | Nicht zutreffend | Dieses Konto wird verwendet, wenn eine neue Kalkulationsversion für einen Standardkostenartikel aktiviert wird, um den Lagerbestand neu zu bewerten. |
| Abweichung bei Kostenänderung | 510320 | Abweichung bei Kostenänderung | Ausgaben | Entweder | Nein | Fr | Nicht zutreffend | Dieses Konto wird verwendet, wenn es Unterschiede bei den Standardkosten zwischen den Standorten gibt oder wenn ein Artikel zurückgegeben wird und sich die ursprünglichen Standardkosten von den aktuellen Standardkosten für ein Produkt unterscheiden. |
| Abweichung bei Produktionslosgröße | 510370 | Abweichung bei Produktionslosgröße | Ausgaben | Entweder | Nein | Fr | Nicht zutreffend | Dieses Konto wird verwendet, wenn es Differenzen zwischen der Kalkulationsbasis der Stückliste und der tatsächlichen Menge für die Nachkalkulation des Fertigungsauftrags gibt. |
| Produktionspreisabweichung | 510340 | Produktionspreisabweichung | Ausgaben | Entweder | Nein | Fr | Nicht zutreffend | Dieses Konto wird verwendet, wenn es Preisunterschiede zwischen den geschätzten Kosten und den tatsächlichen Kosten für einen Produktionsauftrag gibt. |
| Abweichung bei Produktionsmenge | 510350 | Abweichung bei Produktionsmenge | Ausgaben | Entweder | Nein | Fr | Nicht zutreffend | Dieses Konto wird verwendet, wenn es Mengendifferenzen zwischen den geschätzten Kosten und den tatsächlichen Kosten für einen Produktionsauftrag gibt. |
| Abweichung bei Produktionsersetzung | 510360 | Abweichung bei Produktionsersetzung | Ausgaben | Entweder | Nein | Fr | Nicht zutreffend | Dieses Konto wird verwendet, wenn es bei einem Produktionsauftrag zu einem unerwarteten Verbrauch kommt. |
| Rundungsabweichung | 618160 | Rundungsdifferenz | Ausgaben | Entweder | Nein | Fr | Nicht zutreffend | Dieses Konto wird verwendet, wenn bei der Nachkalkulation der Produktionskosten eine Rundungsdifferenz auftritt. |
