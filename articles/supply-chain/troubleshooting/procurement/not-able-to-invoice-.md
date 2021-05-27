---
title: Sie können einen Kundenauftrag nicht in Rechnung stellen
description: Sie können den ursprünglichen Kundenauftrag und die ursprüngliche Direktlieferungsbestellung nicht mehr in Rechnung stellen, nachdem Sie die Option „Rechnung automatisch buchen“ aktiviert haben.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026537"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="01ed3-103">Sie können einen Kundenauftrag nicht in Rechnung stellen</span><span class="sxs-lookup"><span data-stu-id="01ed3-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="01ed3-104">KB-Nummer: 4611793</span><span class="sxs-lookup"><span data-stu-id="01ed3-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="01ed3-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="01ed3-105">Symptoms</span></span>

<span data-ttu-id="01ed3-106">Sie können den ursprünglichen Kundenauftrag und die ursprüngliche Direktlieferungsbestellung nicht mehr in Rechnung stellen, nachdem Sie die Option **Rechnung automatisch buchen** auf der Seite **Intercompany** für einen Kreditor aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="01ed3-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="01ed3-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="01ed3-107">Resolution</span></span>

<span data-ttu-id="01ed3-108">Das Synchronisationsverhalten für Intercompany- und Direktlieferungsbestellungs-Rechnungen wird durch die in [Einrichten von Parametern zum Buchen eines Intercompany-Auftrags](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order) beschriebenen Parameter gesteuert und erzwungen.</span><span class="sxs-lookup"><span data-stu-id="01ed3-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="01ed3-109">Nachdem Sie diese Parameter festgelegt haben, müssen Sie zuerst den Intercompany-Auftrag in Rechnung stellen.</span><span class="sxs-lookup"><span data-stu-id="01ed3-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="01ed3-110">Die ursprünglichen Aufträge und Bestellungen werden dann synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="01ed3-110">The original sales orders and purchase orders will then be synchronized.</span></span>
