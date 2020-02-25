---
title: Personalisierte Produktempfehlungen aktivieren
description: In diesem Thema wird beschrieben, wie Kunden in Microsoft personalisierte Produktempfehlungen zur Verfügung gestellt werden Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b3c6140b8bd3ea15458223c0f61810421d0b2bc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025250"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="fc2a5-103">Personalisierte Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="fc2a5-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc2a5-104">In diesem Thema wird beschrieben, wie Kunden in Microsoft personalisierte Produktempfehlungen zur Verfügung gestellt werden Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fc2a5-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="fc2a5-105">Overview</span></span>

<span data-ttu-id="fc2a5-106">In Dynamics 365 Commerce können Einzelhändler können Produktempfehlungen (auch als Personalisierung bezeichnet) zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="fc2a5-107">Auf diese Weise können personalisierte Empfehlungen online und am Point of Sale (POS) in das Kundenerlebnis einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="fc2a5-108">Wenn die Personalisierungsfunktion aktiviert ist, kann das System die Kauf- und Produktinformationen eines Benutzers verknüpfen, um individuelle Produktempfehlungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="fc2a5-109">Personalisierungsvoraussetzungen</span><span class="sxs-lookup"><span data-stu-id="fc2a5-109">Personalization prerequisites</span></span>

<span data-ttu-id="fc2a5-110">Beachten Sie, dass Produktempfehlungen nur für Commerce-Benutzer unterstützt werden, die ihren Speicher auf Azure Data Lake Store migriert haben, bevor Sie Kunden personalisierte Produktempfehlungen zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="fc2a5-111">Bevor Kunden personalisierte Produktempfehlungen erhalten können, müssen Einzelhändler [Produktempfehlungen einschalten](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fc2a5-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fc2a5-112">Wenn Sie Produktempfehlungen aktivieren, aktivieren Sie auch die Personalisierung.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="fc2a5-113">Wenn Sie jedoch die Personalisierung deaktivieren, werden die anderen Produktempfehlungen nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="fc2a5-114">Weitere Informationen zu Produktempfehlungen finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fc2a5-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="fc2a5-115">Personalisierungen einschalten</span><span class="sxs-lookup"><span data-stu-id="fc2a5-115">Turn on personalization</span></span>

<span data-ttu-id="fc2a5-116">Um die Personalisierung einzuschalten, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="fc2a5-117">Gehen Sie zu **Retail und Commerce \> Produktempfehlungen \> Empfehlungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="fc2a5-118">In der Liste mit freigegebenen Einzelhandelsparametern, wählen Sie **Empfehlungs-Listen** aus.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="fc2a5-119">Legen Sie die Option **Personalisierungen aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Personalisierungen aktivieren](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="fc2a5-121">Wenn Sie die Personalisierung aktivieren, wird der Prozess zum Generieren personalisierter Produktempfehlungslisten gestartet.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="fc2a5-122">Es kann bis zu einem Tag dauern, bis diese Listen online und am POS verfügbar und sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="fc2a5-123">Personalisierte Listen</span><span class="sxs-lookup"><span data-stu-id="fc2a5-123">Personalized lists</span></span>

<span data-ttu-id="fc2a5-124">Der Empfehlungsservice ermöglicht nicht nur die Personalisierung vorhandener maschinengenerierter Listen, sondern ermöglicht auch die Personalisierung der Produkterkennungserfahrung sowohl online als auch am POS.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="fc2a5-125">Nach dem Aktivieren der Personalisierung können Einzelhändler Kunden personalisierte Für Sie ausgewählt-Listen online oder Für Kunden empfohlen-Listen auf POS-Terminals anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="fc2a5-126">Darüber hinaus können Einzelhändler vorhandene Produktempfehlungslisten personalisieren und authentifizierten Benutzern die Möglichkeit zum Deaktivieren gemäß der allgemeinen Datenschutzverordnung (DSGVO) bieten.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="fc2a5-127">Wenn Sie die Personalisierung deaktivieren, deaktivieren Sie auch diese Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="fc2a5-128">Online Für Sie Ausgewählt-Listen</span><span class="sxs-lookup"><span data-stu-id="fc2a5-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="fc2a5-129">Eine Für Sie Ausgewählt-Liste ist eine Liste für künstliches Intelligenz-Maschinelles Lernen (KI-ML), die einem authentifizierten Benutzer eine personalisierte Liste vorgeschlagener Produkte anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="fc2a5-130">Diese Liste basiert auf dem Omnikanal-Kaufverlauf des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="fc2a5-131">Personalisierte Empfehlungen werden dynamisch aktualisiert, wenn der Benutzer mehr Einkäufe tätigt.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="fc2a5-132">Dieser Listentyp unterstützt auch die Kategoriefilterung, sodass Einzelhändler Top-Picks basierend auf Navigationshierarchien anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="fc2a5-133">Bevor die Liste Tipps für Sie auf einer E-Commerce-Seite angezeigt werden kann, müssen die folgenden Benutzeranforderungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="fc2a5-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="fc2a5-134">Benutzer müssen angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-134">Users must be signed in.</span></span> <span data-ttu-id="fc2a5-135">Anonyme Benutzer sehen keine personalisierten Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="fc2a5-136">Benutzer müssen mindestens einen Kauf auf ihrem Konto haben.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="fc2a5-137">Benutzer müssen sich anmelden, um personalisierte Empfehlungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="fc2a5-138">Die folgende Abbildung zeigt ein Beispiel für eine Liste Tipps für Sie auf einer Online-Shop-Seite.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Online Tipps für Sie Liste](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="fc2a5-140">Empfohlen für Kunden-Listen am POS</span><span class="sxs-lookup"><span data-stu-id="fc2a5-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="fc2a5-141">Um das Kundenerlebnis zu verbessern, können Einzelhändler vorhandene Kundendetailseiten durch Hinzufügen einer kontextbezogenen Liste Empfohlen für Kunden personalisieren.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="fc2a5-142">Die folgende Abbildung zeigt ein Beispiel für eine Liste Tipps für Sie auf einem POS-Terminal.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Empfohlen für Kunden-Liste am POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="fc2a5-144">Übernehmen Sie die Personalisierung für vorhandene Empfehlungslisten</span><span class="sxs-lookup"><span data-stu-id="fc2a5-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="fc2a5-145">Einzelhändler können vorhandene Empfehlungslisten wie Neu, Trend, Bestseller, Leute mögen auch und Häufig zusammen gekauft personalisieren.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="fc2a5-146">Wenn die Personalisierung auf vorhandene Listen angewendet wird, werden Elemente, die ein angemeldeter Benutzer zuvor gekauft hat, aus diesen Listen entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="fc2a5-147">Sowohl für anonyme Benutzer als auch für Benutzer, die keine personalisierten Empfehlungen erhalten haben, werden Standardversionen der vorhandenen Listen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="fc2a5-148">Daher müssen Einzelhändler separate Seitenerfahrungen nicht manuell verwalten.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="fc2a5-149">Ein angemeldeter Benutzer hat beispielsweise bereits die schwarze Uhr und die braunen Arbeitsstiefel gekauft, die in der Liste Trend – Standard in der folgenden Abbildung aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="fc2a5-150">Daher werden dem Benutzer anstelle dieser Produkte neue Produkte angezeigt, wie in der Liste Trend – personalisiert gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Personalisierung anwenden](./media/applypersonalization.png)

<span data-ttu-id="fc2a5-152">Gehen Sie folgendermaßen vor, um eine vorhandene Empfehlungsliste in dem Commerce-Site-Generator zu personalisieren.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fc2a5-153">Öffnen Sie eine vorhandene Site Builder-Seite, die ein Produktsammlungsmodul enthält.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="fc2a5-154">Wählen Sie im linken Navigationsbereich Produktsammlungsmodul aus.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="fc2a5-155">Wählen Sie im rechten Navigationsbereich unter **Produkte** die Liste aus.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="fc2a5-156">In dem **Produktlistenkonfiguration auswählen** Dialogfeld unter **Typ** wählen Sie den Listentyp.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="fc2a5-157">Wählen Sie das Kontrollkästchen **Personalisierung anwenden** und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Anwenden der Personalisierung auf eine Trendliste](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="fc2a5-159">Speichern Sie das Seitenfragment, beenden Sie die Bearbeitung und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="fc2a5-160">Nachdem die Seite veröffentlicht wurde, sehen angemeldete Benutzer personalisierte Trendlisten.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc2a5-161">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fc2a5-161">Additional resources</span></span>

[<span data-ttu-id="fc2a5-162">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="fc2a5-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="fc2a5-163">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="fc2a5-163">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="fc2a5-164">DSGVO und Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="fc2a5-164">GDPR and product recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="fc2a5-165">Hinzufügen von Produktempfehlungslisten zu Seiten</span><span class="sxs-lookup"><span data-stu-id="fc2a5-165">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="fc2a5-166">Fügen Sie Empfehlungsbereich für POS-Geräten hinzu</span><span class="sxs-lookup"><span data-stu-id="fc2a5-166">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="fc2a5-167">Übersicht über Produktsammelmodule</span><span class="sxs-lookup"><span data-stu-id="fc2a5-167">Product collection module overview</span></span>](product-collection-module-overview.md)
