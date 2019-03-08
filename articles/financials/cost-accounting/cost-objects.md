---
title: Kostenobjektdimensionen
description: Wenn Sie Kosten analysieren, verwenden Sie Kostenelementdimensionen, um zu bestimmen, wohin Kosten fließen. Sie verwenden Kostenträgerdimensionen, um zu bestimmen, wo Sie Kosten zuweisen sollten. Dieses Thema bietet Informationen über Kostenträgerdimensionen.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 60a6575387a6ebe3b349a61368a7561d78dc69f3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "310345"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="0ac35-105">Kostenobjektdimensionen</span><span class="sxs-lookup"><span data-stu-id="0ac35-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ac35-106">Wenn Sie Kosten analysieren, verwenden Sie Kostenelementdimensionen, um zu bestimmen, wohin Kosten fließen.</span><span class="sxs-lookup"><span data-stu-id="0ac35-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="0ac35-107">Sie verwenden Kostenträgerdimensionen, um zu bestimmen, wo Sie Kosten zuweisen sollten.</span><span class="sxs-lookup"><span data-stu-id="0ac35-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="0ac35-108">Dieses Thema bietet Informationen über Kostenträgerdimensionen.</span><span class="sxs-lookup"><span data-stu-id="0ac35-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="0ac35-109">Ein Kostenträger kann jeder Typ von Objekt sein, den Sie vorkalkulieren möchten, dem Sie Kosten zuteilen möchten oder den sie direkt messen möchten.</span><span class="sxs-lookup"><span data-stu-id="0ac35-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="0ac35-110">Typische Kostenträger sind unter Anderem Produkte, Projekte, Ressourcen, Abteilungen, Kostenstellen und geografische Regionen.</span><span class="sxs-lookup"><span data-stu-id="0ac35-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="0ac35-111">Die Verwaltung verwendet Kostenträger, um Kosten mengenmäßig zu bestimmen und auch um die Rentabilitätsanalyse voranzutreiben.</span><span class="sxs-lookup"><span data-stu-id="0ac35-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="0ac35-112">Kostenträgerdimensionen und Kostenträger-Dimensionsmitglieder</span><span class="sxs-lookup"><span data-stu-id="0ac35-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="0ac35-113">Kostenträger werden als *Kostenträgerdimensionen* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0ac35-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="0ac35-114">Nachdem Sie sich entschieden haben, auf welche Entität die Kostenträgerdimension verweisen soll, müssen Sie die einzelnen Dimensionswerte angeben oder sie in die Kostenrechnung aus anderen Quellsystemen importieren.</span><span class="sxs-lookup"><span data-stu-id="0ac35-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="0ac35-115">Diese einzelnen Dimensionswerte sind als *Kostenträger-Dimensionsmitglieder* bekannt.</span><span class="sxs-lookup"><span data-stu-id="0ac35-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="0ac35-116">Sie möchten beispielsweise die Finanzdimension, die als „Kostenstelle” bezeichnet wird, als die Kostenträgerdimension verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ac35-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="0ac35-117">Um zu sehen, wie Kosten zu einzelnen Kostenstellen fließen, müssen Sie die Kostenträger-Dimensionsmitglieder importieren.</span><span class="sxs-lookup"><span data-stu-id="0ac35-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="0ac35-118">In diesem Fall sind die Kostenträger-Dimensionsmitglieder die Istkostenstellen, beispielsweise Vertrieb, Produktion, Verwaltung und geografische Orte.</span><span class="sxs-lookup"><span data-stu-id="0ac35-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="0ac35-119">Das folgende Screenshot zeigt ein Beispiel von Kostenstellen als die Kostenträgerdimension mit ihren Istkostenstellen als Kostenträger-Dimensionsmitglieder an.</span><span class="sxs-lookup"><span data-stu-id="0ac35-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="0ac35-120">[![Kostenobjektdimension](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="0ac35-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="0ac35-121">Kostenträger-Dimensionsmitglieder über Datenkonnektoren importieren</span><span class="sxs-lookup"><span data-stu-id="0ac35-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="0ac35-122">Um den Import von den Kostenträgerdimensionsmitgliedern zu erleichtern, verwenden Sie Datenkonnektoren, um die Werte aus den Entitäten abzurufen, die Sie als Kostenträgerdimensionen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="0ac35-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="0ac35-123">Sie können entweder die bereits erstellten Datenkonnektoren oder benutzerdefinierte Datenkonnektoren, die Sie erstellen, verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ac35-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>



