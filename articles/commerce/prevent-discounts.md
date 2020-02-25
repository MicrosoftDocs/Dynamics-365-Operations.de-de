---
title: Optionen zur Sperrung von Rabatten für Einzelhandelsprodukte
description: Es gibt verschiedene Ursachen, warum Einzelhändler mehrere Produkte nicht als ermäßigt anzeigen wollen, entweder während einer Aktion oder während des Verkaufs am Point-of-Sale.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 822bd39bca3a95f073bacea90a8ee58eada50ae2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022699"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="9888d-103">Optionen zur Sperrung von Rabatten für Einzelhandelsprodukte</span><span class="sxs-lookup"><span data-stu-id="9888d-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9888d-104">Es gibt verschiedene Ursachen, warum Einzelhändler mehrere Produkte nicht als ermäßigt anzeigen wollen, entweder während einer Aktion oder während des Verkaufs am Point-of-Sale.</span><span class="sxs-lookup"><span data-stu-id="9888d-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="9888d-105">Die folgenden Optionen, die auf der Registerkarte **Commerce** aus freigegebenen Produkten gefunden werden können, ermöglichen es zu verhindern, alle oder manuell Rabatte zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9888d-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="9888d-106">Die Einstellungen können auf Kategorieebene von der Einzelhandelskategoriehierarchie auch angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9888d-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="9888d-107">**Sperren Sie Alle Rabatte**: Wählen Sie diese Option aus, um alle Arten Rabatte, die angewendet werden können, für dieses Produkt zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="9888d-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="9888d-108">Dazu zählen Aktionen wie Angebots-Sortiment, Mengen und Schwellenwertrabatte sowie manuelle Positions- und Buchungsrabatte, die im Zuge eines Verkaufs von einem POS-Benutzer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9888d-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="9888d-109">**Sperren Sie manuelle Rabatte**: Wählen Sie diese Option, um manuelle Positions- oder Buchungsrabatte nur zu verhindern, die im Rahmen eines Verkaufs von einem POS-Benutzer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9888d-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="9888d-110">Produkte mit dieser Option, die ausgewählt werden, stehen für Aktionen, wie Mischungs- und Abgleichungs- und Menge und Schwellenwertrabatte immer noch zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9888d-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="9888d-111">Hinweis: Diese Einstellungen schränken nicht den Preisüberschreibungsarbeitsgang ein, da dieses den Basispreis festlegt und Rabatt nicht behandelt werden. .</span><span class="sxs-lookup"><span data-stu-id="9888d-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="9888d-112">[![Rabattfeld verhindern](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="9888d-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
