---
title: Konfigurieren einer Commerce-Vorschauumgebung
description: In diesem Thema wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Vorschauumgebung nach ihrer Bereitstellung konfiguriert wird.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906138"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="4dd0d-103">Konfigurieren einer Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="4dd0d-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4dd0d-104">In diesem Thema wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Vorschauumgebung nach ihrer Bereitstellung konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="4dd0d-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4dd0d-105">Overview</span></span>

<span data-ttu-id="4dd0d-106">Führen Sie die in diesem Thema beschriebenen Verfahren erst aus, nachdem Ihre Commerce-Vorschauumgebung bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="4dd0d-107">Informationen zum Bereitstellen Ihrer Commerce-Vorschauumgebung nach deren Bereitstellung finden Sie unter [Stellen Sie eine Commerce-Vorschauumgebung bereit](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="4dd0d-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="4dd0d-108">Nachdem Ihre Commerce-Vorschauumgebung vollständig bereitgestellt wurde, müssen zusätzliche Konfigurationsschritte nach der Bereitstellung ausgeführt werden, bevor Sie mit der Evaluierung der Umgebung beginnen können.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="4dd0d-109">Um diese Schritte auszuführen, müssen Sie Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce und Dynamics 365 Retail verwenden.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="4dd0d-110">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="4dd0d-110">Before you start</span></span>

1. <span data-ttu-id="4dd0d-111">Melden Sie sich beim [LCS-Portal](https://lcs.dynamics.com) an.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="4dd0d-112">Gehen Sie zu Ihrem Projekt.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-112">Go to your project.</span></span>
1. <span data-ttu-id="4dd0d-113">Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="4dd0d-114">Wählen Sie Ihre Umgebung in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="4dd0d-115">Wählen Sie in den Umgebungsinformationen rechts die Option **Vollständige Details** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="4dd0d-116">Wählen Sie **Anmelden** aus, um ein Menü zu öffnen, und dann **An Umgebung anmelden**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="4dd0d-117">Stellen Sie sicher, dass die juristische Person **USRT** oben rechts ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="4dd0d-118">Konfigurieren Sie die Verkaufsstelle in LCS</span><span class="sxs-lookup"><span data-stu-id="4dd0d-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="4dd0d-119">Mitarbeiter Ihrer Identität zuordnen</span><span class="sxs-lookup"><span data-stu-id="4dd0d-119">Associate a worker with your identity</span></span>

<span data-ttu-id="4dd0d-120">Gehen Sie folgendermaßen vor, um einen Mitarbeiter Ihrer Identität in LCS zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="4dd0d-121">Navigieren Sie über das Menü links zu **Module \> Retail \> Mitarbeiter \> Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="4dd0d-122">Suchen Sie in der Liste den folgenden Datensatz, und wählen Sie ihn aus: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="4dd0d-123">Wählen Sie im Aktivitätsbereich **Retail** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="4dd0d-124">Wählen Sie **Vorhandene Identität zuordnen** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="4dd0d-125">Geben Sie im Feld **E-Mail** rechts neben **Suchen mithilfe von E-Mails** Ihre E-Mail-Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="4dd0d-126">Wählen Sie **Suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-126">Select **Search**.</span></span>
1. <span data-ttu-id="4dd0d-127">Wählen Sie den Datensatz mit Ihrem Namen aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="4dd0d-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-128">Select **OK**.</span></span>
1. <span data-ttu-id="4dd0d-129">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="4dd0d-130">Aktivieren von Cloud POS</span><span class="sxs-lookup"><span data-stu-id="4dd0d-130">Activate Cloud POS</span></span>

<span data-ttu-id="4dd0d-131">Führen Sie die folgenden Schritte aus, um Cloud POS in LCS zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="4dd0d-132">Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="4dd0d-133">Wählen Sie Ihre Umgebung in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="4dd0d-134">Wählen Sie in den Umgebungsinformationen rechts die Option **Vollständige Details** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="4dd0d-135">Wählen Sie **Anmelden** aus, um ein Menü zu öffnen, und dann **Bei Cloud Point of Sale anmelden**, um die Verkaufsstelle (POS) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="4dd0d-136">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-136">Select **Next**.</span></span>
1. <span data-ttu-id="4dd0d-137">Melden Sie sich mit Ihrem Microsoft Azure Active Directory-Konto (Azure AD) an.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="4dd0d-138">Wählen Sie unter **Shopname** **San Francisco** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="4dd0d-139">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-139">Select **Next**.</span></span>
1. <span data-ttu-id="4dd0d-140">Wählen Sie unter **Register und Gerät** **SANFRAN-1** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="4dd0d-141">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-141">Select **Activate**.</span></span> <span data-ttu-id="4dd0d-142">Sie werden abgemeldet und zur POS-Anmeldeseite weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="4dd0d-143">Sie können sich nun bei der Cloud POS-Erfahrung mit der Operator-ID **000713** und dem Kennwort **123** anmelden.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="4dd0d-144">Ihre Site in Commerce einrichten</span><span class="sxs-lookup"><span data-stu-id="4dd0d-144">Set up your site in Commerce</span></span>

<span data-ttu-id="4dd0d-145">Gehen Sie folgendermaßen vor, um Ihre Vorschau-Site in Commerce einzurichten.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4dd0d-146">Melden Sie sich beim Commerce-Site-Management-Tool mit der URL an, die Sie bei der Initialisierung von E-Commerce während der Bereitstellung notiert haben (siehe [E-Commerce initialisieren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="4dd0d-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="4dd0d-147">Wählen Sie die Site **Fabrikam** aus, um das Einstellungsdialogfeld der Site zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="4dd0d-148">Wählen Sie die Domäne aus, die Sie bei der Initialisierung von E-Commerce eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="4dd0d-149">Wählen Sie als Standardkanal **Erweiterter Fabrikam Online-Store** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="4dd0d-150">(Stellen Sie sicher, dass Sie **erweiterter** Online-Store auswählen.)</span><span class="sxs-lookup"><span data-stu-id="4dd0d-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="4dd0d-151">Wählen Sie als Standardsprache **de-de** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="4dd0d-152">Lassen Sie das Feld **Pfad** unverändert.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="4dd0d-153">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-153">Select **OK**.</span></span> <span data-ttu-id="4dd0d-154">Die Liste der Seiten auf der Site wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="4dd0d-155">Jobs in Retail aktivieren</span><span class="sxs-lookup"><span data-stu-id="4dd0d-155">Enable jobs in Retail</span></span>

<span data-ttu-id="4dd0d-156">Um Jobs in Retail zu aktivieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="4dd0d-157">Melden Sie sich bei der Umgebung (HQ) an.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="4dd0d-158">Navigieren Sie über das Menü links zu **Retail \> Abfragen und Berichte \> Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="4dd0d-159">Die verbleibenden Schritte dieses Verfahrens müssen für jeden der folgenden Jobs ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="4dd0d-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="4dd0d-160">Einzelhandelsauftrag für E-Mail-Benachrichtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="4dd0d-160">Process retail order email notification</span></span>
    * <span data-ttu-id="4dd0d-161">Produktverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="4dd0d-161">Product availability</span></span>
    * <span data-ttu-id="4dd0d-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="4dd0d-162">P-0001</span></span>
    * <span data-ttu-id="4dd0d-163">Einzelvorgang für Aufträge synchronisieren</span><span class="sxs-lookup"><span data-stu-id="4dd0d-163">Synchronize orders job</span></span>

1. <span data-ttu-id="4dd0d-164">Verwenden Sie den Schnellfilter, um nach dem Auftrag anhand seines Namens zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="4dd0d-165">Wenn der Status des Auftrags **Zurückhalten** lautet, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="4dd0d-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="4dd0d-166">Wählen Sie den Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-166">Select the record.</span></span>
    1. <span data-ttu-id="4dd0d-167">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** die Option **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="4dd0d-168">Wählen Sie **Im Wartezustand** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="4dd0d-169">Führen Sie die vollständige Datensynchronisierung im Einzelhandel durch</span><span class="sxs-lookup"><span data-stu-id="4dd0d-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="4dd0d-170">Gehen Sie folgendermaßen vor, um die vollständige Datensynchronisierung in Retail auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="4dd0d-171">Navigieren Sie über das Menü links zu **Module \> Retail \> Zentralverwaltungseinrichtung \> Retail Steuerprogramm \> Kanaldatenbank**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="4dd0d-172">In der Liste links wird der Kanal **Standard** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="4dd0d-173">Wählen Sie den anderen verfügbaren Kanal.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-173">Select the other available channel.</span></span> <span data-ttu-id="4dd0d-174">Dieser Kanal heißt **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="4dd0d-175">Wählen Sie **Vollständige Datensynchronisierung** im Aktionsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="4dd0d-176">Geben Sie **9999** als Vertriebsplan ein.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="4dd0d-177">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-177">Select **OK**.</span></span>
1. <span data-ttu-id="4dd0d-178">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="4dd0d-179">Testen der Kreditkartendaten, um Testkäufe durchzuführen</span><span class="sxs-lookup"><span data-stu-id="4dd0d-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="4dd0d-180">Um Testtransaktionen auf der Site durchzuführen, können Sie diese Testkreditkartendaten verwenden:</span><span class="sxs-lookup"><span data-stu-id="4dd0d-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="4dd0d-181">**Kartennummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="4dd0d-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="4dd0d-182">**Ablaufdatum:** 10/20</span><span class="sxs-lookup"><span data-stu-id="4dd0d-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="4dd0d-183">**Kartenprüfwert-Code (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="4dd0d-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4dd0d-184">Sie sollten unter keinen Umständen versuchen, die tatsächlichen Kreditkarteninformationen auf der Testseite zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4dd0d-185">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="4dd0d-185">Next steps</span></span>

<span data-ttu-id="4dd0d-186">Nachdem die Bereitstellungs- und Konfigurationsschritte abgeschlossen sind, können Sie Ihre Vorschauumgebung bewerten.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="4dd0d-187">Verwenden Sie die URL des Commerce-Site-Management-Tools, um zur Autorenerfahrung zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="4dd0d-188">Verwenden Sie die URL des Commerce-Site-Management-Tools, um zur Retail-Kundensite-Erfahrung zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="4dd0d-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="4dd0d-189">Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Vorschauumgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Vorschauumgebung konfigurieren](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="4dd0d-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4dd0d-190">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4dd0d-190">Additional resources</span></span>

[<span data-ttu-id="4dd0d-191">Commerce-Vorschauumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="4dd0d-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="4dd0d-192">Bereitstellen einer Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="4dd0d-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="4dd0d-193">Konfigurieren optionaler Funktionen für eine Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="4dd0d-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="4dd0d-194">Commerce-Vorschauumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="4dd0d-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="4dd0d-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="4dd0d-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="4dd0d-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="4dd0d-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="4dd0d-197">Microsoft Azure-Portal</span><span class="sxs-lookup"><span data-stu-id="4dd0d-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="4dd0d-198">Dynamics 365 Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="4dd0d-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="4dd0d-199">Hilferessourcen für Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="4dd0d-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)