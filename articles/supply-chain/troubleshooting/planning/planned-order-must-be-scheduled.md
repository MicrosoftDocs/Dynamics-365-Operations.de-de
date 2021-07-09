---
title: Geplanter Produktionsauftrag muss eingeplant werden, bevor er fixiert werden kann
description: Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie eine Fehlermeldung, die besagt, dass der Auftrag eingeplant werden muss, bevor er fixiert werden kann.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294087"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="1b586-103">Geplanter Produktionsauftrag muss eingeplant werden, bevor er fixiert werden kann</span><span class="sxs-lookup"><span data-stu-id="1b586-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="1b586-104">Fehlercode: SYS309802</span><span class="sxs-lookup"><span data-stu-id="1b586-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="1b586-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="1b586-105">Symptoms</span></span>

<span data-ttu-id="1b586-106">Wenn Sie versuchen, einen geplanten Auftrag zu fixieren, erhalten Sie die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="1b586-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="1b586-107">Der geplante Produktionsauftrag muss geplant werden, bevor er umgewandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b586-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="1b586-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="1b586-108">Cause</span></span>

<span data-ttu-id="1b586-109">Die geplanten Start- und Endtermine können nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="1b586-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="1b586-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="1b586-110">Resolution</span></span>

<span data-ttu-id="1b586-111">Gehen Sie folgendermaßen vor, um Start- und Endtermine für den geplanten Auftrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1b586-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="1b586-112">Gehen Sie zu **Produktprogrammplanung \> Gesamtplanung \> Geplante Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="1b586-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="1b586-113">Öffnen Sie den betreffenden geplanten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="1b586-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="1b586-114">Geben Sie auf dem Inforegister **Allgemein** im Abschnitt **Terminiert** die Daten in den Feldern **Startdatum** und **Enddatum** an.</span><span class="sxs-lookup"><span data-stu-id="1b586-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
