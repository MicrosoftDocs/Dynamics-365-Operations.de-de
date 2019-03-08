---
title: Variantenregeln
description: Dieser Artikel enthält allgemeine Informationen zu Variantenregeln. Variantenregeln definieren Beziehungen zwischen Artikeln in einer Stückliste (BOM) für Produkte, die die Technologie der dimensionsbasierten Konfiguration verwenden.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13f37cb4e472e91862e963a4952adcf61e6adcea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "319361"
---
# <a name="configuration-rules"></a><span data-ttu-id="3654d-104">Variantenregeln</span><span class="sxs-lookup"><span data-stu-id="3654d-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3654d-105">Dieser Artikel enthält allgemeine Informationen zu Variantenregeln.</span><span class="sxs-lookup"><span data-stu-id="3654d-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="3654d-106">Variantenregeln definieren Beziehungen zwischen Artikeln in einer Stückliste (BOM) für Produkte, die die Technologie der dimensionsbasierten Konfiguration verwenden.</span><span class="sxs-lookup"><span data-stu-id="3654d-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="3654d-107">Variantenregeln sind nur verfügbar, wenn Sie dimensionsbasierte Konfigurationsmodelle definieren.</span><span class="sxs-lookup"><span data-stu-id="3654d-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="3654d-108">Variantenregeln werden dazu verwendet, bestimmte Artikelkombinationen in einer Stückliste (BOM) entweder zu erzwingen oder zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="3654d-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="3654d-109">Nachdem eine Stückliste erstellt wurde und die jeweiligen Artikel den entsprechenden Variantengruppen zugewiesen wurden, können Sie eine oder mehrere Variantenregeln definieren.</span><span class="sxs-lookup"><span data-stu-id="3654d-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="3654d-110">Wenn zwei Artikel zusammen gehören, wird der Operator **Auswählen** verwendet, um Einbeziehung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3654d-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="3654d-111">Wenn zwei Artikel sich gegenseitig ausschließen, wird der Operator **Auswahl aufheben** verwendet, um Ausschluss sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3654d-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="3654d-112">**Hinweis:** Diese Informationen gelten nur für Produktmaster, die dimensionsbasierte Konfigurationstechnologie verwenden.</span><span class="sxs-lookup"><span data-stu-id="3654d-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="3654d-113">Vorhandene Varianten sind von nachfolgenden Änderungen der Variantenregeln nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="3654d-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="3654d-114">Es ist jedoch wichtig, die Regeln vor der Definition einer neuen Variante festzulegen und diese zu prüfen, wenn Sie vermuten, dass die Regeln geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="3654d-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="3654d-115">**Hinweis:** Die Methode **Auswählen** bedeutet, dass die abgeleitete Variantengruppe, Artikelnummer und Variante automatisch ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3654d-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="3654d-116">Die Methode **Auswahl aufheben** bedeutet, dass die abgeleitete Variantengruppe, Artikelnummer und Variante nicht ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3654d-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="additional-resources"></a><span data-ttu-id="3654d-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3654d-117">Additional resources</span></span>
--------

[<span data-ttu-id="3654d-118">Dimensionsbasierte Produktkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3654d-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)



