---
title: Fahrt-Status einrichten
description: Dieses Thema beschreibt, wie Sie die Statuswerte einrichten, die Benutzer Fahrten zuweisen können.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 80433c17ed9d790d88b20ecc253c8e4459ffea10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829787"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="08f7d-103">Einrichten des Status einer Fahrt</span><span class="sxs-lookup"><span data-stu-id="08f7d-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08f7d-104">Auf der Seite **Fahrtstatus** legen Sie die Statuswerte fest, die Benutzer den Fahrten zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="08f7d-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="08f7d-105">Benutzer können allen Ebenen einer Fahrt Statuswerte zuweisen: Fahrt, Transportcontainer, Palette, Einkaufsbestellung und Artikel (Einkaufs- und Umlagerungsauftragszeilen).</span><span class="sxs-lookup"><span data-stu-id="08f7d-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="08f7d-106">Sie werden für zwei Zwecke verwendet:</span><span class="sxs-lookup"><span data-stu-id="08f7d-106">They are used for two purposes:</span></span>

- <span data-ttu-id="08f7d-107">Den Benutzer über den Status der Fahrt, des Transportcontainers, der Palette, der Einkaufsbestellung oder des Artikels zu informieren (Einkaufs- und Umlagerungsauftragszeilen).</span><span class="sxs-lookup"><span data-stu-id="08f7d-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="08f7d-108">Begrenzen Sie die Verwendung des Kalkulationsbereichs, indem Sie Änderungen oder Löschungen verhindern.</span><span class="sxs-lookup"><span data-stu-id="08f7d-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="08f7d-109">Um die Status Ihrer Fahrten festzulegen, gehen Sie zu **Gesamttransportkosten \> Einrichten \> Fahrten-Status**.</span><span class="sxs-lookup"><span data-stu-id="08f7d-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="08f7d-110">Dort können Sie mit Hilfe der Schaltflächen im Aktivitätsbereich Status hinzufügen, entfernen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="08f7d-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="08f7d-111">Jeder Kalkulationsbereich hat seinen eigenen Satz und seine eigene Hierarchie von Fahrt-Status.</span><span class="sxs-lookup"><span data-stu-id="08f7d-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="08f7d-112">Daher müssen Sie auf der Seite **Fahrtstatus** im Feld **Kalkulationsbereich** zunächst den Kostenbereich auswählen, für den Sie Fahrtstatus anzeigen oder erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="08f7d-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="08f7d-113">Legen Sie dann für jeden Fahrtstatus die Felder fest, die in der folgenden Tabelle beschrieben sind, je nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="08f7d-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="08f7d-114">Beachten Sie, dass der Status einer Fahrt auch automatisch durch Systemereignisse geändert werden kann, z.B. durch Regeln, die mit Hilfe des Tracking-Control-Centers festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="08f7d-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="08f7d-115">Feld</span><span class="sxs-lookup"><span data-stu-id="08f7d-115">Field</span></span> | <span data-ttu-id="08f7d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08f7d-116">Description</span></span> |
|---|---|
| <span data-ttu-id="08f7d-117">Seereisestatus</span><span class="sxs-lookup"><span data-stu-id="08f7d-117">Voyage status</span></span> | <span data-ttu-id="08f7d-118">Geben Sie den Namen des Status der Fahrt ein.</span><span class="sxs-lookup"><span data-stu-id="08f7d-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="08f7d-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08f7d-119">Description</span></span> | <span data-ttu-id="08f7d-120">Geben Sie eine Beschreibung für den Status der Fahrt ein.</span><span class="sxs-lookup"><span data-stu-id="08f7d-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="08f7d-121">Änderung</span><span class="sxs-lookup"><span data-stu-id="08f7d-121">Modify</span></span> | <span data-ttu-id="08f7d-122">Aktivieren Sie dieses Kontrollkästchen, wenn Benutzer Fahrten, die diesen Status haben, ändern dürfen.</span><span class="sxs-lookup"><span data-stu-id="08f7d-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="08f7d-123">Löschen</span><span class="sxs-lookup"><span data-stu-id="08f7d-123">Delete</span></span> | <span data-ttu-id="08f7d-124">Aktivieren Sie dieses Kontrollkästchen, wenn Benutzer Fahrten, die diesen Status haben, löschen dürfen.</span><span class="sxs-lookup"><span data-stu-id="08f7d-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="08f7d-125">Obligatorisch</span><span class="sxs-lookup"><span data-stu-id="08f7d-125">Mandatory</span></span> | <span data-ttu-id="08f7d-126">Aktivieren Sie dieses Kontrollkästchen, um den Status der Fahrt obligatorisch zu machen, so dass er nicht übersprungen werden kann.</span><span class="sxs-lookup"><span data-stu-id="08f7d-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="08f7d-127">Übergeordnet</span><span class="sxs-lookup"><span data-stu-id="08f7d-127">Parent</span></span> | <span data-ttu-id="08f7d-128">Verwenden Sie dieses Feld, um eine Hierarchie zwischen den Statuswerten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08f7d-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="08f7d-129">Fahrt-Statuswerte können (entweder manuell oder automatisch) nur abwärts in der Hierarchie geändert werden, von einem übergeordneten Status zu einem seiner untergeordneten Statuswerte.</span><span class="sxs-lookup"><span data-stu-id="08f7d-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="08f7d-130">Sie müssen nur die spezifischen Fahrt-Status festlegen, die Ihre Organisation verwendet.</span><span class="sxs-lookup"><span data-stu-id="08f7d-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="08f7d-131">Typische Fahrtstatus sind *Bestätigt*, *Waren in Zustellung*, *Eingegangen*, *Bereit zur Kalkulation* und *Kalkuliert*.</span><span class="sxs-lookup"><span data-stu-id="08f7d-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="08f7d-132">Es können aber auch andere Zustände vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="08f7d-132">However, other statuses might be present.</span></span>
