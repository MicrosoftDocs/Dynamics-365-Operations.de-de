---
title: Zeit und Anwesenheit im Einzelhandel
description: "In diesem Thema werden Szenarien beschreiben, die für die Verwaltung von Zeit und Anwesenheit Microsoft Dynamics 365 for Retail unterstützt werden."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ebbf3c72b4c34cba95ecd2fb3ce506af393acc34
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="retail-time-and-attendance"></a><span data-ttu-id="43e2f-103">Einzelhandelszeit und Anwesenheit</span><span class="sxs-lookup"><span data-stu-id="43e2f-103">Retail time and attendance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="43e2f-104">In diesem Thema werden Szenarien beschreiben, die für die Verwaltung von Zeit und Anwesenheit Microsoft Dynamics 365 for Retail unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="43e2f-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="43e2f-105">Verwalten Sie Arbeitskrafteinstellung und Feinterminierung</span><span class="sxs-lookup"><span data-stu-id="43e2f-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="43e2f-106">Ausgangskonfiguration</span><span class="sxs-lookup"><span data-stu-id="43e2f-106">Initial configuration</span></span>

-   <span data-ttu-id="43e2f-107">Führen Sie den Konfigurationsassistenten aus.</span><span class="sxs-lookup"><span data-stu-id="43e2f-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="43e2f-108">Registrieren Sie Arbeitskräfte als Zeiterfassungsarbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="43e2f-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="43e2f-109">Planen von Arbeitskraftzeitplänen</span><span class="sxs-lookup"><span data-stu-id="43e2f-109">Plan worker schedules</span></span>

-   <span data-ttu-id="43e2f-110">Wenden Sie Profile durch Verwendung der Arbeitsplanung an.</span><span class="sxs-lookup"><span data-stu-id="43e2f-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="43e2f-111">Weitere Informationen finden Sie unter <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span><span class="sxs-lookup"><span data-stu-id="43e2f-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="43e2f-112">Informationen zu den Konfigurationsschritten finden Sie unter <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span><span class="sxs-lookup"><span data-stu-id="43e2f-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="43e2f-113">Einzelhandelsspezifische Konfiguration</span><span class="sxs-lookup"><span data-stu-id="43e2f-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="43e2f-114">Aktivieren Sie ein Funktionsprofil für die Zeiterfassung für Arbeitskräfte, für die Sie Zeiterfassungen aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="43e2f-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="43e2f-115">Klicken Sie auf **POS-Funktionensprofile** &gt; **Funktionen** &gt; **POS-Zeiterfassungen** &gt; **Zeiterfassungen aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="43e2f-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="43e2f-116">Konfigurieren Sie Point-of-Sale-Berechtigungsgruppen (POS), um die Berechtigung zum Anzeigen von Zeiterfassungseinträgen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="43e2f-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="43e2f-117">Diese Berechtigung ermöglicht einem Benutzer die Anzeige der Zeiterfassungen anderer Arbeitskräfte im Shop (und von jedem anderen Shops, dem der Benutzer zugeordnet ist, über das Adressbuch).</span><span class="sxs-lookup"><span data-stu-id="43e2f-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="43e2f-118">Sie sollten diese Berechtigung für eine Managerrolle aber nicht für eine Kassiererrolle aktivieren.</span><span class="sxs-lookup"><span data-stu-id="43e2f-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="43e2f-119">Klicken Sie auf **POS-Berechtigungsgruppen** &gt; **Zeiterfassungseinträge anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="43e2f-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="43e2f-120">Kassenzeit</span><span class="sxs-lookup"><span data-stu-id="43e2f-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="43e2f-121">Kassierer- und Nichtkassiererzeiterfassungen</span><span class="sxs-lookup"><span data-stu-id="43e2f-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="43e2f-122">Im POS:</span><span class="sxs-lookup"><span data-stu-id="43e2f-122">On POS:</span></span>
    -   <span data-ttu-id="43e2f-123">Einstempel-Vorgänge:</span><span class="sxs-lookup"><span data-stu-id="43e2f-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="43e2f-124">Melden Sie sich mit einem Vorgäng ohne Kassenlade oder mit einer neuen Schicht an.</span><span class="sxs-lookup"><span data-stu-id="43e2f-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="43e2f-125">Wählen Sie einen Zeituhrarbeitsgang aus.</span><span class="sxs-lookup"><span data-stu-id="43e2f-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="43e2f-126">Wählen Sie einen gewünschten Vorgang aus:</span><span class="sxs-lookup"><span data-stu-id="43e2f-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="43e2f-127">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-127">Clock-in</span></span>
            -   <span data-ttu-id="43e2f-128">Pause für Arbeit</span><span class="sxs-lookup"><span data-stu-id="43e2f-128">Break for Work</span></span>
            -   <span data-ttu-id="43e2f-129">Mittagspause</span><span class="sxs-lookup"><span data-stu-id="43e2f-129">Break for Lunch</span></span>
            -   <span data-ttu-id="43e2f-130">Ausstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="43e2f-131">Aktueller Status:</span><span class="sxs-lookup"><span data-stu-id="43e2f-131">Current state</span></span></th>
    <th><span data-ttu-id="43e2f-132">Verfügbare Vorgänge</span><span class="sxs-lookup"><span data-stu-id="43e2f-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="43e2f-133">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="43e2f-134">Pause für Arbeit</span><span class="sxs-lookup"><span data-stu-id="43e2f-134">Break for Work</span></span></li>
    <li><span data-ttu-id="43e2f-135">Mittagspause</span><span class="sxs-lookup"><span data-stu-id="43e2f-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="43e2f-136">Ausstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="43e2f-137">Pause für Arbeit</span><span class="sxs-lookup"><span data-stu-id="43e2f-137">Break for Work</span></span></td>
    <td><span data-ttu-id="43e2f-138">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="43e2f-139">Mittagspause</span><span class="sxs-lookup"><span data-stu-id="43e2f-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="43e2f-140">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="43e2f-141">Ausstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-141">Clock-out</span></span></td>
    <td><span data-ttu-id="43e2f-142">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="43e2f-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="43e2f-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="43e2f-144">Sehen Sie die Bestätigungsmeldung an, und überprüfen Sie, ob die Uhrzeit der aktuellen Aktivität korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="43e2f-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="43e2f-145">Arbeitsprotokoll:</span><span class="sxs-lookup"><span data-stu-id="43e2f-145">Logbook:</span></span>
    -   <span data-ttu-id="43e2f-146">Klicken Sie auf **Arbeitsprotokoll**, um die Zeituhraktivität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="43e2f-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="43e2f-147">Verwenden Sei Zeitfilter, um unterschiedliche Zeitfenster auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="43e2f-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="43e2f-148">Wenn Sie an mehreren Filialstandorten arbeiten, Sie Ihre Zeiterfassungen von allen Shops, in denen Sie Zeit erfasst haben.</span><span class="sxs-lookup"><span data-stu-id="43e2f-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="43e2f-149">Sie können den Shopfilter verwenden, um Zeiterfassungen von einem ausgewählten Shop anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="43e2f-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="43e2f-150">Unterschiedliche Zeitzonen:</span><span class="sxs-lookup"><span data-stu-id="43e2f-150">Different time zones:</span></span>
    -   <span data-ttu-id="43e2f-151">Wenn Sie Zeit von einem anderen Standort (für das Kassiererarbeitsprotokoll oder mithilfe von **Zeiterfassungseinträge anzeigen** für ein Managerszenario) anzeigen und dieser Standort in einer anderen Zeitzone ist, werden die Zeiterfassungen, die Sie sehen, in Ihre lokale Zeitzone umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="43e2f-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="43e2f-152">Beispielsweise sind Sie ein Manager für zwei Shops, eine in Arizona und der andere im Nevada.</span><span class="sxs-lookup"><span data-stu-id="43e2f-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="43e2f-153">Ein Kassierer Einstempeln erfasst ein an 9:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="43e2f-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="43e2f-154">in Arizona.</span><span class="sxs-lookup"><span data-stu-id="43e2f-154">in Arizona.</span></span> <span data-ttu-id="43e2f-155">In diesem Moment ist es in Nevada 8:00 Uhr.</span><span class="sxs-lookup"><span data-stu-id="43e2f-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="43e2f-156">Wenn Sie also im Shop in Nevada sind und Zeiterfassungen anzeigen, wird die Zeiterfassung als 8 Uhr angegeben.</span><span class="sxs-lookup"><span data-stu-id="43e2f-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="43e2f-157">Zeiterfassungsarbeitskräfte anzeigen</span><span class="sxs-lookup"><span data-stu-id="43e2f-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="43e2f-158">Anzeigen von Arbeitskraftzeiterfassungen und Filtern nach Shop oder Aktivitätstyp</span><span class="sxs-lookup"><span data-stu-id="43e2f-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="43e2f-159">Im POS:</span><span class="sxs-lookup"><span data-stu-id="43e2f-159">On POS:</span></span>

