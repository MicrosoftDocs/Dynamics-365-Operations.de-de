---
title: Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung aktivieren
description: In diesem Thema wird das Aktivieren und Testen von Azure Data Lake Storage für eine Dynamics 365 Commerce-Umgebung erläutert. Dies ist eine Grundvoraussetzung für die Aktivierung von Produktempfehlungen.
author: bebeale
ms.date: 04/13/2020
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
ms.openlocfilehash: 61f96dae0643e3383afd91864e4c145f3b5c04c8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792606"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="81cfb-103">Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung aktivieren</span><span class="sxs-lookup"><span data-stu-id="81cfb-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="81cfb-104">In diesem Thema wird das Aktivieren und Testen von Azure Data Lake Storage für eine Dynamics 365 Commerce-Umgebung erläutert. Dies ist eine Grundvoraussetzung für die Aktivierung von Produktempfehlungen.</span><span class="sxs-lookup"><span data-stu-id="81cfb-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="81cfb-105">Bei der Dynamics 365 Commerce-Lösung werden alle Produkt- und Transaktionsinformationen im Entitätsspeicher der Umgebung nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="81cfb-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="81cfb-106">Um diese Daten für andere Dynamics 365-Dienste wie Datenanalyse, Business Intelligence und personalisierte Empfehlungen zugänglich zu machen, muss die Umgebung mit einer kundeneigenen Azure Data Lake Storage Gen 2 Lösung verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="81cfb-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="81cfb-107">Da Azure Data Lake Storage in einer Umgebung konfiguriert ist, werden alle erforderlichen Daten aus dem Entitätsspeicher gespiegelt, während sie weiterhin geschützt sind und vom Kunden gesteuert werden können.</span><span class="sxs-lookup"><span data-stu-id="81cfb-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="81cfb-108">Wenn Produktempfehlungen oder personalisierte Empfehlungen auch in der Umgebung aktiviert sind, erhält der Produktempfehlungsstapel Zugriff auf den dedizierten Ordner in Azure Data Lake Storage, um die Kundendaten abzurufen und Empfehlungen basierend auf diesen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="81cfb-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="81cfb-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="81cfb-109">Prerequisites</span></span>

