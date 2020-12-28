---
title: Aufgabenverwaltung in POS
description: Dieses Thema beschreibt die Aufgabenverwaltung in der Microsoft Dynamics 365 Commerce-Point-of-Sale-Anwendung (POS).
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412627"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="e884c-103">Aufgabenverwaltung in POS</span><span class="sxs-lookup"><span data-stu-id="e884c-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e884c-104">Dieses Thema beschreibt die Aufgabenverwaltung in der Microsoft Dynamics 365 Commerce-Point-of-Sale-Anwendung (POS).</span><span class="sxs-lookup"><span data-stu-id="e884c-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="e884c-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e884c-105">Overview</span></span>

<span data-ttu-id="e884c-106">Die POS-Anwendung Dynamics 365 Commerce verfügt über Aufgabenverwaltungsfunktionen, mit denen Filialleiter und Mitarbeiter Aufgaben verwalten und den Aufgabenstatus aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="e884c-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="e884c-107">Die Mitarbeiter der Filiale können auf die Aufgaben zugreifen, indem sie entweder die Kachel **Aufgaben** auf der POS-Homepage oder die Aufgabenbenachrichtigungen auswählen.</span><span class="sxs-lookup"><span data-stu-id="e884c-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="e884c-108">Standardmäßig werden Filialmitarbeiter zur Registerkarte **Meine Aufgaben** geführt, wo sie die ihnen zugewiesenen Aufgaben einsehen können.</span><span class="sxs-lookup"><span data-stu-id="e884c-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="e884c-109">Sie können jedoch problemlos zu den Registern **Überfällige Aufgaben**, **Öffnende Aufgaben** und **Aufgabenlisten** wechseln.</span><span class="sxs-lookup"><span data-stu-id="e884c-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="e884c-110">Aufgabenvorgänge für Filialleiter</span><span class="sxs-lookup"><span data-stu-id="e884c-110">Task operations for store managers</span></span>

<span data-ttu-id="e884c-111">Filialleiter können die folgenden Aufgaben in der POS-Anwendung mit Hilfe der Schaltflächen in der Befehlsleiste ausführen:</span><span class="sxs-lookup"><span data-stu-id="e884c-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="e884c-112">**Zuweisen** - ausgewählte Aufgaben einem Filialmitarbeiter zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e884c-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="e884c-113">**Aufgabenstatus** - Den Status ausgewählter Aufgaben ändern.</span><span class="sxs-lookup"><span data-stu-id="e884c-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="e884c-114">**Filter** - Standardmäßig werden nur aktive Aufgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e884c-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="e884c-115">Durch Anwendung von Filtern können Manager jedoch alle Aufgaben anzeigen, auch solche, die abgeschlossen oder abgebrochen wurden.</span><span class="sxs-lookup"><span data-stu-id="e884c-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="e884c-116">**Neue Aufgabe** - Erstellen Sie eine Aufgabe unter einer bestehenden Aufgabenliste oder erstellen Sie eine Einzweck-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="e884c-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="e884c-117">Die Mitarbeiter der Filiale können die folgenden Aufgabenvorgänge in der POS-Anwendung mit Hilfe der Schaltflächen in der Befehlsleiste ausführen:</span><span class="sxs-lookup"><span data-stu-id="e884c-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="e884c-118">**Aufgabenstatus** - Den Status ausgewählter Aufgaben ändern.</span><span class="sxs-lookup"><span data-stu-id="e884c-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="e884c-119">**Filter** - Standardmäßig werden nur aktive Aufgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e884c-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="e884c-120">Durch Anwendung von Filtern können die Mitarbeiter jedoch alle Aufgaben anzeigen, auch solche, die abgeschlossen oder abgebrochen wurden.</span><span class="sxs-lookup"><span data-stu-id="e884c-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="e884c-121">Die folgende Abbildung zeigt die Registerkarte **Meine Aufgaben** in der POS-Anwendung Handel.</span><span class="sxs-lookup"><span data-stu-id="e884c-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Registerkarte „Meine Aufgaben“ in der Anwendung „Commerce POS“.](media/POS-task-management.png)

<span data-ttu-id="e884c-123">Die folgende Abbildung zeigt die Registerkarte **Aufgabenlisten**.</span><span class="sxs-lookup"><span data-stu-id="e884c-123">The following illustration shows the **Task lists** tab.</span></span>

![Registerkarte Aufgabenlisten in der Anwendung Commerce POS](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="e884c-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e884c-125">Additional resources</span></span>

[<span data-ttu-id="e884c-126">Überblick über die Aufgabenverwaltung</span><span class="sxs-lookup"><span data-stu-id="e884c-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="e884c-127">Aufgabenverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e884c-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="e884c-128">Aufgabenlisten erstellen und Aufgaben hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e884c-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="e884c-129">Arbeitspläne den Filialen oder Mitarbeitern zuweisen</span><span class="sxs-lookup"><span data-stu-id="e884c-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
