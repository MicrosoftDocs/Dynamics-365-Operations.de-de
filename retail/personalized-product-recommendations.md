---
title: "Personalisierte Produktempfehlungsübersicht"
description: "In Dynamics 365 for Retail können Produktempfehlungen auf dem POS-Gerät angezeigt werden. Empfehlungen sind Artikel, die Ihre Kunden möglicherweise interessieren und zwar auf Basis der ihrer Einkaufshistorie, Artikel auf einem Wunschzettel und Artikel, die andere Kunden online und in der physische Filiale gekauft haben. Für Einzelhändler mit großen Katalogen, helfen Empfehlungen den Kunden bei der Produkterfassung. Indem Produkte zur Schau gestellt werden, die sich an den Interessen und Kaufgewohnheiten eines Kunden orientieren, erhalten Einzelhändler Upsell-Möglichkeiten und die Kundenbindung wird gestärkt. In Dynamics 365 for Retail werden Produktempfehlungen von kognitiven Diensten und Microsoft Azure Machine Learning unterstützt."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: a3a3b5e87a797c29c13b180c248d1782805c4c31
ms.contentlocale: de-de
ms.lasthandoff: 06/29/2017


---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="54a3b-107">Personalisierte Produktempfehlungsübersicht</span><span class="sxs-lookup"><span data-stu-id="54a3b-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="54a3b-108">In Dynamics 365 for Retail können Produktempfehlungen auf dem POS-Gerät angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="54a3b-108">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="54a3b-109">Empfehlungen sind Artikel, die Ihre Kunden möglicherweise interessieren und zwar auf Basis der ihrer Einkaufshistorie, Artikel auf einem Wunschzettel und Artikel, die andere Kunden online und in der physische Filiale gekauft haben.</span><span class="sxs-lookup"><span data-stu-id="54a3b-109">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="54a3b-110">Für Einzelhändler mit großen Katalogen, helfen Empfehlungen den Kunden bei der Produkterfassung.</span><span class="sxs-lookup"><span data-stu-id="54a3b-110">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="54a3b-111">Indem Produkte zur Schau gestellt werden, die sich an den Interessen und Kaufgewohnheiten eines Kunden orientieren, erhalten Einzelhändler Upsell-Möglichkeiten und die Kundenbindung wird gestärkt.</span><span class="sxs-lookup"><span data-stu-id="54a3b-111">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="54a3b-112">In Dynamics 365 for Retail werden Produktempfehlungen von kognitiven Diensten und Microsoft Azure Machine Learning unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54a3b-112">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>

<a name="scenarios"></a><span data-ttu-id="54a3b-113">Szenarien</span><span class="sxs-lookup"><span data-stu-id="54a3b-113">Scenarios</span></span>
---------

<span data-ttu-id="54a3b-114">Produktempfehlungen werden für die folgenden POS-Szenarien aktiviert.</span><span class="sxs-lookup"><span data-stu-id="54a3b-114">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="54a3b-115">Sie sind in Cloud POS oder Modern POS (MPOS) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="54a3b-115">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="54a3b-116">Auf der **Produktdetails** Seite:</span><span class="sxs-lookup"><span data-stu-id="54a3b-116">On the **Product details** page:</span></span>

-   <span data-ttu-id="54a3b-117">Wenn ein Shopmitarbeiter eine **Produktdetails** Seite besucht, wenn er auf die vorherigen Buchungen über verschiedene Kanälen schaut, schlägt das Empfehlungsmodul zusätzliche Artikel vor, die wahrscheinlich zusammen eingekauft werden.</span><span class="sxs-lookup"><span data-stu-id="54a3b-117">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="54a3b-118">Falls der Shopmitarbeiter einen Kunden der Buchung hinzufügt und dann eine **Produktdetails** Seite besucht, stellt das Empfehlungsmodul personalisierte Empfehlungen mithilfe der Buchungshistorie des Kunden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="54a3b-118">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="54a3b-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="54a3b-119">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="54a3b-120">Auf der **Transaktionen** Seite:</span><span class="sxs-lookup"><span data-stu-id="54a3b-120">On the **Transaction** page:</span></span>

-   <span data-ttu-id="54a3b-121">Das Empfehlungsmodul schlägt Artikel auf Basis der gesamten Liste von Artikeln im Warenkorb vor.</span><span class="sxs-lookup"><span data-stu-id="54a3b-121">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="54a3b-122">Falls der Shopmitarbeiter einen Kunden der Buchung hinzufügt stellt das Empfehlungsmodul personalisierte Empfehlungen mithilfe der Buchungshistorie des Kunden und des Warenkorbs zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="54a3b-122">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

