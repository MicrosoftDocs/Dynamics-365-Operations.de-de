---
title: Vorschau und Veröffentlichung eines Experiments
description: In diesem Thema wird beschrieben, wie Sie ein Experiment in Dynamics 365 Commerce in der Vorschau anzeigen und veröffentlichen.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930205"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="af6a0-103">Vorschau und Veröffentlichung eines Experiments</span><span class="sxs-lookup"><span data-stu-id="af6a0-103">Preview and publish an experiment</span></span>

<span data-ttu-id="af6a0-104">In diesem Thema wird beschrieben, wie Sie in Dynamics 365 Commerce eine Vorschau Ihres Experiments anzeigen und veröffentlichen, nachdem Sie [Ihr Experiment verbunden und Ihre Variationen bearbeitet haben](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="af6a0-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="af6a0-105">Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="af6a0-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="af6a0-106">Weitere Schritte werden in separaten Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="af6a0-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="af6a0-107">[ ![User Journey zum Experimentieren – Vorschau und Veröffentlichung](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="af6a0-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="af6a0-108">Eine Vorschau Ihrer Experimentvarianten anzeigen</span><span class="sxs-lookup"><span data-stu-id="af6a0-108">Preview your experiment variations</span></span>
<span data-ttu-id="af6a0-109">Sie können eine Vorschau Ihrer Variationen anzeigen und sie weiter bearbeiten, bis sie so aussehen, wie Sie es möchten.</span><span class="sxs-lookup"><span data-stu-id="af6a0-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

1. <span data-ttu-id="af6a0-110">Verwenden Sie im Site Builder das Dropdown-Menü für Variationen unterhalb der Befehlsleiste, um den Inhalt auszuwählen, für den Sie eine Vorschau anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="af6a0-110">In site builder, use the variations drop-down menu below the command bar to select the content you want to preview.</span></span> 
1. <span data-ttu-id="af6a0-111">Wählen Sie **Vorschau** in der oberen Leiste.</span><span class="sxs-lookup"><span data-stu-id="af6a0-111">Select **Preview** in the top bar.</span></span> <span data-ttu-id="af6a0-112">Eine Vorschau des Inhalts, wenn er veröffentlicht wird, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af6a0-112">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="af6a0-113">Um eine Vorschau einer anderen Variante anzuzeigen, wählen Sie sie aus der Dropdown-Liste aus, und wählen Sie nochmal **Vorschau**.</span><span class="sxs-lookup"><span data-stu-id="af6a0-113">To preview a different variation, select it from the variation drop-down and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="af6a0-114">Ihr Experiment veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="af6a0-114">Publish your experiment</span></span>
<span data-ttu-id="af6a0-115">Wenn Sie keine Veröffentlichungsgruppe verwenden, um zu planen, wann Ihr Experiment live geschaltet wird, und Sie sofort veröffentlichen möchten, wählen Sie **Veröffentlichen** in der Befehlsleiste.</span><span class="sxs-lookup"><span data-stu-id="af6a0-115">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="af6a0-116">Alle zum Experiment gehörenden Variationen werden veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="af6a0-116">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="af6a0-117">Wenn die Seite eine unveröffentlichte URL enthält, müssen Sie zuerst die URL veröffentlichen, da sie sonst für die Benutzer Ihrer Website nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="af6a0-117">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="af6a0-118">Weitere Details finden Sie unter [Speichern, Vorschau und Veröffentlichung einer Seite](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="af6a0-118">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="af6a0-119">Verwenden Sie Veröffentlichungsgruppen, um zu planen, wann Ihr Experiment live geschaltet wird</span><span class="sxs-lookup"><span data-stu-id="af6a0-119">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="af6a0-120">Im Site Builder erstellte Variationen können mithilfe einer Veröffentlichungsgruppe für die Veröffentlichung geplant werden.</span><span class="sxs-lookup"><span data-stu-id="af6a0-120">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="af6a0-121">Innerhalb einer Veröffentlichungsgruppe können Sie eine Seite oder ein Fragment mit Ihrem Experiment verbinden, indem Sie zu den Registerkarten **Experimente**, **Seiten** oder **Fragmente** wechseln. Weitere Informationen finden Sie im Thema [Ein Experiment verbinden und Variationen bearbeiten](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="af6a0-121">Within a publish group, you can connect a page or fragment to your experiment by going to the **Experiments** tab or the **Pages** or **Fragments** tab. For more information, see [Connect an experiment and edit variations](experimentation-connect-edit.md) topic.</span></span> <span data-ttu-id="af6a0-122">Weitere Informationen zu Veröffentlichungsgruppen finden Sie unter [Arbeiten mit Veröffentlichungsgruppen](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="af6a0-122">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="af6a0-123">Bei der Verwendung von Veröffentlichungsgruppen mit Experimenten sind einige wichtige Überlegungen zu beachten.</span><span class="sxs-lookup"><span data-stu-id="af6a0-123">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="af6a0-124">Wenn Sie einer Veröffentlichungsgruppe eine Seite oder ein Fragment hinzufügen, an der bzw. dem ein Experiment ausgeführt wird, wird das Experiment von der Seite oder dem Fragment in der Veröffentlichungsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="af6a0-124">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="af6a0-125">Experimente, die mit Seiten einer Live-Site verbunden sind, stehen Seiten innerhalb von Veröffentlichungsgruppen nicht zur Verfügung und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="af6a0-125">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="af6a0-126">Ebenso stehen Seiten, an denen Experimente in einer Live-Site ausgeführt werden, anderen Experimenten in Veröffentlichungsgruppen nicht zur Verfügung und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="af6a0-126">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="af6a0-127">Wenn Sie eine Veröffentlichungsgruppe veröffentlichen oder planen, wird der gesamte Inhalt der Veröffentlichungsgruppe veröffentlicht, unabhängig davon, ob der Veröffentlichungsgruppe ein Experiment zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="af6a0-127">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="af6a0-128">Da eine Veröffentlichungsgruppe nach der Veröffentlichung auf einer Live-Site weiterhin besteht, bleiben auch die Experimente in der Veröffentlichungsgruppe bestehen.</span><span class="sxs-lookup"><span data-stu-id="af6a0-128">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="af6a0-129">Daher können Sie andere Experimente nicht mit derselben Seite oder demselben Fragment verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="af6a0-129">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="af6a0-130">Um diese Einschränkung zu vermeiden, löschen Sie alle Veröffentlichungsgruppen mit bestehenden Experimenten.</span><span class="sxs-lookup"><span data-stu-id="af6a0-130">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="af6a0-131">Wenn Sie ein Experiment auf einer Live-Site löschen möchten, das auch in einer Veröffentlichungsgruppe vorhanden ist, löschen Sie es zuerst aus der Veröffentlichungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="af6a0-131">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="af6a0-132">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="af6a0-132">Previous step</span></span>
[<span data-ttu-id="af6a0-133">Ein Experiment verbinden und bearbeiten</span><span class="sxs-lookup"><span data-stu-id="af6a0-133">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="af6a0-134">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="af6a0-134">Next step</span></span>
[<span data-ttu-id="af6a0-135">Ein Experiment ausführen und überwachen</span><span class="sxs-lookup"><span data-stu-id="af6a0-135">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
