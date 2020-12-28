---
title: Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren
description: In diesem Thema wird beschrieben, wie Sie Produktempfehlungen „Produkte mit ähnlichem Aussehen kaufen“ in Microsoft Dynamics 365 Commerce aktivieren.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412638"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="9003a-103">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="9003a-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9003a-104">In diesem Thema wird beschrieben, wie Sie Produktempfehlungen „Produkte mit ähnlichem Aussehen kaufen“ in Microsoft Dynamics 365 Commerce aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9003a-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9003a-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9003a-105">Overview</span></span>

<span data-ttu-id="9003a-106">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ in Dynamics 365 Commerce nutzt die Kraft der künstlichen Intelligenz und des maschinellen Lernens (AI-ML), um Kunden Empfehlungen für visuell ähnliche Produkte zu geben.</span><span class="sxs-lookup"><span data-stu-id="9003a-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="9003a-107">Durch die Bereitstellung von Empfehlungen für „Produkte mit ähnlichem Aussehen kaufen“ für alle Einzelhandelskanäle in Commerce können Einzelhändler die Kundenzufriedenheit steigern, indem sie Kunden dabei helfen, leicht zu finden, wonach sie suchen.</span><span class="sxs-lookup"><span data-stu-id="9003a-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="9003a-108">Die Funktionalität für Empfehlungen zum „Produkte mit ähnlichem Aussehen kaufen“ verwendet Produktbilder von Startproduktvarianten, um visuell ähnliche Produkte im Produktkatalog eines Einzelhändlers zu finden und zu empfehlen.</span><span class="sxs-lookup"><span data-stu-id="9003a-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="9003a-109">Empfehlungen für „Produkte mit ähnlichem Aussehen kaufen“ sind sowohl in POS‑ als auch in E-Commerce-Bereichen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9003a-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="9003a-110">Beispielszenarien</span><span class="sxs-lookup"><span data-stu-id="9003a-110">Example scenarios</span></span>

- <span data-ttu-id="9003a-111">Ein Kunde sieht sich einen schwarz gestreiften Pullover an und erhält eine Empfehlung für einen ähnlichen Pullover in Rot.</span><span class="sxs-lookup"><span data-stu-id="9003a-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="9003a-112">Der Kunde wählt das empfohlene Produkt anstelle des ursprünglich angezeigten Produkts aus und erhält dann Empfehlungen für ähnliche Produkte in Rot.</span><span class="sxs-lookup"><span data-stu-id="9003a-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="9003a-113">Ein Kunde verwendet Empfehlungen für „Produkte mit ähnlichem Aussehen kaufen“, um passende Ohrringe für einen Ring zu finden, den der Kunde kaufen möchte.</span><span class="sxs-lookup"><span data-stu-id="9003a-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="9003a-114">In der Commerce-Zentrale die Empfehlung „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="9003a-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="9003a-115">Produktempfehlungen werden nur für Commerce-Kunden unterstützt, die ihren Speicher zu Azure Data Lake Gen2 migriert haben.</span><span class="sxs-lookup"><span data-stu-id="9003a-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9003a-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9003a-116">Prerequisites</span></span>

<span data-ttu-id="9003a-117">Bevor Einzelhändler ihren Kunden Empfehlungen für „Produkte mit ähnlichem Aussehen kaufen“ zeigen können, sind zwei Schritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="9003a-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="9003a-118">[Produktempfehlungen aktivieren](enable-product-recommendations.md) in der Commerce-Zentrale.</span><span class="sxs-lookup"><span data-stu-id="9003a-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="9003a-119">Stellen Sie sicher, dass der Medienserver HTTPS-Aufrufe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9003a-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="9003a-120">Damit das Empfehlungsmodul auf die Produktbilder zugreifen kann, müssen Einzelhändler die Produkt-URLs generieren.</span><span class="sxs-lookup"><span data-stu-id="9003a-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="9003a-121">Folgen Sie diesen Schritten, um Produkt-URLs in der Commerce-Zentrale zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9003a-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9003a-122">Wechseln Sie zu **Produktbilder**.</span><span class="sxs-lookup"><span data-stu-id="9003a-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="9003a-123">Wählen Sie im Aktivitätsbereich **Medienvorlage definieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9003a-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="9003a-124">Wählen Sie im Eigenschaftenbereich **Medienvorlage definieren** unter **Medien-URLs** die Option **URLs generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9003a-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="9003a-125">Wenn Sie die Empfehlungsfunktion „Produkte mit ähnlichem Aussehen kaufen“ aktivieren, beginnt der Prozess zum Generieren von Produktempfehlungslisten.</span><span class="sxs-lookup"><span data-stu-id="9003a-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="9003a-126">Es kann bis zu einem Tag dauern, bis diese Listen online und an den POS-Terminals verfügbar und sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="9003a-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="9003a-127">Führen Sie die folgenden Schritte aus, um die Empfehlungsfunktion „Produkte mit ähnlichem Aussehen kaufen“ in der Commerce-Zentrale zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9003a-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9003a-128">Navigieren Sie zu **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="9003a-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="9003a-129">Suchen Sie in der Liste der verfügbaren Funktionen **Produkte mit ähnlichem Aussehen kaufen** und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="9003a-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="9003a-130">Wählen Sie im rechten Bereich aus **Aktivieren** aus, um den Dienst einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="9003a-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="9003a-131">Die folgende Abbildung zeigt die Funktion **Produkte mit ähnlichem Aussehen kaufen** auf der Seite **Funktionsverwaltung** in der Commerce-Zentrale.</span><span class="sxs-lookup"><span data-stu-id="9003a-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Die Funktion „Produkte mit ähnlichem Aussehen kaufen“ auf der Seite Funktionsverwaltung in der Commerce-Zentrale](./media/enableshopsimilarlooks.png)

