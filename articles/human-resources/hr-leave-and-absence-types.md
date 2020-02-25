---
title: Urlaubs- und Abwesenheitstypen konfigurieren
description: Einrichten von Abwesenheitstypen, die Mitarbeiter in Anspruch nehmen können in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009186"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="d7b12-103">Urlaubs- und Abwesenheitstypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d7b12-103">Configure leave and absence types</span></span>

<span data-ttu-id="d7b12-104">Abwesenheitstypen in Dynamics 365 Human Resources definieren die verschiedenen Arten von Abwesenheitszeiten, die Mitarbeiter melden können.</span><span class="sxs-lookup"><span data-stu-id="d7b12-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="d7b12-105">Sie können die Abwesenheitstypen an die Bedürfnisse Ihrer Organisation anpassen.</span><span class="sxs-lookup"><span data-stu-id="d7b12-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="d7b12-106">Beispiele für Abwesenheitstypen sind:</span><span class="sxs-lookup"><span data-stu-id="d7b12-106">Examples of leave types include:</span></span>

- <span data-ttu-id="d7b12-107">Entlohnte Zeit (PTO)</span><span class="sxs-lookup"><span data-stu-id="d7b12-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="d7b12-108">Unbezahlter Sonderurlaub</span><span class="sxs-lookup"><span data-stu-id="d7b12-108">Unpaid leave</span></span>
- <span data-ttu-id="d7b12-109">Bezahlter Urlaub</span><span class="sxs-lookup"><span data-stu-id="d7b12-109">Paid vacation</span></span>
- <span data-ttu-id="d7b12-110">Krankheitsbedingte Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="d7b12-110">Sick leave</span></span>
- <span data-ttu-id="d7b12-111">Medizinischer Urlaub</span><span class="sxs-lookup"><span data-stu-id="d7b12-111">Medical leave</span></span>
- <span data-ttu-id="d7b12-112">Familienurlaub</span><span class="sxs-lookup"><span data-stu-id="d7b12-112">Family leave</span></span>
- <span data-ttu-id="d7b12-113">Kurzfristige Behinderung</span><span class="sxs-lookup"><span data-stu-id="d7b12-113">Short-term disability</span></span>
- <span data-ttu-id="d7b12-114">Trauerurlaub</span><span class="sxs-lookup"><span data-stu-id="d7b12-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="d7b12-115">Fügen Sie einen Abwesenehitstyp hinzu</span><span class="sxs-lookup"><span data-stu-id="d7b12-115">Add a leave type</span></span>

1. <span data-ttu-id="d7b12-116">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="d7b12-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="d7b12-117">Unter **Installieren**, wählen Sie **Urlaubs- und Abwesenheitstypen**.</span><span class="sxs-lookup"><span data-stu-id="d7b12-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="d7b12-118">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d7b12-118">Select **New**.</span></span>

4. <span data-ttu-id="d7b12-119">Geben Sie einen Namen für den Abwesenheitstyp ein unter **Typ** wählen Sie einen Workflow aus unter **Workflow-ID** und geben Sie eine Beschreibung ein unter **Beschreibung**.</span><span class="sxs-lookup"><span data-stu-id="d7b12-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="d7b12-120">Unter **Allgemein**, wählen Sie **Keine**, **Geplant**, oder **Nicht geplant** aus der Dropdown-Liste **Kategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="d7b12-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="d7b12-121">Wählen Sie einen Einkommenscode aus der **Einkommenscode** Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="d7b12-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="d7b12-122">Unter **Ursachencode erforderlich** wählen Sie, ob Sie einen Ursachencode benötigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7b12-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="d7b12-123">Wenn Sie Ursachencodes benötigen, müssen Sie diese möglicherweise hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7b12-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="d7b12-124">Unter **Ursachencodes** wählen Sie **Hinzufügen**, wählen Sie einen Ursachencode und dann das Kontrollkästchen **aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="d7b12-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="d7b12-125">Unter **Beschränken Sie den Zugriff auf ausgewählte Rollen** wählen Sie, ob Sie den Zugriff einschränken möchten.</span><span class="sxs-lookup"><span data-stu-id="d7b12-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="d7b12-126">Wählen Sie dann die Sicherheitsrollen unter **Sicherheitsrollen für diesen Urlaubstyp**.</span><span class="sxs-lookup"><span data-stu-id="d7b12-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="d7b12-127">Die Sicherheitsrollen werden in dem Workflow definiert, den Sie unter **Workflow-ID** früher in diesem Verfahren ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d7b12-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="d7b12-128">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d7b12-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="d7b12-129">Vorschaufunktionen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d7b12-129">Configure preview features</span></span>

<span data-ttu-id="d7b12-130">Wenn Sie die Vorschaufunktionen für Urlaub und Abwesenheit aktiviert haben, müssen Sie auch die Einstellungen für sie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d7b12-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="d7b12-131">Stellen Sie Rundungsoptionen für die Urlaubsart ein.</span><span class="sxs-lookup"><span data-stu-id="d7b12-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="d7b12-132">Optionen umfassen **Keine**, **Oben**, **Unten**, und **Nächste**.</span><span class="sxs-lookup"><span data-stu-id="d7b12-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="d7b12-133">Sie können auch die Rundungsgenauigkeit für den Urlaubstyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="d7b12-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="d7b12-134">Stellen **Urlaubskorrekturen** für den Abwesenheitstyp ein.</span><span class="sxs-lookup"><span data-stu-id="d7b12-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="d7b12-135">Wenn Sie diese Option auswählen, verwendet die Personalabteilung die Anzahl der Feiertage, die auf einen Arbeitstag fallen, um zu bestimmen, wie Freizeit für die Urlaubsart angesammelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7b12-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="d7b12-136">Wenn beispielsweise der Weihnachtstag auf einen Montag fällt, zieht die Personalabteilung bei der Verarbeitung von Rückstellungen einen Tag von der Urlaubsart ab.</span><span class="sxs-lookup"><span data-stu-id="d7b12-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="d7b12-137">Sie legen den Urlaub im Arbeitszeitkalender fest.</span><span class="sxs-lookup"><span data-stu-id="d7b12-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="d7b12-138">Weitere Informationen finden Sie unter [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="d7b12-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="d7b12-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7b12-139">See also</span></span>

- [<span data-ttu-id="d7b12-140">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="d7b12-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="d7b12-141">Einen Urlaubs- und Abwesenheitsplan erstellen</span><span class="sxs-lookup"><span data-stu-id="d7b12-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="d7b12-142">Einen Arbeitszeitkalender erstellen</span><span class="sxs-lookup"><span data-stu-id="d7b12-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)