<span data-ttu-id="54a3b-123">**Hinweis** Zum Anzeigen von Empfehlungen auf der Seite **Buchung** muss der Einzelhändler das Bildschirmlayout in Dynamics 365 for Retail aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="54a3b-123">**Note**  To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="54a3b-124">Das Steuerelement **Empfehlungen** muss auf der Seite **Buchung** abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="54a3b-124">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="54a3b-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="54a3b-125">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="54a3b-126">Auf der **Kundendetails** Seite:</span><span class="sxs-lookup"><span data-stu-id="54a3b-126">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="54a3b-127">Das Empfehlungsmodul schlägt Artikel auf Basis der Benutzerkennung und von Artikeln in der Wunschliste vor.</span><span class="sxs-lookup"><span data-stu-id="54a3b-127">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="54a3b-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="54a3b-128">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="54a3b-129">Konfigurieren von Dynamics 365 for Retail zum Aktivieren von POS-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="54a3b-129">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="54a3b-130">Um Produktempfehlungen einzurichten, muss Folgendes eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="54a3b-130">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="54a3b-131">Überprüfen Sie, ob Sie die richtige **Juristische Person** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="54a3b-131">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="54a3b-132">Navigieren Sie zu **Entitätsspeicher**, wählen Sie **Einzelhandelsverkauf** aus, und klicken Sie dann **Aktualisierung**. Diese Angaben werden verwendet die Demodaten (oder Ihre Daten) aus der betrieblichen Datenbank werden und es auf Entitätsspeicher.</span><span class="sxs-lookup"><span data-stu-id="54a3b-132">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.** **This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="54a3b-133">Optional: Um Empfehlungen zum Buchungsbildschirm anzuzeigen, navigieren Sie zu **Bildschirmlayout**, wählen das Bildschirmlayout, starten den **Bildschirmlayoutdesigner** und dann legen das **Empfehlungssteuerelement** ab.</span><span class="sxs-lookup"><span data-stu-id="54a3b-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout, **choose your screen layout, launch the **Screen layout designer**,** **and then drop the **recommendations control **where needed.</span></span>
4.  <span data-ttu-id="54a3b-134">Wechseln Sie **Einzelhandelsparameter**, wählen Sie **Machine-learning** aus, wählen Sie die Option **Ja** unter **POS-Empfehlungen aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="54a3b-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes **under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="54a3b-135">Weitere Empfehlungen zu POS erhalten Sie mit dem Konfigurationseinzelvorgang **1110**.</span><span class="sxs-lookup"><span data-stu-id="54a3b-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="54a3b-136">Um Änderungen widerzuspiegeln der im POS-Designer durchgeführt wurden, aktivieren Sie Kanalkonfigurationseinzelvorgang **1070**.</span><span class="sxs-lookup"><span data-stu-id="54a3b-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="54a3b-137">[]()Wie funktioniert das?</span><span class="sxs-lookup"><span data-stu-id="54a3b-137">[]()How does it work?</span></span>
<span data-ttu-id="54a3b-138">Wenn Sie die **Entitätsspeicher** Entität aktualisieren, finden folgenden Aktionen statt.</span><span class="sxs-lookup"><span data-stu-id="54a3b-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="54a3b-139">Daten in dem von den kognitiven Diensten erforderlichem Format werden aus der operationalen Datenbank von Dynamics 365 for Retail extrahiert und an den Entitäts-Store gesendet.</span><span class="sxs-lookup"><span data-stu-id="54a3b-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="54a3b-140">Die Daten werden von Azure Data Factory (ADF) verwendet, um die Daten mithilfe der Hive-Skripte als Teil der ADF-Aktivitäten bereinigen.</span><span class="sxs-lookup"><span data-stu-id="54a3b-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="54a3b-141">Bereinigte Daten werden im Blob gespeichert.</span><span class="sxs-lookup"><span data-stu-id="54a3b-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="54a3b-142">Daten vom Blob-Speicher werden von den Cognitive-Services-API verwendet, um ein Empfehlungsmodell zu schulen.</span><span class="sxs-lookup"><span data-stu-id="54a3b-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="54a3b-143">Wenn Sie **Empfehlungen aktivieren** aktivieren und die Konfigurationseinzelvorgänge aktivieren, werden folgenden Aktionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54a3b-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="54a3b-144">Anmeldeinformationen und ID für das Modell werden der API entnommen und in der operationalen Datenbank von Dynamics 365 for Retail, in der web.config für AOS und auch auf dem Retail-Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="54a3b-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="54a3b-145">Model-Anmeldeinformationen und - kennung werden für CRT bereitgestellt, so dass Anforderungen für Produktempfehlungen aus Cloud POS und MPOS im onlinemodus durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="54a3b-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="54a3b-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54a3b-146">See also</span></span>
--------

[<span data-ttu-id="54a3b-147">Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät</span><span class="sxs-lookup"><span data-stu-id="54a3b-147">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




