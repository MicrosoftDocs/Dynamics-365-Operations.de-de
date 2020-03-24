---
title: Produktempfehlungen aktivieren
description: In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127881"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="1ad86-103">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="1ad86-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ad86-104">In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="1ad86-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="1ad86-105">Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1ad86-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="1ad86-106">Produktempfehlungen Vor-Prüfung</span><span class="sxs-lookup"><span data-stu-id="1ad86-106">Recommendations pre-check</span></span>

<span data-ttu-id="1ad86-107">Vor dem Aktivieren beachten Sie, dass Produktempfehlungen nur für Commerce-Kunden unterstützt werden, die ihren Speicher für die Nutzung von Azure Data Lake Storage (ADLS) migriert haben.</span><span class="sxs-lookup"><span data-stu-id="1ad86-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="1ad86-108">Schritte zum Aktivieren von ADLS finden Sie unter [So aktivieren Sie ADLS in einer Dynamics 365-Umgebung](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1ad86-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="1ad86-109">Außerdem stellen Sie sicher, dass RetailSale-Messungen aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="1ad86-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="1ad86-110">Weitere Informationen über diesen Einrichtungsprozess finden Sie [hier.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="1ad86-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="1ad86-111">Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="1ad86-111">Turn on recommendations</span></span>

<span data-ttu-id="1ad86-112">Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="1ad86-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="1ad86-113">Gehen Sie zu **Retail und Commerce &gt; Produktempfehlungen &gt; Empfehlungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="1ad86-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="1ad86-114">In der Liste der freigegebenen Parameter wählen Sie **Empfehlungs-Listen** aus.</span><span class="sxs-lookup"><span data-stu-id="1ad86-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="1ad86-115">Legen Sie die Option **Empfehlungen aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="1ad86-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Produktempfehlungen aktivieren](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="1ad86-117">Diese Verfahren startet den Vorgang zum Generieren von Produktempfehlungslisten.</span><span class="sxs-lookup"><span data-stu-id="1ad86-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="1ad86-118">Bis zu mehreren Stunden können erforderlich sein, bevor die Listen zur Verfügung stehen und können an der Verkaufsstelle (POS) oder in Dynamics 365 Commerce angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ad86-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="1ad86-119">Konfigurieren Sie Empfehlungslistenparameter</span><span class="sxs-lookup"><span data-stu-id="1ad86-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="1ad86-120">Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte.</span><span class="sxs-lookup"><span data-stu-id="1ad86-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="1ad86-121">Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1ad86-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="1ad86-122">Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1ad86-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="1ad86-123">Empfehlungen für POS-Geräte anzeigen</span><span class="sxs-lookup"><span data-stu-id="1ad86-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="1ad86-124">Nachdem Empfehlungen im Commerce-Back-Office aktiviert wurden, muss der Empfehlungsbereich zum Bildschirm der POS-Steuerung über das Layouttool hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1ad86-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="1ad86-125">Informationen zu diesem Vorgang finden Sie unter [Hinzufügen eines Empfehlungssteuerelements zum Transaktionsbildschirm auf POS-Geräten](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="1ad86-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="1ad86-126">Personalisierte Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="1ad86-126">Enable personalized recommendations</span></span>

<span data-ttu-id="1ad86-127">Weitere Informationen zum Empfangen personalisierter Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1ad86-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ad86-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1ad86-128">Additional resources</span></span>

[<span data-ttu-id="1ad86-129">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="1ad86-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1ad86-130">ADLS in einer Dynamics 365 Commerce-Umgebung aktivieren</span><span class="sxs-lookup"><span data-stu-id="1ad86-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1ad86-131">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="1ad86-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1ad86-132">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="1ad86-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1ad86-133">Empfehlungslisten zu einer E-Commerce-Site hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1ad86-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="1ad86-134">Produktempfehlungen am POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1ad86-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1ad86-135">Empfehlungen zum Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1ad86-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1ad86-136">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="1ad86-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1ad86-137">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="1ad86-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1ad86-138">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="1ad86-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="1ad86-139">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="1ad86-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

