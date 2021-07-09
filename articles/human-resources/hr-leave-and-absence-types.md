---
title: Urlaubs- und Abwesenheitstypen konfigurieren
description: Einrichten von Abwesenheitstypen, die Mitarbeiter in Anspruch nehmen können in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e4c4b9c83ca648c21ac20bd20b739af8a6b9ed
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271126"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="d88b9-103">Urlaubs- und Abwesenheitstypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d88b9-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d88b9-104">Abwesenheitstypen in Dynamics 365 Human Resources definieren die verschiedenen Arten von Abwesenheitszeiten, die Mitarbeiter melden können.</span><span class="sxs-lookup"><span data-stu-id="d88b9-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="d88b9-105">Sie können die Abwesenheitstypen an die Bedürfnisse Ihrer Organisation anpassen.</span><span class="sxs-lookup"><span data-stu-id="d88b9-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="d88b9-106">Beispiele für Abwesenheitstypen sind:</span><span class="sxs-lookup"><span data-stu-id="d88b9-106">Examples of leave types include:</span></span>

- <span data-ttu-id="d88b9-107">Entlohnte Zeit (PTO)</span><span class="sxs-lookup"><span data-stu-id="d88b9-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="d88b9-108">Unbezahlter Sonderurlaub</span><span class="sxs-lookup"><span data-stu-id="d88b9-108">Unpaid leave</span></span>
- <span data-ttu-id="d88b9-109">Bezahlter Urlaub</span><span class="sxs-lookup"><span data-stu-id="d88b9-109">Paid vacation</span></span>
- <span data-ttu-id="d88b9-110">Krankheitsbedingte Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="d88b9-110">Sick leave</span></span>
- <span data-ttu-id="d88b9-111">Medizinischer Urlaub</span><span class="sxs-lookup"><span data-stu-id="d88b9-111">Medical leave</span></span>
- <span data-ttu-id="d88b9-112">Familienurlaub</span><span class="sxs-lookup"><span data-stu-id="d88b9-112">Family leave</span></span>
- <span data-ttu-id="d88b9-113">Kurzfristige Behinderung</span><span class="sxs-lookup"><span data-stu-id="d88b9-113">Short-term disability</span></span>
- <span data-ttu-id="d88b9-114">Trauerurlaub</span><span class="sxs-lookup"><span data-stu-id="d88b9-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="d88b9-115">Fügen Sie einen Abwesenehitstyp hinzu</span><span class="sxs-lookup"><span data-stu-id="d88b9-115">Add a leave type</span></span>

1. <span data-ttu-id="d88b9-116">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="d88b9-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d88b9-117">Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitstypen**.</span><span class="sxs-lookup"><span data-stu-id="d88b9-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="d88b9-118">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d88b9-118">Select **New**.</span></span>

4. <span data-ttu-id="d88b9-119">Geben Sie einen Namen für den Abwesenheitstyp ein unter **Typ** wählen Sie einen Workflow aus unter **Workflow-ID** und geben Sie eine Beschreibung ein unter **Beschreibung**.</span><span class="sxs-lookup"><span data-stu-id="d88b9-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="d88b9-120">Unter **Allgemein**, wählen Sie **Keine**, **Geplant**, oder **Nicht geplant** aus der Dropdown-Liste **Kategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="d88b9-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="d88b9-121">Wählen Sie einen Einkommenscode aus der **Einkommenscode** Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="d88b9-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="d88b9-122">Unter **Ursachencode erforderlich** wählen Sie, ob Sie einen Ursachencode benötigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d88b9-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="d88b9-123">Wenn Sie Ursachencodes benötigen, müssen Sie diese möglicherweise hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d88b9-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="d88b9-124">Unter **Ursachencodes** wählen Sie **Hinzufügen**, wählen Sie einen Ursachencode und dann das Kontrollkästchen **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="d88b9-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="d88b9-125">Unter **Beschränken Sie den Zugriff auf ausgewählte Rollen** wählen Sie, ob Sie den Zugriff einschränken möchten.</span><span class="sxs-lookup"><span data-stu-id="d88b9-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="d88b9-126">Wählen Sie dann die Sicherheitsrollen unter **Sicherheitsrollen für diesen Urlaubstyp**.</span><span class="sxs-lookup"><span data-stu-id="d88b9-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="d88b9-127">Die Sicherheitsrollen werden in dem Workflow definiert, den Sie unter **Workflow-ID** früher in diesem Verfahren ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d88b9-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="d88b9-128">Wählen Sie unter **Kalenderfarbe** aus, welche Farbe in Urlaubs- und Abwesenheitskalendern für diesen Urlaubstyp angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d88b9-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="d88b9-129">Unter **Suspendierungsbeziehungen** wählen Sie, ob dieser Urlaubstyp entweder einen anderen Urlaubstyp aussetzt oder von einem anderen Urlaubstyp ausgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d88b9-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="d88b9-130">Wenn ein Antrag auf Beurlaubung für die Art der Aussetzung des Urlaubs gestellt wird, wird automatisch eine Aussetzung der Beurlaubung für die Art der Aussetzung des Urlaubs erstellt.</span><span class="sxs-lookup"><span data-stu-id="d88b9-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="d88b9-131">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d88b9-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="d88b9-132">Konfigurieren Sie die Urlaubstypregeln</span><span class="sxs-lookup"><span data-stu-id="d88b9-132">Configure leave type rules</span></span>

