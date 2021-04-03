---
title: Synchronisieren von Produktbewertungen in Dynamics 365 Commerce
description: In diesem Thema wird das Synchronisieren von Produktbewertungen in Microsoft Dynamics 365 Commerce beschrieben.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ab6de4bfa619df74bafc5511affddd516bdb34f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260308"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="f858c-103">Synchronisieren von Produktbewertungen in Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f858c-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f858c-104">In diesem Thema wird das Synchronisieren von Produktbewertungen in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f858c-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f858c-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f858c-105">Overview</span></span>

<span data-ttu-id="f858c-106">Um Produktbewertungen in Mehrkanal-Lösungen, z. B. am Point of Sale (POS) und in Callcentern, zu verwenden, müssen die Produktbewertungen aus dem Dienst Bewertungen und Überprüfungen in die Commerce-Kanaldatenbank importiert werden.</span><span class="sxs-lookup"><span data-stu-id="f858c-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="f858c-107">Wenn Produktbewertungen in Mehrkanal-Lösungen zur Verfügung gestellt werden, können sie Kunden indirekt bei ihren Interaktionen mit Vertriebspartnern unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f858c-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="f858c-108">In diesem Thema werden folgende Aufgaben beschrieben:</span><span class="sxs-lookup"><span data-stu-id="f858c-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="f858c-109">Konfigurieren Sie **Produktbewertungsjob synchronisieren** als Batchauftrag zum Synchronisieren von Produktbewertungen aus dem **Bewertungs- und Überprüfungsservice**.</span><span class="sxs-lookup"><span data-stu-id="f858c-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="f858c-110">Sicherstellen, dass der Batchauftrag für die Produktbewertungssynchronisierung erfolgreich war</span><span class="sxs-lookup"><span data-stu-id="f858c-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="f858c-111">Bereitstellen von Produktbewertungen am POS</span><span class="sxs-lookup"><span data-stu-id="f858c-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="f858c-112">Konfigurieren eines Batchauftrags zum Synchronisieren von Produktbewertungen</span><span class="sxs-lookup"><span data-stu-id="f858c-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f858c-113">Vor dem Start sicherstellen, dass Version 10.0.6 oder höher von Dynamics 365 Commerce Retail installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f858c-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="f858c-114">Commerce-Planer initialisieren</span><span class="sxs-lookup"><span data-stu-id="f858c-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="f858c-115">Um den Commerce-Planer zu initialisieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f858c-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="f858c-116">Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Commerce-Planer initialisieren**.</span><span class="sxs-lookup"><span data-stu-id="f858c-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="f858c-117">Suchen Sie alternativ nach „Commerce-Planer initialisieren“.</span><span class="sxs-lookup"><span data-stu-id="f858c-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="f858c-118">Stellen Sie im Dialogfeld **Commerce-Planer initialisieren** sicher, dass die Option **Vorhandene Konfiguration löschen** auf **Nein** gesetzt ist, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f858c-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="f858c-119">Den Unterauftrag RetailProductRating prüfen</span><span class="sxs-lookup"><span data-stu-id="f858c-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="f858c-120">Um sicherzustellen, dass der Unterauftrag **RetailProductRating** vorhanden ist, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="f858c-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="f858c-121">Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Planer-Unteraufträge**.</span><span class="sxs-lookup"><span data-stu-id="f858c-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="f858c-122">Suchen Sie alternativ nach „Steuerprogrammunteraufträge“.</span><span class="sxs-lookup"><span data-stu-id="f858c-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="f858c-123">Finden oder suchen Sie in der Unterauftragsliste den Unterauftrag **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="f858c-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="f858c-124">Die folgende Abbildung zeigt ein Beispiel der Seite Unterauftragsdetails in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f858c-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![Details des Unterauftrags RetailProductRating](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="f858c-126">Wenn Sie den Unterauftrag **RetailProductRating** nicht finden, haben Sie vielleicht den Auftrag **Synchronisieren von Produktbewertungen** und den Auftrag **1040 CDX** ausgeführt, bevor Sie den Commerce-Planer initialisiert haben.</span><span class="sxs-lookup"><span data-stu-id="f858c-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="f858c-127">Befolgen Sie in diesem Fall die Schritte, um den Auftrag **Vollständige Datensynchronisierung** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f858c-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="f858c-128">Gehen Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Kanaldatenbank**.</span><span class="sxs-lookup"><span data-stu-id="f858c-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="f858c-129">Suchen Sie alternativ nach „Kanaldatenbank“.</span><span class="sxs-lookup"><span data-stu-id="f858c-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="f858c-130">Wählen Sie die zu synchronisierende Kanaldatenbank aus.</span><span class="sxs-lookup"><span data-stu-id="f858c-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="f858c-131">Wählen Sie **Vollständige Datensynchronisierung** im Aktivitätsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="f858c-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="f858c-132">Wählen Sie im Dropdown-Dialogfeld **Vertriebsplan auswählen** die Option **1040 - Produkte** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f858c-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="f858c-133">Wiederholen Sie die Schritte der vorherigen Prozedur, um zu prüfen, ob der Unterauftrag **RetailProductRating** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f858c-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="f858c-134">Produktbewertungen importieren</span><span class="sxs-lookup"><span data-stu-id="f858c-134">Import product ratings</span></span>

