---
title: Preisregulierungen und Rabatte
description: Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Microsoft Dynamics 365 for Retail.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 61ac8e5fbdc4d91bb5bc5372a7fb96633043473a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "350963"
---
# <a name="price-adjustments-and-discounts"></a>Preisregulierungen und Rabatte

[!include [banner](includes/banner.md)]

Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Microsoft Dynamics 365 for Retail.

Sie können in Dynamics 365 for Retail Preisregulierungen an Produkten vornehmen und zudem Rabatte einrichten, die auf einen Positionsartikel oder eine Transaktion in der Verkaufsstelle (POS), in einem Callcenterauftrag oder einem Onlineauftrag angewendet werden. Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden. Für sowohl Preisregulierungen als auch Rabatte können Sie ein einzelnes Start- und Enddatum bzw. einen Wiederholungszeitraum, einen Rabattcode und einige weitere Attribute angeben. Preisregulierungen und Rabatte können auf Produkte, Varianten oder Kategorien angewendet werden. Entspricht mehr als ein Rabatt einem Produkt, erhält ein Debitor möglicherweise entweder einen der Rabatte oder einen kombinierten Rabatt, abhängig von der Konfiguration des Rabatts. Dynamics 365 for Retail übernimmt automatisch den Rabatt oder die Kombination von Rabatten, die dem Kunden den besten Preis ermöglichen. Wenn Sie eine Preisregulierung oder einen Rabatt einrichten, sollten Sie sich vergewissern, dass Sie bestätigen, dass Preisgruppen den richtigen Kanälen, Katalogen, Zuordnungen oder Treueprogrammen zugeordnet sind, für die der Rabatt gelten soll. Auch wenn Sie die Rabattkennung automatisch generieren möchten, können Sie Nummernkreise auf der Seite **Einzelhandelsparameter** einrichten, bevor Sie einen neuen Rabatt oder eine Preisregulierung definieren.

> [!NOTE]
> Sie können eine Preisregulierung oder einen Rabatt löschen. Allerdings gehen statistische Daten verloren.

## <a name="types-of-discounts"></a>Rabatttypen

Es gibt vier Arten von Einzelhandelsrabatten:

- **Einfacher Rabatt** - ein einzelner Prozentsatz oder ein Betrag.
- **Mengenrabatt** – Ein Rabatt, der bei Kauf von zwei oder mehr Produkten angewendet wird.
- **Rabatt für Angebots-Sortiment** – Ein Rabatt, der beim Kauf einer bestimmten Kombination von Produkten angewendet wird.
- **Schwellenwertrabatt** – Ein Rabatt, der angewendet wird, wenn die Summe der Buchung höher als ein angegebener Betrag ist.

Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden. Preisgruppen können anschließend Kanälen, Katalogen, Zuordnungen und Treueprogrammen zugeordnet werden.
