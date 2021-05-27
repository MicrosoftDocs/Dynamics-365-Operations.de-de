---
title: Produktempfehlungen aktivieren
description: Dieses Thema erläutert, wie Produktempfehlungen erstellt werden, die auf dem maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) basieren, welches Microsoft Dynamics 365 Commerce-Kunden zur Verfügung steht.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 873266405638cd277eb748ad7e966ba8a4976b13
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019858"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="20e5b-103">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="20e5b-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="20e5b-104">Dieses Thema erläutert, wie Produktempfehlungen erstellt werden, die auf dem maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) basieren, welches Microsoft Dynamics 365 Commerce-Kunden zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="20e5b-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="20e5b-105">Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="20e5b-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="20e5b-106">Produktempfehlungen Vor-Prüfung</span><span class="sxs-lookup"><span data-stu-id="20e5b-106">Recommendations pre-check</span></span>

<span data-ttu-id="20e5b-107">Vor dem Aktivieren beachten Sie, dass Produktempfehlungen nur für Commerce-Kunden unterstützt werden, die ihren Speicher für die Nutzung von Azure Data Lake Storage migriert haben.</span><span class="sxs-lookup"><span data-stu-id="20e5b-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="20e5b-108">Die folgenden Konfigurationen müssen im Backoffice aktiviert sein, bevor Empfehlungen aktiviert werden können:</span><span class="sxs-lookup"><span data-stu-id="20e5b-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="20e5b-109">Stellen Sie sicher, dass Azure Data Lake Storage in der Umgebung gekauft und erfolgreich überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="20e5b-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="20e5b-110">Weitere Informationen finden Sie unter [Stellen Sie sicher, dass Azure Data Lake Storage in der Umgebung gekauft und erfolgreich überprüft wurde](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="20e5b-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="20e5b-111">Stellen Sie sicher, dass die Aktualisierung des Entitätsspeichers automatisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="20e5b-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="20e5b-112">Weitere Informationen finden Sie unter [Stellen Sie sicher, dass die Aktualisierung des Entitätsspeichers automatisiert wurde](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="20e5b-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="20e5b-113">Bestätigen Sie, das die Azure AD Identitätskonfiguration einen Eintrag für Empfehlungen enthält.</span><span class="sxs-lookup"><span data-stu-id="20e5b-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="20e5b-114">Weitere Informationen zur Durchführung dieser Aktion finden Sie unten.</span><span class="sxs-lookup"><span data-stu-id="20e5b-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="20e5b-115">Außerdem stellen Sie sicher, dass RetailSale-Messungen aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="20e5b-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="20e5b-116">Weitere Informationen zu diesem Einrichtungsprozess finden Sie unter [Mit Maßnahmen arbeiten](/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="20e5b-116">To learn more about this set up process, see [Work with measures](/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="20e5b-117">Azure AD Identitätskonfiguration</span><span class="sxs-lookup"><span data-stu-id="20e5b-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="20e5b-118">Dieser Schritt ist für alle Kunden erforderlich, die eine Infrastruktur als Servicekonfiguration (IaaS) ausführen.</span><span class="sxs-lookup"><span data-stu-id="20e5b-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="20e5b-119">Für Kunden, die mit Service Fabric (SF) arbeiten, sollte dieser Schritt automatisch erfolgen. Wir empfehlen, zu überprüfen, ob die Einstellung wie erwartet konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="20e5b-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="20e5b-120">Einstellung</span><span class="sxs-lookup"><span data-stu-id="20e5b-120">Setup</span></span>

