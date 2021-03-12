---
title: Konfigurieren Sie die Aufgabenverwaltung
description: In diesem Thema wird beschrieben, wie die Aufgabenverwaltungsfunktionen in Microsoft Dynamics 365 Commerce konfiguriert werden.
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
ms.openlocfilehash: e880305d02fd9f10464fe3f65a2774a44da258c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006234"
---
# <a name="configure-task-management"></a><span data-ttu-id="8b707-103">Konfigurieren der Aufgabenverwaltung</span><span class="sxs-lookup"><span data-stu-id="8b707-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8b707-104">In diesem Thema wird beschrieben, wie die Aufgabenverwaltungsfunktionen in Microsoft Dynamics 365 Commerce konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8b707-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8b707-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8b707-105">Overview</span></span>

<span data-ttu-id="8b707-106">Bevor Dynamics 365 Commerce Manager und Mitarbeiter die Aufgabenverwaltungsfunktionen im Handel nutzen können, muss die Aufgabenverwaltung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8b707-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="8b707-107">Zu den Konfigurationsschritten gehören die Erteilung von Berechtigungen an Manager und Mitarbeiter, die Verteilung von Berechtigungen an POS-Kunden, die Einrichtung von POS-Benachrichtigungen und die Konfiguration der Kachel **Aufgaben** auf der Startseite einer POS-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8b707-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="8b707-108">Konfigurieren von Berechtigungen für Filialleiter</span><span class="sxs-lookup"><span data-stu-id="8b707-108">Configure permissions for store managers</span></span>

<span data-ttu-id="8b707-109">Jeder Mitarbeiter in einem bestimmten Geschäft kann alle Aufgaben, die diesem Geschäft zugeordnet sind, einsehen.</span><span class="sxs-lookup"><span data-stu-id="8b707-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="8b707-110">Er kann auch den Status der ihm zugeordneten Aufgaben aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8b707-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="8b707-111">Personen wie Filialleiter müssen jedoch über Aufgabenmanagementberechtigungen verfügen, um Aufgaben zu verwalten, die der Filiale zugeordnet sind, und um Einzweck-Aufgaben zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b707-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="8b707-112">Führen Sie die folgenden Schritte aus, um Aufgabenverwaltungsberechtigungen für Filialleiter zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8b707-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="8b707-113">Gehen Sie zu **Retail and Commerce \> Mitarbeiter \> Berechtigungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="8b707-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="8b707-114">Wählen Sie eine bestimmte Berechtigungsgruppe (z.B. **Manager**) und wählen Sie dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="8b707-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="8b707-115">Setzen Sie auf der Registerkarte **Berechtigungen** die Option **Aufgabenverwaltung erlauben** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8b707-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="8b707-116">Fügen Sie auf der Registerkarte **Benachrichtigungen** den Vorgang **Aufgabenverwaltung** hinzu und geben Sie einen Wert in das Feld **Anzeigereihenfolge** ein.</span><span class="sxs-lookup"><span data-stu-id="8b707-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="8b707-117">Geben Sie z.B. **2** ein, wenn die Operation **Auftragserfüllung** bereits einen Wert von **Anzeigereihenfolge** von **1** hat.</span><span class="sxs-lookup"><span data-stu-id="8b707-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8b707-118">Wenn eine nicht leitende Person die Berechtigung zur Aufgabenverwaltung in der Kasse haben muss, können Sie der Person die Berechtigung erteilen.</span><span class="sxs-lookup"><span data-stu-id="8b707-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="8b707-119">Alternativ dazu können Sie eine neue Berechtigungsgruppe für Nicht-Manager anlegen und die Option **Aufgabenverwaltung erlauben** auf **Ja** setzen.</span><span class="sxs-lookup"><span data-stu-id="8b707-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="8b707-120">Die folgende Abbildung zeigt, wie Sie Aufgabenverwaltungsberechtigungen für Filialleiter konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="8b707-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Konfigurieren von Aufgabenverwaltungsberechtigungen für Filialleiter](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="8b707-122">Konfigurieren Sie Berechtigungen für Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="8b707-122">Configure permissions for employees</span></span>