1. <span data-ttu-id="d88b9-133">Stellen Sie Rundungsoptionen für die Urlaubsart ein.</span><span class="sxs-lookup"><span data-stu-id="d88b9-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="d88b9-134">Optionen umfassen **Keine**, **Oben**, **Unten**, und **Nächste**.</span><span class="sxs-lookup"><span data-stu-id="d88b9-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="d88b9-135">Sie können auch die Rundungsgenauigkeit für den Urlaubstyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="d88b9-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="d88b9-136">Stellen **Urlaubskorrekturen** für den Abwesenheitstyp ein.</span><span class="sxs-lookup"><span data-stu-id="d88b9-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="d88b9-137">Wenn Sie diese Option auswählen, verwendet die Personalabteilung die Anzahl der Feiertage, die auf einen Arbeitstag fallen, um zu bestimmen, wie Freizeit für die Urlaubsart angesammelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d88b9-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="d88b9-138">Wenn beispielsweise der Weihnachtstag auf einen Montag fällt, zieht die Personalabteilung bei der Verarbeitung von Rückstellungen einen Tag von der Urlaubsart ab.</span><span class="sxs-lookup"><span data-stu-id="d88b9-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="d88b9-139">Sie legen den Urlaub im Arbeitszeitkalender fest.</span><span class="sxs-lookup"><span data-stu-id="d88b9-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="d88b9-140">Weitere Informationen finden Sie unter [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="d88b9-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="d88b9-141">Einstellen des **Vortragstyps** für den Urlaubstyp.</span><span class="sxs-lookup"><span data-stu-id="d88b9-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="d88b9-142">Wenn Sie diese Option auswählen, werden alle Vortragsguthaben auf die angegebene Urlaubsart übertragen.</span><span class="sxs-lookup"><span data-stu-id="d88b9-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="d88b9-143">Die Art des Vortragstyps für den Urlaub muss ebenfalls in den Urlaubs- und Abwesenheitsplan aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="d88b9-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
4. <span data-ttu-id="d88b9-144">Definieren von **Ablaufregeln** für den Urlaubstyp.</span><span class="sxs-lookup"><span data-stu-id="d88b9-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="d88b9-145">Wenn Sie diese Option konfigurieren, können Sie die Einheit Tage oder Monate wählen und die Dauer für den Verfall festlegen.</span><span class="sxs-lookup"><span data-stu-id="d88b9-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiration.</span></span> <span data-ttu-id="d88b9-146">Das Gültigkeitsdatum der Verfallsregel wird verwendet, um zu bestimmen, wann der Batchauftrag ausgeführt wird, der den Urlaubsverfall verarbeitet, oder das Datum, an dem die Regel in Kraft tritt.</span><span class="sxs-lookup"><span data-stu-id="d88b9-146">The effective date of the expiration rule is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="d88b9-147">Der Verfall selbst findet immer am Startdatum der Abgrenzungsperiode statt.</span><span class="sxs-lookup"><span data-stu-id="d88b9-147">The expiration itself will always occur on the accrual period start date.</span></span> <span data-ttu-id="d88b9-148">Wenn z. B. das Abgrenzungszeitraum-Startdatum der 3. August 2021 ist und die Verfallsregel auf 6 Monate festgelegt wurde, wird die Regel basierend auf dem Verfalls-Offset vom Abgrenzungszeitraum-Startdatum verarbeitet, so dass sie am 3. Februar 2022 ausgeführt würde.</span><span class="sxs-lookup"><span data-stu-id="d88b9-148">For example, if the accrual period start date is August 3, 2021, and the expiration rule was set at 6 months, the rule will be processed based on the expiration offset from the accrual period start date, so it would be executed on February 3, 2022.</span></span> <span data-ttu-id="d88b9-149">Zum Zeitpunkt des Ablaufs vorhandene Urlaubsguthaben werden von der Urlaubsart abgezogen und im Urlaubsguthaben ausgewiesen.</span><span class="sxs-lookup"><span data-stu-id="d88b9-149">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span>
 
## <a name="see-also"></a><span data-ttu-id="d88b9-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d88b9-150">See also</span></span>

- [<span data-ttu-id="d88b9-151">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="d88b9-151">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="d88b9-152">Einen Urlaubs- und Abwesenheitsplan erstellen</span><span class="sxs-lookup"><span data-stu-id="d88b9-152">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="d88b9-153">Einen Arbeitszeitkalender erstellen</span><span class="sxs-lookup"><span data-stu-id="d88b9-153">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="d88b9-154">Urlaub aussetzen</span><span class="sxs-lookup"><span data-stu-id="d88b9-154">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)
- [<span data-ttu-id="d88b9-155">Einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="d88b9-155">Create a buy and sell leave request workflow</span></span>](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
