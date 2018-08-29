---
title: Zeit- und Anwesenheitsverwaltung in Retail
description: "In diesem Thema werden Szenarien beschreiben, die für die Verwaltung von Zeit und Anwesenheit Microsoft Dynamics 365 for Retail unterstützt werden."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 21c29c3c37dfacdd98f5c3ec7698f07623da2285
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="a4270-103">Zeit- und Anwesenheitsverwaltung in Retail</span><span class="sxs-lookup"><span data-stu-id="a4270-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4270-104">In diesem Thema werden Szenarien beschreiben, die für die Verwaltung von Zeit und Anwesenheit Microsoft Dynamics 365 for Retail unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a4270-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="a4270-105">Verwalten Sie Arbeitskrafteinstellung und Feinterminierung</span><span class="sxs-lookup"><span data-stu-id="a4270-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="a4270-106">Ausgangskonfiguration</span><span class="sxs-lookup"><span data-stu-id="a4270-106">Initial configuration</span></span>

-   <span data-ttu-id="a4270-107">Führen Sie den Konfigurationsassistenten aus.</span><span class="sxs-lookup"><span data-stu-id="a4270-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="a4270-108">Registrieren Sie Arbeitskräfte als Zeiterfassungsarbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="a4270-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="a4270-109">Planen von Arbeitskraftzeitplänen</span><span class="sxs-lookup"><span data-stu-id="a4270-109">Plan worker schedules</span></span>

-   <span data-ttu-id="a4270-110">Wenden Sie Profile durch Verwendung der Arbeitsplanung an.</span><span class="sxs-lookup"><span data-stu-id="a4270-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="a4270-111">Weitere Informationen finden Sie unter <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span><span class="sxs-lookup"><span data-stu-id="a4270-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="a4270-112">Weitere Informationen zu den Konfigurationsschritten finden Sie unter <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span><span class="sxs-lookup"><span data-stu-id="a4270-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="a4270-113">Einzelhandelsspezifische Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a4270-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="a4270-114">Aktivieren Sie ein Funktionsprofil für die Zeiterfassung für Arbeitskräfte, für die Sie Zeiterfassungen aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a4270-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="a4270-115">Klicken Sie auf **POS-Funktionensprofile** &gt; **Funktionen** &gt; **POS-Zeiterfassungen** &gt; **Zeiterfassungen aktivieren.**</span><span class="sxs-lookup"><span data-stu-id="a4270-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="a4270-116">Konfigurieren Sie Point-of-Sale-Berechtigungsgruppen (POS), um die Berechtigung zum Anzeigen von Zeiterfassungseinträgen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a4270-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="a4270-117">Diese Berechtigung ermöglicht einem Benutzer die Anzeige der Zeiterfassungen anderer Arbeitskräfte im Shop (und von jedem anderen Shops, dem der Benutzer zugeordnet ist, über das Adressbuch).</span><span class="sxs-lookup"><span data-stu-id="a4270-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="a4270-118">Sie sollten diese Berechtigung für eine Managerrolle aber nicht für eine Kassiererrolle aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a4270-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="a4270-119">Klicken Sie auf **POS-Berechtigungsgruppen** &gt; **Zeiterfassungseinträge anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="a4270-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="a4270-120">Kassenzeit</span><span class="sxs-lookup"><span data-stu-id="a4270-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="a4270-121">Kassierer- und Nichtkassiererzeiterfassungen</span><span class="sxs-lookup"><span data-stu-id="a4270-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="a4270-122">Im POS:</span><span class="sxs-lookup"><span data-stu-id="a4270-122">On POS:</span></span>
    -   <span data-ttu-id="a4270-123">Einstempel-Vorgänge:</span><span class="sxs-lookup"><span data-stu-id="a4270-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="a4270-124">Melden Sie sich mit einem Vorgäng ohne Kassenlade oder mit einer neuen Schicht an.</span><span class="sxs-lookup"><span data-stu-id="a4270-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="a4270-125">Wählen Sie einen Zeituhrarbeitsgang aus.</span><span class="sxs-lookup"><span data-stu-id="a4270-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="a4270-126">Wählen Sie einen gewünschten Vorgang aus:</span><span class="sxs-lookup"><span data-stu-id="a4270-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="a4270-127">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-127">Clock-in</span></span>
            -   <span data-ttu-id="a4270-128">Pause für Arbeit</span><span class="sxs-lookup"><span data-stu-id="a4270-128">Break for Work</span></span>
            -   <span data-ttu-id="a4270-129">Mittagspause</span><span class="sxs-lookup"><span data-stu-id="a4270-129">Break for Lunch</span></span>
            -   <span data-ttu-id="a4270-130">Ausstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="a4270-131">Aktueller Status:</span><span class="sxs-lookup"><span data-stu-id="a4270-131">Current state</span></span></th>
    <th><span data-ttu-id="a4270-132">Verfügbare Vorgänge</span><span class="sxs-lookup"><span data-stu-id="a4270-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="a4270-133">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="a4270-134">Pause für Arbeit</span><span class="sxs-lookup"><span data-stu-id="a4270-134">Break for Work</span></span></li>
    <li><span data-ttu-id="a4270-135">Mittagspause</span><span class="sxs-lookup"><span data-stu-id="a4270-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="a4270-136">Ausstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a4270-137">Pause für Arbeit</span><span class="sxs-lookup"><span data-stu-id="a4270-137">Break for Work</span></span></td>
    <td><span data-ttu-id="a4270-138">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="a4270-139">Mittagspause</span><span class="sxs-lookup"><span data-stu-id="a4270-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="a4270-140">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="a4270-141">Ausstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-141">Clock-out</span></span></td>
    <td><span data-ttu-id="a4270-142">Einstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="a4270-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="a4270-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="a4270-144">Sehen Sie die Bestätigungsmeldung an, und überprüfen Sie, ob die Uhrzeit der aktuellen Aktivität korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="a4270-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="a4270-145">Arbeitsprotokoll:</span><span class="sxs-lookup"><span data-stu-id="a4270-145">Logbook:</span></span>
    -   <span data-ttu-id="a4270-146">Klicken Sie auf **Arbeitsprotokoll**, um die Zeituhraktivität anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a4270-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="a4270-147">Verwenden Sei Zeitfilter, um unterschiedliche Zeitfenster auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a4270-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="a4270-148">Wenn Sie an mehreren Filialstandorten arbeiten, Sie Ihre Zeiterfassungen von allen Shops, in denen Sie Zeit erfasst haben.</span><span class="sxs-lookup"><span data-stu-id="a4270-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="a4270-149">Sie können den Shopfilter verwenden, um Zeiterfassungen von einem ausgewählten Shop anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a4270-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="a4270-150">Unterschiedliche Zeitzonen:</span><span class="sxs-lookup"><span data-stu-id="a4270-150">Different time zones:</span></span>
    -   <span data-ttu-id="a4270-151">Wenn Sie Zeit von einem anderen Standort (für das Kassiererarbeitsprotokoll oder mithilfe von **Zeiterfassungseinträge anzeigen** für ein Managerszenario) anzeigen und dieser Standort in einer anderen Zeitzone ist, werden die Zeiterfassungen, die Sie sehen, in Ihre lokale Zeitzone umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="a4270-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="a4270-152">Beispielsweise sind Sie ein Manager für zwei Shops, eine in Arizona und der andere im Nevada.</span><span class="sxs-lookup"><span data-stu-id="a4270-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="a4270-153">Ein Kassierer Einstempeln erfasst ein an 9:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="a4270-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="a4270-154">in Arizona.</span><span class="sxs-lookup"><span data-stu-id="a4270-154">in Arizona.</span></span> <span data-ttu-id="a4270-155">In diesem Moment ist es in Nevada 8:00 Uhr.</span><span class="sxs-lookup"><span data-stu-id="a4270-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="a4270-156">Wenn Sie also im Shop in Nevada sind und Zeiterfassungen anzeigen, wird die Zeiterfassung als 8 Uhr angegeben.</span><span class="sxs-lookup"><span data-stu-id="a4270-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="a4270-157">Zeiterfassungsarbeitskräfte anzeigen</span><span class="sxs-lookup"><span data-stu-id="a4270-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="a4270-158">Anzeigen von Arbeitskraftzeiterfassungen und Filtern nach Shop oder Aktivitätstyp</span><span class="sxs-lookup"><span data-stu-id="a4270-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="a4270-159">Im POS:</span><span class="sxs-lookup"><span data-stu-id="a4270-159">On POS:</span></span>

