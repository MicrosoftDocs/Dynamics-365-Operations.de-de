---
title: Eine Dynamics 365 Commerce-Evaluierungsumgebung konfigurieren
description: In diesem Thema wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Auswertungsumgebung nach ihrer Bereitstellung konfiguriert wird.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e80830a1cb0864c7eef19857b91e36ad27cdef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795858"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="71929-103">Eine Dynamics 365 Commerce-Evaluierungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="71929-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71929-104">In diesem Thema wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Auswertungsumgebung nach ihrer Bereitstellung konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="71929-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="71929-105">Führen Sie die in diesem Thema beschriebenen Prozeduren erst aus, nachdem Ihre Commerce-Auswertungsumgebung bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="71929-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="71929-106">Informationen zum Bereitstellen Ihrer Commerce-Auswertungsumgebung finden Sie unter [Bereitstellen einer Commerce-Auswertungsumgebung](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="71929-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="71929-107">Nachdem Ihre Commerce-Auswertungsumgebung vollständig bereitgestellt wurde, müssen zusätzliche Konfigurationsschritte nach der Bereitstellung ausgeführt werden, bevor Sie mit der Evaluierung der Umgebung beginnen können.</span><span class="sxs-lookup"><span data-stu-id="71929-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="71929-108">Um diese Schritte abzuschließen, müssen Sie Microsoft Dynamics Lifecycle Services (LCS) und Dynamics 365 Commerce verwenden.</span><span class="sxs-lookup"><span data-stu-id="71929-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="71929-109">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="71929-109">Before you start</span></span>