-   <span data-ttu-id="43e2f-160">Wählen Sie **Zeiterfassungseinträge anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="43e2f-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="43e2f-161">Sie sehen Zeituhrerfassungsaktivitäten von allen Arbeitskräften, die den gleichen Filialen zugewiesen sind, denen Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="43e2f-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="43e2f-162">Sie können den Aktivitätstyp und Shopfilter verwenden, um Zeiterfassungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="43e2f-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="43e2f-163">Verarbeiten und Verwalten von Zeit- und Anwesenheitserfassungen</span><span class="sxs-lookup"><span data-stu-id="43e2f-163">Process and manage time registrations</span></span>
<span data-ttu-id="43e2f-164">Ein Dynamics 365 for Retail Benutzer folgt dem Workflow, um Zeiterfassungen zu berechnen, zu genehmigen und in die Lohnabrechnung zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="43e2f-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="43e2f-165">Primäre Vorgänge</span><span class="sxs-lookup"><span data-stu-id="43e2f-165">Primary operations</span></span>

-   <span data-ttu-id="43e2f-166">Berechnen</span><span class="sxs-lookup"><span data-stu-id="43e2f-166">Calculate</span></span>
-   <span data-ttu-id="43e2f-167">Genehmigen</span><span class="sxs-lookup"><span data-stu-id="43e2f-167">Approve</span></span>
-   <span data-ttu-id="43e2f-168">An Lohnabrechnung übertragen</span><span class="sxs-lookup"><span data-stu-id="43e2f-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="43e2f-169">Andere allgemeine Vorgänge</span><span class="sxs-lookup"><span data-stu-id="43e2f-169">Other common operations</span></span>

-   <span data-ttu-id="43e2f-170">Massenausstempeln</span><span class="sxs-lookup"><span data-stu-id="43e2f-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="43e2f-171">Erfassen der Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="43e2f-171">Register Absence</span></span>

<span data-ttu-id="43e2f-172">Weitere Informationen zum Verarbeiten von Zeit- und Anwesenheitserfassungen finden Sie unter <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span><span class="sxs-lookup"><span data-stu-id="43e2f-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>




