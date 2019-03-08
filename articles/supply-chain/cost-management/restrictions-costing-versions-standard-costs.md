---
title: Einschränkungen für eine Nachkalkulationsversion für Standardkosten
description: In diesem Thema werden die Einschränkungen beschrieben, die für eine Nachkalkulationsversion für Standardkosten gelten.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0383f78ea5cfa42183e0bfe8a96d7d3866766e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "309793"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="8a849-103">Einschränkungen für eine Nachkalkulationsversion für Standardkosten</span><span class="sxs-lookup"><span data-stu-id="8a849-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a849-104">In diesem Thema werden die Einschränkungen beschrieben, die für eine Nachkalkulationsversion für Standardkosten gelten.</span><span class="sxs-lookup"><span data-stu-id="8a849-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="8a849-105">Durch die folgenden Einschränkungen wird besser gewährleistet, dass die Standardprinzipien der Nachkalkulation eingehalten werden:</span><span class="sxs-lookup"><span data-stu-id="8a849-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="8a849-106">Belastungen müssen in die Kosten eines Artikels einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="8a849-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="8a849-107">Die Belastungen für einen produzierten Artikel stellen die amortisierten konstanten Kosten aus den Stücklisten- und Arbeitsplaninformationen dar.</span><span class="sxs-lookup"><span data-stu-id="8a849-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="8a849-108">Die Gebühren müssen daher in den Einheitenkosten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="8a849-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="8a849-109">Die Belastungen für einen eingekauften Artikel werden ebenfalls in die Einheitenkosten des Artikels einbezogen.</span><span class="sxs-lookup"><span data-stu-id="8a849-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="8a849-110">Die Berechnung von Standardkosten für produzierte Artikel muss auf den Kostendatensätzen in einer Nachkalkulationsversion für Standardkosten basieren.</span><span class="sxs-lookup"><span data-stu-id="8a849-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="8a849-111">Alternative Quellen für Kostendaten können ausschließlich mit einer Nachkalkulationsversion für geplante Kosten – beispielsweise mit Einkaufspreis-Handelsvereinbarungen für eingekaufte Artikel – verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a849-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="8a849-112">Alternative Quellen für Kostendaten werden durch die Stücklistenberechnungsgruppe definiert.</span><span class="sxs-lookup"><span data-stu-id="8a849-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="8a849-113">Herstellkostenkalkulationen müssen unter Verwendung eines Stücklistenauflösungsmodus mit nur einer Ebene ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8a849-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="8a849-114">Die Artikelkostendaten für Standardkosten können in eine andere Nachkalkulationsversion mit Standardkosten oder geplanten Kosten kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="8a849-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="8a849-115">Die Artikelkostendaten für geplante Kosten können dagegen nicht in eine Kostenversion mit Standardkosten kopiert werden, da die weiter oben in diesem Thema aufgeführten Einschränkungen nicht für geplante Kosten gelten.</span><span class="sxs-lookup"><span data-stu-id="8a849-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="8a849-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8a849-116">Related topics</span></span>
--------

[<span data-ttu-id="8a849-117">Nachkalkulationsversionen</span><span class="sxs-lookup"><span data-stu-id="8a849-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="8a849-118">Aktualisieren der Standardkosten in einer Umgebung ohne Produktionstätigkeit</span><span class="sxs-lookup"><span data-stu-id="8a849-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="8a849-119">Vorbereiten der Verwaltung von Standardkosten für produzierte Artikel</span><span class="sxs-lookup"><span data-stu-id="8a849-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

