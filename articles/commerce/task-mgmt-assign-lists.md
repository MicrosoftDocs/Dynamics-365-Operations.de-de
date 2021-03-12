---
title: Aufgabenlisten zu Filialen oder Mitarbeitern zuordnen
description: In diesem Thema wird beschrieben, wie Sie den Filialen oder Mitarbeitern in Microsoft Dynamics 365 Commerce Aufgabenlisten zuweisen.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ee924f5bf95d47814e7ca09b392a3d10b5e9b9dc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006259"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="930b4-103">Aufgabenlisten zu Filialen oder Mitarbeitern zuordnen</span><span class="sxs-lookup"><span data-stu-id="930b4-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="930b4-104">In diesem Thema wird beschrieben, wie Sie den Filialen oder Mitarbeitern in Microsoft Dynamics 365 Commerce Aufgabenlisten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="930b4-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="930b4-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="930b4-105">Overview</span></span>

<span data-ttu-id="930b4-106">Mit der Aufgabenverwaltung in Dynamics 365 Commerce können Sie eine Aufgabenliste mehreren Filialen oder Mitarbeitern oder einer Kombination aus Filialen und Mitarbeitern zuweisen.</span><span class="sxs-lookup"><span data-stu-id="930b4-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="930b4-107">Beispielsweise könnte ein Regionalmanager für 20 Filialen allen 20 Filialen die Aufgabenliste **Feiertagssaisonvorbereitung** zuweisen wollen.</span><span class="sxs-lookup"><span data-stu-id="930b4-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="930b4-108">Starten Sie den Prozess der Aufgabenlistenzuweisung</span><span class="sxs-lookup"><span data-stu-id="930b4-108">Start the task list assignment process</span></span>

