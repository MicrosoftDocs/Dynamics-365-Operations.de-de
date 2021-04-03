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
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 18ba781795058de6228c712c6a22e59038e96368
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478361"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="1d362-103">Aufgabenverwaltung in POS</span><span class="sxs-lookup"><span data-stu-id="1d362-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d362-104">Dieses Thema beschreibt die Aufgabenverwaltung in der Microsoft Dynamics 365 Commerce-Point-of-Sale-Anwendung (POS).</span><span class="sxs-lookup"><span data-stu-id="1d362-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="1d362-105">Die POS-Anwendung Dynamics 365 Commerce verfügt über Aufgabenverwaltungsfunktionen, mit denen Filialleiter und Mitarbeiter Aufgaben verwalten und den Aufgabenstatus aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="1d362-105">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="1d362-106">Die Mitarbeiter der Filiale können auf die Aufgaben zugreifen, indem sie entweder die Kachel **Aufgaben** auf der POS-Homepage oder die Aufgabenbenachrichtigungen auswählen.</span><span class="sxs-lookup"><span data-stu-id="1d362-106">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="1d362-107">Standardmäßig werden Filialmitarbeiter zur Registerkarte **Meine Aufgaben** geführt, wo sie die ihnen zugewiesenen Aufgaben einsehen können.</span><span class="sxs-lookup"><span data-stu-id="1d362-107">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="1d362-108">Sie können jedoch problemlos zu den Registern **Überfällige Aufgaben**, **Öffnende Aufgaben** und **Aufgabenlisten** wechseln.</span><span class="sxs-lookup"><span data-stu-id="1d362-108">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="1d362-109">Aufgabenvorgänge für Filialleiter</span><span class="sxs-lookup"><span data-stu-id="1d362-109">Task operations for store managers</span></span>

<span data-ttu-id="1d362-110">Filialleiter können die folgenden Aufgaben in der POS-Anwendung mit Hilfe der Schaltflächen in der Befehlsleiste ausführen:</span><span class="sxs-lookup"><span data-stu-id="1d362-110">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="1d362-111">**Zuweisen** - ausgewählte Aufgaben einem Filialmitarbeiter zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1d362-111">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="1d362-112">**Aufgabenstatus** - Den Status ausgewählter Aufgaben ändern.</span><span class="sxs-lookup"><span data-stu-id="1d362-112">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="1d362-113">**Filter** - Standardmäßig werden nur aktive Aufgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d362-113">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="1d362-114">Durch Anwendung von Filtern können Manager jedoch alle Aufgaben anzeigen, auch solche, die abgeschlossen oder abgebrochen wurden.</span><span class="sxs-lookup"><span data-stu-id="1d362-114">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="1d362-115">**Neue Aufgabe** - Erstellen Sie eine Aufgabe unter einer bestehenden Aufgabenliste oder erstellen Sie eine Einzweck-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1d362-115">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="1d362-116">Die Mitarbeiter der Filiale können die folgenden Aufgabenvorgänge in der POS-Anwendung mit Hilfe der Schaltflächen in der Befehlsleiste ausführen:</span><span class="sxs-lookup"><span data-stu-id="1d362-116">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="1d362-117">**Aufgabenstatus** - Den Status ausgewählter Aufgaben ändern.</span><span class="sxs-lookup"><span data-stu-id="1d362-117">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="1d362-118">**Filter** - Standardmäßig werden nur aktive Aufgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d362-118">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="1d362-119">Durch Anwendung von Filtern können die Mitarbeiter jedoch alle Aufgaben anzeigen, auch solche, die abgeschlossen oder abgebrochen wurden.</span><span class="sxs-lookup"><span data-stu-id="1d362-119">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="1d362-120">Die folgende Abbildung zeigt die Registerkarte **Meine Aufgaben** in der POS-Anwendung Handel.</span><span class="sxs-lookup"><span data-stu-id="1d362-120">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Registerkarte „Meine Aufgaben“ in der Anwendung „Commerce POS“.](media/POS-task-management.png)

<span data-ttu-id="1d362-122">Die folgende Abbildung zeigt die Registerkarte **Aufgabenlisten**.</span><span class="sxs-lookup"><span data-stu-id="1d362-122">The following illustration shows the **Task lists** tab.</span></span>

![Registerkarte Aufgabenlisten in der Anwendung Commerce POS](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="1d362-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1d362-124">Additional resources</span></span>

[<span data-ttu-id="1d362-125">Überblick über die Aufgabenverwaltung</span><span class="sxs-lookup"><span data-stu-id="1d362-125">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="1d362-126">Aufgabenverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="1d362-126">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="1d362-127">Aufgabenlisten erstellen und Aufgaben hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1d362-127">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="1d362-128">Arbeitspläne den Filialen oder Mitarbeitern zuweisen</span><span class="sxs-lookup"><span data-stu-id="1d362-128">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
