---
title: Fehlerbehebung bei der Prozessfertigung
description: Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der Prozessfertigung auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966179"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="9d8a8-103">Fehlersuche in der Prozessfertigung</span><span class="sxs-lookup"><span data-stu-id="9d8a8-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="9d8a8-104">Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der Prozessfertigung auftreten können.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="9d8a8-105">Wenn ich das Jobkartengerät verwende, um eine Teilmenge für den letzten Auftrag in einem Produktionsauftrag zu melden, werden alle vorherigen Aufträge in diesem Auftrag, die den Status „In Bearbeitung“ haben, automatisch beendet.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="9d8a8-106">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-106">This behavior is by design.</span></span> <span data-ttu-id="9d8a8-107">Auf der Seite **Produktionsauftragsvorgaben** gibt es auf der Registerkarte **Als beendet melden** eine Option, die **Arbeitsplan beenden** heißt.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="9d8a8-108">Wenn dieses Thema auf *Ja* festgelegt ist, wird eine Erfassung für den Arbeitsplan erstellt, wenn eine Arbeitskraft das Jobkartengerät oder das Jobkartenterminal verwendet, um den letzten Vorgang zu melden.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="9d8a8-109">Diese Erfassung kennzeichnet alle Vorgänge als abgeschlossen und beendet alle Produktionsaufträge.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="9d8a8-110">Wenn die Option **Arbeitsplan als beendet markieren** auf *Ja* festgelegt ist, berücksichtigt das System nicht den Auftragsstatus, den die Arbeitskraft ausgewählt hat, als sie den letzten Vorgang meldete.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="9d8a8-111">Das System berücksichtigt auch nicht, ob die Arbeitskraft eine volle oder eine Teilmenge meldet.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="9d8a8-112">Wenn ich versuche, einen Lagerabschluss zu machen, erhalte ich die folgende Warnmeldung: „Es wurde keine Ausführung der Nachkalkulation mit einem Datum %1, das mit dem Periodenende übereinstimmt, registriert.“</span><span class="sxs-lookup"><span data-stu-id="9d8a8-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="9d8a8-113">In Versionen vor 10.0.13 erhalten Sie beim Bestandsabschluss die folgende fehlerhafte Warnmeldung, wenn Sie nicht den Lean Production Costing Flow verwenden:</span><span class="sxs-lookup"><span data-stu-id="9d8a8-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="9d8a8-114">Sie sind dabei, einen Bestandsabschluss mit einem Datum %1 auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="9d8a8-115">Es wurde keine Ausführung einer Nachkalkulation mit einem Datum %1 registriert, das dem Periodenende entspricht.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="9d8a8-116">Bitte denken Sie daran, eine Nachkalkulation mit einem Datum %1 auszuführen, das dem Periodenende entspricht.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="9d8a8-117">Die Bewertung der Bestände, der Selbstkosten und der Abweichungen ist möglicherweise im Nebenbuch oder im Hauptbuch nicht korrekt, bis dies ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="9d8a8-118">Dieses Problem wurde in Version 10.0.13 und später behoben.</span><span class="sxs-lookup"><span data-stu-id="9d8a8-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="9d8a8-119">Weitere Informationen finden Sie in [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="9d8a8-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
