---
title: "Lagerplatz für Produktions-Warenabgang"
description: "In diesem Thema wird die Hierarchie beschrieben, die verwendet wird, um den Lagerplatz für den Produktions-Warenabgang zu identifizieren."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: e53c8e96579dba3b47bef0c00e55b8fa786fc55c
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="production-output-location"></a><span data-ttu-id="d1111-103">Lagerplatz für Produktions-Warenabgang</span><span class="sxs-lookup"><span data-stu-id="d1111-103">Production output location</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d1111-104">In diesem Thema wird die Hierarchie beschrieben, die verwendet wird, um den Lagerplatz für den Produktions-Warenabgang zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d1111-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="d1111-105">Der Lagerplatz für den Produktions-Warenabgang ist der Lagerplatz, an dem die fertigen Waren zuerst gelagert werden, nachdem sie hergestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d1111-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="d1111-106">Normalerweise ist dieser Lagerplatz nahe dem Produktionsprozess gelegen, durch den die fertigen Produkte hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d1111-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="d1111-107">Der Lagerplatz für den Produktions-Warenabgang wird als Zwischenlager für das Material verwendet, bevor es in den Lieferungsbereich verschoben wird, einen Lagerplatz, einen Lagerplatz für den Wareneingang für den nachfolgenden Produktionsprozess und so weiter.</span><span class="sxs-lookup"><span data-stu-id="d1111-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="d1111-108">Ein standardmäßiger Lagerplatz für den Produktions-Warenabgang wird festgelegt, wenn die fertigen Waren in einem Produktionsauftrag oder einem Chargenauftrag gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d1111-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="d1111-109">Die folgende Hierarchie wird verwendet, um diesen Abgangslagerplatz zu identifizieren:</span><span class="sxs-lookup"><span data-stu-id="d1111-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="d1111-110">Verwenden Sie den Abgangslagerplatz, der im Produktionsauftrag oder dem Chargenauftragskopf definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1111-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="d1111-111">Wenn sich dort kein Lagerplatz befindet, verwenden Sie den Abgangslagerplatz, der in der Ressource definiert ist, die vom letzten Vorgang verwendet wird, der im Produktionsarbeitsplan definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1111-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="d1111-112">Wenn sich dort kein Lagerplatz befindet, verwenden Sie den Abgangslagerplatz, der in der Ressourcengruppe definiert ist, die von der Ressource für den letzten Vorgang verwendet wird, der im Produktionsarbeitsplan definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1111-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="d1111-113">Wenn sich dort kein Lagerplatz befindet, verwenden Sie den Abgangslagerplatz, der für den Lagerort definiert ist, der für den Produktionsauftrag definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1111-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="d1111-114">Ein standardmäßiger Lagerplatz für den Produktions-Warenabgang wird nur für Produkte festgelegt, die mithilfe erweiterter Lagerortprozesse eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="d1111-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="d1111-115">Wenn dieser Artikeltyp als fertig gemeldet wird, wird Lagerortarbeit des Typs **Eingelagerte Fertigerzeugnisse** oder **Einlagerung von Co-Produkt und Nebenprodukt** erstellt.</span><span class="sxs-lookup"><span data-stu-id="d1111-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="d1111-116">Dieser Arbeitstyp verwendet den Lagerplatz für den Produktions-Warenabgang als Entnahmeort.</span><span class="sxs-lookup"><span data-stu-id="d1111-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="d1111-117">Der Einlagerungslagerplatz wird durch Lagerplatzrichtlinien festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d1111-117">The put-away location is determined by the location directives.</span></span>