<span data-ttu-id="81cfb-110">Kunden müssen Azure Data Lake Storage in einem Azure-Abonnement konfiguriert haben, dessen Inhaber sie sind.</span><span class="sxs-lookup"><span data-stu-id="81cfb-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="81cfb-111">Dieses Thema behandelt nicht den Kauf eines Azure-Abonnements oder die Einrichtung eines Azure Data Lake Storage fähigen Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="81cfb-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="81cfb-112">Weitere Informationen zu Azure Data Lake Storage finden Sie in der [offiziellen Gen2 Azure Data Lake Storage](https://azure.microsoft.com/pricing/details/storage/data-lake)-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="81cfb-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="81cfb-113">Konfigurationsschritte</span><span class="sxs-lookup"><span data-stu-id="81cfb-113">Configuration steps</span></span>

<span data-ttu-id="81cfb-114">Dieser Abschnitt behandelt die Konfigurationsschritte, die zum Aktivieren von Azure Data Lake Storage in einer Umgebung erforderlich sind, und bezieht sich auf Produktempfehlungen.</span><span class="sxs-lookup"><span data-stu-id="81cfb-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="81cfb-115">Eine ausführlichere Übersicht über die zum Aktivieren von Azure Data Lake Storage erforderlichen Schritte finden Sie unter [Stellen Sie den Entity Store als Data Lake zur Verfügung](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="81cfb-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="81cfb-116">Aktivieren Sie Azure Data Lake Storage in der Umgebung</span><span class="sxs-lookup"><span data-stu-id="81cfb-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="81cfb-117">Melden Sie sich beim Back-Office-Portal der Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="81cfb-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="81cfb-118">Suchen Sie nach **Systemparameter** und navigieren Sie zur Registerkarte **Datenverbindungen**.</span><span class="sxs-lookup"><span data-stu-id="81cfb-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="81cfb-119">Setzen Sie **Integration von Data Lake aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="81cfb-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="81cfb-120">Setzen Sie **Data Lake schrittweise aktualisieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="81cfb-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="81cfb-121">Geben Sie die folgenden erforderlichen Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="81cfb-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="81cfb-122">**Anwendungs-ID** // **Anwendungsschlüssel** // **DNS-Name** – Erforderlich, um eine Verbindung zu KeyVault herzustellen, in dem der Azure Data Lake Storage Schlüssel gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="81cfb-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="81cfb-123">**Schlüsselname** – Der geheime Schlüssel, der in KeyVault gespeichert und zur Azure Data Lake Storage Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81cfb-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="81cfb-124">Speichern Sie Ihre Änderungen in der oberen linken Ecke der Seite.</span><span class="sxs-lookup"><span data-stu-id="81cfb-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="81cfb-125">Das folgende Bild zeigt ein Beispiel für eine Azure Data Lake Storage Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="81cfb-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Beispiel einer Azure Data Lake Storage Konfiguration](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="81cfb-127">Testen Sie die Azure Data Lake Storage Verbindung</span><span class="sxs-lookup"><span data-stu-id="81cfb-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="81cfb-128">Testen Sie die Verbindung zu KeyVault mit dem Link **Azure Key Vault testen**.</span><span class="sxs-lookup"><span data-stu-id="81cfb-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="81cfb-129">Testen Sie die Verbindung zu Azure Data Lake Storage mit dem Link **Azure Storage testen**.</span><span class="sxs-lookup"><span data-stu-id="81cfb-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="81cfb-130">Wenn die Tests fehlschlagen, überprüfen Sie noch einmal, ob alle oben hinzugefügten KeyVault-Informationen korrekt sind, und versuchen Sie es dann erneut.</span><span class="sxs-lookup"><span data-stu-id="81cfb-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="81cfb-131">Sobald die Verbindungstests erfolgreich sind, müssen Sie die automatische Aktualisierung für den Entitätsspeicher aktivieren.</span><span class="sxs-lookup"><span data-stu-id="81cfb-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="81cfb-132">Gehen Sie folgendermaßen vor, um die automatische Aktualisierung für den Entitätsspeicher zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="81cfb-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="81cfb-133">Suchen Sie nach **Entitätsspeicher**.</span><span class="sxs-lookup"><span data-stu-id="81cfb-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="81cfb-134">Navigieren Sie in der Liste auf der linken Seite zum **RetailSales**-Eintrag, und wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="81cfb-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="81cfb-135">Vergewissern Sie sich, dass **Automatische Aktualisierung aktiviert** auf **Ja** gesetzt ist, und wählen Sie **Aktualisieren** und dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="81cfb-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="81cfb-136">Die folgende Abbildung zeigt ein Beispiel für einen Entitätsspeicher mit aktivierter automatischer Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="81cfb-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Beispiel eines Entitätsspeichers mit aktivierter automatischer Aktualisierung](./media/exampleADLSConfig2.png)

<span data-ttu-id="81cfb-138">Azure Data Lake Storage ist jetzt für die Umgebung konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="81cfb-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="81cfb-139">Ist die Konfiguration noch nicht vollständig, befolgen Sie für die Umgebung die Schritte [Produktempfehlungen und -personalisierung aktivieren](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="81cfb-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81cfb-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="81cfb-140">Additional resources</span></span>

[<span data-ttu-id="81cfb-141">Entitätsspeicher als Data Lake zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="81cfb-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="81cfb-142">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="81cfb-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="81cfb-143">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="81cfb-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="81cfb-144">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="81cfb-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="81cfb-145">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="81cfb-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="81cfb-146">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="81cfb-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="81cfb-147">Produktempfehlungen in POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="81cfb-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="81cfb-148">Empfehlungen dem Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="81cfb-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="81cfb-149">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="81cfb-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="81cfb-150">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="81cfb-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="81cfb-151">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="81cfb-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="81cfb-152">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="81cfb-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
