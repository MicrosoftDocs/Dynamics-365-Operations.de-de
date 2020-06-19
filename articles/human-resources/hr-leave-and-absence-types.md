---
title: Urlaubs- und Abwesenheitstypen konfigurieren
description: Einrichten von Abwesenheitstypen, die Mitarbeiter in Anspruch nehmen können in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1802938f54a1d78e6ea60572a76177a037192ae0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428592"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="f83f2-103">Urlaubs- und Abwesenheitstypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f83f2-103">Configure leave and absence types</span></span>

<span data-ttu-id="f83f2-104">Abwesenheitstypen in Dynamics 365 Human Resources definieren die verschiedenen Arten von Abwesenheitszeiten, die Mitarbeiter melden können.</span><span class="sxs-lookup"><span data-stu-id="f83f2-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="f83f2-105">Sie können die Abwesenheitstypen an die Bedürfnisse Ihrer Organisation anpassen.</span><span class="sxs-lookup"><span data-stu-id="f83f2-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="f83f2-106">Beispiele für Abwesenheitstypen sind:</span><span class="sxs-lookup"><span data-stu-id="f83f2-106">Examples of leave types include:</span></span>

- <span data-ttu-id="f83f2-107">Entlohnte Zeit (PTO)</span><span class="sxs-lookup"><span data-stu-id="f83f2-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="f83f2-108">Unbezahlter Sonderurlaub</span><span class="sxs-lookup"><span data-stu-id="f83f2-108">Unpaid leave</span></span>
- <span data-ttu-id="f83f2-109">Bezahlter Urlaub</span><span class="sxs-lookup"><span data-stu-id="f83f2-109">Paid vacation</span></span>
- <span data-ttu-id="f83f2-110">Krankheitsbedingte Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="f83f2-110">Sick leave</span></span>
- <span data-ttu-id="f83f2-111">Medizinischer Urlaub</span><span class="sxs-lookup"><span data-stu-id="f83f2-111">Medical leave</span></span>
- <span data-ttu-id="f83f2-112">Familienurlaub</span><span class="sxs-lookup"><span data-stu-id="f83f2-112">Family leave</span></span>
- <span data-ttu-id="f83f2-113">Kurzfristige Behinderung</span><span class="sxs-lookup"><span data-stu-id="f83f2-113">Short-term disability</span></span>
- <span data-ttu-id="f83f2-114">Trauerurlaub</span><span class="sxs-lookup"><span data-stu-id="f83f2-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="f83f2-115">Fügen Sie einen Abwesenehitstyp hinzu</span><span class="sxs-lookup"><span data-stu-id="f83f2-115">Add a leave type</span></span>

1. <span data-ttu-id="f83f2-116">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="f83f2-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="f83f2-117">Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitstypen**.</span><span class="sxs-lookup"><span data-stu-id="f83f2-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="f83f2-118">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f83f2-118">Select **New**.</span></span>

4. <span data-ttu-id="f83f2-119">Geben Sie einen Namen für den Abwesenheitstyp ein unter **Typ** wählen Sie einen Workflow aus unter **Workflow-ID** und geben Sie eine Beschreibung ein unter **Beschreibung**.</span><span class="sxs-lookup"><span data-stu-id="f83f2-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="f83f2-120">Unter **Allgemein**, wählen Sie **Keine**, **Geplant**, oder **Nicht geplant** aus der Dropdown-Liste **Kategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="f83f2-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="f83f2-121">Wählen Sie einen Einkommenscode aus der **Einkommenscode** Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="f83f2-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="f83f2-122">Unter **Ursachencode erforderlich** wählen Sie, ob Sie einen Ursachencode benötigen möchten.</span><span class="sxs-lookup"><span data-stu-id="f83f2-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="f83f2-123">Wenn Sie Ursachencodes benötigen, müssen Sie diese möglicherweise hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f83f2-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="f83f2-124">Unter **Ursachencodes** wählen Sie **Hinzufügen**, wählen Sie einen Ursachencode und dann das Kontrollkästchen **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="f83f2-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="f83f2-125">Unter **Beschränken Sie den Zugriff auf ausgewählte Rollen** wählen Sie, ob Sie den Zugriff einschränken möchten.</span><span class="sxs-lookup"><span data-stu-id="f83f2-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="f83f2-126">Wählen Sie dann die Sicherheitsrollen unter **Sicherheitsrollen für diesen Urlaubstyp**.</span><span class="sxs-lookup"><span data-stu-id="f83f2-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="f83f2-127">Die Sicherheitsrollen werden in dem Workflow definiert, den Sie unter **Workflow-ID** früher in diesem Verfahren ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="f83f2-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="f83f2-128">Unter **Suspendierungsbeziehungen** wählen Sie, ob dieser Urlaubstyp entweder einen anderen Urlaubstyp aussetzt oder von einem anderen Urlaubstyp ausgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f83f2-128">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="f83f2-129">Wenn ein Antrag auf Beurlaubung für die Art der Aussetzung des Urlaubs gestellt wird, wird automatisch eine Aussetzung der Beurlaubung für die Art der Aussetzung des Urlaubs erstellt.</span><span class="sxs-lookup"><span data-stu-id="f83f2-129">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="f83f2-130">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f83f2-130">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="f83f2-131">Konfigurieren Sie die Urlaubstypregeln</span><span class="sxs-lookup"><span data-stu-id="f83f2-131">Configure leave type rules</span></span>

