---
title: Aufgabenlisten erstellen und Aufgaben hinzufügen
description: Dieses Thema beschreibt, wie Sie Aufgabenlisten erstellen und Aufgaben in Microsoft Dynamics 365 Commerce hinzufügen können.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cca5e0efd6516d02c372e8a616b6bb0c39f3088c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006209"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="afecd-103">Aufgabenlisten erstellen und Aufgaben hinzufügen</span><span class="sxs-lookup"><span data-stu-id="afecd-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="afecd-104">Dieses Thema beschreibt, wie Sie Aufgabenlisten erstellen und Aufgaben in Microsoft Dynamics 365 Commerce hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="afecd-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="afecd-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="afecd-105">Overview</span></span>

<span data-ttu-id="afecd-106">Eine *Aufgabe* definiert eine bestimmte Arbeit oder eine Aktion, die jemand an oder vor einem bestimmten Fälligkeitsdatum erledigen muss.</span><span class="sxs-lookup"><span data-stu-id="afecd-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="afecd-107">In Dynamics 365 Commerce kann eine Aufgabe detaillierte Anweisungen und Informationen über eine Kontaktperson enthalten.</span><span class="sxs-lookup"><span data-stu-id="afecd-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="afecd-108">Sie kann auch Links zu Back-Office-Vorgängen, POS-Vorgängen oder Seiten der Website enthalten, um die Produktivität zu verbessern und den Kontext zu schaffen, den der Aufgabeninhaber zur effizienten Erledigung der Aufgabe benötigt.</span><span class="sxs-lookup"><span data-stu-id="afecd-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="afecd-109">Eine *Aufgabenliste* ist eine Sammlung von Aufgaben, die als Teil eines Geschäftsprozesses erledigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="afecd-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="afecd-110">Zum Beispiel könnte es eine Aufgabenliste geben, die ein neuer Mitarbeiter während der Einarbeitung erledigen muss, eine Aufgabenliste für Kassierer, die in Abendschichten arbeiten, oder eine Aufgabenliste, die zur Vorbereitung des Geschäfts auf eine bevorstehende Urlaubssaison erledigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="afecd-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="afecd-111">Im Handel kann jede Aufgabenliste, die ein Zieldatum hat, einer beliebigen Anzahl von Filialen oder Mitarbeitern zugeordnet werden, und sie kann so konfiguriert werden, dass sie sich wiederholt.</span><span class="sxs-lookup"><span data-stu-id="afecd-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="afecd-112">Sowohl Manager als auch Mitarbeiter können im Backoffice des Bereichs Handel Aufgabenlisten erstellen und sie dann einer Reihe von Filialen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="afecd-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="afecd-113">Erstellen Sie eine Aufgabenliste</span><span class="sxs-lookup"><span data-stu-id="afecd-113">Create a task list</span></span>

<span data-ttu-id="afecd-114">Um einen Aufgabenplan zu erstellen, führen Sie folgende Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="afecd-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="afecd-115">Gehen Sie zu **Retail and Commerce \> Aufgabenverwaltung \> Aufgabenverwaltung Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="afecd-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="afecd-116">Wählen Sie **Neu**, und geben Sie dann Werte in die Felder **Name**, **Beschreibung** und **Besitzer** ein.</span><span class="sxs-lookup"><span data-stu-id="afecd-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="afecd-117">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="afecd-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="afecd-118">Aufgaben zu einer Aufgabenliste hinzufügen</span><span class="sxs-lookup"><span data-stu-id="afecd-118">Add tasks to a task list</span></span>

