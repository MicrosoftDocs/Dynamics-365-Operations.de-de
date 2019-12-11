---
title: Produktempfehlungen aktivieren
description: In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770138"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="9b68a-103">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9b68a-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9b68a-104">In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="9b68a-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="9b68a-105">Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9b68a-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="9b68a-106">Produktempfehlungen Vor-Prüfung</span><span class="sxs-lookup"><span data-stu-id="9b68a-106">Recommendations pre-check</span></span>
<span data-ttu-id="9b68a-107">Vor dem Aktivieren beachten Sie, dass Produktempfehlungen nur für F&O-Debitoren unterstützt werden, die 10.0.6 Builds unterstützen und die Lagerung unter Verwendung von BDL migriert haben.</span><span class="sxs-lookup"><span data-stu-id="9b68a-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="9b68a-108">Außerdem stellen Sie sicher, dass RetailSale-Messungen aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="9b68a-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="9b68a-109">Weitere Informationen über diesen Einrichtungsprozess finden Sie [hier.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="9b68a-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="9b68a-110">Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9b68a-110">Turn on recommendations</span></span>

<span data-ttu-id="9b68a-111">Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="9b68a-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="9b68a-112">Gehen Sie zu **Einzelhandel** &gt; **Produktempfehlungen** &gt; **Empfehlungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="9b68a-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="9b68a-113">In der Liste mit freigegebenen Retailparametern, wählen Sie **Empfehlungs-Listen** aus.</span><span class="sxs-lookup"><span data-stu-id="9b68a-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="9b68a-114">Legen Sie die Option **Empfehlungen aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="9b68a-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![Produktempfehlungen aktivieren](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="9b68a-116">Diese Verfahren startet den Vorgang zum Generieren von Produktempfehlungslisten.</span><span class="sxs-lookup"><span data-stu-id="9b68a-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="9b68a-117">Bis zu mehreren Stunden können erforderlich sein, bevor die Listen zur Verfügung stehen und können an der Verkaufsstelle (POS) oder in Dynamics 365 for Commerce angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9b68a-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="9b68a-118">Konfigurieren Sie Empfehlungslistenparameter</span><span class="sxs-lookup"><span data-stu-id="9b68a-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="9b68a-119">Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte.</span><span class="sxs-lookup"><span data-stu-id="9b68a-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="9b68a-120">Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9b68a-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="9b68a-121">Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="9b68a-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="9b68a-122">Empfehlungen für POS-Geräte anzeigen</span><span class="sxs-lookup"><span data-stu-id="9b68a-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="9b68a-123">Nachdem Empfehlungen im Back Office aktiviert wurden, muss der Empfehlungsbereich auf dem Bildschirm der POS-STeuerung über das Layouttool hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9b68a-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="9b68a-124">Weitere Informationen über diesen Prozess finden Sie [hier.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="9b68a-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9b68a-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9b68a-125">Additional resources</span></span>

[<span data-ttu-id="9b68a-126">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="9b68a-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9b68a-127">Hinzufügen von Produktempfehlungslisten zu Seiten</span><span class="sxs-lookup"><span data-stu-id="9b68a-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="9b68a-128">Fügen Sie Empfehlungsbereich für POS-Geräten hinzu</span><span class="sxs-lookup"><span data-stu-id="9b68a-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


