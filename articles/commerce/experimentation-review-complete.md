---
title: Eine Variation höher stufen und ein Experiment abschließen
description: In diesem Thema wird beschrieben, wie Sie eine erfolgreiche Variation höher stufen und ein Experiment in Dynamics 365 Commerce abschließen können.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930200"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="4c393-103">Eine Variation höher stufen und ein Experiment abschließen</span><span class="sxs-lookup"><span data-stu-id="4c393-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="4c393-104">In diesem Thema wird beschrieben, wie Sie die Variation höher stufen, mit der die besten Ergebnisse in Ihrem Experiment erzielt wurden, und wie Sie das Experiment abschließen.</span><span class="sxs-lookup"><span data-stu-id="4c393-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="4c393-105">Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="4c393-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="4c393-106">Weitere Schritte werden in separaten Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="4c393-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="4c393-107">[ ![User Journey zum Experimentieren – Überprüfung und Abschluss](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="4c393-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="4c393-108">Nachdem Sie [Ihr Experiment ausgeführt](experimentation-run-monitor.md) und genügend Daten gesammelt haben, um zu bestimmen, welche Variation Sie auf Ihrer Live-Site verwenden möchten, stufen Sie die Variation höher und beenden das Experiment.</span><span class="sxs-lookup"><span data-stu-id="4c393-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="4c393-109">Eine Variation höher stufen</span><span class="sxs-lookup"><span data-stu-id="4c393-109">Promote a variation</span></span>
<span data-ttu-id="4c393-110">Verwenden Sie die Daten und Analysen zum Experiment im Drittanbieterdienst, um zu entscheiden, welche Variante die besten Ergebnisse liefert.</span><span class="sxs-lookup"><span data-stu-id="4c393-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="4c393-111">Gehen Sie wie folgt vor, um den aktuellen Inhalt der Live-Site durch die Gewinnervariante zu ersetzen, damit sie allen Benutzern Ihrer Website zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="4c393-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="4c393-112">Gehen Sie zur Registerkarte **Experimente** im Site Builder, und wählen Sie das Experiment aus.</span><span class="sxs-lookup"><span data-stu-id="4c393-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="4c393-113">Wählen Sie **Experiment abschließen** in der oberen Leiste aus.</span><span class="sxs-lookup"><span data-stu-id="4c393-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="4c393-114">Wählen Sie im Dialogmenü **Experiment abschließen** die Option **Versuchsdaten überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="4c393-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="4c393-115">Der Dienst eines Drittanbieters wird geöffnet, in dem Sie die Metriken überprüfen und feststellen können, welche Variation am besten funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4c393-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="4c393-116">Wählen Sie im Dialogmenü **Experiment abschließen** im Site Builder die Gewinnervariante aus, und wählen Sie dann **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="4c393-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="4c393-117">Öffnen Sie den Dienst eines Drittanbieters und beenden Sie das Experiment.</span><span class="sxs-lookup"><span data-stu-id="4c393-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="4c393-118">Wählen Sie im Site Builder **Abschließen** aus, um die ursprüngliche Live-Seite zu überschreiben und die Gewinnervariante zu veröffentlichen, damit sie allen Benutzern Ihrer Website zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="4c393-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="4c393-119">Wenn Sie die aktuelle Live-Seite beibehalten und keine Variation veröffentlichen möchten, wählen Sie **Originalseite erneut veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="4c393-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="4c393-120">Experiment löschen</span><span class="sxs-lookup"><span data-stu-id="4c393-120">Delete your experiment</span></span>
<span data-ttu-id="4c393-121">Während es nicht erforderlich ist, ein abgeschlossenes Experiment in Commerce zu löschen, können Sie es löschen, um Speicherplatz zu sparen oder Ihren Arbeitsbereich zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="4c393-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="4c393-122">Gehen Sie wie folgt vor, um ein Experiment zu löschen.</span><span class="sxs-lookup"><span data-stu-id="4c393-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="4c393-123">Gehen Sie zur Registerkarte **Experimente** im Site Builder, und wählen Sie das Experiment aus.</span><span class="sxs-lookup"><span data-stu-id="4c393-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="4c393-124">Wenn das Experiment noch aktiv ist, beenden Sie das Experiment im Dienst eines Drittanbieters, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="4c393-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="4c393-125">Wählen Sie **Veröffentlichung aufheben** in der Befehlsleiste aus, um den Variationsinhalt von der Live-Site zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4c393-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="4c393-126">Wählen Sie **Löschen** in der Befehlsleiste aus, um das Experiment zu löschen.</span><span class="sxs-lookup"><span data-stu-id="4c393-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="4c393-127">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="4c393-127">Previous step</span></span>
[<span data-ttu-id="4c393-128">Ein Experiment ausführen und überwachen</span><span class="sxs-lookup"><span data-stu-id="4c393-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
