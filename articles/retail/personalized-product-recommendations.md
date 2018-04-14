---
title: "Personalisierte Produktempfehlungsübersicht"
description: "Dieses Thema enthält Informationen zu Dynamics 365 for Retail-Produktempfehlungen, die im Feld Verkaufsstelle (POS)- Gerät angezeigt werden können."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e6bab3de11dbd2aba8b1330284986514a6ac1dfc
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="db0bd-103">Personalisierte Produktempfehlungsübersicht</span><span class="sxs-lookup"><span data-stu-id="db0bd-103">Personalized product recommendations overview</span></span>

[!INCLUDE [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="db0bd-104">Wir entfernen die aktuelle Version des Produktempfehlungs-Service, da wir für diese Funktion einen besseren Algorithmus und neuere Einzelhandels-ausgerichtete Funktionen neu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="db0bd-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="db0bd-105">Weitere Informationen finden Sie unter [Entfernte oder veraltete Funktionen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features)</span><span class="sxs-lookup"><span data-stu-id="db0bd-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> <span data-ttu-id="db0bd-106">Navigieren Sie zum unteren Bereich der Seite, wenn Sie die vorhandenen Probleme mit bereit aktivierten Produktempfehlungen für Ihre Umgebung gegenüberstellen.</span><span class="sxs-lookup"><span data-stu-id="db0bd-106">Navigate to the bottom of the page if you are facing issues with already-enabled product recommendations for your environment.</span></span> 

<span data-ttu-id="db0bd-107">In Dynamics 365 for Retail können Produktempfehlungen auf dem POS-Gerät angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="db0bd-107">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="db0bd-108">Empfehlungen sind Artikel, die Ihre Kunden möglicherweise interessieren und zwar auf Basis der ihrer Einkaufshistorie, Artikel auf einem Wunschzettel und Artikel, die andere Kunden online und in der physische Filiale gekauft haben.</span><span class="sxs-lookup"><span data-stu-id="db0bd-108">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="db0bd-109">Für Einzelhändler mit großen Katalogen, helfen Empfehlungen den Kunden bei der Produkterfassung.</span><span class="sxs-lookup"><span data-stu-id="db0bd-109">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="db0bd-110">Indem Produkte zur Schau gestellt werden, die sich an den Interessen und Kaufgewohnheiten eines Kunden orientieren, erhalten Einzelhändler Upsell-Möglichkeiten und die Kundenbindung wird gestärkt.</span><span class="sxs-lookup"><span data-stu-id="db0bd-110">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="db0bd-111">In Dynamics 365 for Retail werden Produktempfehlungen von kognitiven Diensten und Microsoft Azure Machine Learning unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db0bd-111">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="db0bd-112">Szenarien</span><span class="sxs-lookup"><span data-stu-id="db0bd-112">Scenarios</span></span>
---------

<span data-ttu-id="db0bd-113">Produktempfehlungen werden für die folgenden POS-Szenarien aktiviert.</span><span class="sxs-lookup"><span data-stu-id="db0bd-113">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="db0bd-114">Sie sind in Cloud POS oder Modern POS (MPOS) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db0bd-114">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="db0bd-115">Auf der **Produktdetails** Seite:</span><span class="sxs-lookup"><span data-stu-id="db0bd-115">On the **Product details** page:</span></span>

-   <span data-ttu-id="db0bd-116">Wenn ein Shopmitarbeiter eine **Produktdetails** Seite besucht, wenn er auf die vorherigen Buchungen über verschiedene Kanälen schaut, schlägt das Empfehlungsmodul zusätzliche Artikel vor, die wahrscheinlich zusammen eingekauft werden.</span><span class="sxs-lookup"><span data-stu-id="db0bd-116">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="db0bd-117">Falls der Shopmitarbeiter einen Kunden der Buchung hinzufügt und dann eine **Produktdetails** Seite besucht, stellt das Empfehlungsmodul personalisierte Empfehlungen mithilfe der Buchungshistorie des Kunden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="db0bd-117">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="db0bd-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="db0bd-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="db0bd-119">Auf der **Transaktionen** Seite:</span><span class="sxs-lookup"><span data-stu-id="db0bd-119">On the **Transaction** page:</span></span>

-   <span data-ttu-id="db0bd-120">Das Empfehlungsmodul schlägt Artikel auf Basis der gesamten Liste von Artikeln im Warenkorb vor.</span><span class="sxs-lookup"><span data-stu-id="db0bd-120">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="db0bd-121">Falls der Shopmitarbeiter einen Kunden der Buchung hinzufügt stellt das Empfehlungsmodul personalisierte Empfehlungen mithilfe der Buchungshistorie des Kunden und des Warenkorbs zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="db0bd-121">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="db0bd-122">Zum Anzeigen von Empfehlungen auf der Seite **Buchung** muss der Einzelhändler das Bildschirmlayout in Dynamics 365 for Retail aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="db0bd-122">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="db0bd-123">Das Steuerelement **Empfehlungen** muss auf der Seite **Buchung** abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db0bd-123">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="db0bd-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="db0bd-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="db0bd-125">Auf der **Kundendetails** Seite:</span><span class="sxs-lookup"><span data-stu-id="db0bd-125">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="db0bd-126">Das Empfehlungsmodul schlägt Artikel auf Basis der Benutzerkennung und von Artikeln in der Wunschliste vor.</span><span class="sxs-lookup"><span data-stu-id="db0bd-126">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="db0bd-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="db0bd-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="db0bd-128">Konfigurieren von Dynamics 365 for Retail zum Aktivieren von POS-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="db0bd-128">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="db0bd-129">Um Produktempfehlungen einzurichten, muss Folgendes eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="db0bd-129">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="db0bd-130">Überprüfen Sie, ob Sie die richtige **Juristische Person** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db0bd-130">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="db0bd-131">Navigieren Sie zu **Entitätsshop** auf **Retail-Verkauf**, und klicken Sie dann **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="db0bd-131">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="db0bd-132">Dies verwendet die Demodaten (oder Ihre Daten) aus der betrieblichen Datenbank und verschieben sie in den Entitätsspeicher.</span><span class="sxs-lookup"><span data-stu-id="db0bd-132">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="db0bd-133">Optional: Um Empfehlungen zum Buchungsbildschirm anzuzeigen, navigieren Sie zu **Bildschirmlayout**, wählen das Bildschirmlayout, starten den **Bildschirmlayoutdesigner** und dann legen das **Empfehlungssteuerelement** ab.</span><span class="sxs-lookup"><span data-stu-id="db0bd-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="db0bd-134">Wechseln Sie **Einzelhandelsparameter**, wählen Sie **Machine-Llearning** aus, wählen Sie die Option **Ja** unter **POS-Empfehlungen aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="db0bd-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="db0bd-135">Weitere Empfehlungen zu POS erhalten Sie mit dem Konfigurationseinzelvorgang **1110**.</span><span class="sxs-lookup"><span data-stu-id="db0bd-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="db0bd-136">Um Änderungen widerzuspiegeln der im POS-Designer durchgeführt wurden, aktivieren Sie Kanalkonfigurationseinzelvorgang **1070**.</span><span class="sxs-lookup"><span data-stu-id="db0bd-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="db0bd-137">[]()Wie funktioniert das?</span><span class="sxs-lookup"><span data-stu-id="db0bd-137">[]()How does it work?</span></span>
<span data-ttu-id="db0bd-138">Wenn Sie die **Entitätsspeicher** Entität aktualisieren, finden folgenden Aktionen statt.</span><span class="sxs-lookup"><span data-stu-id="db0bd-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="db0bd-139">Daten in dem von den kognitiven Diensten erforderlichem Format werden aus der operationalen Datenbank von Dynamics 365 for Retail extrahiert und an den Entitäts-Store gesendet.</span><span class="sxs-lookup"><span data-stu-id="db0bd-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="db0bd-140">Die Daten werden von Azure Data Factory (ADF) verwendet, um die Daten mithilfe der Hive-Skripte als Teil der ADF-Aktivitäten bereinigen.</span><span class="sxs-lookup"><span data-stu-id="db0bd-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="db0bd-141">Bereinigte Daten werden im Blob gespeichert.</span><span class="sxs-lookup"><span data-stu-id="db0bd-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="db0bd-142">Daten vom Blob-Speicher werden von den Cognitive-Services-API verwendet, um ein Empfehlungsmodell zu schulen.</span><span class="sxs-lookup"><span data-stu-id="db0bd-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="db0bd-143">Wenn Sie **Empfehlungen aktivieren** aktivieren und die Konfigurationseinzelvorgänge aktivieren, werden folgenden Aktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db0bd-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="db0bd-144">Anmeldeinformationen und ID für das Modell werden der API entnommen und in der operationalen Datenbank von Dynamics 365 for Retail, in der web.config für AOS und auch auf dem Retail-Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="db0bd-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="db0bd-145">Model-Anmeldeinformationen und - kennung werden für CRT bereitgestellt, so dass Anforderungen für Produktempfehlungen aus Cloud POS und MPOS im onlinemodus durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="db0bd-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="db0bd-146">Beheben Sie Probleme, wo Sie Produktempfehlungen bereits aktiviert haben</span><span class="sxs-lookup"><span data-stu-id="db0bd-146">Troubleshoot issues where you have Product recommendations already enabled</span></span> 
> - <span data-ttu-id="db0bd-147">Navigieren Sie zu **Einzelhandelsparameter** > **Lernfähigkeit einer Maschine** > **Produktempfehlungen sperren** und führen Sie **Globaler Konfigurationsjob aus**.</span><span class="sxs-lookup"><span data-stu-id="db0bd-147">Navigate to **Retail Parameters** > **Machine learning** > **Disable product recommendations** and run **Global configuration job [1110]**.</span></span> <span data-ttu-id="db0bd-148">Wenn Sie nicht in der Lage sind, die Registerkarte **Lernfähigkeit einer Maschine** zu suchen, wenden Sie sich bitte an den Dynamics Support.</span><span class="sxs-lookup"><span data-stu-id="db0bd-148">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span> 
> 
> - <span data-ttu-id="db0bd-149">Wenn Sie die**Empfehlungssteuerung** Ihrem Buchungsbildschirm mithilfe von **Designer für Bildschirmlayout** hinzugefügt haben, entfernen Sie diese auch.</span><span class="sxs-lookup"><span data-stu-id="db0bd-149">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span> 



<a name="see-also"></a><span data-ttu-id="db0bd-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db0bd-150">See also</span></span>
--------

[<span data-ttu-id="db0bd-151">Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät</span><span class="sxs-lookup"><span data-stu-id="db0bd-151">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




