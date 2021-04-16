---
title: Interaktion zwischen Servicestatus und Statusfeld
description: Im Formular "Serviceauftärge wird im Feld "Fortschritt" im Serviceauftragskopf der Status des gesamten Serviceauftrags angezeigt, und unter "Statusberichte" wird der Status der einzelnen Serviceauftragspositionen angegeben.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a767f4fddb79e720e5466791e984025de16a932a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824461"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="d42f5-103">Interaktion zwischen Servicestatus und Statusfeld</span><span class="sxs-lookup"><span data-stu-id="d42f5-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d42f5-104">Im Formular "**Serviceauftärge** wird im Feld "**Fortschritt**" im Serviceauftragskopf der Status des gesamten Serviceauftrags angezeigt, und unter "**Statusberichte**" wird der Status der einzelnen Serviceauftragspositionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="d42f5-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d42f5-105">Status</span><span class="sxs-lookup"><span data-stu-id="d42f5-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="d42f5-106">Position 1 Status</span><span class="sxs-lookup"><span data-stu-id="d42f5-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="d42f5-107">Position 2 Status</span><span class="sxs-lookup"><span data-stu-id="d42f5-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="d42f5-108">Position 3 Status</span><span class="sxs-lookup"><span data-stu-id="d42f5-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d42f5-109"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-110"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-111"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-112"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d42f5-113"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-114"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-115"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-116"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d42f5-117"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-118"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-119"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-120"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d42f5-121"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-122"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-123"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-124"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d42f5-125"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-126"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-127"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-128"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d42f5-129"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-130"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-131"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="d42f5-132"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="d42f5-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d42f5-133">Der Fortschritt eines Serviceauftrags vollzieht sich, wenn alle Positionen den Status **Erstellt** besitzen. Er ist nach wie vor aktiv, wenn einige der Positionen den Status **Storniert** oder **Gebucht** besitzen.</span><span class="sxs-lookup"><span data-stu-id="d42f5-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="d42f5-134">Werden alle Positionen in einem Serviceauftrag als **Gebucht** markiert, lautet der Fortschritt des Statusauftrags **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="d42f5-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="d42f5-135">Gilt für einige Positionen der Status **Gebucht** und für andere **Storniert**, gilt für den Fortschritt nach wie vor der Status **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="d42f5-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]