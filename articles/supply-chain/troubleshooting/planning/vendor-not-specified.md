---
title: Kreditor wird beim Fixieren geplanter Aufträge nicht angegeben
description: Wenn Sie versuchen, geplante Aufträge zu fixieren, erhalten Sie eine Fehlermeldung, die besagt, dass kein Kreditor angegeben ist.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cf41295045211f8a714194494028922d573c9e9e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294080"
---
# <a name="vendor-isnt-specified-when-planned-orders-are-firmed"></a><span data-ttu-id="64ac1-103">Kreditor wird beim Fixieren geplanter Aufträge nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="64ac1-103">Vendor isn't specified when planned orders are firmed</span></span>

<span data-ttu-id="64ac1-104">Fehlercode: SYS23532</span><span class="sxs-lookup"><span data-stu-id="64ac1-104">Error code: SYS23532</span></span>

## <a name="symptoms"></a><span data-ttu-id="64ac1-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="64ac1-105">Symptoms</span></span>

<span data-ttu-id="64ac1-106">Wenn Sie versuchen, geplante Aufträge zu fixieren, erhalten Sie die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="64ac1-106">When you try to firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="64ac1-107">Lieferant ist nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="64ac1-107">Vendor is not specified</span></span>

## <a name="resolution"></a><span data-ttu-id="64ac1-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="64ac1-108">Resolution</span></span>

<span data-ttu-id="64ac1-109">Gehen Sie folgendermaßen vor, um einen Kreditor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="64ac1-109">To specify a vendor, follow these steps.</span></span>

1. <span data-ttu-id="64ac1-110">Öffnen Sie den geplanter Auftrag, in dem ein Kreditor fehlt.</span><span class="sxs-lookup"><span data-stu-id="64ac1-110">Open the planned order that is missing a vendor.</span></span>
1. <span data-ttu-id="64ac1-111">Wählen Sie auf dem Inforegister **Geplanter Vorrat** im Feld **Lieferant** einen Kreditor aus.</span><span class="sxs-lookup"><span data-stu-id="64ac1-111">On the **Planned supply** FastTab, in the **Vendor** field, select a vendor.</span></span>
