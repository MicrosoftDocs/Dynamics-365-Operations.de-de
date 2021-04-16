---
title: Personalisierte Produktempfehlungen aktivieren
description: In diesem Thema wird beschrieben, wie Kunden in Microsoft Dynamics 365 Commerce personalisierte Produktempfehlungen zur Verfügung gestellt werden.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dc0fbff437bfa948d70a03479561542106805bdb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804428"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="1c52a-103">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="1c52a-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c52a-104">In diesem Thema wird beschrieben, wie Kunden in Microsoft Dynamics 365 Commerce personalisierte Produktempfehlungen zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1c52a-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1c52a-105">In Dynamics 365 Commerce können Einzelhändler können Produktempfehlungen (auch als Personalisierung bezeichnet) zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="1c52a-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="1c52a-106">Auf diese Weise können personalisierte Empfehlungen online und am Point of Sale (POS) in das Kundenerlebnis einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="1c52a-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="1c52a-107">Wenn die Personalisierungsfunktion aktiviert ist, kann das System die Kauf- und Produktinformationen eines Benutzers verknüpfen, um individuelle Produktempfehlungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1c52a-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="1c52a-108">Personalisierungsvoraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1c52a-108">Personalization prerequisites</span></span>

<span data-ttu-id="1c52a-109">Beachten Sie, dass Produktempfehlungen nur für Commerce-Benutzer unterstützt werden, die ihren Speicher auf Azure Data Lake Store migriert haben, bevor Sie Kunden personalisierte Produktempfehlungen zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="1c52a-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="1c52a-110">Bevor Kunden personalisierte Produktempfehlungen erhalten können, müssen Einzelhändler [Produktempfehlungen einschalten](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1c52a-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1c52a-111">Wenn Sie Produktempfehlungen aktivieren, aktivieren Sie auch die Personalisierung.</span><span class="sxs-lookup"><span data-stu-id="1c52a-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="1c52a-112">Wenn Sie jedoch die Personalisierung deaktivieren, werden die anderen Produktempfehlungen nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1c52a-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="1c52a-113">Weitere Informationen zu Produktempfehlungen finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1c52a-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="1c52a-114">Personalisierungen einschalten</span><span class="sxs-lookup"><span data-stu-id="1c52a-114">Turn on personalization</span></span>