1. <span data-ttu-id="71929-110">Melden Sie sich beim [LCS-Portal](https://lcs.dynamics.com) an.</span><span class="sxs-lookup"><span data-stu-id="71929-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="71929-111">Gehen Sie zu Ihrem Projekt.</span><span class="sxs-lookup"><span data-stu-id="71929-111">Go to your project.</span></span>
1. <span data-ttu-id="71929-112">Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="71929-113">Wählen Sie Ihre Umgebung in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="71929-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="71929-114">Wählen Sie in den Umgebungsinformationen rechts die Option **Bei Umgebung anmelden** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="71929-115">Sie werden zur Zentralverwaltung von Commerce übermittelt.</span><span class="sxs-lookup"><span data-stu-id="71929-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="71929-116">Stellen Sie sicher, dass die juristische Person **USRT** oben rechts ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="71929-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="71929-117">Stellen Sie bei Aktivitäten nach der Bereitstellung in der Commerce-Zentralverwaltung sicher, dass die juristische Person **USRT** immer ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="71929-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="71929-118">Die Verkaufsstelle konfigurieren</span><span class="sxs-lookup"><span data-stu-id="71929-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="71929-119">Mitarbeiter Ihrer Identität zuordnen</span><span class="sxs-lookup"><span data-stu-id="71929-119">Associate a worker with your identity</span></span>

<span data-ttu-id="71929-120">Gehen Sie in der Commerce-Zentralverwaltung folgendermaßen vor, um einen Mitarbeiter Ihrer Identität zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="71929-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="71929-121">Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Einzelhandel und Handel \> Mitarbeiter \> Arbeitskräfte** zu gehen.</span><span class="sxs-lookup"><span data-stu-id="71929-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="71929-122">Suchen Sie in der Liste den folgenden Datensatz, und wählen Sie ihn aus: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="71929-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="71929-123">Wählen Sie im Aktionsbereich **Commerce** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="71929-124">Wählen Sie **Vorhandene Identität zuordnen** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="71929-125">Geben Sie im Feld **E-Mail** rechts neben **Suchen mithilfe von E-Mails** Ihre E-Mail-Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="71929-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="71929-126">Wählen Sie **Suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-126">Select **Search**.</span></span>
1. <span data-ttu-id="71929-127">Wählen Sie den Datensatz mit Ihrem Namen aus.</span><span class="sxs-lookup"><span data-stu-id="71929-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="71929-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71929-128">Select **OK**.</span></span>
1. <span data-ttu-id="71929-129">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="71929-130">Aktivieren von Cloud POS</span><span class="sxs-lookup"><span data-stu-id="71929-130">Activate Cloud POS</span></span>

<span data-ttu-id="71929-131">Führen Sie diese Schritte in LCS aus, um Cloud POS zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="71929-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="71929-132">Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="71929-133">Wählen Sie Ihre Umgebung in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="71929-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="71929-134">Wählen Sie in den Umgebungsinformationen rechts die Option **Bei Cloud-Verkaufsstelle anmelden** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="71929-135">Wählen Sie **Weiter** aus, um das Dialogfeld **Bevor Sie anfangen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="71929-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="71929-136">Lassen Sie das Feld **Server-URL** wie es ist.</span><span class="sxs-lookup"><span data-stu-id="71929-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="71929-137">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="71929-137">Select **Next**.</span></span>
1. <span data-ttu-id="71929-138">Melden Sie sich mit Ihrem Microsoft Azure Active Directory-Konto (Azure AD) an.</span><span class="sxs-lookup"><span data-stu-id="71929-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="71929-139">Unter **Ladenname** wählen Sie **San Francisco** und dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="71929-140">Wählen Sie unter **Register und Gerät** **SANFRAN-1** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="71929-141">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-141">Select **Activate**.</span></span> <span data-ttu-id="71929-142">Sie werden abgemeldet und zur POS-Anmeldeseite weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="71929-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="71929-143">Sie können sich nun bei der Cloud POS-Erfahrung mit der Operator-ID **000713** und dem Kennwort **123** anmelden.</span><span class="sxs-lookup"><span data-stu-id="71929-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="71929-144">Ihre Site in Commerce einrichten</span><span class="sxs-lookup"><span data-stu-id="71929-144">Set up your site in Commerce</span></span>

<span data-ttu-id="71929-145">Gehen Sie folgendermaßen vor, um Ihre Auswertungswebsite in Commerce einzurichten.</span><span class="sxs-lookup"><span data-stu-id="71929-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="71929-146">Melden Sie sich beim Website-Generator mit der URL an, die Sie bei der Initialisierung von E-Commerce während der Bereitstellung notiert haben (siehe [E-Commerce initialisieren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="71929-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="71929-147">Wählen Sie die Site **Fabrikam** aus, um das Einstellungsdialogfeld der Site zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="71929-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="71929-148">Wählen Sie die Domäne aus, die Sie bei der Initialisierung von E-Commerce eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="71929-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="71929-149">Wählen Sie als Standardkanal **Erweiterter Fabrikam Online-Store** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="71929-150">(Stellen Sie sicher, dass Sie **erweiterter** Online-Store auswählen.)</span><span class="sxs-lookup"><span data-stu-id="71929-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="71929-151">Wählen Sie als Standardsprache **de-de** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="71929-152">Lassen Sie das Feld **Pfad** unverändert.</span><span class="sxs-lookup"><span data-stu-id="71929-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="71929-153">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71929-153">Select **OK**.</span></span> <span data-ttu-id="71929-154">Die Liste der Seiten auf der Site wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="71929-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="71929-155">Aufträge aktivieren</span><span class="sxs-lookup"><span data-stu-id="71929-155">Enable jobs</span></span>

<span data-ttu-id="71929-156">Um Jobs in Commerce zu ermöglichen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="71929-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="71929-157">Melden Sie sich bei der Umgebung (HQ) an.</span><span class="sxs-lookup"><span data-stu-id="71929-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="71929-158">Verwenden Sie das Menü auf der linken Seite, um zu **Retail and Commerce \> Anfragen und Berichte \> Batch-Jobs** zu gehen.</span><span class="sxs-lookup"><span data-stu-id="71929-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="71929-159">Die verbleibenden Schritte dieses Verfahrens müssen für jeden der folgenden Jobs ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="71929-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="71929-160">Einzelhandelsauftrag für E-Mail-Benachrichtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="71929-160">Process retail order email notification</span></span>
    * <span data-ttu-id="71929-161">Produktverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="71929-161">Product availability</span></span>
    * <span data-ttu-id="71929-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="71929-162">P-0001</span></span>
    * <span data-ttu-id="71929-163">Einzelvorgang für Aufträge synchronisieren</span><span class="sxs-lookup"><span data-stu-id="71929-163">Synchronize orders job</span></span>

1. <span data-ttu-id="71929-164">Verwenden Sie den Schnellfilter, um nach dem Auftrag anhand seines Namens zu suchen.</span><span class="sxs-lookup"><span data-stu-id="71929-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="71929-165">Wenn der Status des Auftrags **Wird ausgeführt** lautet, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="71929-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="71929-166">Wählen Sie den Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="71929-166">Select the record.</span></span>
    1. <span data-ttu-id="71929-167">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** die Option **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="71929-168">Wählen Sie **Wird abgebrochen** aus, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="71929-169">Optional können Sie auch das Serienintervall für die folgenden Einzelvorgänge auf eine (1) Minute festlegen:</span><span class="sxs-lookup"><span data-stu-id="71929-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="71929-170">E-Mail-Benachrichtigungseinzelvorgang für Einzelhandelsauftrag verarbeiten</span><span class="sxs-lookup"><span data-stu-id="71929-170">Process retail order email notification job</span></span>
* <span data-ttu-id="71929-171">P-0001-Einzelvorgang</span><span class="sxs-lookup"><span data-stu-id="71929-171">P-0001 job</span></span>
* <span data-ttu-id="71929-172">Einzelvorgang für Aufträge synchronisieren</span><span class="sxs-lookup"><span data-stu-id="71929-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="71929-173">Vollständige Datensynchronisation ausführen</span><span class="sxs-lookup"><span data-stu-id="71929-173">Run full data synchronization</span></span>

<span data-ttu-id="71929-174">Um die vollständige Datensynchronisierung in Commerce auszuführen, führen Sie diese Schritte in der Commerce-Zentralverwaltung aus.</span><span class="sxs-lookup"><span data-stu-id="71929-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="71929-175">Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Kanaldatenbank** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="71929-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="71929-176">Wählen Sie den Kanal mit der Bezeichnung **scXXXXXXXXX** aus.</span><span class="sxs-lookup"><span data-stu-id="71929-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="71929-177">Wählen Sie **Vollständige Datensynchronisierung** im Aktionsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="71929-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="71929-178">Geben Sie **9999** als Vertriebsplan ein.</span><span class="sxs-lookup"><span data-stu-id="71929-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="71929-179">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71929-179">Select **OK**.</span></span>
1. <span data-ttu-id="71929-180">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71929-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="71929-181">Testen der Kreditkartendaten, um Testkäufe durchzuführen</span><span class="sxs-lookup"><span data-stu-id="71929-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="71929-182">Um Testtransaktionen auf der Site durchzuführen, können Sie diese Testkreditkartendaten verwenden:</span><span class="sxs-lookup"><span data-stu-id="71929-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="71929-183">**Kartennummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="71929-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="71929-184">**Ablaufdatum:** 10/20</span><span class="sxs-lookup"><span data-stu-id="71929-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="71929-185">**Kartenprüfwert-Code (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="71929-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71929-186">Sie sollten unter keinen Umständen versuchen, die tatsächlichen Kreditkarteninformationen auf der Testseite zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="71929-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="71929-187">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="71929-187">Next steps</span></span>

<span data-ttu-id="71929-188">Nachdem die Bereitstellungs- und Konfigurationsschritte abgeschlossen sind, können Sie mit der Verwendung Ihrer Auswertungsumgebung beginnen.</span><span class="sxs-lookup"><span data-stu-id="71929-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="71929-189">Verwenden Sie die URL des Commerce-Website-Generators, um zur Erstellungsumgebung zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="71929-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="71929-190">Verwenden Sie die URL der Commerce-Website, um zur Umgebung der Einzelhandelskundenwebsite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="71929-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="71929-191">Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Auswertungsumgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Auswertungsumgebung konfigurieren](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="71929-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71929-192">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="71929-192">Additional resources</span></span>

[<span data-ttu-id="71929-193">Dynamics 365 Commerce-Auswertungsumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="71929-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="71929-194">Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="71929-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="71929-195">Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="71929-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="71929-196">BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="71929-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="71929-197">Dynamics 365 Commerce-Auswertungsumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="71929-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="71929-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="71929-198">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="71929-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="71929-199">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="71929-200">Microsoft Azure-Portal</span><span class="sxs-lookup"><span data-stu-id="71929-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="71929-201">Dynamics 365 Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="71929-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
