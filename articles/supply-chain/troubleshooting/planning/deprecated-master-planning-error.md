---
title: Sie erhalten einen Fehler, wenn Sie die integrierte Produktprogrammplanung ausführen
description: Wenn Sie die außer Betrieb genommene integrierte Masterplanungs-Engine ausführen, erhalten Sie eine Fehlermeldung.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294084"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="b9abe-103">Sie erhalten einen Fehler, wenn Sie die integrierte Produktprogrammplanung ausführen</span><span class="sxs-lookup"><span data-stu-id="b9abe-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="b9abe-104">Fehlercode: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="b9abe-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="b9abe-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="b9abe-105">Symptoms</span></span>

<span data-ttu-id="b9abe-106">Wenn Sie die Produktprogrammplanung mit der veralteten, integrierten Masterplan-Engine ausführen, erhalten Sie die folgende Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="b9abe-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="b9abe-107">Sie erhalten diese Fehlermeldung, weil die eingebaute Produktprogrammplanung für Szenarien verwendet wurde, die von der Planungsoptimierung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b9abe-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="b9abe-108">Sie sollten jetzt zur Planungsoptimierung migrieren, da die derzeitige eingebaute Produktprogrammplanung außer Betrieb genommen wird.</span><span class="sxs-lookup"><span data-stu-id="b9abe-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="b9abe-109">Beachten Sie, dass dieser Lauf der Produktprogrammplanung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b9abe-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="b9abe-110">Falls Ihre Migration starke Abhängigkeiten von anstehenden Funktionen hat, kann eine Ausnahme zur weiteren Verwendung der eingebauten Produktprogrammplanung beantragt werden.</span><span class="sxs-lookup"><span data-stu-id="b9abe-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="b9abe-111">Bitte füllen Sie den folgenden Fragebogen aus, um die Migration zur Planungsoptimierung zu starten und ggf. eine Ausnahme zu beantragen.</span><span class="sxs-lookup"><span data-stu-id="b9abe-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="b9abe-112">Fragebogen zur Migration zur Planungsoptimierung und zur Ausnahme</span><span class="sxs-lookup"><span data-stu-id="b9abe-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="b9abe-113">Ursache</span><span class="sxs-lookup"><span data-stu-id="b9abe-113">Cause</span></span>

<span data-ttu-id="b9abe-114">Wenn Sie die Planung ausführen und keine Funktionen zur Produktionssteuerung verwenden, sollten Sie eine Migration auf Planungsoptimierung in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="b9abe-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="b9abe-115">Die eingebaute Masterplanplanung wird außer Betrieb genommen.</span><span class="sxs-lookup"><span data-stu-id="b9abe-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="b9abe-116">Wenn Sie sie also weiterhin verwenden möchten, ohne die Fehlermeldung zu erhalten, müssen Sie eine Ausnahme bei Microsoft beantragen.</span><span class="sxs-lookup"><span data-stu-id="b9abe-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="b9abe-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="b9abe-117">Resolution</span></span>

<span data-ttu-id="b9abe-118">Weitere Informationen zur Migration zur Planungsoptimierung oder zur Beantragung einer Ausnahme, damit Sie stattdessen weiterhin die veraltete integrierte Planungs-Engine verwenden können, finden Sie unter [Migration zur Planungsoptimierung für die Masterplanung](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="b9abe-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