<span data-ttu-id="9003a-133">Nach Abschluss der vorhergehenden Aufgaben werden POS-Terminals automatisch um kontextabhängigen Bereich **Produkte mit ähnlichem Aussehen kaufen** erweitert.</span><span class="sxs-lookup"><span data-stu-id="9003a-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="9003a-134">Durch die Auswahl **Weitere Details** können Benutzer von POS-Terminals zu einer speziellen Seite „Produkte mit ähnlichem Aussehen kaufen“ weitergeleitet werden, auf der weitere Filter angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9003a-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="9003a-135">Wenn Sie die Empfehlungsfunktion „Produkte mit ähnlichem Aussehen kaufen“ deaktivieren, sind keine anderen Arten von Produktempfehlungen betroffen.</span><span class="sxs-lookup"><span data-stu-id="9003a-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="9003a-136">Weitere Informationen zu Produktempfehlungen finden Sie unter [Überblick über Produktempfehlungen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9003a-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="9003a-137">Mithilfe des Commerce Site Builder eine Schaltfläche mit ähnlichem Aussehen zu den Produktdetailseiten hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9003a-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="9003a-138">Nachdem Sie die Empfehlungsfunktion „Produkte mit ähnlichem Aussehen kaufen“ in der Commerce-Zentrale aktiviert haben, können Einzelhändler mit einer Option im Commerce Site Builder eine Schaltfläche **Produkte mit ähnlichem Aussehen kaufen** auf einer beliebigen Produktdetailseite (PDP) zum Kauffeld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9003a-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="9003a-139">Ein Kunde, der diese Schaltfläche auswählt, wird zu einer speziellen Seite „Produkte mit ähnlichem Aussehen kaufen“ weitergeleitet, auf der visuell ähnliche Produkte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9003a-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="9003a-140">Dort kann der Kunde Auswahlen verwenden, um die Produkte weiter zu filtern.</span><span class="sxs-lookup"><span data-stu-id="9003a-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="9003a-141">Gehen Sie folgendermaßen vor, um eine Schaltfläche **Produkte mit ähnlichem Aussehen kaufen** zu einem PDP mithilfe des Commerce Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9003a-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9003a-142">Öffnen Sie eine vorhandene Site Builder-Seite, die ein Kauffeld enthält.</span><span class="sxs-lookup"><span data-stu-id="9003a-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="9003a-143">Wählen Sie im linken Navigationsbereich das Kauffeld aus.</span><span class="sxs-lookup"><span data-stu-id="9003a-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="9003a-144">Wählen Sie im rechten Navigationsbereich das Kontrollkästchen **Link für „Produkte mit ähnlichem Aussehen kaufen“ aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9003a-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="9003a-145">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="9003a-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="9003a-146">Nach der Veröffentlichung der Seite enthält die PDP eine Schaltfläche **Produkte mit ähnlichem Aussehen kaufen**.</span><span class="sxs-lookup"><span data-stu-id="9003a-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="9003a-147">Die folgende Abbildung zeigt das Kontrollkästchen **Links für „Produkte mit ähnlichem Aussehen kaufen“ aktivieren** und die Schaltfläche **Produkte mit ähnlichem Aussehen kaufen** auf einer Beispiel-PDP im Site Builder.</span><span class="sxs-lookup"><span data-stu-id="9003a-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Das Kontrollkästchen „Link für Produkte mit ähnlichem Aussehen kaufen“ und die Schaltfläche „Ähnliches Aussehen“ kaufen auf einer Beispiel-PDP im Site Builder aktivieren](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="9003a-149">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9003a-149">Additional resources</span></span>

[<span data-ttu-id="9003a-150">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="9003a-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9003a-151">Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung</span><span class="sxs-lookup"><span data-stu-id="9003a-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9003a-152">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9003a-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9003a-153">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="9003a-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9003a-154">Produktempfehlungen am POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9003a-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9003a-155">Empfehlungen zum Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9003a-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9003a-156">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="9003a-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9003a-157">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="9003a-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9003a-158">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="9003a-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9003a-159">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="9003a-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