<span data-ttu-id="f858c-135">Führen Sie die folgenden Schritte aus, um Produktbewertungen aus dem Bewertungs- und Überprüfungsdienst in Commerce zu importieren.</span><span class="sxs-lookup"><span data-stu-id="f858c-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="f858c-136">Navigieren Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Produktbewertungsauftrag synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="f858c-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="f858c-137">Suchen Sie alternativ nach „Produktbewertungsauftrag synchronisieren“.</span><span class="sxs-lookup"><span data-stu-id="f858c-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="f858c-138">Wählen Sie im Dialogfeld **Produktbewertungen** auf dem Inforegister **Im Hintergrund ausführen** die Option **Wiederholung** aus.</span><span class="sxs-lookup"><span data-stu-id="f858c-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="f858c-139">Legen Sie im Dialogfeld **Wiederholung definieren** ein Wiederholungsmuster fest.</span><span class="sxs-lookup"><span data-stu-id="f858c-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="f858c-140">(Der empfohlene Wert beträgt zwei Stunden.) Planen Sie keine Wiederholung, die kürzer als eine Stunde ist.</span><span class="sxs-lookup"><span data-stu-id="f858c-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="f858c-141">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="f858c-141">Select **OK**.</span></span>
1. <span data-ttu-id="f858c-142">Legen Sie die Option **Stapelverarbeitungsvorgang** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="f858c-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="f858c-143">Diese Einstellung stellt sicher, dass Sie die Protokolle überwachen und den Status von Batchaufträgen überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="f858c-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="f858c-144">Wählen Sie **OK** aus, um den Batchauftrag zu planen.</span><span class="sxs-lookup"><span data-stu-id="f858c-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="f858c-145">Die folgende Abbildung zeigt ein Beispiel der Batchauftragskonfiguration in Commerce.</span><span class="sxs-lookup"><span data-stu-id="f858c-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Konfiguration des Batchauftrags zum Synchronisieren von Produktbewertungen](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="f858c-147">Sicherstellen, dass der Batchauftrag für die Produktbewertungssynchronisierung erfolgreich war</span><span class="sxs-lookup"><span data-stu-id="f858c-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="f858c-148">Um sicherzustellen, dass der Batchauftrag **Produktbewertungen synchronisieren** erfolgreich war, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="f858c-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="f858c-149">Navigieren Sie zu **Einzelhandel und Handel \> Systemadministrator \> Abfragen \> Batchaufträge** oder bei Verwendung einer Commerce-Lagermengeneinheit stattdessen zu **Einzelhandel und Handel \> Abfragen und Berichte \> Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="f858c-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="f858c-150">Suchen Sie alternativ nach „Batchaufträge“.</span><span class="sxs-lookup"><span data-stu-id="f858c-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="f858c-151">Um die Details des Batchauftrags in der Batchauftragsliste anzuzeigen, suchen Sie in der Spalte **Auftragsbeschreibung** nach einer Beschreibung mit „Produktbewertungen abrufen“.</span><span class="sxs-lookup"><span data-stu-id="f858c-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="f858c-152">Wählen Sie die Auftrags-ID aus, um die Details des Batchauftrags anzuzeigen, z. B. das geplante Startdatum/die geplante Startzeit und den Wiederholungstext.</span><span class="sxs-lookup"><span data-stu-id="f858c-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="f858c-153">Die folgende Abbildung zeigt ein Beispiel für die Batchauftragsdetails in Commerce, wenn die Ausführung des Batchauftrags in zweistündigen Intervallen geplant ist.</span><span class="sxs-lookup"><span data-stu-id="f858c-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Details des Batchauftrags zum Synchronisieren von Produktbewertungen](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="f858c-155">Bereitstellen von Produktbewertungen am POS</span><span class="sxs-lookup"><span data-stu-id="f858c-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="f858c-156">Die Bewertungs- und Prüfungslösung in Dynamics 365 Commerce ist eine Mehrkanallösung.</span><span class="sxs-lookup"><span data-stu-id="f858c-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="f858c-157">Produktbewertungen werden jedoch standardmäßig nicht am POS angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f858c-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="f858c-158">Damit Kunden in Geschäften Bewertungen und Beurteilungen sehen können, wenn sie von Vertriebspartnern unterstützt werden, müssen Sie die Produktbewertungen am POS aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f858c-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="f858c-159">Gehen Sie folgendermaßen vor, um Produktbewertungen am POS zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f858c-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="f858c-160">Gehen Sie zu **Einzelhandel und Handel \> Commerce-Einrichtung \> Parameter \> Commerce-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="f858c-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="f858c-161">Suchen Sie alternativ nach „Commerce-Parametern“.</span><span class="sxs-lookup"><span data-stu-id="f858c-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="f858c-162">Wählen Sie auf der Registerkarte **Konfigurationsparameter** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f858c-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="f858c-163">Geben Sie einen Namen, wie **RatingsAndReviews.EnableProductRatingsForRetailStores**, ein, und setzen Sie den Wert auf **true**.</span><span class="sxs-lookup"><span data-stu-id="f858c-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="f858c-164">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f858c-164">Select **Save**.</span></span>
1. <span data-ttu-id="f858c-165">Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="f858c-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="f858c-166">Suchen Sie alternativ nach „Vertriebsplan“.</span><span class="sxs-lookup"><span data-stu-id="f858c-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="f858c-167">Wählen Sie in der Auftragsliste **1110** (**globale Konfiguration**) und dann **Jetzt ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="f858c-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="f858c-168">Überprüfen Sie nach erfolgreicher Ausführung des Auftrags, ob die Produktbewertungen jetzt am POS angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f858c-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="f858c-169">Die folgende Abbildung zeigt ein Beispiel für die Konfiguration der Commerce-Parameter zum Aktivieren der Produktbewertungen am POS.</span><span class="sxs-lookup"><span data-stu-id="f858c-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![Konfiguration der Commerce-Parameter für Produktbewertungen am POS](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="f858c-171">Die folgende Abbildung zeigt ein Beispiel für Produktbewertungen am POS.</span><span class="sxs-lookup"><span data-stu-id="f858c-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Produktbewertungen am POS](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="f858c-173">Die folgende Abbildung zeigt ein Beispiel für Produktbewertungen in Callcenter-Kanälen.</span><span class="sxs-lookup"><span data-stu-id="f858c-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Produktbewertungen in einem Callcenterkanal](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="f858c-175">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f858c-175">Additional resources</span></span>

[<span data-ttu-id="f858c-176">Überblick über Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="f858c-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="f858c-177">Abonnieren zum Verwenden von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="f858c-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="f858c-178">Verwalten von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="f858c-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="f858c-179">Konfigurieren von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="f858c-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]