---
title: Einschränkungen für eine Nachkalkulationsversion für Standardkosten
description: In diesem Thema werden die Einschränkungen beschrieben, die für eine Nachkalkulationsversion für Standardkosten gelten.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2348d7721cd281bb2a1b5af007c98ce69377a412
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214434"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="4fd7c-103">Einschränkungen für eine Nachkalkulationsversion für Standardkosten</span><span class="sxs-lookup"><span data-stu-id="4fd7c-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fd7c-104">In diesem Thema werden die Einschränkungen beschrieben, die für eine Nachkalkulationsversion für Standardkosten gelten.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="4fd7c-105">Durch die folgenden Einschränkungen wird besser gewährleistet, dass die Standardprinzipien der Nachkalkulation eingehalten werden:</span><span class="sxs-lookup"><span data-stu-id="4fd7c-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="4fd7c-106">Belastungen müssen in die Kosten eines Artikels einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="4fd7c-107">Die Belastungen für einen produzierten Artikel stellen die amortisierten konstanten Kosten aus den Stücklisten- und Arbeitsplaninformationen dar.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="4fd7c-108">Die Gebühren müssen daher in den Einheitenkosten enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="4fd7c-109">Die Belastungen für einen eingekauften Artikel werden ebenfalls in die Einheitenkosten des Artikels einbezogen.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="4fd7c-110">Die Berechnung von Standardkosten für produzierte Artikel muss auf den Kostendatensätzen in einer Nachkalkulationsversion für Standardkosten basieren.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="4fd7c-111">Alternative Quellen für Kostendaten können ausschließlich mit einer Nachkalkulationsversion für geplante Kosten – beispielsweise mit Einkaufspreis-Handelsvereinbarungen für eingekaufte Artikel – verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="4fd7c-112">Alternative Quellen für Kostendaten werden durch die Stücklistenberechnungsgruppe definiert.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="4fd7c-113">Herstellkostenkalkulationen müssen unter Verwendung eines Stücklistenauflösungsmodus mit nur einer Ebene ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="4fd7c-114">Die Artikelkostendaten für Standardkosten können in eine andere Nachkalkulationsversion mit Standardkosten oder geplanten Kosten kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="4fd7c-115">Die Artikelkostendaten für geplante Kosten können dagegen nicht in eine Kostenversion mit Standardkosten kopiert werden, da die weiter oben in diesem Thema aufgeführten Einschränkungen nicht für geplante Kosten gelten.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="4fd7c-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4fd7c-116">Related topics</span></span>
--------

[<span data-ttu-id="4fd7c-117">Nachkalkulationsversionen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="4fd7c-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="4fd7c-118">Aktualisieren der Standardkosten in einer Umgebung ohne Produktion</span><span class="sxs-lookup"><span data-stu-id="4fd7c-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="4fd7c-119">Vorbereiten der Verwaltung von Standardkosten für produzierte Artikel</span><span class="sxs-lookup"><span data-stu-id="4fd7c-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

