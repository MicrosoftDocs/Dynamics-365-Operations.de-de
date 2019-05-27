---
title: Dimensionen erstellen und Dimensionsmitglieder importieren
description: Die Kostenrechnung ist ein unabhängiges Modul, das Masterdaten aus anderen Modulen erfordert.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d48ba0a0b80d251e107baa0ceeb66d8e328f13dc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565718"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="43a6b-103">Dimensionen erstellen und Dimensionsmitglieder importieren</span><span class="sxs-lookup"><span data-stu-id="43a6b-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43a6b-104">Die Kostenrechnung ist ein unabhängiges Modul, das Masterdaten aus anderen Modulen erfordert.</span><span class="sxs-lookup"><span data-stu-id="43a6b-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="43a6b-105">Diese Daten werden in wie folgt kategorisiert:</span><span class="sxs-lookup"><span data-stu-id="43a6b-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="43a6b-106">Kostenelemente</span><span class="sxs-lookup"><span data-stu-id="43a6b-106">Cost elements</span></span>
-  <span data-ttu-id="43a6b-107">Kostenobjekte</span><span class="sxs-lookup"><span data-stu-id="43a6b-107">Cost objects</span></span>
-  <span data-ttu-id="43a6b-108">Statistische Dimensionen</span><span class="sxs-lookup"><span data-stu-id="43a6b-108">Statistical dimensions</span></span>

<span data-ttu-id="43a6b-109">Ein **Kostenelement** entspricht einem kostenrelevanten Artikel in dem Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="43a6b-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="43a6b-110">Ein **Kostenträger** entspricht einem Typ der Finanzdimension wie Produkte, Kostenstellen und Projekte, für die Sie Kosten schätzen, zuweisen oder direkt messen möchten.</span><span class="sxs-lookup"><span data-stu-id="43a6b-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="43a6b-111">Eine **Statistischen Dimension** und seine Mitgliedern werden verwendet, um nicht monetäre Einträge in der Kostenrechnung zu erfassen und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="43a6b-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="43a6b-112">Statistische Dimensionswerte können als Verrechnungsgrundlage in den Richtlinien wie Kostenaufteilung und Prozentsatz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43a6b-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="43a6b-113">Das folgende Diagramm veranschaulicht die Dimensionen, die in der Kostenrechnung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43a6b-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="43a6b-114">[![Kostenrechnungsdimensionen](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="43a6b-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="43a6b-115">Nachdem die Daten in die Kostenrechnung importiert wurden, können Variablengruppen verwendet werden, um unterschiedliche Perspektiven zu erstellen, die Manager auf allen Ebenen der Organisation Einblicke geben.</span><span class="sxs-lookup"><span data-stu-id="43a6b-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="43a6b-116">Unter den folgenden Themen finden Sie Informationen zum Erstellen von Dimensionen und importieren von Dimensionsmitgliedern.</span><span class="sxs-lookup"><span data-stu-id="43a6b-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="43a6b-117">Kostenelementdimensionen</span><span class="sxs-lookup"><span data-stu-id="43a6b-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="43a6b-118">Kostenelemente erstellen (Aufgabenleitfaden)</span><span class="sxs-lookup"><span data-stu-id="43a6b-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="43a6b-119">Kostenobjektdimensionen</span><span class="sxs-lookup"><span data-stu-id="43a6b-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="43a6b-120">Kostenelemente erstellen (Aufgabenleitfaden)</span><span class="sxs-lookup"><span data-stu-id="43a6b-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="43a6b-121">Kostenelement-Dimensionselemente einem allgemeinen Satz von Dimensionselementen zuordnen</span><span class="sxs-lookup"><span data-stu-id="43a6b-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="43a6b-122">Eine Kostenelementdimension zuordnen (Aufgabenleitfaden)</span><span class="sxs-lookup"><span data-stu-id="43a6b-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="43a6b-123">Statistische Dimensionselement und statistischen Maßnahmenanbieter-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="43a6b-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)






