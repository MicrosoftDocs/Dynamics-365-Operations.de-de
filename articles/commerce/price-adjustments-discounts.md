---
title: Preisregulierungen und Rabatte
description: Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Commerce.
author: josaw1
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.industry: Retail
ms.search.form: RetailParameters, RetailPeriodicDiscount
ms.openlocfilehash: ff90df814d6930b5cf92772e430625943e0ae983
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279088"
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

> [!NOTE]
> Der Mix-and-Match-Rabatt und der Schwellenrabatt haben die Eigenschaften „Nicht rabattfähige Produkte zählen“ bzw. „Nicht rabattierbare Produkte auf den Schwellenwert anrechnen“. Wenn diese Eigenschaften aktiviert sind, kann ein Artikel, für den kein Rabatt in Frage kommt, dennoch dazu beitragen, eine Transaktion für den Rabatt zu qualifizieren, aber der nicht rabattfähige Artikel erhält keinen Rabatt. 
> 
> Wenn Sie beispielsweise einen Mix-and-Match-Rabatt mit zwei Zeilen A und B erstellen, bei dem ein Kunde 10 % Rabatt auf beide Artikel erhalten soll, aber Artikel A die Konfiguration „Alle Rabatte verhindern“ aktiviert hat, dann würde dies normalerweise den Artikel stoppen A von der Ermäßigung ab. Wenn jedoch die Eigenschaft „Nicht rabattierbare Produkte zählen“ aktiviert ist, kann Artikel A verwendet werden, um sich für den Mix-and-Match-Rabatt zu qualifizieren, aber der Rabatt von 10 % wird nur auf Artikel B angewendet. Eine ähnliche Logik gilt für den Schwellenrabatt. 
>
> Die Eigenschaft „Nicht rabattfähige Produkte zum Schwellenwert zählen“ hat jedoch eine zusätzliche Funktion im Vergleich zur Eigenschaft „Nicht rabattierbare Produkte zählen“ der Mix-and-Match-Rabatte. Wenn der Schwellenrabatt aktiviert ist und es für einen Artikel einen bestehenden Rabatt gibt, der den Artikel von anderen Rabatten abhalten würde, würde der für diesen Artikel bezahlte Preis den Schwellenwert erreichen, aber dieser Artikel erhält keine zusätzlichen Rabatte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
