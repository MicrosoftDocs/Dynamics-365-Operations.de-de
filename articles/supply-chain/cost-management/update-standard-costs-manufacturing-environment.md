---
title: Aktualisieren der Standardkosten in einer Produktionsumgebung
description: "Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten in einer Umgebung ohne Produktionstätigkeit."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d228623455a54bb4e7801c42843093ff71ce874b
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="cda87-103">Aktualisieren der Standardkosten in einer Produktionsumgebung</span><span class="sxs-lookup"><span data-stu-id="cda87-103">Update standard costs in a manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cda87-104">Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten in einer Umgebung ohne Produktionstätigkeit.</span><span class="sxs-lookup"><span data-stu-id="cda87-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="cda87-105">Aktualisierungen können neue Artikel, Kostenkategorien oder Berechnungsformeln für indirekte Kosten darstellen.</span><span class="sxs-lookup"><span data-stu-id="cda87-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="cda87-106">Sie können auch Korrekturen und Kostenänderungen wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="cda87-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="cda87-107">Der Typ der Aktualisierung beeinflusst die Schritte, die erforderlich sind, um Standardkosten zu aktualisieren, wie in den folgenden Fällen veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="cda87-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="cda87-108">Geben Sie die erwarteten Standardkostenänderungen für eingekaufte Artikel ein, und ändern Sie anschließend den Status der Artikelkostendatensätze für das entsprechende Datum auf **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="cda87-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="cda87-109">Sie führen jedoch keine Neuberechnung der Kosten für produzierte Artikel durch, für die die eingekauften Artikel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cda87-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="cda87-110">Sie geben die Standardkosten für einen neuen eingekauften Artikel ein, führen jedoch keine Neuberechnung der Kosten für produzierte Artikel mit einer Stücklistenversion (BOM) durch, die den neuen eingekauften Artikel als Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="cda87-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="cda87-111">Sie korrigieren oder ändern die Kosten eines eingekauften Artikels oder Sie ändern die Kostengruppe, die einem eingekauften Artikel zugewiesen ist und berechnen die Kosten für alle produzierten Artikel mit einer Stücklistenversion, die den eingekauften Artikel als Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="cda87-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="cda87-112">Sie ändern die Kosten für eine Kostenkategorie und berechnen die Kosten für alle produzierten Artikel mit einer Arbeitsplanversion, die Arbeitsgänge des Arbeitsplans mit dieser Kostenkategorie enthält.</span><span class="sxs-lookup"><span data-stu-id="cda87-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="cda87-113">Ändern Sie die Kostenkategorien, die Arbeitsgängen des Arbeitsplans zugewiesen sind, oder die Kostengruppe, die Kostenkategorien zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cda87-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="cda87-114">Berechnen Sie anschließend die Kosten für alle produzierten Artikel mit einer Arbeitsplanversion, die Arbeitsgänge des Arbeitsplans mit dieser Kostenkategorie enthält.</span><span class="sxs-lookup"><span data-stu-id="cda87-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="cda87-115">Sie ändern eine Berechnungsformel für indirekte Kosten und berechnen die Kosten für alle produzierten Artikel, auf die sich diese Änderung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="cda87-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="cda87-116">Sie ändern den Produktionsstandort eines produzierten Artikels oder fügen einen Produktionsstandort hinzu und berechnen die Produktionskosten des Artikels für diesen Standort.</span><span class="sxs-lookup"><span data-stu-id="cda87-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="cda87-117">Sie führen eine (Neu-)Berechnung der Kosten für einen produzierten Artikel durch und berechnen die Kosten für alle produzierten Artikel mit einer Stücklistenversion neu, die den produzierten Artikel als Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="cda87-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="cda87-118">Sie berechnen die Kosten für einen neuen produzierten Artikel auf Basis der Informationen zur definierten, genehmigten und aktiven Stückliste bzw. zum Arbeitsplan.</span><span class="sxs-lookup"><span data-stu-id="cda87-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="cda87-119">Überlegen Sie in jedem der aufgeführten Fälle sehr sorgfältig, wie die Standardkosten aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="cda87-119">Each case requires careful consideration about how to update standard costs.</span></span>




