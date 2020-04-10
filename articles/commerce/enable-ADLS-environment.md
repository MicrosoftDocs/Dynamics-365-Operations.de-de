---
title: ADLS in Dynamics 365 Commerce-Umgebung aktivieren
description: In diesem Thema wird das Aktivieren und Testen von Azure Data Lake Storage (ADLS) für eine Dynamics 365 Commerce-Umgebung erläutert. Dies ist eine Grundvoraussetzung für die Aktivierung von Produktempfehlungen.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: 3c037f5603af5af84917084eefa1edd508891c0d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154435"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="8d3fc-103">ADLS in Dynamics 365 Commerce-Umgebung aktivieren</span><span class="sxs-lookup"><span data-stu-id="8d3fc-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d3fc-104">In diesem Thema wird das Aktivieren und Testen von Azure Data Lake Storage (ADLS) für eine Dynamics 365 Commerce-Umgebung erläutert. Dies ist eine Grundvoraussetzung für die Aktivierung von Produktempfehlungen.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="8d3fc-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8d3fc-105">Overview</span></span>

<span data-ttu-id="8d3fc-106">Bei der Dynamics 365 Commerce-Lösung werden alle Produkt- und Transaktionsinformationen im Entitätsspeicher der Umgebung nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="8d3fc-107">Um diese Daten für andere Dynamics 365-Dienste wie Datenanalyse, Business Intelligence und personalisierte Empfehlungen zugänglich zu machen, muss die Umgebung mit einer kundeneigenen Azure Data Lake Storage Gen 2 (ADLS)-Lösung verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="8d3fc-108">Da ADLS in einer Umgebung konfiguriert ist, werden alle erforderlichen Daten aus dem Entitätsspeicher gespiegelt, während sie weiterhin geschützt sind und vom Kunden gesteuert werden können.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="8d3fc-109">Wenn Produktempfehlungen oder personalisierte Empfehlungen auch in der Umgebung aktiviert sind, erhält der Produktempfehlungsstapel Zugriff auf den dedizierten Ordner in ADLS, um die Kundendaten abzurufen und Empfehlungen basierend auf diesen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d3fc-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-110">Prerequisites</span></span>

<span data-ttu-id="8d3fc-111">Kunden müssen ADLS in einem Azure-Abonnement konfiguriert haben, dessen Inhaber sie sind.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="8d3fc-112">Dieses Thema behandelt nicht den Kauf eines Azure-Abonnements oder die Einrichtung eines ADLS-fähigen Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="8d3fc-113">Weitere Informationen zu ADLS finden Sie in der [offiziellen ADLS-Dokumentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="8d3fc-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="8d3fc-114">Konfigurationsschritte</span><span class="sxs-lookup"><span data-stu-id="8d3fc-114">Configuration steps</span></span>

<span data-ttu-id="8d3fc-115">In diesem Abschnitt werden die Konfigurationsschritte beschrieben, die zum Aktivieren von ADLS in einer Umgebung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="8d3fc-116">Aktivieren Sie ADLS der Umgebung</span><span class="sxs-lookup"><span data-stu-id="8d3fc-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="8d3fc-117">Melden Sie sich beim Back-Office-Portal der Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="8d3fc-118">Suchen Sie nach **Systemparameter** und navigieren Sie zur Registerkarte **Datenverbindungen**.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="8d3fc-119">Setzen Sie **Integration von Data Lake aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="8d3fc-120">Setzen Sie **Data Lake schrittweise aktualisieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="8d3fc-121">Geben Sie die folgenden erforderlichen Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="8d3fc-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="8d3fc-122">**Anwendungs-ID** // **Anwendungsgeheimnis** // **DNS-Name** – Erforderlich, um eine Verbindung zu KeyVault herzustellen, in dem das ADLS-Geheimnis gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="8d3fc-123">**Geheimnisname** – Der Geheimnisname, der in KeyVault gespeichert und zur ADLS-Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="8d3fc-124">Speichern Sie Ihre Änderungen in der oberen linken Ecke der Seite.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="8d3fc-125">Das folgende Bild zeigt ein Beispiel für eine ADLS-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-125">The following image shows an example ADLS configuration.</span></span>

![Beispiel einer ADLS-Konfiguration](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="8d3fc-127">Testen Sie die ADLS-Verbindung</span><span class="sxs-lookup"><span data-stu-id="8d3fc-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="8d3fc-128">Testen Sie die Verbindung zu KeyVault mit dem Link **Azure Key Vault testen**.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="8d3fc-129">Testen Sie die Verbindung zu ADLS mit dem Link **Azure Storage testen**.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="8d3fc-130">Wenn die Tests fehlschlagen, überprüfen Sie noch einmal, ob alle oben hinzugefügten KeyVault-Informationen korrekt sind, und versuchen Sie es dann erneut.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="8d3fc-131">Sobald die Verbindungstests erfolgreich sind, müssen Sie die automatische Aktualisierung für den Entitätsspeicher aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="8d3fc-132">Gehen Sie folgendermaßen vor, um die automatische Aktualisierung für den Entitätsspeicher zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="8d3fc-133">Suchen Sie nach **Entitätsspeicher**.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="8d3fc-134">Navigieren Sie in der Liste auf der linken Seite zum **RetailSales**-Eintrag, und wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="8d3fc-135">Vergewissern Sie sich, dass **Automatische Aktualisierung aktiviert** auf **Ja** gesetzt ist, und wählen Sie **Aktualisieren** und dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="8d3fc-136">Die folgende Abbildung zeigt ein Beispiel für einen Entitätsspeicher mit aktivierter automatischer Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Beispiel eines Entitätsspeichers mit aktivierter automatischer Aktualisierung](./media/exampleADLSConfig2.png)

<span data-ttu-id="8d3fc-138">ADLS ist jetzt für die Umgebung konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="8d3fc-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="8d3fc-139">Ist die Konfiguration noch nicht vollständig, befolgen Sie für die Umgebung die Schritte [Produktempfehlungen und -personalisierung aktivieren](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8d3fc-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d3fc-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-140">Additional resources</span></span>

[<span data-ttu-id="8d3fc-141">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8d3fc-142">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="8d3fc-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8d3fc-143">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="8d3fc-143">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8d3fc-144">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-144">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8d3fc-145">Produktempfehlungen am POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-145">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="8d3fc-146">Empfehlungen zum Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-146">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8d3fc-147">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-147">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8d3fc-148">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-148">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="8d3fc-149">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="8d3fc-149">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8d3fc-150">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="8d3fc-150">Product recommendations FAQ</span></span>](faq-recommendations.md)


