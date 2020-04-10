---
title: Produktionsauftrag freigeben
description: Diese Prozedur zeigt an, wie ein Produktionsauftrag freigegeben wird.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e98adea620d74bdb7a90cedc9b256d9883b27525
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148959"
---
# <a name="release-a-production-order"></a><span data-ttu-id="01a66-103">Produktionsauftrag freigeben</span><span class="sxs-lookup"><span data-stu-id="01a66-103">Release a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01a66-104">Diese Prozedur zeigt an, wie ein Produktionsauftrag freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="01a66-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="01a66-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="01a66-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="01a66-106">Dies ist die vierte Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="01a66-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="01a66-107">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="01a66-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="01a66-108">Wählen Sie im Raster einen Produktionsauftrag aus, der den Status "Eingeplant" hat.</span><span class="sxs-lookup"><span data-stu-id="01a66-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="01a66-109">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="01a66-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="01a66-110">Klicken Sie auf "Freigabe".</span><span class="sxs-lookup"><span data-stu-id="01a66-110">Click Release.</span></span>
    * <span data-ttu-id="01a66-111">Auf dieser Seite können Sie die Freigabe des ausgewählten Bereichs von Produktionsaufträgen bestätigen.</span><span class="sxs-lookup"><span data-stu-id="01a66-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="01a66-112">Klicken Sie auf "Auswählen", wenn Sie Aufträge hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="01a66-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="01a66-113">Der "Freigabeschritt" zeigt an, wann der Produktionsauftrag für die Produktionszeiterfassung freigegeben wird, sodass die Zeiterfassungsoperatoren den Status zu Produktionseinzelvorgängen melden können.</span><span class="sxs-lookup"><span data-stu-id="01a66-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="01a66-114">Produktionsunterlagen, die relevante Informationen zum Verarbeiten der Einzelvorgänge enthalten, können ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="01a66-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="01a66-115">Die Lagerortarbeit für die Rohmaterialentnahme wird für die Artikel generiert, die für den Lagerortprozess eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="01a66-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="01a66-116">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="01a66-116">Click the General tab.</span></span>
    * <span data-ttu-id="01a66-117">Wählen Sie aus, welche Produktionsberichte gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01a66-117">Select which production reports should be printed.</span></span> <span data-ttu-id="01a66-118">Der Bericht "Einzelvorgangsliste" druckt eine Seite für jeden geplanten Einzelvorgang aus und erfordert, dass der Produktionsauftrag auf der Einzelvorgangebene eingeplant wird.</span><span class="sxs-lookup"><span data-stu-id="01a66-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="01a66-119">Der Bericht enthält Informationen über die geplante Start- und Endzeit, die zu produzierende Menge und welche Ressource den Einzelvorgang verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="01a66-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="01a66-120">Der Bericht "Arbeitsplan" sammelt die gleichen Informationen auf der gleichen Seite, aber druckt keine Seite für jeden Einzelvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="01a66-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="01a66-121">Der Bericht "Arbeitsplanliste" zeigt nur die Arbeitsgänge aber nicht die Einzelvorgänge an.</span><span class="sxs-lookup"><span data-stu-id="01a66-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="01a66-122">Daher ist für diesen Bericht keine Feinterminierung erforderlich, aber sie kann verwendet werden, wenn Produktionsaufträge auf der Arbeitsgangsebene geplant werden.</span><span class="sxs-lookup"><span data-stu-id="01a66-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="01a66-123">Klicken Sie auf das Kontrollkästchen "Arbeitsplanliste drucken".</span><span class="sxs-lookup"><span data-stu-id="01a66-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="01a66-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="01a66-124">Click OK.</span></span>
7. <span data-ttu-id="01a66-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="01a66-125">Close the page.</span></span>

