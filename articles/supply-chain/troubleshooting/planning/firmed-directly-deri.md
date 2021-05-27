---
title: Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit laufender Überprüfung verarbeitet
description: Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit dem Status „Wird überprüft“ verarbeitet.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026549"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="b4e04-103">Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit laufender Überprüfung verarbeitet</span><span class="sxs-lookup"><span data-stu-id="b4e04-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="b4e04-104">KB-Nummer: 4612450</span><span class="sxs-lookup"><span data-stu-id="b4e04-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="b4e04-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="b4e04-105">Symptoms</span></span>

<span data-ttu-id="b4e04-106">Direkt abgeleitete umgewandelte Aufträge werden von einem Workflow mit dem Status *Wird überprüft* verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b4e04-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="b4e04-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="b4e04-107">Resolution</span></span>

<span data-ttu-id="b4e04-108">Wenn die Änderungsnachverfolgung aktiviert ist, wird abgeleiteten umgewandelten Aufträgen (Unterauftragsbestellung) den Status *Wird überprüft*.</span><span class="sxs-lookup"><span data-stu-id="b4e04-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="b4e04-109">Wenn eine Bestellung abgeleitet wird (eine Unterauftragsbestellung), wird sie daher nur an einen Workflow gesendet.</span><span class="sxs-lookup"><span data-stu-id="b4e04-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="b4e04-110">Wenn es sich bei einer Bestellung um eine umgewandelte geplante Einkaufsbestellung handelt, wird diese automatisch genehmigt, um sicherzustellen, dass die Planungs-Engine keine neuen geplanten Bestellungen erstellt, während die Bestellung den Status *Entwurf* hat.</span><span class="sxs-lookup"><span data-stu-id="b4e04-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