<span data-ttu-id="1c52a-115">Um die Personalisierung einzuschalten, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="1c52a-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="1c52a-116">In der Commerce-Zentrale suchen Sie nach **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="1c52a-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="1c52a-117">Wählen Sie **Alles** aus, um eine Liste der verfügbaren Funktionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1c52a-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="1c52a-118">Geben Sie im Suchfeld **Empfehlungen** ein.</span><span class="sxs-lookup"><span data-stu-id="1c52a-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="1c52a-119">Wählen Sie die Funktion **Personalisierte Produktempfehlungen** aus.</span><span class="sxs-lookup"><span data-stu-id="1c52a-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="1c52a-120">Wählen sie im Eigenschaftsbereich **Personalisierte Produktempfehlungen** die Option **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1c52a-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Personalisierungen aktivieren](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="1c52a-122">Wenn Sie die Personalisierung aktivieren, wird der Prozess zum Generieren personalisierter Produktempfehlungslisten gestartet.</span><span class="sxs-lookup"><span data-stu-id="1c52a-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="1c52a-123">Es kann bis zu einem Tag dauern, bis diese Listen online und am POS verfügbar und sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="1c52a-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="1c52a-124">Personalisierte Listen</span><span class="sxs-lookup"><span data-stu-id="1c52a-124">Personalized lists</span></span>

<span data-ttu-id="1c52a-125">Der Empfehlungsservice ermöglicht nicht nur die Personalisierung vorhandener maschinengenerierter Listen, sondern ermöglicht auch die Personalisierung der Produkterkennungserfahrung sowohl online als auch am POS.</span><span class="sxs-lookup"><span data-stu-id="1c52a-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="1c52a-126">Nach dem Aktivieren der Personalisierung können Einzelhändler Kunden personalisierte Für Sie ausgewählt-Listen online oder Für Kunden empfohlen-Listen auf POS-Terminals anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1c52a-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="1c52a-127">Darüber hinaus können Einzelhändler vorhandene Produktempfehlungslisten personalisieren und authentifizierten Benutzern die Möglichkeit zum Deaktivieren gemäß der allgemeinen Datenschutzverordnung (DSGVO) bieten.</span><span class="sxs-lookup"><span data-stu-id="1c52a-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="1c52a-128">Wenn Sie die Personalisierung deaktivieren, deaktivieren Sie auch diese Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1c52a-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="1c52a-129">Online Für Sie Ausgewählt-Listen</span><span class="sxs-lookup"><span data-stu-id="1c52a-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="1c52a-130">Eine Für Sie Ausgewählt-Liste ist eine Liste für künstliches Intelligenz-Maschinelles Lernen (KI-ML), die einem authentifizierten Benutzer eine personalisierte Liste vorgeschlagener Produkte anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1c52a-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="1c52a-131">Diese Liste basiert auf dem Omnikanal-Kaufverlauf des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1c52a-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="1c52a-132">Personalisierte Empfehlungen werden dynamisch aktualisiert, wenn der Benutzer mehr Einkäufe tätigt.</span><span class="sxs-lookup"><span data-stu-id="1c52a-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="1c52a-133">Dieser Listentyp unterstützt auch die Kategoriefilterung, sodass Einzelhändler Top-Picks basierend auf Navigationshierarchien anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="1c52a-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="1c52a-134">Bevor die Liste Tipps für Sie auf einer E-Commerce-Seite angezeigt werden kann, müssen die folgenden Benutzeranforderungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="1c52a-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="1c52a-135">Benutzer müssen angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="1c52a-135">Users must be signed in.</span></span> <span data-ttu-id="1c52a-136">Anonyme Benutzer sehen keine personalisierten Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="1c52a-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="1c52a-137">Benutzer müssen mindestens einen Kauf auf ihrem Konto haben.</span><span class="sxs-lookup"><span data-stu-id="1c52a-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="1c52a-138">Benutzer müssen sich anmelden, um personalisierte Empfehlungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1c52a-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="1c52a-139">Die folgende Abbildung zeigt ein Beispiel für eine Liste Tipps für Sie auf einer Online-Shop-Seite.</span><span class="sxs-lookup"><span data-stu-id="1c52a-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Online Tipps für Sie Liste](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="1c52a-141">Empfohlen für Kunden-Listen am POS</span><span class="sxs-lookup"><span data-stu-id="1c52a-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="1c52a-142">Um das Kundenerlebnis zu verbessern, können Einzelhändler vorhandene Kundendetailseiten durch Hinzufügen einer kontextbezogenen Liste Empfohlen für Kunden personalisieren.</span><span class="sxs-lookup"><span data-stu-id="1c52a-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="1c52a-143">Die folgende Abbildung zeigt ein Beispiel für eine Liste Tipps für Sie auf einem POS-Terminal.</span><span class="sxs-lookup"><span data-stu-id="1c52a-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Empfohlen für Kunden-Liste am POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="1c52a-145">Übernehmen Sie die Personalisierung für vorhandene Empfehlungslisten</span><span class="sxs-lookup"><span data-stu-id="1c52a-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="1c52a-146">Einzelhändler können vorhandene Empfehlungslisten wie Neu, Trend, Bestseller, Leute mögen auch und Häufig zusammen gekauft personalisieren.</span><span class="sxs-lookup"><span data-stu-id="1c52a-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="1c52a-147">Wenn die Personalisierung auf vorhandene Listen angewendet wird, werden Elemente, die ein angemeldeter Benutzer zuvor gekauft hat, aus diesen Listen entfernt.</span><span class="sxs-lookup"><span data-stu-id="1c52a-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="1c52a-148">Sowohl für anonyme Benutzer als auch für Benutzer, die keine personalisierten Empfehlungen erhalten haben, werden Standardversionen der vorhandenen Listen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c52a-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="1c52a-149">Daher müssen Einzelhändler separate Seitenerfahrungen nicht manuell verwalten.</span><span class="sxs-lookup"><span data-stu-id="1c52a-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="1c52a-150">Ein angemeldeter Benutzer hat beispielsweise bereits die schwarze Uhr und die braunen Arbeitsstiefel gekauft, die in der Liste Trend – Standard in der folgenden Abbildung aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1c52a-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="1c52a-151">Daher werden dem Benutzer anstelle dieser Produkte neue Produkte angezeigt, wie in der Liste Trend – personalisiert gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c52a-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Personalisierung anwenden](./media/applypersonalization.png)

<span data-ttu-id="1c52a-153">Gehen Sie folgendermaßen vor, um eine vorhandene Empfehlungsliste in dem Commerce-Site-Generator zu personalisieren.</span><span class="sxs-lookup"><span data-stu-id="1c52a-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1c52a-154">Öffnen Sie eine vorhandene Site Builder-Seite, die ein Produktsammlungsmodul enthält.</span><span class="sxs-lookup"><span data-stu-id="1c52a-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="1c52a-155">Wählen Sie im linken Navigationsbereich Produktsammlungsmodul aus.</span><span class="sxs-lookup"><span data-stu-id="1c52a-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="1c52a-156">Wählen Sie im rechten Navigationsbereich unter **Produkte** die Liste aus.</span><span class="sxs-lookup"><span data-stu-id="1c52a-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="1c52a-157">In dem **Produktlistenkonfiguration auswählen** Dialogfeld unter **Typ** wählen Sie den Listentyp.</span><span class="sxs-lookup"><span data-stu-id="1c52a-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="1c52a-158">Wählen Sie das Kontrollkästchen **Personalisierung anwenden** und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1c52a-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Anwenden der Personalisierung auf eine Trendliste](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="1c52a-160">Speichern Sie das Seitenfragment, beenden Sie die Bearbeitung und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="1c52a-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="1c52a-161">Nachdem die Seite veröffentlicht wurde, sehen angemeldete Benutzer personalisierte Trendlisten.</span><span class="sxs-lookup"><span data-stu-id="1c52a-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c52a-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1c52a-162">Additional resources</span></span>

[<span data-ttu-id="1c52a-163">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="1c52a-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1c52a-164">Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung</span><span class="sxs-lookup"><span data-stu-id="1c52a-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1c52a-165">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="1c52a-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="1c52a-166">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="1c52a-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="1c52a-167">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="1c52a-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1c52a-168">Produktempfehlungen am POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1c52a-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1c52a-169">Empfehlungen zum Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1c52a-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1c52a-170">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="1c52a-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1c52a-171">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="1c52a-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1c52a-172">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="1c52a-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="1c52a-173">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="1c52a-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
