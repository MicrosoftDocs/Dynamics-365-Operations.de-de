---
title: Hilfsmittel zur Kandidatenauswahl ermitteln und bereitstellen
description: Einen qualifizierten Pool von Kandidaten zu finden, um freie Stellen zu füllen, kann schwierig sein, insbesondere wenn eine Position einzigartige Qualifikationen erfordert.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d8a05ad7f100e6c54ccf1ecf7b76509cf44dbb8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143948"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="d44b8-103">Hilfsmittel zur Kandidatenauswahl ermitteln und bereitstellen</span><span class="sxs-lookup"><span data-stu-id="d44b8-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d44b8-104">Einen qualifizierten Pool von Kandidaten zu finden, um freie Stellen zu füllen, kann schwierig sein, insbesondere wenn eine Position einzigartige Qualifikationen erfordert.</span><span class="sxs-lookup"><span data-stu-id="d44b8-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="d44b8-105">Allerdings sind Kandidaten mit den von Ihnen benötigten Qualifikationen möglicherweise bereits in Ihrer Organisation beschäftigt.</span><span class="sxs-lookup"><span data-stu-id="d44b8-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="d44b8-106">Sie können nach einer bestimmten Qualifikation unter vorhandenen Mitarbeitern oder neuen Bewerbern suchen.</span><span class="sxs-lookup"><span data-stu-id="d44b8-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="d44b8-107">Dies ermöglicht es einem Personalbeschaffungsmitarbeiter, Bewerber schnell zu erfassen und zu rastern, die sich jetzt oder in der Vergangenheit für eine offene Stelle beworben haben, oder es können potenzielle Kandidaten aus ihrem vorhandenen von Mitarbeiter gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="d44b8-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="d44b8-108">Verwenden Sie diese Aufgabenaufzeichnung, um zu erfahren, wie die Qualifikationszuordnungsfunktionalität Sie dabei unterstützen kann, die richtige Person für eine offene Stelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="d44b8-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="d44b8-109">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="d44b8-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d44b8-110">Wechseln Sie zu "Personalverwaltung" > "Kompetenzen" > "Qualifikationsanalyse" > "Qualifikationszuordnungsprofile".</span><span class="sxs-lookup"><span data-stu-id="d44b8-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="d44b8-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d44b8-111">Click New.</span></span>
3. <span data-ttu-id="d44b8-112">Geben Sie im Feld "Qualifikationszuordnung" einen Namen für Ihre Qualifikationszuordnung ein.</span><span class="sxs-lookup"><span data-stu-id="d44b8-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="d44b8-113">Beispiel: Buchhalter.</span><span class="sxs-lookup"><span data-stu-id="d44b8-113">Example: Accountant.</span></span>
4. <span data-ttu-id="d44b8-114">Geben Sie im Feld Beschreibung eine Beschreibung der Qualifikationszuordnung ein.</span><span class="sxs-lookup"><span data-stu-id="d44b8-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="d44b8-115">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="d44b8-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="d44b8-116">Klicken Sie auf "Profil abrufen".</span><span class="sxs-lookup"><span data-stu-id="d44b8-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="d44b8-117">Verwenden Sie "Profil abrufen", um die Daten zu "Bescheinigung", "Qualifikation" und "Bildung" von einer ausgewählten "Person", "Stelle" oder "Kurs" als Basis für Ihre Suche zu beziehen.</span><span class="sxs-lookup"><span data-stu-id="d44b8-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="d44b8-118">Sie können dann Kriterien hinzufügen oder entfernen und angeben, ob die Kriterien optional sind und die Wichtigkeit der Kriterien anordnen.</span><span class="sxs-lookup"><span data-stu-id="d44b8-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="d44b8-119">Klicken Sie auf "Stelle".</span><span class="sxs-lookup"><span data-stu-id="d44b8-119">Click Job.</span></span>
8. <span data-ttu-id="d44b8-120">Geben Sie im Feld "Stelle" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d44b8-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="d44b8-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d44b8-121">Click OK.</span></span>
10. <span data-ttu-id="d44b8-122">Erweitern Sie das Bereichsinforegister, und fügen Sie alle weiteren Informationen, wie Abteilung, hinzu.</span><span class="sxs-lookup"><span data-stu-id="d44b8-122">Expand the range fast tab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="d44b8-123">Erweitern Sie das Bescheinigungen-Inforegister, um die Bescheinigungen anzuzeigen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d44b8-123">Expand the certificates fast tab to view or edit the certificates.</span></span>
12. <span data-ttu-id="d44b8-124">Erweitern Sie das Inforegister "Qualifikationen", um die Qualifikationen anzuzeigen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d44b8-124">Expand the Skills fast tab to view or edit the skills.</span></span>
13. <span data-ttu-id="d44b8-125">Erweitern Sie das Inforegister "Bildung", um die Bildungskriterien anzuzeigen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d44b8-125">Expand the Education fast tab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="d44b8-126">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="d44b8-126">Click Execute.</span></span>
15. <span data-ttu-id="d44b8-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d44b8-127">Click OK.</span></span>
16. <span data-ttu-id="d44b8-128">Klicken Sie auf "Ergebnis".</span><span class="sxs-lookup"><span data-stu-id="d44b8-128">Click Result.</span></span>
17. <span data-ttu-id="d44b8-129">Klicken Sie auf "Ergebnis".</span><span class="sxs-lookup"><span data-stu-id="d44b8-129">Click Result.</span></span>
18. <span data-ttu-id="d44b8-130">Klicken Sie auf Fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="d44b8-130">Click Resume.</span></span>
19. <span data-ttu-id="d44b8-131">Klicken Sie auf "Bescheinigungen".</span><span class="sxs-lookup"><span data-stu-id="d44b8-131">Click Certificates.</span></span>
    * <span data-ttu-id="d44b8-132">Sie können dann weitere Details zu jeder aufgeführten Person abrufen und Details zu ihrer Bildung, ihren Qualifikationen, ihrer beruflichen Erfahrung, usw. anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d44b8-132">You can drill further into each person listed and see details regarding their education, skills, professional experience etc.</span></span>  
20. <span data-ttu-id="d44b8-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d44b8-133">Close the page.</span></span>
21. <span data-ttu-id="d44b8-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d44b8-134">Close the page.</span></span>
22. <span data-ttu-id="d44b8-135">Wählen Sie das Ergebnis erneut aus.</span><span class="sxs-lookup"><span data-stu-id="d44b8-135">Select result again.</span></span>
23. <span data-ttu-id="d44b8-136">Klicken Sie auf "Bericht".</span><span class="sxs-lookup"><span data-stu-id="d44b8-136">Click Report.</span></span>
    * <span data-ttu-id="d44b8-137">Der Bericht führt die besten Übereinstimmungen oben im Bericht auf.</span><span class="sxs-lookup"><span data-stu-id="d44b8-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="d44b8-138">Sie können sehen, dass dort ein Lückenelement aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="d44b8-138">You can see that there is a gap element listed.</span></span>  <span data-ttu-id="d44b8-139">Dies ist die Differenz zwischen der Ebene, die auf der Qualifikationszuordnung aufgeführt war und der Ebene der Qualifikation, die der Person zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d44b8-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="d44b8-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d44b8-140">Close the page.</span></span>
25. <span data-ttu-id="d44b8-141">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d44b8-141">Click Save.</span></span>

