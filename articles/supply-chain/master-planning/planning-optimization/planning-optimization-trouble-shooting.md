---
title: Fehlerbehebung in Planungsoptimierung
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Planungsoptimierung auftreten können.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812882"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="eb84b-103">Fehlerbehebung in Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="eb84b-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb84b-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit Planungsoptimierung auftreten können.</span><span class="sxs-lookup"><span data-stu-id="eb84b-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="eb84b-105">Die Installation des Planungsoptimierungs-Add-Ins wird nicht abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="eb84b-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="eb84b-106">Die Voraussetzung für die Planungsoptimierung ist eine LCS-fähige (Lifecycle Services) Hochverfügbarkeitsumgebung, Ebene 2 oder höher (keine OneBox-Umgebung) mit Dynamics 365 Supply Chain Management Version 10.0.7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="eb84b-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="eb84b-107">Wenn Sie versuchen, das Add-In in einer OneBox-Umgebung zu installieren, wird die Installation nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="eb84b-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="eb84b-108">**Beheben**: Brechen Sie die Installation ab, und verwenden Sie eine Hochverfügbarkeitsumgebung, Tier 2 oder höher (keine OneBox-Umgebung).</span><span class="sxs-lookup"><span data-stu-id="eb84b-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="eb84b-109">Die Planung von Stapeljobs schlägt fehl, wenn die Planungsoptimierung aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="eb84b-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="eb84b-110">Wenn Sie die Planungsoptimierung aktivieren, wird das integrierte Masterplanungsmodul automatisch deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="eb84b-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="eb84b-111">Planungs-Batchjobs, die für das eingebaute Supply Chain Management-Planungsmodul erstellt wurden, werden fehlschlagen, wenn sie ausgelöst werden, während die Planungsoptimierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="eb84b-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="eb84b-112">Möglicherweise erhalten Sie eine Fehlermeldung wie *Dieser Vorgang löste eine Masterplanung aus, die nicht unterstützt wird, wenn die Planungsoptimierung aktiviert ist*.</span><span class="sxs-lookup"><span data-stu-id="eb84b-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="eb84b-113">**Beheben**: Brechen Sie alle Masterplanungs-Batchjobs ab, die für das integrierte Supply Chain Management-Planungsmodul erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="eb84b-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="eb84b-114">Die Ergebnisse der Planungsoptimierung unterscheiden sich von früheren Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="eb84b-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="eb84b-115">Die Planungsoptimierung unterscheidet sich in einigen Bereichen vom integrierten Masterplanungsdesign.</span><span class="sxs-lookup"><span data-stu-id="eb84b-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="eb84b-116">Dies kann auch durch ausstehende Funktionen verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="eb84b-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="eb84b-117">**Beheben**: Führen Sie die Anpassungsanalyse für die Planungsoptimierung durch, und analysieren Sie dann die Ergebnisse, während Sie die zugehörige Dokumentation lesen, um die Auswirkungen zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="eb84b-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="eb84b-118">Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="eb84b-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="eb84b-119">Die Planungsoptimierung kann nicht aktiviert werden</span><span class="sxs-lookup"><span data-stu-id="eb84b-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="eb84b-120">Der **Verbindungsstatus** muss **Verbunden** sein, bevor Sie **Planungsoptimierung verwenden** auf **Ja** setzen können.</span><span class="sxs-lookup"><span data-stu-id="eb84b-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="eb84b-121">Weitere Informationen finden Sie unter [Erststart mit Planungsoptimierung](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="eb84b-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="eb84b-122">**Beheben**: Stellen Sie sicher, dass das Plannungsoptimierungs-Add-In erfolgreich installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="eb84b-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="eb84b-123">Während der CTP wird eine Fehlermeldung angezeigt</span><span class="sxs-lookup"><span data-stu-id="eb84b-123">Error message is shown during CTP</span></span>

<span data-ttu-id="eb84b-124">Wenn Sie versuchen, CTP (Verfügbarkeitszusage) aus einem Kaufauftrag auszuführen, wenn die Planungsoptimierung aktiviert ist, wird die folgende Fehlermeldung angezeigt: *Dieser Vorgang löste eine Masterplanung aus, die nicht unterstützt wird, wenn die Planungsoptimierung aktiviert ist*.</span><span class="sxs-lookup"><span data-stu-id="eb84b-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="eb84b-125">Dies hängt mit einer ausstehenden Funktion zusammen, die im Rahmen der Unterstützung von Fertigungsaufträgen geplant ist.</span><span class="sxs-lookup"><span data-stu-id="eb84b-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="eb84b-126">**Beheben**: Vermeiden Sie CTP-Berechnungen, wenn die Planungsoptimierung aktiviert ist, bis die CTP-Unterstützung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eb84b-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb84b-127">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="eb84b-127">Additional resources</span></span>

[<span data-ttu-id="eb84b-128">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="eb84b-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="eb84b-129">Passanalyse zu Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="eb84b-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]