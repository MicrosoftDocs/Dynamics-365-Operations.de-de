---
title: Den Status eines Experiments überprüfen
description: In diesem Thema wird erläutert, welchen Status ein Experiment im Experimentierlebenszyklus in Dynamics 365 Commerce hat.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ae459ddaf947db6c3de2602a706390edab49efa1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250857"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="a225d-103">Den Status eines Experiments überprüfen</span><span class="sxs-lookup"><span data-stu-id="a225d-103">Review the status of an experiment</span></span>
<span data-ttu-id="a225d-104">Das Einrichten und Ausführen eines Experiments in Dynamics 365 Commerce umfasst viele Schritte.</span><span class="sxs-lookup"><span data-stu-id="a225d-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a225d-105">Informationen zum Experimentierlebenszyklus finden Sie unter [Experimentieren in Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a225d-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="a225d-106">Um zu erfahren, wo sich ein Experiment im Lebenszyklus befindet, wählen Sie **Experimente** im linken Navigationsbereich im Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="a225d-106">To learn where an experiment is in the lifecycle, in Commerce site builder select **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="a225d-107">Eine Liste von Experimenten wird mit dem Status jedes Experiments sowohl in Commerce als auch im Drittanbieterdienst angezeigt, der zum Erstellen von Experimenten, Zuweisen von Variationen und Analysieren von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a225d-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="a225d-108">In der Spalte **Commerce-Status** können die folgenden Werte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a225d-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="a225d-109">**Entwurf** – Das Experiment ist mit einer Seite oder einem Fragment in Commerce verbunden und wird bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="a225d-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="a225d-110">**Veröffentlicht** – Die Experimentvarianten können auf Ihrer Website angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a225d-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="a225d-111">Wenn das Experiment im Dienst eines Drittanbieters ausgeführt wird, sehen Benutzer der Website eine Variation der Seite oder des Fragments, die bzw. das vom Dienst eines Drittanbieters ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="a225d-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="a225d-112">**Unveröffentlicht** – Das Experiment ist auf Ihrer Website nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a225d-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="a225d-113">Benutzer der Website sehen nur eine Standardversion der Seite oder des Fragments, auch wenn das Experiment im Dienst eines Drittanbieters ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a225d-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="a225d-114">**Abgeschlossen** – Das Experiment hat seinen Lauf genommen und eine Variation wurde für die Benutzung durch alle Website-Benutzer höher gestuft.</span><span class="sxs-lookup"><span data-stu-id="a225d-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="a225d-115">Entsprechend können in der Spalte **Drittanbieterstatus** die folgenden Werte angezeigt werden, um anzuzeigen, welchen Status die Experimente im Drittanbieterdienst haben.</span><span class="sxs-lookup"><span data-stu-id="a225d-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="a225d-116">**Entwurf** – Das Experiment wird im Drittanbieterdienst eingerichtet, aber noch nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="a225d-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="a225d-117">**Wird ausgeführt** – Das Experiment wurde im Drittanbieterdienst gestartet und sammelt Daten.</span><span class="sxs-lookup"><span data-stu-id="a225d-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="a225d-118">**Angehalten** – Das Experiment wird angehalten und es werden keine Daten erfasst.</span><span class="sxs-lookup"><span data-stu-id="a225d-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="a225d-119">Sie müssen das Experiment fortsetzen, damit die Daten erneut erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="a225d-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="a225d-120">**Archiviert** – Das Experiment hat seinen Lauf genommen und wurde für spätere Referenzzwecke im Drittanbieterdienst katalogisiert.</span><span class="sxs-lookup"><span data-stu-id="a225d-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="a225d-121">Das folgende Diagramm zeigt beide Statussätze und ihre Beziehung zueinander.</span><span class="sxs-lookup"><span data-stu-id="a225d-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="a225d-122">[ ![Experimentierstatus](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a225d-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]