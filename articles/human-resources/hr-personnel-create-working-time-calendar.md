---
title: Kalender erstellen und Arbeitszeiten festlegen
description: Kalender beschreiben die Kapazität und die Arbeitszeiten von betrieblichen Ressourcen. In diesem Artikel wird erläutert, wie ein Arbeitskalender auf der Grundlage eines Schichtmodells definiert wird.
author: andreabichsel
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f28e11613cb9e10b258e1c373890505fb6e71d29
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804912"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="07705-104">Kalender erstellen und Arbeitszeiten festlegen</span><span class="sxs-lookup"><span data-stu-id="07705-104">Create calendars and generate working times</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="07705-105">Kalender beschreiben die Kapazität und die Arbeitszeiten von betrieblichen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="07705-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="07705-106">In diesem Artikel wird erläutert, wie ein Arbeitskalender auf der Grundlage eines Schichtmodells definiert wird.</span><span class="sxs-lookup"><span data-stu-id="07705-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="07705-107">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="07705-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="07705-108">Wählen Sie auf der Startseite **Ressourcenlebenszyklus-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="07705-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="07705-109">Wählen Sie **Kalender** aus.</span><span class="sxs-lookup"><span data-stu-id="07705-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="07705-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="07705-110">Select **New**.</span></span>
4. <span data-ttu-id="07705-111">Klassifizieren Sie im Feld **Kalender** den Kalender.</span><span class="sxs-lookup"><span data-stu-id="07705-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="07705-112">Dies ist die Kennung des Kalenders, der als Referenz beim Zuweisen von Kalendern verwendet wird (z. B. zu einer betrieblichen Ressource oder Ressourcengruppe).</span><span class="sxs-lookup"><span data-stu-id="07705-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="07705-113">Geben Sie im Feld **Name** einen Namen für den Kalender ein.</span><span class="sxs-lookup"><span data-stu-id="07705-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="07705-114">Geben Sie im Feld **Standardarbeitstag in Stunden** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="07705-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="07705-115">Stellen Sie sicher, dass die Zeile ausgewählt ist, und wählen Sie dann **Arbeitszeiten** im Aktivitätsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="07705-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="07705-116">Wählen Sie **Arbeitszeiten einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="07705-116">Select **Compose working times**.</span></span> <span data-ttu-id="07705-117">Generieren Sie Arbeitsstunden für jeden Tag in der Periode, in der Sie Arbeit planen möchten.</span><span class="sxs-lookup"><span data-stu-id="07705-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="07705-118">Im Laufe der Zeit können Sie Arbeitszeiten für zusätzliche Perioden generieren.</span><span class="sxs-lookup"><span data-stu-id="07705-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="07705-119">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="07705-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="07705-120">Dies ist der erste Tag, an dem dieser Kalender offen sein muss.</span><span class="sxs-lookup"><span data-stu-id="07705-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="07705-121">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="07705-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="07705-122">Dies ist der erste Tag, an dem dieser Kalender offen ist.</span><span class="sxs-lookup"><span data-stu-id="07705-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="07705-123">Geben Sie im Feld **Schichtmodell** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="07705-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="07705-124">Die Schichtmodell definiert die Arbeitsstunden für jeden Wochentag.</span><span class="sxs-lookup"><span data-stu-id="07705-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="07705-125">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="07705-125">Select **OK**.</span></span>
13. <span data-ttu-id="07705-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="07705-126">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]