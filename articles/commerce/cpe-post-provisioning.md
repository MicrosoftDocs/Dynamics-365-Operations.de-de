---
title: Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung
description: In diesem Thema wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Auswertungsumgebung nach ihrer Bereitstellung konfiguriert wird.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fa92a581a96de6bed26b4a0c6601ebd9d5088347
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993424"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="d1ad9-103">Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="d1ad9-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1ad9-104">In diesem Thema wird erläutert, wie eine Microsoft Dynamics 365 Commerce-Auswertungsumgebung nach ihrer Bereitstellung konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="d1ad9-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d1ad9-105">Overview</span></span>

<span data-ttu-id="d1ad9-106">Führen Sie die in diesem Thema beschriebenen Prozeduren erst aus, nachdem Ihre Commerce-Auswertungsumgebung bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="d1ad9-107">Informationen zum Bereitstellen Ihrer Commerce-Auswertungsumgebung finden Sie unter [Bereitstellen einer Commerce-Auswertungsumgebung](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="d1ad9-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="d1ad9-108">Nachdem Ihre Commerce-Auswertungsumgebung vollständig bereitgestellt wurde, müssen zusätzliche Konfigurationsschritte nach der Bereitstellung ausgeführt werden, bevor Sie mit der Evaluierung der Umgebung beginnen können.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="d1ad9-109">Um diese Schritte abzuschließen, müssen Sie Microsoft Dynamics Lifecycle Services (LCS) und Dynamics 365 Commerce verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="d1ad9-110">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="d1ad9-110">Before you start</span></span>

1. <span data-ttu-id="d1ad9-111">Melden Sie sich beim [LCS-Portal](https://lcs.dynamics.com) an.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="d1ad9-112">Gehen Sie zu Ihrem Projekt.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-112">Go to your project.</span></span>
1. <span data-ttu-id="d1ad9-113">Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d1ad9-114">Wählen Sie Ihre Umgebung in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="d1ad9-115">Wählen Sie in den Umgebungsinformationen rechts die Option **Bei Umgebung anmelden** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="d1ad9-116">Sie werden zur Zentralverwaltung von Commerce übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="d1ad9-117">Stellen Sie sicher, dass die juristische Person **USRT** oben rechts ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="d1ad9-118">Stellen Sie bei Aktivitäten nach der Bereitstellung in der Commerce-Zentralverwaltung sicher, dass die juristische Person **USRT** immer ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="d1ad9-119">Die Verkaufsstelle konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d1ad9-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="d1ad9-120">Mitarbeiter Ihrer Identität zuordnen</span><span class="sxs-lookup"><span data-stu-id="d1ad9-120">Associate a worker with your identity</span></span>

<span data-ttu-id="d1ad9-121">Gehen Sie in der Commerce-Zentralverwaltung folgendermaßen vor, um einen Mitarbeiter Ihrer Identität zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="d1ad9-122">Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Einzelhandel und Handel \> Mitarbeiter \> Arbeitskräfte** zu gehen.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="d1ad9-123">Suchen Sie in der Liste den folgenden Datensatz, und wählen Sie ihn aus: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="d1ad9-124">Wählen Sie im Aktionsbereich **Commerce** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="d1ad9-125">Wählen Sie **Vorhandene Identität zuordnen** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="d1ad9-126">Geben Sie im Feld **E-Mail** rechts neben **Suchen mithilfe von E-Mails** Ihre E-Mail-Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="d1ad9-127">Wählen Sie **Suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-127">Select **Search**.</span></span>
1. <span data-ttu-id="d1ad9-128">Wählen Sie den Datensatz mit Ihrem Namen aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="d1ad9-129">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-129">Select **OK**.</span></span>
1. <span data-ttu-id="d1ad9-130">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="d1ad9-131">Aktivieren von Cloud POS</span><span class="sxs-lookup"><span data-stu-id="d1ad9-131">Activate Cloud POS</span></span>

<span data-ttu-id="d1ad9-132">Führen Sie diese Schritte in LCS aus, um Cloud POS zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="d1ad9-133">Wählen Sie aus dem oberen Menü **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d1ad9-134">Wählen Sie Ihre Umgebung in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="d1ad9-135">Wählen Sie in den Umgebungsinformationen rechts die Option **Bei Cloud-Verkaufsstelle anmelden** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="d1ad9-136">Wählen Sie **Weiter** aus, um das Dialogfeld **Bevor Sie anfangen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="d1ad9-137">Lassen Sie das Feld **Server-URL** wie es ist.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="d1ad9-138">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-138">Select **Next**.</span></span>
1. <span data-ttu-id="d1ad9-139">Melden Sie sich mit Ihrem Microsoft Azure Active Directory-Konto (Azure AD) an.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="d1ad9-140">Unter **Ladenname** wählen Sie **San Francisco** und dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="d1ad9-141">Wählen Sie unter **Register und Gerät** **SANFRAN-1** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="d1ad9-142">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-142">Select **Activate**.</span></span> <span data-ttu-id="d1ad9-143">Sie werden abgemeldet und zur POS-Anmeldeseite weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="d1ad9-144">Sie können sich nun bei der Cloud POS-Erfahrung mit der Operator-ID **000713** und dem Kennwort **123** anmelden.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="d1ad9-145">Ihre Site in Commerce einrichten</span><span class="sxs-lookup"><span data-stu-id="d1ad9-145">Set up your site in Commerce</span></span>

<span data-ttu-id="d1ad9-146">Gehen Sie folgendermaßen vor, um Ihre Auswertungswebsite in Commerce einzurichten.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d1ad9-147">Melden Sie sich beim Website-Generator mit der URL an, die Sie bei der Initialisierung von E-Commerce während der Bereitstellung notiert haben (siehe [E-Commerce initialisieren](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="d1ad9-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="d1ad9-148">Wählen Sie die Site **Fabrikam** aus, um das Einstellungsdialogfeld der Site zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="d1ad9-149">Wählen Sie die Domäne aus, die Sie bei der Initialisierung von E-Commerce eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="d1ad9-150">Wählen Sie als Standardkanal **Erweiterter Fabrikam Online-Store** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="d1ad9-151">(Stellen Sie sicher, dass Sie **erweiterter** Online-Store auswählen.)</span><span class="sxs-lookup"><span data-stu-id="d1ad9-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="d1ad9-152">Wählen Sie als Standardsprache **de-de** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="d1ad9-153">Lassen Sie das Feld **Pfad** unverändert.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="d1ad9-154">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-154">Select **OK**.</span></span> <span data-ttu-id="d1ad9-155">Die Liste der Seiten auf der Site wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="d1ad9-156">Aufträge aktivieren</span><span class="sxs-lookup"><span data-stu-id="d1ad9-156">Enable jobs</span></span>

<span data-ttu-id="d1ad9-157">Um Jobs in Commerce zu ermöglichen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d1ad9-158">Melden Sie sich bei der Umgebung (HQ) an.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="d1ad9-159">Verwenden Sie das Menü auf der linken Seite, um zu **Retail and Commerce \> Anfragen und Berichte \> Batch-Jobs** zu gehen.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="d1ad9-160">Die verbleibenden Schritte dieses Verfahrens müssen für jeden der folgenden Jobs ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="d1ad9-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="d1ad9-161">Einzelhandelsauftrag für E-Mail-Benachrichtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="d1ad9-161">Process retail order email notification</span></span>
    * <span data-ttu-id="d1ad9-162">Produktverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="d1ad9-162">Product availability</span></span>
    * <span data-ttu-id="d1ad9-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="d1ad9-163">P-0001</span></span>
    * <span data-ttu-id="d1ad9-164">Einzelvorgang für Aufträge synchronisieren</span><span class="sxs-lookup"><span data-stu-id="d1ad9-164">Synchronize orders job</span></span>

1. <span data-ttu-id="d1ad9-165">Verwenden Sie den Schnellfilter, um nach dem Auftrag anhand seines Namens zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="d1ad9-166">Wenn der Status des Auftrags **Wird ausgeführt** lautet, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d1ad9-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="d1ad9-167">Wählen Sie den Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-167">Select the record.</span></span>
    1. <span data-ttu-id="d1ad9-168">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** die Option **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="d1ad9-169">Wählen Sie **Wird abgebrochen** aus, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="d1ad9-170">Optional können Sie auch das Serienintervall für die folgenden Einzelvorgänge auf eine (1) Minute festlegen:</span><span class="sxs-lookup"><span data-stu-id="d1ad9-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="d1ad9-171">E-Mail-Benachrichtigungseinzelvorgang für Einzelhandelsauftrag verarbeiten</span><span class="sxs-lookup"><span data-stu-id="d1ad9-171">Process retail order email notification job</span></span>
* <span data-ttu-id="d1ad9-172">P-0001-Einzelvorgang</span><span class="sxs-lookup"><span data-stu-id="d1ad9-172">P-0001 job</span></span>
* <span data-ttu-id="d1ad9-173">Einzelvorgang für Aufträge synchronisieren</span><span class="sxs-lookup"><span data-stu-id="d1ad9-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="d1ad9-174">Vollständige Datensynchronisation ausführen</span><span class="sxs-lookup"><span data-stu-id="d1ad9-174">Run full data synchronization</span></span>

<span data-ttu-id="d1ad9-175">Um die vollständige Datensynchronisierung in Commerce auszuführen, führen Sie diese Schritte in der Commerce-Zentralverwaltung aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="d1ad9-176">Verwenden Sie das Menü auf der linken Seite, um zu **Module \> Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Commerce-Planer \> Kanaldatenbank** zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="d1ad9-177">Wählen Sie den Kanal mit der Bezeichnung **scXXXXXXXXX** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="d1ad9-178">Wählen Sie **Vollständige Datensynchronisierung** im Aktionsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="d1ad9-179">Geben Sie **9999** als Vertriebsplan ein.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="d1ad9-180">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-180">Select **OK**.</span></span>
1. <span data-ttu-id="d1ad9-181">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="d1ad9-182">Testen der Kreditkartendaten, um Testkäufe durchzuführen</span><span class="sxs-lookup"><span data-stu-id="d1ad9-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="d1ad9-183">Um Testtransaktionen auf der Site durchzuführen, können Sie diese Testkreditkartendaten verwenden:</span><span class="sxs-lookup"><span data-stu-id="d1ad9-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="d1ad9-184">**Kartennummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="d1ad9-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="d1ad9-185">**Ablaufdatum:** 10/20</span><span class="sxs-lookup"><span data-stu-id="d1ad9-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="d1ad9-186">**Kartenprüfwert-Code (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="d1ad9-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1ad9-187">Sie sollten unter keinen Umständen versuchen, die tatsächlichen Kreditkarteninformationen auf der Testseite zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d1ad9-188">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d1ad9-188">Next steps</span></span>

<span data-ttu-id="d1ad9-189">Nachdem die Bereitstellungs- und Konfigurationsschritte abgeschlossen sind, können Sie mit der Verwendung Ihrer Auswertungsumgebung beginnen.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="d1ad9-190">Verwenden Sie die URL des Commerce-Website-Generators, um zur Erstellungsumgebung zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="d1ad9-191">Verwenden Sie die URL der Commerce-Website, um zur Umgebung der Einzelhandelskundenwebsite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="d1ad9-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="d1ad9-192">Informationen zum Konfigurieren optionaler Funktionen für Ihre Commerce-Auswertungsumgebung erhalten Sie unter [Optionale Funktionen für eine Commerce-Auswertungsumgebung konfigurieren](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="d1ad9-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1ad9-193">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d1ad9-193">Additional resources</span></span>

[<span data-ttu-id="d1ad9-194">Dynamics 365 Commerce-Auswertungsumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="d1ad9-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="d1ad9-195">Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="d1ad9-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="d1ad9-196">Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d1ad9-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="d1ad9-197">BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d1ad9-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="d1ad9-198">Dynamics 365 Commerce-Auswertungsumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="d1ad9-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="d1ad9-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d1ad9-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="d1ad9-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="d1ad9-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="d1ad9-201">Microsoft Azure-Portal</span><span class="sxs-lookup"><span data-stu-id="d1ad9-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="d1ad9-202">Dynamics 365 Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="d1ad9-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
