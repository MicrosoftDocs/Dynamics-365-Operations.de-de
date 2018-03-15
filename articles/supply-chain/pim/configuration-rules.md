---
title: Variantenregeln
description: "Dieser Artikel enthält allgemeine Informationen zu Variantenregeln. Variantenregeln definieren Beziehungen zwischen Artikeln in einer Stückliste (BOM) für Produkte, die die Technologie der dimensionsbasierten Konfiguration verwenden."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bc8e606cdc0bc5a45321c67ce9b089059f226df2
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---

# <a name="configuration-rules"></a><span data-ttu-id="f47ac-104">Variantenregeln</span><span class="sxs-lookup"><span data-stu-id="f47ac-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f47ac-105">Dieser Artikel enthält allgemeine Informationen zu Variantenregeln.</span><span class="sxs-lookup"><span data-stu-id="f47ac-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="f47ac-106">Variantenregeln definieren Beziehungen zwischen Artikeln in einer Stückliste (BOM) für Produkte, die die Technologie der dimensionsbasierten Konfiguration verwenden.</span><span class="sxs-lookup"><span data-stu-id="f47ac-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="f47ac-107">Variantenregeln sind nur verfügbar, wenn Sie dimensionsbasierte Konfigurationsmodelle definieren.</span><span class="sxs-lookup"><span data-stu-id="f47ac-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="f47ac-108">Variantenregeln werden dazu verwendet, bestimmte Artikelkombinationen in einer Stückliste (BOM) entweder zu erzwingen oder zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f47ac-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="f47ac-109">Nachdem eine Stückliste erstellt wurde und die jeweiligen Artikel den entsprechenden Variantengruppen zugewiesen wurden, können Sie eine oder mehrere Variantenregeln definieren.</span><span class="sxs-lookup"><span data-stu-id="f47ac-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="f47ac-110">Wenn zwei Artikel zusammen gehören, wird der Operator **Auswählen** verwendet, um Einbeziehung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f47ac-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="f47ac-111">Wenn zwei Artikel sich gegenseitig ausschließen, wird der Operator **Auswahl aufheben** verwendet, um Ausschluss sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f47ac-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="f47ac-112">**Hinweis:** Diese Informationen gelten nur für Produktmaster, die dimensionsbasierte Konfigurationstechnologie verwenden.</span><span class="sxs-lookup"><span data-stu-id="f47ac-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="f47ac-113">Vorhandene Varianten sind von nachfolgenden Änderungen der Variantenregeln nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="f47ac-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="f47ac-114">Es ist jedoch wichtig, die Regeln vor der Definition einer neuen Variante festzulegen und diese zu prüfen, wenn Sie vermuten, dass die Regeln geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="f47ac-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="f47ac-115">**Hinweis:** Die Methode **Auswählen** bedeutet, dass die abgeleitete Variantengruppe, Artikelnummer und Variante automatisch ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="f47ac-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="f47ac-116">Die Methode **Auswahl aufheben** bedeutet, dass die abgeleitete Variantengruppe, Artikelnummer und Variante nicht ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f47ac-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="f47ac-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f47ac-117">See also</span></span>
--------

[<span data-ttu-id="f47ac-118">Dimensionsbasierte Produktkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f47ac-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




