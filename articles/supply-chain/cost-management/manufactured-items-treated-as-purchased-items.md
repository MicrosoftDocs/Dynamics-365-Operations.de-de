---
title: Einrichten von Produkten, die produziert werden oder beschafft werden
description: 'Produkte können auf unterschiedliche Arten bezogen werden: Sie können produziert (hergestellt) oder beschafft (eingekauft) werden. In diesem Artikel werden einige typische Punkte beschrieben, die Sie berücksichtigen müssen, wenn Sie Produkte zur Inanspruchnahme mehrerer Quellen konfigurieren.'
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e68488a714764e7260fb141ccecdc361a8fd7bfa
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214710"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="0f96f-104">Einrichten von Produkten, die produziert werden oder beschafft werden</span><span class="sxs-lookup"><span data-stu-id="0f96f-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f96f-105">Produkte können auf unterschiedliche Arten bezogen werden: Sie können produziert (hergestellt) oder beschafft (eingekauft) werden.</span><span class="sxs-lookup"><span data-stu-id="0f96f-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="0f96f-106">In diesem Artikel werden einige typische Punkte beschrieben, die Sie berücksichtigen müssen, wenn Sie Produkte zur Inanspruchnahme mehrerer Quellen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0f96f-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="0f96f-107">Die Inanspruchnahme mehrerer Quellen wird in der Regel für einen gekauften Artikel verwendet, die gelegentlich produziert werden, oder wenn ein Artikel, der in erster Linie ein produzierter Artikel war, geändert wird, sodass dieser nun in erster Linie ein eingekaufter Artikel ist.</span><span class="sxs-lookup"><span data-stu-id="0f96f-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="0f96f-108">Der Artikel wird zunächst als produzierter Artikel festgelegt, um die Stückliste und die Arbeitsplaninformationen zu definieren und die Produktionsaufträge für den Artikel zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0f96f-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="0f96f-109">Der Produktionstyp soll auf **Stückliste** festgelegt werden (oder, für die Fertigungsverarbeitung**Formel** oder **Kuppelprodukt**).</span><span class="sxs-lookup"><span data-stu-id="0f96f-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="0f96f-110">Wenn Sie Standardkosten verwenden, kann der Artikelkostendatensatz für den produzierten Artikel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f96f-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="0f96f-111">Der Artikelkostendatensatz entspricht möglicherweise nicht den Standardkosten, die für Kaufzwecke vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="0f96f-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="0f96f-112">Die gewünschten Standardkosten müssen in diesem Fall manuell eingegeben und für den Artikelkostendatensatz aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0f96f-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="0f96f-113">Für die Kostenberechnung, sollten Sie eine spezielle Stückliste und einen Arbeitsplan verwenden, die die Zubehörmischung des Produkts im Laufe eines Finanzzeitraums darstellen, um die Abweichungen im Zeitverlauf zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="0f96f-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="0f96f-114">Außerdem kann ein produzierter Artikel, der sich an einem bestimmten Standort befindet, an einen anderen Standort umgelagert werden.</span><span class="sxs-lookup"><span data-stu-id="0f96f-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="0f96f-115">Daher müssen die Kosten des Artikels für den Standort, an den der Artikel umgelagert wird, manuell eingegeben und aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0f96f-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="0f96f-116">Bei Verwendung des produzierten Artikels als Komponente in höher eingestuften Produkten sollten die Kosten der Komponente als gekaufte Artikel behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="0f96f-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="0f96f-117">Diese Richtlinie ist gültig – egal, ob die Kosten der Komponente berechnet oder manuell eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="0f96f-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="0f96f-118">Dies bedeutet, dass bei einer Stücklistenkalkulation die Kosten des Artikels als gekaufte Komponente behandelt werden sollten, anstatt die Stückliste und die Arbeitsplaninformationen des Artikel zur Kostenberechnung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f96f-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="0f96f-119">Diese Berechnung kann durch Auswählen der Kennzeichnung **Stücklistenauflösung beenden** verhindert werden, die in die dem Artikel zugeordneten Herstellkostenkalkulationsgruppe eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="0f96f-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="0f96f-120">Um die Auflösung für die Berechnungen der Produktprogrammplanung zu verhindern, legen Sie mittels den Stücklistenauflösungszeitraum in der Artikeldeckung oder der Abdeckungsgruppe auf 0 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="0f96f-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="0f96f-121">Der Artikel wird in der Berechnung der Produktprogrammplanung als gekaufter Artikel behandelt (wie beispielsweise die Empfehlung von Bestellvorschlägen). Weitere Berechnungen für die Stücklisten- und Arbeitsplaninformationen werden nicht durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f96f-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>





