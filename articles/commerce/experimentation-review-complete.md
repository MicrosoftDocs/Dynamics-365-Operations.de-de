---
title: Eine Variation höher stufen und ein Experiment abschließen
description: In diesem Thema wird beschrieben, wie Sie eine erfolgreiche Variation höher stufen und ein Experiment in Dynamics 365 Commerce abschließen können.
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
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097092"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="c834f-103">Eine Variation höher stufen und ein Experiment abschließen</span><span class="sxs-lookup"><span data-stu-id="c834f-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="c834f-104">In diesem Thema wird beschrieben, wie Sie die Variation höher stufen, mit der die besten Ergebnisse in Ihrem Experiment erzielt wurden, und wie Sie das Experiment abschließen.</span><span class="sxs-lookup"><span data-stu-id="c834f-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="c834f-105">Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="c834f-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c834f-106">Weitere Schritte werden in separaten Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="c834f-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="c834f-107">[ ![User Journey zum Experimentieren – Überprüfung und Abschluss](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c834f-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="c834f-108">Nachdem Sie [Ihr Experiment ausgeführt](experimentation-run-monitor.md) und genügend Daten gesammelt haben, um zu bestimmen, welche Variation Sie auf Ihrer Live-Site verwenden möchten, stufen Sie die Variation höher und beenden das Experiment.</span><span class="sxs-lookup"><span data-stu-id="c834f-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="c834f-109">Eine Variation höher stufen</span><span class="sxs-lookup"><span data-stu-id="c834f-109">Promote a variation</span></span>
<span data-ttu-id="c834f-110">Verwenden Sie die Daten und Analysen zum Experiment im Drittanbieterdienst, um zu entscheiden, welche Variante die besten Ergebnisse liefert.</span><span class="sxs-lookup"><span data-stu-id="c834f-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="c834f-111">Sie können sie dann höher stufen, um den aktuellen Inhalt der Live-Site durch die Gewinnervariante zu ersetzen, damit sie allen Benutzern Ihrer Website zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="c834f-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="c834f-112">Befolgen Sie diese Schritte, um die Gewinnvariante zu fördern.</span><span class="sxs-lookup"><span data-stu-id="c834f-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="c834f-113">Wählen Sie im Commerce Site Builder **Experimente** im linken Navigationsbereich und wählen Sie das Experiment.</span><span class="sxs-lookup"><span data-stu-id="c834f-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="c834f-114">Auf der Befehlsleiste wählen Sie **Experiment abschließen**.</span><span class="sxs-lookup"><span data-stu-id="c834f-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="c834f-115">Wählen Sie im Dialogfeld **Experiment abschließen** die Option **Versuchsdaten überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="c834f-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="c834f-116">Der Dienst eines Drittanbieters wird geöffnet, in dem Sie die Metriken überprüfen und feststellen können, welche Variation am besten funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c834f-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="c834f-117">Wählen Sie im Dialogfeld **Experiment abschließen** im Site Builder die Gewinnervariante aus, und wählen Sie dann **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="c834f-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="c834f-118">Öffnen Sie den Dienst eines Drittanbieters und beenden Sie das Experiment.</span><span class="sxs-lookup"><span data-stu-id="c834f-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="c834f-119">Wählen Sie im Site Builder **Abschließen** aus, um die ursprüngliche Live-Seite zu überschreiben und die Gewinnervariante zu veröffentlichen, damit sie allen Benutzern Ihrer Website zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="c834f-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="c834f-120">Wenn Sie die aktuelle Live-Seite beibehalten und keine Variation veröffentlichen möchten, wählen Sie **Originalseite erneut veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="c834f-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="c834f-121">Experiment löschen</span><span class="sxs-lookup"><span data-stu-id="c834f-121">Delete your experiment</span></span>
<span data-ttu-id="c834f-122">Während es nicht erforderlich ist, ein abgeschlossenes Experiment in Commerce zu löschen, können Sie es löschen, um Speicherplatz zu sparen oder Ihren Arbeitsbereich zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="c834f-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="c834f-123">Um Ihre Experimentvariationen im Commerce Site Builder zu löschen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="c834f-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c834f-124">Wählen Sie **Experimente** im linken Navigationsbereich und wählen Sie das Experiment.</span><span class="sxs-lookup"><span data-stu-id="c834f-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="c834f-125">Wenn das Experiment noch aktiv ist, beenden Sie das Experiment im Dienst eines Drittanbieters, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="c834f-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="c834f-126">Wählen Sie **Veröffentlichung aufheben**  in der Befehlsleiste aus, um den Variationsinhalt aus der Live-Site zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c834f-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="c834f-127">Wählen Sie **Löschen** aus, um das Experiment zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c834f-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="c834f-128">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="c834f-128">Previous step</span></span>
[<span data-ttu-id="c834f-129">Experiment durchführen und überwachen</span><span class="sxs-lookup"><span data-stu-id="c834f-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
