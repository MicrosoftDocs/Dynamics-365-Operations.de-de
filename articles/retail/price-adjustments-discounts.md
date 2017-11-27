---
title: Preisregulierungen und Rabatte
description: "Dieser Artikel enthält Informationen zu Preisregulierungen und Rabatten für Microsoft Dynamics 365 for Retail."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9220cc12abf7134d425e088939d20ea03239a75a
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="price-adjustments-and-discounts"></a>Preisregulierungen und Rabatte

[!include[banner](includes/banner.md)]


Dieser Artikel enthält Informationen zu Preisregulierungen und Rabatten für Microsoft Dynamics 365 for Retail.

Im Dynamics 365 for Retail können Sie Preisregulierungen an Produkten vornehmen und Rabatte einrichten, die einem Artikel oder einer Buchung einer Verkaufsstelle (POS), in einem Callcenterauftrag oder in einer Onlinebestellung angewendet werden. Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden. Für sowohl Preisregulierungen als auch Rabatte können Sie ein einzelnes Start- und Enddatum bzw. einen Wiederholungszeitraum, einen Rabattcode und einige weitere Attribute angeben. Preisregulierungen und Rabatte können auf Produkte, Varianten oder Kategorien angewendet werden. Entspricht mehr als ein Rabatt einem Produkt, erhält ein Debitor möglicherweise entweder einen der Rabatte oder einen kombinierten Rabatt, abhängig von der Konfiguration des Rabatts. Dynamics 365 for Retail übernimmt automatisch den Rabatt oder die Kombination von Rabatten, die dem Debitor den besten Preis ermöglichen. Wenn Sie eine Preisregulierung oder einen Rabatt einrichten, sollten Sie sich vergewissern, dass Sie bestätigen, dass Preisgruppen den richtigen Kanälen, Katalogen, Zuordnungen oder Treueprogrammen zugeordnet sind, für die der Rabatt gelten soll. Auch wenn Sie die Rabattkennung automatisch generieren möchten, können Sie Nummernkreise auf der Seite **Einzelhandelsparameter** einrichten, bevor Sie einen neuen Rabatt oder eine Preisregulierung definieren. **Hinweis:** Sie können eine Preisregulierung oder einen Rabatt löschen. Allerdings gehen statistische Daten verloren.

### <a name="types-of-discounts"></a>Rabatttypen

Es gibt vier Arten von Einzelhandelsrabatten:

-   **Einfacher Rabatt** - ein einzelner Prozentsatz oder ein Betrag.
-   **Mengenrabatt** – Ein Rabatt, der bei Kauf von zwei oder mehr Produkten angewendet wird.
-   **Rabatt für Angebots-Sortiment** – Ein Rabatt, der beim Kauf einer bestimmten Kombination von Produkten angewendet wird.
-   **Schwellenwertrabatt** – Ein Rabatt, der angewendet wird, wenn die Summe der Buchung höher als ein angegebener Betrag ist.

Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden. Preisgruppen können anschließend Kanälen, Katalogen, Zuordnungen und Treueprogrammen zugeordnet werden.




