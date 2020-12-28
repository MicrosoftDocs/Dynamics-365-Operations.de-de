---
title: Ein Experiment verbinden und Variationen bearbeiten
description: In diesem Thema wird beschrieben, wie Sie ein Experiment in einem Dienst eines Drittanbieters mit Dynamics 365 Commerce verbinden und wie man Variationen für das Experiment bearbeitet.
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
ms.openlocfilehash: 030640ba8907ae52c198ac96ad2c243b533d8c53
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4412705"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="83d6d-103">Ein Experiment verbinden und Variationen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="83d6d-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="83d6d-104">In diesem Thema wird beschrieben, wie Sie Ihr Experiment in Commerce verbinden und Änderungen an Ihren Variationen vornehmen, damit sie mit Ihrer Hypothese übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="83d6d-105">Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="83d6d-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="83d6d-106">Weitere Schritte werden in separaten Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="83d6d-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="83d6d-107">[ ![User Journey zum Experimentieren – Verbindung und Bearbeitung](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="83d6d-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="83d6d-108">Nach dem [Einrichten Ihres Experiments](experimentation-setup.md) in einem Drittanbieterdienst verbinden Sie das Experiment mit Dynamics 365 Commerce und bearbeiten Sie die Experimentvarianten.</span><span class="sxs-lookup"><span data-stu-id="83d6d-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="83d6d-109">Planen von Aspekten</span><span class="sxs-lookup"><span data-stu-id="83d6d-109">Planning considerations</span></span>

<span data-ttu-id="83d6d-110">Bevor Sie Ihr Experiment in Commerce verbinden, müssen Sie einige Entscheidungen treffen, die sich auf die Art und Weise auswirken, wie Commerce Ihre Inhalte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="83d6d-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="83d6d-111">Den Umfang Ihres Experiments bestimmen</span><span class="sxs-lookup"><span data-stu-id="83d6d-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="83d6d-112">Wenn Sie ein Experiment verbinden, werden Sie aufgefordert, den Umfang des Experiments zu definieren.</span><span class="sxs-lookup"><span data-stu-id="83d6d-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="83d6d-113">Experimente sind definiert als **teilweiser** Umfang oder **ganzer** Umfang.</span><span class="sxs-lookup"><span data-stu-id="83d6d-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="83d6d-114">Wählen Sie **teilweise**, wenn Sie ein Experiment für einen bestimmten Teil einer Seite durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="83d6d-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="83d6d-115">Wenn Sie diese Option auswählen, müssen Sie angeben, welche Module im Experiment enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="83d6d-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="83d6d-116">Änderungen, die an Teilen der Standardseite oder des Standardfragments vorgenommen werden, die nicht mit dem Experiment zusammenhängen, werden automatisch über Variationen hinweg synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="83d6d-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="83d6d-117">Wählen Sie **ganz**, wenn Sie ein Experiment für eine ganze Seite oder ein Fragment durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="83d6d-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="83d6d-118">Es werden separate Kopien der Standardseite oder des Standardfragments erstellt.</span><span class="sxs-lookup"><span data-stu-id="83d6d-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="83d6d-119">Sie müssen nicht auswählen, welche Module im Experiment enthalten sind, da die gesamte Bearbeitungsfläche geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="83d6d-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="83d6d-120">Sie können Module nach Bedarf hinzufügen, löschen oder neu anordnen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="83d6d-121">Wenn jedoch Änderungen an der Standardseite oder dem Standardfragment vorgenommen werden, mit denen das Experiment verknüpft ist, müssen diese Änderungen über alle Variationen hinweg manuell synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="83d6d-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="83d6d-122">Wenn Sie Ihr Experiment einer Seite zuordnen, die ein Layout verwendet, können Sie das Experiment nur als **ganz** festlegen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="83d6d-123">Entscheiden Sie, ob Sie planen möchten, wann Ihr Experiment veröffentlicht wird</span><span class="sxs-lookup"><span data-stu-id="83d6d-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="83d6d-124">Wenn Sie planen möchten, wann Ihr Experiment auf Ihrer Live-Site veröffentlicht wird, stellen Sie sicher, dass der Inhalt, den Sie dem Experiment zuordnen möchten, in einer Veröffentlichungsgruppe verfügbar ist, *bevor* Sie das Experiment verbinden.</span><span class="sxs-lookup"><span data-stu-id="83d6d-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="83d6d-125">Weitere Informationen zu Veröffentlichungsgruppen finden Sie unter [Arbeiten mit Veröffentlichungsgruppen](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="83d6d-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="83d6d-126">Ihr Experiment verbinden</span><span class="sxs-lookup"><span data-stu-id="83d6d-126">Connect your experiment</span></span>
<span data-ttu-id="83d6d-127">Um Ihr Experiment zu verbinden, starten Sie den Assistenten **Experiment verbinden**.</span><span class="sxs-lookup"><span data-stu-id="83d6d-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="83d6d-128">Der Assistent führt Sie durch die Schritte, die zum Verbinden Ihres Experiments erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="83d6d-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="83d6d-129">Wenn Sie den Assistenten abgeschlossen haben, ist Ihr Experiment verbunden und Variationen werden erstellt und können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="83d6d-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="83d6d-130">Führen Sie die folgenden Schritte aus, um Ihr Experiment in Commerce Site Builder zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="83d6d-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="83d6d-131">Um den **Experiment verbinden** Assistent zu starten, wählen Sie **Experimente** im linken Navigationsbereich und wählen Sie dann **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="83d6d-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="83d6d-132">Alternativ können Sie über einen Seiten- oder Fragmenteditor auf den Assistenten zugreifen, indem Sie ihn bearbeiten und **Experiment verbinden** in der Befehlsleiste auswählen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="83d6d-133">Eine Seite kann jeweils nur mit einem Experiment verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="83d6d-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="83d6d-134">Um eine Seite mit einem anderen Experiment zu verbinden, löschen Sie zuerst das Experiment, mit dem die Seite derzeit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="83d6d-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="83d6d-135">Wählen Sie die Seite oder das Fragment aus, an der bzw. dem Sie Ihr Experiment ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="83d6d-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="83d6d-136">Stellen Sie den Experimentierbereich auf **teilweise** oder **ganz** ein, basierend auf der Auswahl, die Sie im Abschnitt oben [Bestimmen Sie den Umfang Ihres Experiments](#determine-the-scope-of-your-experiment) getroffen haben.</span><span class="sxs-lookup"><span data-stu-id="83d6d-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="83d6d-137">Das Funktionsflag zum **Experimentieren an Seiten oder Fragmenten** muss aktiviert sein, wenn Sie mit einer ganzen Seite oder einem Fragment experimentieren möchten.</span><span class="sxs-lookup"><span data-stu-id="83d6d-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="83d6d-138">Weitere Informationen finden Sie im Thema [Experimentieren in Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83d6d-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="83d6d-139">Wählen Sie im letzten Schritt des Assistenten die Option **Variationen generieren und Assistenten beenden**.</span><span class="sxs-lookup"><span data-stu-id="83d6d-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="83d6d-140">Für das Experiment werden Variationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="83d6d-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="83d6d-141">Ihre Variationen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="83d6d-141">Edit your variations</span></span>
<span data-ttu-id="83d6d-142">Wenn Sie den Assistenten beenden, werden Variationen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="83d6d-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="83d6d-143">Als Nächstes bearbeiten Sie die Variationen so, dass sie die Auswahlmöglichkeiten widerspiegeln, die Sie in der Experimenthypothese überprüfen müssen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="83d6d-144">Wählen Sie eines der folgenden Verfahren, das dem Umfang entspricht, den Sie für Ihr Experiment im Abschnitt oben [Bestimmen Sie den Umfang Ihres Experiments](#determine-the-scope-of-your-experiment) ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="83d6d-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="83d6d-145">Variationen für Experimente mit Teilumfang bearbeiten</span><span class="sxs-lookup"><span data-stu-id="83d6d-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="83d6d-146">Befolgen Sie diese Schritte, wenn Sie den Umfang Ihres Experiments als **teilweise** definiert haben im Assistenten **Experiment verbinden**.</span><span class="sxs-lookup"><span data-stu-id="83d6d-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="83d6d-147">Verwenden Sie in der Editoransicht das Dropdown-Menü für Variationen unter der Befehlsleiste, um jede Variation basierend auf Ihrer ursprünglichen Hypothese zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="83d6d-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="83d6d-148">Möglicherweise möchten Sie auch eine Steuerungs- oder Basisvariation einrichten, indem Sie eine der Variationen unverändert lassen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="83d6d-149">Wählen Sie das Modul aus, an dem experimentiert werden soll, wählen Sie die Auslassungspunkte (...) aus und wählen Sie dann **Zum Experiment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="83d6d-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="83d6d-150">Variationen für Experimente mit vollem Umfang bearbeiten</span><span class="sxs-lookup"><span data-stu-id="83d6d-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="83d6d-151">Wenn Sie den Umfang Ihres Experiments als **ganz** im Assistenten **Experiment verbinden** definiert haben, verwenden Sie in der Editoransicht das Dropdown-Menü für Variationen unter der Befehlsleiste, um jede Variation basierend auf Ihrer ursprünglichen Hypothese zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="83d6d-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="83d6d-152">In jedem Fall möchten Sie möglicherweise auch eine Steuerungs- oder Basisvariation einrichten, indem Sie eine der Variationen unverändert lassen.</span><span class="sxs-lookup"><span data-stu-id="83d6d-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="83d6d-153">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="83d6d-153">Previous step</span></span>
[<span data-ttu-id="83d6d-154">Einrichten eines Experiments</span><span class="sxs-lookup"><span data-stu-id="83d6d-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="83d6d-155">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="83d6d-155">Next step</span></span>
[<span data-ttu-id="83d6d-156">Vorschau und Veröffentlichung eines Experiments</span><span class="sxs-lookup"><span data-stu-id="83d6d-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
