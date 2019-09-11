---
title: POS-Berechtigungsgruppen erstellen
description: In diesem Thema wird erläutert, wie Sie eine POS-Berechtigungsgruppe erstellen.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914797"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="64e47-103">POS-Berechtigungsgruppen erstellen</span><span class="sxs-lookup"><span data-stu-id="64e47-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="64e47-104">In diesem Thema wird erläutert, wie Sie eine POS-Berechtigungsgruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="64e47-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="64e47-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USRT.</span><span class="sxs-lookup"><span data-stu-id="64e47-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="64e47-106">Diese Aufgabe ist für die Rolle "Bereichsleiter (Einzelhandel)" vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="64e47-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="64e47-107">Wechseln Sie im Navigationsbereich zu **Module > Einzelhandel > Mitarbeiter > Berechtigungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="64e47-107">In the navigation pane, go to **Modules > Retail > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="64e47-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-108">Select **New**.</span></span>
3. <span data-ttu-id="64e47-109">Geben Sie im Feld **POS-Berechtigungsgruppenkennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="64e47-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="64e47-110">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="64e47-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="64e47-111">Wählen Sie **Ja** im Feld **Zeiterfassungseinträge anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="64e47-112">Sie können verschiedene Berechtigungen für Ihre POS-Berechtigungsgruppe jetzt aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="64e47-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="64e47-113">Bei einigen Berechtigungen können Sie einen Wert festlegen, der verwendet wird, wenn überprüft werden soll, ob der POS-Benutzer die Aktivität ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="64e47-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="64e47-114">Dieses Aufgabenhandbuch ermöglicht einige Berechtigungen, die einem Kassierer zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="64e47-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="64e47-115">Wählen Sie **Ja** im Feld **Auftragserstellung zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="64e47-116">Wählen Sie **Ja** im Feld **Auftragsbearbeitung zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="64e47-117">Wählen Sie **Ja** im Feld **Auftragsabruf zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="64e47-118">Wählen Sie **Ja** im Feld **Kennwortänderung zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="64e47-119">Wählen Sie **Ja** im Feld **Blindschließen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="64e47-120">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="64e47-120">Select **Save**.</span></span> <span data-ttu-id="64e47-121">Nachdem die Änderungen gespeichert sind, müssen Sie den Mitarbeiterverteilungszeitplan ausführen, um die Änderungen an Einzelhandelskanäle zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="64e47-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span> 
12. <span data-ttu-id="64e47-122">Wechseln Sie im Navigationsbereich zu **Module > Personalverwaltung > Einzelvorgänge > Einzelvorgänge**.</span><span class="sxs-lookup"><span data-stu-id="64e47-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="64e47-123">Danach weisen wir die POS-Berechtigungsgruppe einem Einzelvorgang zu.</span><span class="sxs-lookup"><span data-stu-id="64e47-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="64e47-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="64e47-125">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-125">Select **Edit**.</span></span>
15. <span data-ttu-id="64e47-126">Erweitern Sie den Abschnitt **Einzelvorgangsklassifizierung**.</span><span class="sxs-lookup"><span data-stu-id="64e47-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="64e47-127">Geben Sie im Feld "POS-Berechtigungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="64e47-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="64e47-128">Alle Arbeitskräfte in Positionen für diesen Einzelvorgang werden die Einstellungen dieser POS-Berechtigungsgruppe verwenden, es sei denn, die POS-Berechtigungen dieser Arbeitskräfte wurden in ihrer Positionsebene überschrieben.</span><span class="sxs-lookup"><span data-stu-id="64e47-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="64e47-129">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="64e47-129">Select **Save**.</span></span> <span data-ttu-id="64e47-130">Nachdem die Änderungen gespeichert sind, müssen Sie den Mitarbeiterverteilungszeitplan ausführen, um die Änderungen an Einzelhandelskanäle zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="64e47-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

