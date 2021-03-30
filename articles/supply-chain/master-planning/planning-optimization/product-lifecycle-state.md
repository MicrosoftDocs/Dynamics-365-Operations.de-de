---
title: Ausschließen von Produkten, die bestimmte Status im Produktlebenszyklus haben
description: In diesem Thema wird erklärt, wie Sie Produkte basierend auf ihrem Status im Lebenszyklus ausschließen können, wenn die Funktionalität der Planungsoptimierung verwendet wird.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1e0c734db763ffa69e2d6540a07d5fa04c22ea1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227817"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="b8b95-103">Ausschließen von Produkten, die bestimmte Status im Produktlebenszyklus haben</span><span class="sxs-lookup"><span data-stu-id="b8b95-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8b95-104">Freigegebene Produkte und freigegebene Produktversionen enthalten ein **Produktlebenszyklus-Status**-Feld.</span><span class="sxs-lookup"><span data-stu-id="b8b95-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="b8b95-105">Mit diesem Feld können Sie u. a. steuern, welche Produkte bei der Produktprogrammplanung berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b8b95-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="b8b95-106">Sie können Lebenszyklusstatus nach Bedarf hinzufügen, entfernen und bearbeiten, indem Sie zu **Produktinformationsmanagement \> Einrichten \> Produktlebenszyklusstatus** gehen.</span><span class="sxs-lookup"><span data-stu-id="b8b95-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="b8b95-107">Legen Sie für jeden Produktlebenszyklus-Status die Option **Ist aktiv für die Planung** auf *Ja* fest, wenn Produkte, die diesen Status haben, bei der Produktprogrammplanung berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b8b95-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="b8b95-108">Wenn die Option auf *Nein* festgelegt ist, werden die zugehörigen Produkte und Varianten von der gesamten Produktprogrammplanung und allen Berechnungen auf Stücklisten-Ebene ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b8b95-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="b8b95-109">Freigegebene Produkte und Varianten, bei denen das Feld **Produktlebenszyklus-Status** leer gelassen wird, werden so behandelt, als hätten sie einen Produktlebenszyklus-Status, bei dem die Option **Ist für die Planung aktiv** auf *Ja* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b8b95-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="b8b95-110">Mit anderen Worten: Sie werden bei der Produktprogrammplanung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b8b95-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="b8b95-111">Um unnötige Liefervorschläge zu vermeiden, empfehlen wir Ihnen dringend, alle veralteten freigegebenen Produkte und Varianten mit einem Produktlebenszyklus-Status zu verknüpfen, bei dem die Option **Ist aktiv für die Planung** auf *Nein* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b8b95-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="b8b95-112">Diese Vorgehensweise ist besonders wichtig, wenn Sie mit Produktkonfigurationsvarianten arbeiten, die nicht wiederverwendbar sind, weil dadurch Verschwendung vermieden werden kann.</span><span class="sxs-lookup"><span data-stu-id="b8b95-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="b8b95-113">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b8b95-113">Related resources</span></span>

<span data-ttu-id="b8b95-114">Weitere Informationen zu den Status im Produktlebenszyklus finden Sie unter [Übersicht über den Status im Produktlebenszyklus](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="b8b95-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="b8b95-115">Detaillierte Informationen mit Schritten zur Verwendung von Produktlebenszyklusstatus zum Ausschluss von Produkten aus der Produktprogrammplanung und Berechnungen auf Stücklistenebene finden Sie unter [Erstellen eines Produktlebenszyklusstatus zum Ausschluss von Produkten aus der Produktprogrammplanung](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="b8b95-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]