1. <span data-ttu-id="20e5b-121">Suchen Sie im Backoffice nach den Seiten **Azure Active Directory Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="20e5b-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="20e5b-122">Überprüfen Sie, ob ein Eintrag für RecommendationSystemApplication-1 vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="20e5b-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="20e5b-123">Wenn der Eintrag nicht vorhanden ist, fügen Sie einen neuen Eintrag mit den folgenden Informationen hinzu:</span><span class="sxs-lookup"><span data-stu-id="20e5b-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="20e5b-124">**Client-ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="20e5b-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="20e5b-125">**Name** – RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="20e5b-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="20e5b-126">**Benutzeridentifikation** – RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="20e5b-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="20e5b-127">Seite speichern und schließen</span><span class="sxs-lookup"><span data-stu-id="20e5b-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="20e5b-128">Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="20e5b-128">Turn on recommendations</span></span>

<span data-ttu-id="20e5b-129">Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="20e5b-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="20e5b-130">In der Commerce-Zentrale suchen Sie nach **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="20e5b-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="20e5b-131">Wählen Sie **Alles** aus, um eine Liste der verfügbaren Funktionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="20e5b-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="20e5b-132">Geben Sie im Suchfeld **Empfehlungen** ein.</span><span class="sxs-lookup"><span data-stu-id="20e5b-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="20e5b-133">Wählen Sie die Funktion **Produktempfehlungen** aus.</span><span class="sxs-lookup"><span data-stu-id="20e5b-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="20e5b-134">Wählen sie im Eigenschaftsbereich **Produktempfehlungen** die Option **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="20e5b-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Aktivieren von Empfehlungen](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="20e5b-136">Diese Verfahren startet den Vorgang zum Generieren von Produktempfehlungslisten.</span><span class="sxs-lookup"><span data-stu-id="20e5b-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="20e5b-137">Es kann bis zu mehreren Stunden dauern, bis die Listen an der Verkaufsstelle (POS) oder in Dynamics 365 Commerce angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="20e5b-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="20e5b-138">Konfigurieren Sie Empfehlungslistenparameter</span><span class="sxs-lookup"><span data-stu-id="20e5b-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="20e5b-139">Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte.</span><span class="sxs-lookup"><span data-stu-id="20e5b-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="20e5b-140">Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="20e5b-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="20e5b-141">Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="20e5b-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="20e5b-142">Empfehlungen für POS-Geräte anzeigen</span><span class="sxs-lookup"><span data-stu-id="20e5b-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="20e5b-143">Nachdem Empfehlungen im Commerce-Back-Office aktiviert wurden, muss der Empfehlungsbereich zum Bildschirm der POS-Steuerung über das Layouttool hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="20e5b-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="20e5b-144">Informationen zu diesem Vorgang finden Sie unter [Hinzufügen eines Empfehlungssteuerelements zum Transaktionsbildschirm auf POS-Geräten](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="20e5b-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="20e5b-145">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="20e5b-145">Enable personalized recommendations</span></span>

<span data-ttu-id="20e5b-146">In Dynamics 365 Commerce können Einzelhändler können Produktempfehlungen (auch als Personalisierung bezeichnet) zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="20e5b-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="20e5b-147">Auf diese Weise können die personalisierten Empfehlungen online und am Point of Sale (POS) in das Kundenerlebnis einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="20e5b-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="20e5b-148">Wenn die Personalisierungsfunktion aktiviert ist, kann das System die Kauf- und Produktinformationen eines Benutzers verknüpfen, um individuelle Produktempfehlungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="20e5b-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="20e5b-149">Weitere Informationen zum Empfangen von personalisierten Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="20e5b-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20e5b-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="20e5b-150">Additional resources</span></span>

[<span data-ttu-id="20e5b-151">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="20e5b-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="20e5b-152">Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung</span><span class="sxs-lookup"><span data-stu-id="20e5b-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="20e5b-153">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="20e5b-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="20e5b-154">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="20e5b-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="20e5b-155">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="20e5b-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="20e5b-156">Produktempfehlungen am POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="20e5b-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="20e5b-157">Empfehlungen zum Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="20e5b-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="20e5b-158">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="20e5b-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="20e5b-159">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="20e5b-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="20e5b-160">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="20e5b-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="20e5b-161">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="20e5b-161">Product recommendations FAQ</span></span>](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]