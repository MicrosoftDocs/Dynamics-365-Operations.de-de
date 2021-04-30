---
title: Leasingbenutzerrollen zuweisen
description: In diesem Thema werden die Sicherheitsrollen beschrieben, die in Anlagenleasing verwendet werden. Außerdem wird erläutert, wie Benutzer diesen Rollen zugewiesen werden.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 05728f5027dc079dd413dde1c3aa78cddcea136b
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881059"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="9c2ce-104">Leasingbenutzerrollen zuweisen</span><span class="sxs-lookup"><span data-stu-id="9c2ce-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c2ce-105">In diesem Thema werden die Sicherheitsrollen beschrieben, die in Anlagenleasing verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="9c2ce-106">Außerdem wird erläutert, wie Benutzer diesen Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="9c2ce-107">Drei Benutzerrollen unterscheiden den Zugriff beim Anlagenleasing.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="9c2ce-108">Eine Rolle ist für die Aufrechterhaltung von Mietverträgen geeignet, eine für die Anzeige von Mietverträgen und eine für die Erfüllung der Aufgaben eines Mietvertragsbearbeiter.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="9c2ce-109">Jede Rolle verfügt über spezifische Berechtigungen für alle Mietvertragsseiten. Mit jeder Rolle können Benutzer Mietverträge entsprechend ihren Aufgaben anzeigen, erstellen, bearbeiten oder löschen.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="9c2ce-110">Rolle</span><span class="sxs-lookup"><span data-stu-id="9c2ce-110">Role</span></span>           | <span data-ttu-id="9c2ce-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c2ce-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="9c2ce-112">Mietvertrag verwalten</span><span class="sxs-lookup"><span data-stu-id="9c2ce-112">Maintain Lease</span></span> | <span data-ttu-id="9c2ce-113">Benutzer in dieser Rolle können Mietverträge hinzufügen, bearbeiten, löschen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="9c2ce-114">Diese Rolle richtet sich an tägliche Benutzer, deren Aufgaben das Erstellen und Buchen monatlicher Journaleinträge sowie das Hinzufügen neuer Mietverträge umfassen.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="9c2ce-115">Diese Rolle ermöglicht den Zugriff auf alle Anlagenleasing-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="9c2ce-116">Mietvertrag anzeigen</span><span class="sxs-lookup"><span data-stu-id="9c2ce-116">View Lease</span></span>     | <span data-ttu-id="9c2ce-117">Benutzer in dieser Rolle können nur Mietvertragsdatensätze und Zeitpläne anzeigen und Berichte ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="9c2ce-118">Sie können keine neuen Mietverträge erstellen, keine vorhandenen Mietverträge bearbeiten und keine Journaleinträge für Mietverträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="9c2ce-119">Die Rolle richtet sich an Benutzer, die nur Mietverträge, Leasingpläne und die Transaktionen anzeigen müssen, die für diese Mietverträge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="9c2ce-120">Mietvertragssachbearbeiter</span><span class="sxs-lookup"><span data-stu-id="9c2ce-120">Lease Clerk</span></span>    | <span data-ttu-id="9c2ce-121">Benutzer in dieser Rolle können nur neue Mietverträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="9c2ce-122">Sie können vorhandene Mietverträge nicht bearbeiten oder löschen, keine Leasingpläne anzeigen oder Leasingjournaleinträge buchen.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="9c2ce-123">Diese Rolle ist für Benutzer gedacht, die mit Dateneingabe arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="9c2ce-124">Führen Sie die folgenden Schritte aus, um Benutzer den Rollen zuzuweisen, die beim Anlagenleasing verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="9c2ce-125">Wechseln Sie zu **Systemverwaltung \> Sicherheit \> Benutzer zu Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="9c2ce-126">Wählen Sie **Mietvertrag verwalten**, **Mietvertragsbearbeiter** oder die **Mietvertrag anzeigen**-Rolle und dann **Benutzer manuell zuweisen/ausschließen**.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="9c2ce-127">Wählen Sie den Benutzer aus, der der Rolle zugewiesen werden soll, und wählen Sie dann **Rolle zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="9c2ce-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
