---
title: Produktempfehlungen im POS hinzufügen
description: In diesem Thema wird die Verwendung der Produktempfehlungen bei einem Verkaufsstelle (POS)-Gerät beschrieben.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 437913343d16490fd49a458b5c7a17132be293c6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230935"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="9034a-103">Produktempfehlungen im POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9034a-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9034a-104">Im Kern handelt es sich bei den Produktempfehlungen um eine transformative Geschäftsanwendung, die sich über alle Handelsbereiche erstreckt, um reichhaltige, ansprechende und maßgeschneiderte Erfahrungen bei der Produktfindung zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="9034a-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="9034a-105">Um diese Funktion in POS zu implementieren, führen Sie die Schritte zu [Empfehlungen Ihren POS-Geräten hinzufügen](add-recommendations-control-pos-screen.md) aus.</span><span class="sxs-lookup"><span data-stu-id="9034a-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="9034a-106">Weitere Informationen zu Produktempfehlungsfunktionen finden Sie im [Produktempfehlungsüberblick](../commerce/product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9034a-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="9034a-107">Szenarien</span><span class="sxs-lookup"><span data-stu-id="9034a-107">Scenarios</span></span>

<span data-ttu-id="9034a-108">Produktempfehlungen werden für die folgenden POS-Szenarien aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9034a-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="9034a-109">Sie sind in Cloud POS oder Modern POS (MPOS) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9034a-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="9034a-110">Auf der **Produktdetails** Seite:</span><span class="sxs-lookup"><span data-stu-id="9034a-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="9034a-111">Wenn ein Filialmitarbeiter eine **Produktdetails** Seite besucht, wenn er frühere Transaktionen über verschiedene Kanäle betrachtet, schlägt der Empfehlungsdienst zusätzliche Artikel vor, die wahrscheinlich zusammen gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="9034a-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="9034a-112">[![Empfehlungen zur Produktdetailseite](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="9034a-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="9034a-113">Auf der **Transaktionen** Seite:</span><span class="sxs-lookup"><span data-stu-id="9034a-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="9034a-114">Die Empfehlungs-Engine schlägt Artikel vor, die auf der gesamten Liste der Artikel im Warenkorb basieren, die häufig zusammen gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="9034a-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9034a-115">Zum Anzeigen von Empfehlungen auf der Seite **Buchung** muss der Einzelhändler das Bildschirmlayout in Dynamics 365 Commerce aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9034a-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="9034a-116">Das Steuerelement **Empfehlungen** muss auf der Seite **Buchung** abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9034a-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="9034a-117">[![Empfehlungen auf de Seite „Transaktion“](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="9034a-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="9034a-118">Konfigurieren Sie Commerce, um POS-Empfehlungen zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="9034a-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="9034a-119">Gehen Sie zum Einrichten von Produktempfehlungen folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="9034a-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="9034a-120">Stellen Sie sicher, dass Ihr Service auf **10.0.6 Build** aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9034a-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="9034a-121">Befolgen Sie die Anweisungen zur Vorgehensweise für das [Aktivieren von Produktempfehlungen](../commerce/enable-product-recommendations.md) für Ihr Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="9034a-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="9034a-122">Optional: Um Empfehlungen zum Buchungsbildschirm anzuzeigen, navigieren Sie zu **Bildschirmlayout**, wählen das Bildschirmlayout, starten den **Bildschirmlayoutdesigner** und dann legen das **Empfehlungssteuerelement** ab.</span><span class="sxs-lookup"><span data-stu-id="9034a-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="9034a-123">Wechseln Sie zu **Einzelhandelsparameter**, wählen Sie **Maschinelles Lernen** aus, wählen Sie die Option **Ja** unter **POS-Empfehlungen aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9034a-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="9034a-124">Weitere Empfehlungen zu POS erhalten Sie mit dem Konfigurationseinzelvorgang **1110**.</span><span class="sxs-lookup"><span data-stu-id="9034a-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="9034a-125">Um Änderungen widerzuspiegeln der im POS-Designer durchgeführt wurden, aktivieren Sie Kanalkonfigurationseinzelvorgang **1070**.</span><span class="sxs-lookup"><span data-stu-id="9034a-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="9034a-126">Beheben Sie Probleme, wo Sie Produktempfehlungen bereits aktiviert haben</span><span class="sxs-lookup"><span data-stu-id="9034a-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="9034a-127">Navigieren Sie zu **Commerce Parameter** \> **Empfehlungslisten** \> **Produktempfehlungen deaktivieren** und **globalen Konfigurationsauftrag \[9999\]** ausführen.</span><span class="sxs-lookup"><span data-stu-id="9034a-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="9034a-128">Wenn Sie die **Empfehlungssteuerung** Ihrem Buchungsbildschirm mithilfe von **Designer für Bildschirmlayout** hinzugefügt haben, entfernen Sie diese auch.</span><span class="sxs-lookup"><span data-stu-id="9034a-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="9034a-129">Wenn Sie weitere Fragen haben, lesen Sie die [Produktempfehlungen FAQ](../commerce/faq-recommendations.md) für weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="9034a-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9034a-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9034a-130">Additional resources</span></span>

[<span data-ttu-id="9034a-131">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="9034a-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9034a-132">Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung</span><span class="sxs-lookup"><span data-stu-id="9034a-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9034a-133">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9034a-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9034a-134">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9034a-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="9034a-135">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="9034a-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9034a-136">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="9034a-136">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9034a-137">Empfehlungen dem Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9034a-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9034a-138">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="9034a-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9034a-139">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="9034a-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9034a-140">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="9034a-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9034a-141">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="9034a-141">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]