<span data-ttu-id="8b707-123">Die Mitarbeiter müssen über Berechtigungen zur Erstellung von Aufgabenlisten, zur Verwaltung von Zuordnungskriterien und zur Konfiguration der Wiederholung von Aufgabenlisten verfügen.</span><span class="sxs-lookup"><span data-stu-id="8b707-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="8b707-124">Um diese Berechtigungen zu konfigurieren, ordnen Sie die Mitarbeiter der Rolle **Aufgabenmanager** zu.</span><span class="sxs-lookup"><span data-stu-id="8b707-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="8b707-125">Um die Berechtigungen für einen Mitarbeiter zu konfigurieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8b707-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="8b707-126">Gehen Sie zu **Retail and Commerce \> Mitarbeiter \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="8b707-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="8b707-127">Wählen Sie einen Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="8b707-127">Select an employee.</span></span>
1. <span data-ttu-id="8b707-128">Wählen Sie auf der Registerkarte **Rollen des Benutzers** **Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="8b707-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="8b707-129">Wählen Sie im Dialogfenster **Rollen zu Benutzer** die Rolle **Retail Task Manager** und dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b707-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="8b707-130">Berechtigungen an POS-Kunden verteilen</span><span class="sxs-lookup"><span data-stu-id="8b707-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="8b707-131">Bevor Mitarbeiter POS-Clients verwenden können, müssen die Berechtigungen an diese Clients verteilt und synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8b707-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="8b707-132">Führen Sie die folgenden Schritte aus, um Berechtigungen an POS-Clients zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="8b707-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="8b707-133">Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="8b707-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="8b707-134">Wählen Sie den Verteilungsplan **1060** (**Mitarbeiter**) und wählen Sie dann **Jetzt ausführen**.</span><span class="sxs-lookup"><span data-stu-id="8b707-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="8b707-135">Wählen Sie den Verteilungsplan **1070** (**Kanalkonfiguration**) und wählen Sie dann **Jetzt ausführen**.</span><span class="sxs-lookup"><span data-stu-id="8b707-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="8b707-136">Konfigurieren Sie POS-Benachrichtigungen für Aufgaben</span><span class="sxs-lookup"><span data-stu-id="8b707-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="8b707-137">Die Aufgabenverwaltung muss so konfiguriert werden, dass Benachrichtigungen in der POS-Anwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8b707-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="8b707-138">Um POS-Benachrichtigungen für Aufgaben zu konfigurieren, führen Sie folgende Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8b707-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="8b707-139">Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellung \> POS-Einrichtung \> POS \> POS-Operationen**.</span><span class="sxs-lookup"><span data-stu-id="8b707-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="8b707-140">Suchen Sie den Vorgang **1400** (**Taskmanagement**) und markieren Sie dafür das Ankreuzfeld **Benachrichtigungen aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="8b707-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="8b707-141">Die folgende Abbildung zeigt die Operation **Aufgabenverwaltung** auf der Seite **POS-Operationen**.</span><span class="sxs-lookup"><span data-stu-id="8b707-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Vorgang der Aufgabenverwaltung auf der Seite POS-Operationen](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="8b707-143">Weitere Informationen über die Konfiguration von POS-Benachrichtigungen finden Sie unter [Bestellbenachrichtigungen in der Verkaufsstelle (POS)](notifications-pos.md) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8b707-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="8b707-144">Konfigurieren Sie die Tasks-Kachel auf der Homepage einer POS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="8b707-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="8b707-145">Bevor Sie die Kachel **Aufgaben** auf der Startseite einer POS-Anwendung konfigurieren, finden Sie unter [Bildschirm-Layouts für die Verkaufsstelle (POS)](pos-screen-layouts.md) Informationen über die Konfiguration und das Hinzufügen neuer Schaltflächen zu einem POS-Bildschirm-Layout.</span><span class="sxs-lookup"><span data-stu-id="8b707-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="8b707-146">Um die Kachel **Aufgaben** auf der Homepage einer POS-Anwendung zu konfigurieren, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="8b707-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="8b707-147">Gehen Sie zu **Retail and Commerce \> Kanal-Einrichtung \> POS-Einrichtung \> POS \> Bildschirm-Layouts**.</span><span class="sxs-lookup"><span data-stu-id="8b707-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="8b707-148">Wählen Sie ein Bildschirmlayout, wählen Sie eine Layoutgröße und wählen Sie ein Schaltflächenraster.</span><span class="sxs-lookup"><span data-stu-id="8b707-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="8b707-149">Wählen Sie auf der Registerkarte **Schaltflächenraster** **Designer**, um das ausgewählte Schaltflächenraster zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8b707-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="8b707-150">Fügen Sie eine **Aufgaben** Kachel zum entsprechenden Abschnitt der Homepage hinzu.</span><span class="sxs-lookup"><span data-stu-id="8b707-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="8b707-151">Die folgende Abbildung zeigt ein Beispiel für eine Kachel **Aufgaben** auf einer POS-Homepage.</span><span class="sxs-lookup"><span data-stu-id="8b707-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Aufgaben-Kachel auf einer POS-Homepage](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="8b707-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8b707-153">Additional resources</span></span>

[<span data-ttu-id="8b707-154">Überblick über die Aufgabenverwaltung</span><span class="sxs-lookup"><span data-stu-id="8b707-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="8b707-155">Aufgabenlisten erstellen und Aufgaben hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8b707-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="8b707-156">Arbeitspläne den Filialen oder Mitarbeitern zuweisen</span><span class="sxs-lookup"><span data-stu-id="8b707-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="8b707-157">Aufgabenverwaltung in POS</span><span class="sxs-lookup"><span data-stu-id="8b707-157">Task management in POS</span></span>](task-mgmt-POS.md)
