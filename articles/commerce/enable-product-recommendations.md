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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024955"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="98516-103">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="98516-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="98516-104">In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="98516-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="98516-105">Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="98516-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="98516-106">Produktempfehlungen Vor-Prüfung</span><span class="sxs-lookup"><span data-stu-id="98516-106">Recommendations pre-check</span></span>

<span data-ttu-id="98516-107">Vor dem Aktivieren beachten Sie, dass Produktempfehlungen nur für Commerce-Kunden unterstützt werden, die ihren Speicher für die Nutzung von Azure Data Lake Storage (ADLS) migriert haben.</span><span class="sxs-lookup"><span data-stu-id="98516-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="98516-108">Schritte zum Aktivieren von ADLS finden Sie unter [So aktivieren Sie ADLS in einer Dynamics 365-Umgebung](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="98516-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="98516-109">Außerdem stellen Sie sicher, dass RetailSale-Messungen aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="98516-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="98516-110">Weitere Informationen über diesen Einrichtungsprozess finden Sie [hier.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="98516-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="98516-111">Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="98516-111">Turn on recommendations</span></span>

<span data-ttu-id="98516-112">Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="98516-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="98516-113">Gehen Sie zu **Retail und Commerce &gt; Produktempfehlungen &gt; Empfehlungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="98516-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="98516-114">In der Liste der freigegebenen Parameter wählen Sie **Empfehlungs-Listen** aus.</span><span class="sxs-lookup"><span data-stu-id="98516-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="98516-115">Legen Sie die Option **Empfehlungen aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="98516-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Produktempfehlungen aktivieren](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="98516-117">Diese Verfahren startet den Vorgang zum Generieren von Produktempfehlungslisten.</span><span class="sxs-lookup"><span data-stu-id="98516-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="98516-118">Bis zu mehreren Stunden können erforderlich sein, bevor die Listen zur Verfügung stehen und können an der Verkaufsstelle (POS) oder in Dynamics 365 Commerce angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="98516-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="98516-119">Konfigurieren Sie Empfehlungslistenparameter</span><span class="sxs-lookup"><span data-stu-id="98516-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="98516-120">Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte.</span><span class="sxs-lookup"><span data-stu-id="98516-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="98516-121">Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="98516-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="98516-122">Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="98516-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="98516-123">Empfehlungen für POS-Geräte anzeigen</span><span class="sxs-lookup"><span data-stu-id="98516-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="98516-124">Nachdem Empfehlungen im Commerce-Back-Office aktiviert wurden, muss der Empfehlungsbereich zum Bildschirm der POS-Steuerung über das Layouttool hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="98516-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="98516-125">Informationen zu diesem Vorgang finden Sie unter [Hinzufügen eines Empfehlungssteuerelements zum Transaktionsbildschirm auf POS-Geräten](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="98516-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="98516-126">Personalisierte Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="98516-126">Enable personalized recommendations</span></span>

<span data-ttu-id="98516-127">Weitere Informationen zum Empfangen personalisierter Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="98516-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98516-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="98516-128">Additional resources</span></span>

[<span data-ttu-id="98516-129">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="98516-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="98516-130">Personalisierte Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="98516-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="98516-131">Hinzufügen von Produktempfehlungslisten zu Seiten</span><span class="sxs-lookup"><span data-stu-id="98516-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="98516-132">Fügen Sie Empfehlungsbereich für POS-Geräten hinzu</span><span class="sxs-lookup"><span data-stu-id="98516-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="98516-133">Übersicht über Produktsammelmodule</span><span class="sxs-lookup"><span data-stu-id="98516-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="98516-134">Aktivieren von ADLS in einer Dynamics 365-Umgebung</span><span class="sxs-lookup"><span data-stu-id="98516-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

