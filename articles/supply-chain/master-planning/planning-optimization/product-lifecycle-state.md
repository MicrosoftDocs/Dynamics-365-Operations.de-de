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
ms.openlocfilehash: 02c31aa3862df8dabc2b8c065dc3a94877d237f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992419"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="96291-103">Ausschließen von Produkten, die bestimmte Status im Produktlebenszyklus haben</span><span class="sxs-lookup"><span data-stu-id="96291-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96291-104">Freigegebene Produkte und freigegebene Produktversionen enthalten ein **Produktlebenszyklus-Status**-Feld.</span><span class="sxs-lookup"><span data-stu-id="96291-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="96291-105">Mit diesem Feld können Sie u. a. steuern, welche Produkte bei der Produktprogrammplanung berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="96291-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="96291-106">Sie können Lebenszyklusstatus nach Bedarf hinzufügen, entfernen und bearbeiten, indem Sie zu **Produktinformationsmanagement \> Einrichten \> Produktlebenszyklusstatus** gehen.</span><span class="sxs-lookup"><span data-stu-id="96291-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="96291-107">Legen Sie für jeden Produktlebenszyklus-Status die Option **Ist aktiv für die Planung** auf *Ja* fest, wenn Produkte, die diesen Status haben, bei der Produktprogrammplanung berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96291-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="96291-108">Wenn die Option auf *Nein* festgelegt ist, werden die zugehörigen Produkte und Varianten von der gesamten Produktprogrammplanung und allen Berechnungen auf Stücklisten-Ebene ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="96291-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="96291-109">Freigegebene Produkte und Varianten, bei denen das Feld **Produktlebenszyklus-Status** leer gelassen wird, werden so behandelt, als hätten sie einen Produktlebenszyklus-Status, bei dem die Option **Ist für die Planung aktiv** auf *Ja* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="96291-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="96291-110">Mit anderen Worten: Sie werden bei der Produktprogrammplanung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="96291-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="96291-111">Um unnötige Liefervorschläge zu vermeiden, empfehlen wir Ihnen dringend, alle veralteten freigegebenen Produkte und Varianten mit einem Produktlebenszyklus-Status zu verknüpfen, bei dem die Option **Ist aktiv für die Planung** auf *Nein* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="96291-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="96291-112">Diese Vorgehensweise ist besonders wichtig, wenn Sie mit Produktkonfigurationsvarianten arbeiten, die nicht wiederverwendbar sind, weil dadurch Verschwendung vermieden werden kann.</span><span class="sxs-lookup"><span data-stu-id="96291-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="96291-113">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="96291-113">Related resources</span></span>

<span data-ttu-id="96291-114">Weitere Informationen zu den Status im Produktlebenszyklus finden Sie unter [Übersicht über den Status im Produktlebenszyklus](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="96291-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="96291-115">Detaillierte Informationen mit Schritten zur Verwendung von Produktlebenszyklusstatus zum Ausschluss von Produkten aus der Produktprogrammplanung und Berechnungen auf Stücklistenebene finden Sie unter [Erstellen eines Produktlebenszyklusstatus zum Ausschluss von Produkten aus der Produktprogrammplanung](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="96291-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>