-   <span data-ttu-id="a4270-160">Wählen Sie **Zeiterfassungseinträge anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="a4270-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="a4270-161">Sie sehen Zeituhrerfassungsaktivitäten von allen Arbeitskräften, die den gleichen Filialen zugewiesen sind, denen Sie zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="a4270-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="a4270-162">Sie können den Aktivitätstyp und Shopfilter verwenden, um Zeiterfassungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="a4270-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="a4270-163">Verarbeiten und Verwalten von Zeit- und Anwesenheitserfassungen</span><span class="sxs-lookup"><span data-stu-id="a4270-163">Process and manage time registrations</span></span>
<span data-ttu-id="a4270-164">Ein Dynamics 365 for Retail Benutzer folgt dem Workflow, um Zeiterfassungen zu berechnen, zu genehmigen und in die Lohnabrechnung zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="a4270-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="a4270-165">Primäre Vorgänge</span><span class="sxs-lookup"><span data-stu-id="a4270-165">Primary operations</span></span>

-   <span data-ttu-id="a4270-166">Berechnen</span><span class="sxs-lookup"><span data-stu-id="a4270-166">Calculate</span></span>
-   <span data-ttu-id="a4270-167">Genehmigen</span><span class="sxs-lookup"><span data-stu-id="a4270-167">Approve</span></span>
-   <span data-ttu-id="a4270-168">An Lohnabrechnung übertragen</span><span class="sxs-lookup"><span data-stu-id="a4270-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="a4270-169">Andere allgemeine Vorgänge</span><span class="sxs-lookup"><span data-stu-id="a4270-169">Other common operations</span></span>

-   <span data-ttu-id="a4270-170">Massenausstempeln</span><span class="sxs-lookup"><span data-stu-id="a4270-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="a4270-171">Erfassen der Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="a4270-171">Register Absence</span></span>

<span data-ttu-id="a4270-172">Informationen zum Verarbeiten von Zeit- und Anwesenheitserfassungen finden Sie unter <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span><span class="sxs-lookup"><span data-stu-id="a4270-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>




