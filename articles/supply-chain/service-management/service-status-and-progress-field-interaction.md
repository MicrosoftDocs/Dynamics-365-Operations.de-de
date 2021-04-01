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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66871d07bdfd949e29a704f53b3e5698d996c2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254214"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="80022-103">Interaktion zwischen Servicestatus und Statusfeld</span><span class="sxs-lookup"><span data-stu-id="80022-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="80022-104">Im Formular "**Serviceauftärge** wird im Feld "**Fortschritt**" im Serviceauftragskopf der Status des gesamten Serviceauftrags angezeigt, und unter "**Statusberichte**" wird der Status der einzelnen Serviceauftragspositionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="80022-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80022-105">Status</span><span class="sxs-lookup"><span data-stu-id="80022-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="80022-106">Position 1 Status</span><span class="sxs-lookup"><span data-stu-id="80022-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="80022-107">Position 2 Status</span><span class="sxs-lookup"><span data-stu-id="80022-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="80022-108">Position 3 Status</span><span class="sxs-lookup"><span data-stu-id="80022-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80022-109"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="80022-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-110"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="80022-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-111"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="80022-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-112"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="80022-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80022-113"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="80022-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-114"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="80022-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-115"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="80022-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-116"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="80022-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80022-117"><strong>In Bearbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="80022-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-118"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="80022-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-119"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="80022-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-120"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="80022-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80022-121"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="80022-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-122"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="80022-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-123"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="80022-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-124"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="80022-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80022-125"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="80022-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-126"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="80022-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-127"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="80022-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-128"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="80022-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80022-129"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="80022-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-130"><strong>Gebucht</strong></span><span class="sxs-lookup"><span data-stu-id="80022-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-131"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="80022-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="80022-132"><strong>Storniert</strong></span><span class="sxs-lookup"><span data-stu-id="80022-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80022-133">Der Fortschritt eines Serviceauftrags vollzieht sich, wenn alle Positionen den Status **Erstellt** besitzen. Er ist nach wie vor aktiv, wenn einige der Positionen den Status **Storniert** oder **Gebucht** besitzen.</span><span class="sxs-lookup"><span data-stu-id="80022-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="80022-134">Werden alle Positionen in einem Serviceauftrag als **Gebucht** markiert, lautet der Fortschritt des Statusauftrags **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="80022-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="80022-135">Gilt für einige Positionen der Status **Gebucht** und für andere **Storniert**, gilt für den Fortschritt nach wie vor der Status **Gebucht**.</span><span class="sxs-lookup"><span data-stu-id="80022-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]