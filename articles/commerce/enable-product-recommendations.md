---
title: Produktempfehlungen aktivieren
description: In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154412"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="fd644-103">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="fd644-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd644-104">In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="fd644-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="fd644-105">Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fd644-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="fd644-106">Produktempfehlungen Vor-Prüfung</span><span class="sxs-lookup"><span data-stu-id="fd644-106">Recommendations pre-check</span></span>

<span data-ttu-id="fd644-107">Vor dem Aktivieren beachten Sie, dass Produktempfehlungen nur für Commerce-Kunden unterstützt werden, die ihren Speicher für die Nutzung von Azure Data Lake Storage (ADLS) migriert haben.</span><span class="sxs-lookup"><span data-stu-id="fd644-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="fd644-108">Schritte zum Aktivieren von ADLS finden Sie unter [So aktivieren Sie ADLS in einer Dynamics 365-Umgebung](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fd644-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="fd644-109">Außerdem stellen Sie sicher, dass RetailSale-Messungen aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="fd644-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="fd644-110">Weitere Informationen über diesen Einrichtungsprozess finden Sie [hier.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="fd644-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="fd644-111">Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="fd644-111">Turn on recommendations</span></span>

<span data-ttu-id="fd644-112">Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="fd644-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="fd644-113">Gehen Sie zu **Retail und Commerce &gt; Produktempfehlungen &gt; Empfehlungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="fd644-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="fd644-114">In der Liste der freigegebenen Parameter wählen Sie **Empfehlungs-Listen** aus.</span><span class="sxs-lookup"><span data-stu-id="fd644-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="fd644-115">Legen Sie die Option **Empfehlungen aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="fd644-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Produktempfehlungen aktivieren](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="fd644-117">Diese Verfahren startet den Vorgang zum Generieren von Produktempfehlungslisten.</span><span class="sxs-lookup"><span data-stu-id="fd644-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="fd644-118">Bis zu mehreren Stunden können erforderlich sein, bevor die Listen zur Verfügung stehen und können an der Verkaufsstelle (POS) oder in Dynamics 365 Commerce angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd644-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="fd644-119">Konfigurieren Sie Empfehlungslistenparameter</span><span class="sxs-lookup"><span data-stu-id="fd644-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="fd644-120">Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte.</span><span class="sxs-lookup"><span data-stu-id="fd644-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="fd644-121">Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fd644-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="fd644-122">Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="fd644-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="fd644-123">Empfehlungen für POS-Geräte anzeigen</span><span class="sxs-lookup"><span data-stu-id="fd644-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="fd644-124">Nachdem Empfehlungen im Commerce-Back-Office aktiviert wurden, muss der Empfehlungsbereich zum Bildschirm der POS-Steuerung über das Layouttool hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fd644-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="fd644-125">Informationen zu diesem Vorgang finden Sie unter [Hinzufügen eines Empfehlungssteuerelements zum Transaktionsbildschirm auf POS-Geräten](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="fd644-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="fd644-126">Personalisierte Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="fd644-126">Enable personalized recommendations</span></span>

<span data-ttu-id="fd644-127">Weitere Informationen zum Empfangen personalisierter Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fd644-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd644-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fd644-128">Additional resources</span></span>

[<span data-ttu-id="fd644-129">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="fd644-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="fd644-130">ADLS in einer Dynamics 365 Commerce-Umgebung aktivieren</span><span class="sxs-lookup"><span data-stu-id="fd644-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="fd644-131">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="fd644-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="fd644-132">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="fd644-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="fd644-133">Produktempfehlungen am POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="fd644-133">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="fd644-134">Empfehlungen zum Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="fd644-134">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="fd644-135">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="fd644-135">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="fd644-136">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="fd644-136">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="fd644-137">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="fd644-137">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="fd644-138">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="fd644-138">Product recommendations FAQ</span></span>](faq-recommendations.md)