<span data-ttu-id="afecd-119">Um einer Aufgabenliste Aufgaben hinzuzufügen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="afecd-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="afecd-120">Wählen Sie auf der Registerkarte **Aufgaben** einer bestehenden Aufgabenliste **Neu**, um eine Aufgabe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="afecd-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="afecd-121">Geben Sie im Dialogfeld **Neue Aufgabe erstellen** im Feld **Name** einen Namen für die Aufgabe ein.</span><span class="sxs-lookup"><span data-stu-id="afecd-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="afecd-122">Geben Sie in das Feld **Datenversatz vom Zieldatum** einen positiven oder negativen ganzzahligen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="afecd-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="afecd-123">Geben Sie z.B. **-2** ein, wenn die Aufgabe zwei Tage vor dem Fälligkeitsdatum der Aufgabenliste abgeschlossen sein soll.</span><span class="sxs-lookup"><span data-stu-id="afecd-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="afecd-124">Geben Sie in das Feld **Hinweise** detaillierte Anweisungen ein.</span><span class="sxs-lookup"><span data-stu-id="afecd-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="afecd-125">Geben Sie in das Feld **Ansprechpartner** den Namen eines Fachexperten ein, an den sich der Aufgabeninhaber wenden kann, wenn er Hilfe benötigt.</span><span class="sxs-lookup"><span data-stu-id="afecd-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="afecd-126">Geben Sie im Feld **Aufgabenverknüpfung** eine Verknüpfung ein, die auf der Art der Aufgabe basiert.</span><span class="sxs-lookup"><span data-stu-id="afecd-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="afecd-127">Obwohl Sie das Feld **Zugeordnet zu** verwenden können, um jemandem Aufgaben zuzuweisen, während Sie eine Aufgabenliste erstellen, empfehlen wir Ihnen, die Zuweisung von Aufgaben während der Erstellung der Aufgabenliste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="afecd-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="afecd-128">Ordnen Sie stattdessen die Aufgaben nach der Instanziierung der Liste für einzelne Filialen zu.</span><span class="sxs-lookup"><span data-stu-id="afecd-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="afecd-129">Verwenden Sie Aufgabenverknüpfungen, um die Produktivität der Mitarbeiter zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="afecd-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="afecd-130">Im Bereich Handel können Sie Aufgaben mit bestimmten POS-Operationen verknüpfen, z. B. die Ausführung eines Verkaufsberichts, die Anzeige eines Online-Schulungsvideos zur Orientierung neuer Mitarbeiter oder die Durchführung einer Back-Office-Operation.</span><span class="sxs-lookup"><span data-stu-id="afecd-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="afecd-131">Diese Funktion hilft den Aufgabeninhabern, die Informationen zu erhalten, die sie zur effizienten Erledigung einer Aufgabe benötigen.</span><span class="sxs-lookup"><span data-stu-id="afecd-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="afecd-132">Um Aufgabenverknüpfungen während der Erstellung einer Aufgabe hinzuzufügen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="afecd-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="afecd-133">Wählen Sie auf der Registerkarte **Aufgaben** einer vorhandenen Aufgabenliste **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="afecd-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="afecd-134">Wählen Sie im Dialogfeld **Aufgabe bearbeiten** im Feld **Aufgabenverknüpfung** eine oder mehrere der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="afecd-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="afecd-135">Wählen Sie **Menüpunkt**, um einen Back-Office-Vorgang zu konfigurieren, z.B. „Produkt-Kits“.</span><span class="sxs-lookup"><span data-stu-id="afecd-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="afecd-136">Wählen Sie **POS-Operation**, um eine POS-Operation zu konfigurieren, wie z.B. „Verkaufsberichte“.</span><span class="sxs-lookup"><span data-stu-id="afecd-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="afecd-137">Wählen Sie **URL**, um eine absolute URL zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="afecd-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="afecd-138">Die folgende Abbildung zeigt die Auswahl der Aufgabenverknüpfungen im Dialogfenster **Aufgabe bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="afecd-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Auswahl der Aufgabenverknüpfungen im Dialogfeld „Aufgabe bearbeiten“.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="afecd-140">Konfigurieren Sie eine POS-Operation so, dass sie mit einer Aufgabe verknüpft werden kann</span><span class="sxs-lookup"><span data-stu-id="afecd-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="afecd-141">Um einen POS-Vorgang so zu konfigurieren, dass er mit einer Aufgabe verknüpft werden kann, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="afecd-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="afecd-142">Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellung \> POS-Einrichtung \> POS \> POS-Operationen**.</span><span class="sxs-lookup"><span data-stu-id="afecd-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="afecd-143">Wählen Sie **Bearbeiten**, suchen Sie die POS-Operation und markieren Sie dann das Kontrollkästchen **Aufgabenverwaltung aktivieren** für diese Operation.</span><span class="sxs-lookup"><span data-stu-id="afecd-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="afecd-144">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="afecd-144">Additional resources</span></span>

[<span data-ttu-id="afecd-145">Übersicht über die Aufgabenverwaltung</span><span class="sxs-lookup"><span data-stu-id="afecd-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="afecd-146">Aufgabenverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="afecd-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="afecd-147">Arbeitspläne den Filialen oder Mitarbeitern zuweisen</span><span class="sxs-lookup"><span data-stu-id="afecd-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="afecd-148">Aufgabenverwaltung in POS</span><span class="sxs-lookup"><span data-stu-id="afecd-148">Task management in POS</span></span>](task-mgmt-POS.md)
