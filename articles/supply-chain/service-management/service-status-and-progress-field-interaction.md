---
title: Interaktion zwischen Servicestatus und Statusfeld
description: Im Formular "Serviceauftärge wird im Feld "Fortschritt" im Serviceauftragskopf der Status des gesamten Serviceauftrags angezeigt, und unter "Statusberichte" wird der Status der einzelnen Serviceauftragspositionen angegeben.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a94f2df6a4ddb71a29ff951dfe38618ac7762783
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428394"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="50934-103">Interaktion zwischen Servicestatus und Statusfeld</span><span class="sxs-lookup"><span data-stu-id="50934-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="50934-104">Im Formular "**Serviceauftärge** wird im Feld "**Fortschritt**" im Serviceauftragskopf der Status des gesamten Serviceauftrags angezeigt, und unter "**Statusberichte**" wird der Status der einzelnen Serviceauftragspositionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="50934-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50934-105">Status</span><span class="sxs-lookup"><span data-stu-id="50934-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="50934-106">Position 1 Status</span><span class="sxs-lookup"><span data-stu-id="50934-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="50934-107">Position 2 Status</span><span class="sxs-lookup"><span data-stu-id="50934-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="50934-108">Position 3 Status</span><span class="sxs-lookup"><span data-stu-id="50934-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50934-109"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="50934-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-110"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="50934-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-111"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="50934-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-112"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="50934-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50934-113"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="50934-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-114"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="50934-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-115"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="50934-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-116"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="50934-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50934-117"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="50934-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-118"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="50934-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-119"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="50934-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-120"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="50934-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50934-121"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="50934-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-122"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="50934-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-123"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="50934-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-124"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="50934-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50934-125"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="50934-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-126"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="50934-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-127"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="50934-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-128"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="50934-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50934-129"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="50934-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-130"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="50934-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-131"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="50934-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="50934-132"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="50934-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="50934-133">Der Fortschritt eines Serviceauftrags vollzieht sich, wenn alle Positionen den Status **Erstellt** besitzen. Er ist nach wie vor aktiv, wenn einige der Positionen den Status **Storniert** oder **Gebucht** besitzen.</span><span class="sxs-lookup"><span data-stu-id="50934-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="50934-134">Werden alle Positionen in einem Serviceauftrag als **Gebucht** markiert, lautet der Fortschritt des Statusauftrags **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="50934-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="50934-135">Gilt für einige Positionen der Status **Gebucht** und für andere **Storniert**, gilt für den Fortschritt nach wie vor der Status **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="50934-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


