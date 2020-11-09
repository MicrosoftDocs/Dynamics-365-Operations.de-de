---
title: Ein Experiment ausführen und überwachen
description: In diesem Thema wird beschrieben, wie Sie ein Experiment in einem Drittanbieterdienst ausführen und überwachen. Außerdem wird beschrieben, wie Sie nach Beginn des Experiments Änderungen an Variationen vornehmen.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ee86a6761b27f3c08a65a2e250659cdcfd71db44
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097021"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="f6073-104">Ein Experiment ausführen und überwachen</span><span class="sxs-lookup"><span data-stu-id="f6073-104">Run and monitor an experiment</span></span>

<span data-ttu-id="f6073-105">In diesem Thema wird beschrieben, wie Sie Ihr Experiment in einer Drittanbieter-App ausführen und überwachen und bei Bedarf Variationen ändern.</span><span class="sxs-lookup"><span data-stu-id="f6073-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="f6073-106">Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie zuerst Ihr Experiment in Commerce [veröffentlichen](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="f6073-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="f6073-107">Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="f6073-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f6073-108">Weitere Schritte werden in separaten Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="f6073-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="f6073-109">[ ![User Journey zum Experimentieren – Ausführung und Überwachung](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f6073-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="f6073-110">Nachdem Sie Ihre Variationen veröffentlicht haben, werden alle Schritte ausgeführt, die Sie in Commerce ausführen müssen, um Ihr Experiment abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f6073-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="f6073-111">Der nächste Schritt besteht darin, zu bestimmen, welche Variation jedem Benutzer angezeigt werden soll, wenn er eine Seite anfordert.</span><span class="sxs-lookup"><span data-stu-id="f6073-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="f6073-112">Der Drittanbieterdienst trifft diese Entscheidung, aber zuerst müssen Sie das Experiment innerhalb des Dienstes aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f6073-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="f6073-113">Da die Schritte zum Aktivieren eines Experiments von Dienst zu Dienst unterschiedlich sind, müssen Sie die Anweisungen Ihres Dienstes oder Anbieters befolgen.</span><span class="sxs-lookup"><span data-stu-id="f6073-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="f6073-114">Wenn das Experiment nicht aktiviert ist, wird den Benutzern nur die Standardversion der Seite angezeigt (es werden keine Variationen angezeigt).</span><span class="sxs-lookup"><span data-stu-id="f6073-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="f6073-115">Sie müssen das Experiment lange genug laufen lassen, um Daten für statistisch gültige Ergebnisse zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="f6073-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="f6073-116">Verwenden Sie den Dienst eines Drittanbieters, um die experimentellen Daten und Analysen zu überwachen, während das Experiment ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6073-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="f6073-117">Ihre Variationen anpassen</span><span class="sxs-lookup"><span data-stu-id="f6073-117">Adjust your variations</span></span>
<span data-ttu-id="f6073-118">Wenn Sie aus irgendeinem Grund Ihre Variationen ändern müssen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="f6073-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6073-119">Wenn Sie Änderungen an einem Live-Experiment in Commerce oder dem Drittanbieterdienst vornehmen, können Ihre Ergebnisse erheblich beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f6073-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="f6073-120">Lassen Sie das Experiment seinen Lauf nehmen und lassen Sie dann ein neues Experiment für größere Änderungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f6073-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="f6073-121">Wählen Sie im Commerce Site Builder **Experimente** im linken Navigationsbereich und wählen Sie das Experiment.</span><span class="sxs-lookup"><span data-stu-id="f6073-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="f6073-122">Wählen Sie aus dem Dropdown-Menü die Variante aus, die Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f6073-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="f6073-123">Nehmen Sie die erforderlichen Änderungen vor und zeigen Sie dann die Variationen in der Vorschau an und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="f6073-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="f6073-124">Weitere Informationen finden Sie unter [Vorschau und Veröffentlichung eines Experiments](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="f6073-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="f6073-125">Wechseln Sie zum Drittanbieterdienst, um Änderungen im Zusammenhang mit dem Experimentaufbau vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="f6073-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="f6073-126">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="f6073-126">Previous step</span></span>
[<span data-ttu-id="f6073-127">Vorschau und Veröffentlichung eines Experiments</span><span class="sxs-lookup"><span data-stu-id="f6073-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="f6073-128">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="f6073-128">Next step</span></span>
[<span data-ttu-id="f6073-129">Eine Variation höher stufen und ein Experiment abschließen</span><span class="sxs-lookup"><span data-stu-id="f6073-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
