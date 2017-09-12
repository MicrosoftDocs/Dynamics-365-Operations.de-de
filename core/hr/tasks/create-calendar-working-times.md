--- 
title: Kalender erstellen und Arbeitszeiten generieren
description: "Kalender beschreiben die Kapazität und die Arbeitszeiten von betrieblichen Ressourcen."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d65fe0363e418f9c2e78bd78e802a4b0ea98599c
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="db04f-103">Kalender erstellen und Arbeitszeiten generieren</span><span class="sxs-lookup"><span data-stu-id="db04f-103">Create a calendar and generate working times</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db04f-104">Kalender beschreiben die Kapazität und die Arbeitszeiten von betrieblichen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="db04f-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="db04f-105">Diese Prozedur zeigt Ihnen die Definition eines Arbeitskalenders auf Grundlage eines Schichtmodells.</span><span class="sxs-lookup"><span data-stu-id="db04f-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="db04f-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="db04f-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="db04f-107">Wechseln Sie zu "Alle Arbeitsbereiche" > "Ressourcenlebenszyklusverwaltung".</span><span class="sxs-lookup"><span data-stu-id="db04f-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="db04f-108">Klicken Sei auf "Kalender".</span><span class="sxs-lookup"><span data-stu-id="db04f-108">Click Calendars.</span></span>
3. <span data-ttu-id="db04f-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="db04f-109">Click New.</span></span>
4. <span data-ttu-id="db04f-110">Geben Sie im Feld Kalender einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="db04f-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="db04f-111">Dies ist die Kennung des Kalenders, der als Referenz beim Zuweisen von Kalendern verwendet wird (z. B. zu einer betrieblichen Ressource oder Ressourcengruppe).</span><span class="sxs-lookup"><span data-stu-id="db04f-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="db04f-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="db04f-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="db04f-113">Geben Sie im Feld "Standardarbeitstag in Stunden" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="db04f-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="db04f-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="db04f-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="db04f-115">Klicken Sie auf "Arbeitszeiten".</span><span class="sxs-lookup"><span data-stu-id="db04f-115">Click Working times.</span></span>
9. <span data-ttu-id="db04f-116">Klicken Sie auf "Arbeitszeiten einrichten".</span><span class="sxs-lookup"><span data-stu-id="db04f-116">Click Compose working times.</span></span>
    * <span data-ttu-id="db04f-117">Generieren Sie Arbeitsstunden für jeden Tag in der Periode, in der Sie Arbeit planen möchten.</span><span class="sxs-lookup"><span data-stu-id="db04f-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="db04f-118">Im Laufe der Zeit können Sie Arbeitszeiten für zusätzliche Perioden generieren.</span><span class="sxs-lookup"><span data-stu-id="db04f-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="db04f-119">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="db04f-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="db04f-120">Dies ist der erste Tag, an dem dieser Kalender offen sein muss.</span><span class="sxs-lookup"><span data-stu-id="db04f-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="db04f-121">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="db04f-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="db04f-122">Dies ist der erste Tag, an dem dieser Kalender offen ist.</span><span class="sxs-lookup"><span data-stu-id="db04f-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="db04f-123">Geben Sie im Feld "Schichtmodell" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="db04f-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="db04f-124">Die Schichtmodell definiert die Arbeitsstunden für jeden Wochentag.</span><span class="sxs-lookup"><span data-stu-id="db04f-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="db04f-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="db04f-125">Click OK.</span></span>
14. <span data-ttu-id="db04f-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="db04f-126">Close the page.</span></span>


