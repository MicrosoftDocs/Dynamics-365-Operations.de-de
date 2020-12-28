---
title: Leistungserfassung hinzufügen und Lob an eine Person senden
description: Die Leistungserfassung verwahrt Informationen, die zeigen, wie Sie Ihre Ziele erreichen oder wie Ihre Leistung für einen bestimmten Zeitraum aussieht.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2a90a5f746e49e1a5df9910867e8cd35feb1147
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418616"
---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="6e01e-103">Leistungserfassung hinzufügen und Lob an eine Person senden</span><span class="sxs-lookup"><span data-stu-id="6e01e-103">Add to your performance journal and send praise to someone</span></span>

<span data-ttu-id="6e01e-104">Die Leistungserfassung verwahrt Informationen, die zeigen, wie Sie Ihre Ziele erreichen oder wie Ihre Leistung für einen bestimmten Zeitraum aussieht.</span><span class="sxs-lookup"><span data-stu-id="6e01e-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="6e01e-105">Sie können außerdem Aktivitäten von Mitarbeitern aus der Erfassung loben.</span><span class="sxs-lookup"><span data-stu-id="6e01e-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="6e01e-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="6e01e-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e01e-107">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6e01e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="6e01e-108">Wechseln Sie zu Alle Arbeitsbereiche > Mitarbeiter-Self-Service.</span><span class="sxs-lookup"><span data-stu-id="6e01e-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="6e01e-109">Klicken Sie auf "Leistungserfassung".</span><span class="sxs-lookup"><span data-stu-id="6e01e-109">Click Performance journal.</span></span>
3. <span data-ttu-id="6e01e-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6e01e-110">Click New.</span></span>
4. <span data-ttu-id="6e01e-111">Geben Sie im Feld "Titel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="6e01e-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6e01e-113">Das Leistungserfassungsdatum ist das Datum, an dem die Erfassung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6e01e-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="6e01e-114">Die Quelle zeigt an, woher die Leistungserfassung kam.</span><span class="sxs-lookup"><span data-stu-id="6e01e-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="6e01e-115">Wenn Sie eine erstellen, kommt sie aus "Meine Erfassung".</span><span class="sxs-lookup"><span data-stu-id="6e01e-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="6e01e-116">Wenn Ihr Manager eine erstellt, Kommt diese aus der Managererfassung.</span><span class="sxs-lookup"><span data-stu-id="6e01e-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="6e01e-117">Sie können dieser Erfassung mit Ihrem Manager teilen oder sie nur für sich anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6e01e-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="6e01e-118">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="6e01e-119">Geben Sie im Feld "Abschlussdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="6e01e-120">Wählen Sie im Feld "Entwicklungsplan" "Ja" aus.</span><span class="sxs-lookup"><span data-stu-id="6e01e-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="6e01e-121">Geben Sie im Feld "Schlüsselwörter" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="6e01e-122">Klicken Sie auf "Externen Link hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="6e01e-122">Click Add external link.</span></span>
11. <span data-ttu-id="6e01e-123">Geben Sie im Feld "Beschreibung" die Bezeichnung "Envision" ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="6e01e-124">Geben Sie im Feld „Internetadresse” „https://www.microsoft.com/en/envision/default” ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="6e01e-125">Klicken Sie auf die Bezeichnung mit dem Namen "Leistungserfassung" unter der "Speichern"-Schaltfläche, um zum Raster zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="6e01e-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="6e01e-126">Sie können die ausgewählte Erfassung oder Erfassungen einem Ziel hinzufügen, um es anzuzeigen, wenn Sie das Ziel öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e01e-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="6e01e-127">Ein Link wird im Inforegistername Link hinzugefügt. Wenn Sie eine Erfassung einem Ziel hinzufügen und dann das Ziel einer Überprüfung hinzufügen, wird die Erfassung automatisch bei der Überprüfung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e01e-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="6e01e-128">Sie können die ausgewählte Erfassung oder Erfassungen einer Überprüfung hinzufügen, um sie anzuzeigen, wenn Sie die Überprüfung öffnen.</span><span class="sxs-lookup"><span data-stu-id="6e01e-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="6e01e-129">Ein Link wird in dem Links-Inforegister hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6e01e-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="6e01e-130">Klicken Sie auf "Schnell hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="6e01e-130">Click Quick add.</span></span>
15. <span data-ttu-id="6e01e-131">Geben Sie im Feld "Titel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="6e01e-132">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="6e01e-133">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="6e01e-133">Click Save.</span></span>
18. <span data-ttu-id="6e01e-134">Kicken Sie auf "Lob versenden".</span><span class="sxs-lookup"><span data-stu-id="6e01e-134">Click Send praise.</span></span>
19. <span data-ttu-id="6e01e-135">Wählen Sie eine Person aus der Liste der Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="6e01e-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="6e01e-136">Geben Sie im Textfeld "Danke für die Hilfe bei der Konferenz" ein.</span><span class="sxs-lookup"><span data-stu-id="6e01e-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="6e01e-137">Klicken Sie auf Senden.</span><span class="sxs-lookup"><span data-stu-id="6e01e-137">Click Send.</span></span>