1. <span data-ttu-id="f83f2-132">Stellen Sie Rundungsoptionen für die Urlaubsart ein.</span><span class="sxs-lookup"><span data-stu-id="f83f2-132">Set rounding options for the leave type.</span></span> <span data-ttu-id="f83f2-133">Optionen umfassen **Keine**, **Oben**, **Unten**, und **Nächste**.</span><span class="sxs-lookup"><span data-stu-id="f83f2-133">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="f83f2-134">Sie können auch die Rundungsgenauigkeit für den Urlaubstyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="f83f2-134">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="f83f2-135">Stellen **Urlaubskorrekturen** für den Abwesenheitstyp ein.</span><span class="sxs-lookup"><span data-stu-id="f83f2-135">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="f83f2-136">Wenn Sie diese Option auswählen, verwendet die Personalabteilung die Anzahl der Feiertage, die auf einen Arbeitstag fallen, um zu bestimmen, wie Freizeit für die Urlaubsart angesammelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f83f2-136">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="f83f2-137">Wenn beispielsweise der Weihnachtstag auf einen Montag fällt, zieht die Personalabteilung bei der Verarbeitung von Rückstellungen einen Tag von der Urlaubsart ab.</span><span class="sxs-lookup"><span data-stu-id="f83f2-137">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="f83f2-138">Sie legen den Urlaub im Arbeitszeitkalender fest.</span><span class="sxs-lookup"><span data-stu-id="f83f2-138">You set holidays in the working time calendar.</span></span> <span data-ttu-id="f83f2-139">Weitere Informationen finden Sie unter [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="f83f2-139">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="f83f2-140">Einstellen des **Vortragstyps** für den Urlaubstyp.</span><span class="sxs-lookup"><span data-stu-id="f83f2-140">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="f83f2-141">Wenn Sie diese Option auswählen, werden alle Vortragsguthaben auf die angegebene Urlaubsart übertragen.</span><span class="sxs-lookup"><span data-stu-id="f83f2-141">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="f83f2-142">Die Art des Vortragstyps für den Urlaub muss ebenfalls in den Urlaubs- und Abwesenheitsplan aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f83f2-142">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="f83f2-143">Definieren von **Ablaufregeln** für den Urlaubstyp.</span><span class="sxs-lookup"><span data-stu-id="f83f2-143">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="f83f2-144">Wenn Sie diese Option konfigurieren, können Sie die Einheit der Tage oder Monate auswählen und die Dauer für den Ablauf festlegen.</span><span class="sxs-lookup"><span data-stu-id="f83f2-144">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="f83f2-145">Sie können auch das Datum des Inkrafttretens der Ablaufregel festlegen.</span><span class="sxs-lookup"><span data-stu-id="f83f2-145">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="f83f2-146">Zum Zeitpunkt des Ablaufs vorhandene Urlaubsguthaben werden von der Urlaubsart abgezogen und im Urlaubsguthaben ausgewiesen.</span><span class="sxs-lookup"><span data-stu-id="f83f2-146">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="f83f2-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f83f2-147">See also</span></span>

- [<span data-ttu-id="f83f2-148">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="f83f2-148">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="f83f2-149">Einen Urlaubs- und Abwesenheitsplan erstellen</span><span class="sxs-lookup"><span data-stu-id="f83f2-149">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="f83f2-150">Einen Arbeitszeitkalender erstellen</span><span class="sxs-lookup"><span data-stu-id="f83f2-150">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="f83f2-151">Urlaub aussetzen</span><span class="sxs-lookup"><span data-stu-id="f83f2-151">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

