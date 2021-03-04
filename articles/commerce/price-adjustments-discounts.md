---
title: Preisregulierungen und Rabatte
description: Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0c2adaa5cd935d5b593bfbb3215d3466fcafab7b
ms.sourcegitcommit: 1d74636bf9db5fb33e998322899504b709b4f89f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "4584314"
---
# <a name="price-adjustments-and-discounts"></a>Preisregulierungen und Rabatte

[!include [banner](includes/banner.md)]

Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Commerce.

Sie können in Commerce Preisregulierungen an Produkten vornehmen und zudem Rabatte einrichten, die auf einen Positionsartikel oder eine Transaktion in der Verkaufsstelle (POS), in einem Callcenterauftrag oder einem Onlineauftrag angewendet werden. Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden. Für sowohl Preisregulierungen als auch Rabatte können Sie ein einzelnes Start- und Enddatum bzw. einen Wiederholungszeitraum, einen Rabattcode und einige weitere Attribute angeben. 

Preisregulierungen und Rabatte können auf Produkte, Varianten oder Kategorien angewendet werden. Entspricht mehr als ein Rabatt einem Produkt, erhält ein Debitor möglicherweise entweder einen der Rabatte oder einen kombinierten Rabatt, abhängig von der Konfiguration des Rabatts. Commerce übernimmt automatisch den Rabatt oder die Kombination von Rabatten, die dem Kunden den besten Preis ermöglichen. Wenn Sie eine Preisregulierung oder einen Rabatt einrichten, sollten Sie sich vergewissern, dass Sie bestätigen, dass Preisgruppen den richtigen Kanälen, Katalogen, Zuordnungen oder Treueprogrammen zugeordnet sind, für die der Rabatt gelten soll. Auch wenn Sie die Rabattkennung automatisch generieren möchten, können Sie Nummernkreise auf der Seite **Commerce Parameter** einrichten, bevor Sie einen neuen Rabatt oder eine Preisregulierung definieren.

> [!NOTE]
> Sie können eine Preisregulierung oder einen Rabatt löschen. Allerdings gehen statistische Daten verloren.

## <a name="types-of-discounts"></a>Rabatttypen

Es gibt viele verschiedene Arten von Rabatten:

- **Einfacher Rabatt** - ein einzelner Prozentsatz oder ein Betrag.
- **Mengenrabatt** – Ein Rabatt, der bei Kauf von zwei oder mehr Produkten angewendet wird.
- **Rabatt für Angebots-Sortiment** – Ein Rabatt, der beim Kauf einer bestimmten Kombination von Produkten angewendet wird.
- **Schwellenwertrabatt** – Ein Rabatt, der angewendet wird, wenn die Summe der Buchung höher als ein angegebener Betrag ist.
- **Zahlungsmittelbasierter Rabatt** – Ein Rabatt, der angewendet wird, wenn der Transaktionsbetrag einen angegebenen Betrag überschreitet und eine bestimmte Zahlungsart (z. B. Bargeld, Kredit- oder Debitkarte) zur Zahlung verwendet wird.
- **Lieferrabatt** – Ein Rabatt, der angewendet wird, wenn der Gesamtbetrag der Transaktion einen angegebenen Betrag übersteigt und eine bestimmte Lieferart (z. B. Lieferung in zwei Tagen oder Lieferung über Nacht) beim Auftrag verwendet wird.

Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden. Preisgruppen können anschließend Kanälen, Katalogen, Zuordnungen und Treueprogrammen zugeordnet werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]