<span data-ttu-id="930b4-109">Um den Prozess der Zuweisung eines Aufgabenplans zu beginnen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="930b4-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="930b4-110">Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltung Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="930b4-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="930b4-111">Wählen Sie die Aufgabenliste, die Sie zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="930b4-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="930b4-112">Wählen Sie **Prozess starten**.</span><span class="sxs-lookup"><span data-stu-id="930b4-112">Select **Start process**.</span></span>
1. <span data-ttu-id="930b4-113">Geben Sie im Dialogfeld **Prozess starten** auf der Registerkarte **Allgemein** im Feld **Prozessname** einen Namen ein (z.B. **Ostliche Region speichert**).</span><span class="sxs-lookup"><span data-stu-id="930b4-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="930b4-114">Geben Sie im Feld **Zieldatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="930b4-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="930b4-115">Um die Aufgabenliste den Filialen zuzuordnen, verwenden Sie auf der Registerkarte **Filialen** den Filter **Organisationshierarchie**, um die Filialen zu finden und auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="930b4-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="930b4-116">Um die Aufgabenliste den Mitarbeitern zuzuordnen, suchen und wählen Sie auf der Registerkarte **Arbeiter** die Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="930b4-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="930b4-117">Wählen Sie **OK**, um den Prozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="930b4-117">Select **OK** to start the process.</span></span> <span data-ttu-id="930b4-118">Die Aufgabenliste wird den ausgewählten Filialen oder Mitarbeitern zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="930b4-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="930b4-119">Die folgende Abbildung zeigt ein Beispiel für die Suche und Auswahl von Filialen im Dialogfenster **Prozess starten**.</span><span class="sxs-lookup"><span data-stu-id="930b4-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Suchen und Auswählen von Filialen im Dialogfeld „Prozess starten“.](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="930b4-121">Aufgabenlisten auf wiederkehrender Basis zuweisen</span><span class="sxs-lookup"><span data-stu-id="930b4-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="930b4-122">Einzelhändler haben manchmal wiederkehrende Aufgaben, wie z.B. „Checkliste für den Donnerstagabschluss“ oder „Checkliste für den ersten Tag des Monats“.</span><span class="sxs-lookup"><span data-stu-id="930b4-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="930b4-123">Daher möchten sie die Aufgabenliste möglicherweise auf einer wiederkehrenden Basis zuweisen.</span><span class="sxs-lookup"><span data-stu-id="930b4-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="930b4-124">Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltung Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="930b4-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="930b4-125">Wählen Sie die Aufgabenliste, die Sie zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="930b4-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="930b4-126">Wählen Sie **Prozess starten**.</span><span class="sxs-lookup"><span data-stu-id="930b4-126">Select **Start process**.</span></span>
1. <span data-ttu-id="930b4-127">Geben Sie im Dialogfenster **Prozess starten** auf der Registerkarte **Allgemein** im Feld **Prozessname** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="930b4-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="930b4-128">Setzen Sie die Option **Wiederholung** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="930b4-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="930b4-129">Geben Sie im Feld **Wiederholungszieldatumverschiebung in Tagen** eine Anzahl von Tagen ein.</span><span class="sxs-lookup"><span data-stu-id="930b4-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="930b4-130">Wenn Sie z.B. **4** eingeben, ist das Zieldatum das Wiederholungsdatum plus vier Tage.</span><span class="sxs-lookup"><span data-stu-id="930b4-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="930b4-131">Wählen Sie auf der Registerkarte **Im Hintergrund ausführen** **Wiederholung**.</span><span class="sxs-lookup"><span data-stu-id="930b4-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="930b4-132">Geben Sie im Dialogfenster **Wiederholung definieren** die Häufigkeitskriterien ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="930b4-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="930b4-133">Die folgende Abbildung zeigt ein Beispiel für die Eingabe von Häufigkeitskriterien im Dialogfenster **Rezidivierung definieren**.</span><span class="sxs-lookup"><span data-stu-id="930b4-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Eingabe von Häufigkeitskriterien im Dialogfenster Rekursion definieren](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="930b4-135">Verfolgen Sie den Status der Aufgabenliste</span><span class="sxs-lookup"><span data-stu-id="930b4-135">Track task list status</span></span>

<span data-ttu-id="930b4-136">Wenn Sie ein Regionalleiter oder Filialleiter sind, möchten Sie vielleicht den Status von Aufgabenlisten verfolgen, die mehreren Filialen oder Mitarbeitern zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="930b4-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="930b4-137">Sie können dann die Filialen oder Mitarbeiter nachverfolgen, die die ihnen zugewiesenen Aufgaben nicht rechtzeitig erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="930b4-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="930b4-138">Im Backoffice des Handels können Sie den Status von Aufgabenlisten anzeigen, Aufgaben neu zuweisen oder den Status einer Aufgabe ändern.</span><span class="sxs-lookup"><span data-stu-id="930b4-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="930b4-139">Um den Aufgabenlistenstatus für alle Aufgaben zu verfolgen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="930b4-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="930b4-140">Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltungsprozesse**.</span><span class="sxs-lookup"><span data-stu-id="930b4-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="930b4-141">Wählen Sie die Registerkarte **Alle Aufgabenlisten**, um den Status aller Aufgabenlisten anzuzeigen, die verschiedenen Geschäften zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="930b4-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="930b4-142">Um den Aufgabenlistenstatus für alle Ihnen zugewiesenen Aufgaben zu verfolgen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="930b4-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="930b4-143">Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltungsprozesse**.</span><span class="sxs-lookup"><span data-stu-id="930b4-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="930b4-144">Wählen Sie die Registerkarte **Meine Aufgaben** oder **Alle Aufgaben**, um den Status der Ihnen zugewiesenen Aufgaben anzuzeigen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="930b4-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="930b4-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="930b4-145">Additional resources</span></span>

[<span data-ttu-id="930b4-146">Übersicht über die Aufgabenverwaltung</span><span class="sxs-lookup"><span data-stu-id="930b4-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="930b4-147">Aufgabenverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="930b4-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="930b4-148">Aufgabenlisten erstellen und Aufgaben hinzufügen</span><span class="sxs-lookup"><span data-stu-id="930b4-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="930b4-149">Aufgabenverwaltung in POS</span><span class="sxs-lookup"><span data-stu-id="930b4-149">Task management in POS</span></span>](task-mgmt-POS.md)
