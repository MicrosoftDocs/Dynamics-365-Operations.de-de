---
title: Eine Frage mit vordefinierten Antworten erstellen
description: Fragen mit vordefinierten Antworten ermöglichen die Angabe von Optionen, aus denen der Befragte auswählen kann.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e4f9697fc00798d917db6f7f50d7e3b8739233
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507842"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="31602-103">Eine Frage mit vordefinierten Antworten erstellen</span><span class="sxs-lookup"><span data-stu-id="31602-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31602-104">Fragen mit vordefinierten Antworten ermöglichen die Angabe von Optionen, aus denen der Befragte auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="31602-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="31602-105">Zunächst müssen Sie die Antwortgruppe mit den Antworten erstellen, dann erstellen Sie die Frage, die die Antwortgruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="31602-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="31602-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="31602-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="31602-107">Erstellen einer Antwortgruppe</span><span class="sxs-lookup"><span data-stu-id="31602-107">Create an answer group</span></span>
1. <span data-ttu-id="31602-108">Wechseln Sie zu "Fragebogen" > "Entwurf" > "Antwortgruppen"</span><span class="sxs-lookup"><span data-stu-id="31602-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="31602-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="31602-109">Click New.</span></span>
3. <span data-ttu-id="31602-110">Geben Sie im Feld "Antwortgruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31602-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="31602-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31602-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="31602-112">Verwenden Sie die Randomisierungsfunktionen, um die Antworten bei jeder Verwendung der Antwortgruppe für eine Frage zufällig in einen anderen Reihenfolge anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="31602-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="31602-113">Klicken Sie auf "Antwort".</span><span class="sxs-lookup"><span data-stu-id="31602-113">Click Answer.</span></span>
6. <span data-ttu-id="31602-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="31602-114">Click New.</span></span>
    * <span data-ttu-id="31602-115">"Sequenznummer" steuert die Reihenfolge, in der die Antworten angezeigt werden, es sei denn, "Zufällig festlegen" wird für die Antwortgruppe ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="31602-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="31602-116">Punkte können zu den Antworten für den Fragebogen vergeben werden.</span><span class="sxs-lookup"><span data-stu-id="31602-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="31602-117">Geben Sie im Feld "Punkte" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="31602-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="31602-118">Die richtige Antwort kann markiert werden, um anzugeben, dass die ausgewählte Antwort richtig ist.</span><span class="sxs-lookup"><span data-stu-id="31602-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="31602-119">Dies kann auch für die Punktzahl im Fragebogen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31602-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="31602-120">Geben Sie im Feld "Antwort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31602-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="31602-121">Fahren Sie fort, Antwortauswahloptionen für die Antwortgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="31602-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="31602-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="31602-122">Click New.</span></span>
10. <span data-ttu-id="31602-123">Geben Sie im Feld "Punkte" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="31602-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="31602-124">Geben Sie im Feld "Antwort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31602-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="31602-125">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="31602-125">Click New.</span></span>
13. <span data-ttu-id="31602-126">Geben Sie im Feld "Punkte" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="31602-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="31602-127">Geben Sie im Feld "Antwort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31602-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="31602-128">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="31602-128">Click New.</span></span>
16. <span data-ttu-id="31602-129">Geben Sie im Feld "Punkte" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="31602-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="31602-130">Geben Sie im Feld "Antwort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31602-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="31602-131">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="31602-131">Click New.</span></span>
19. <span data-ttu-id="31602-132">Geben Sie im Feld "Punkte" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="31602-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="31602-133">Geben Sie im Feld "Antwort" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31602-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="31602-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="31602-134">Close the page.</span></span>
22. <span data-ttu-id="31602-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="31602-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="31602-136">Frage erstellen</span><span class="sxs-lookup"><span data-stu-id="31602-136">Create the question</span></span>
1. <span data-ttu-id="31602-137">Wechseln Sie zu "Fragebogen" > "Entwerfen" > "Fragen".</span><span class="sxs-lookup"><span data-stu-id="31602-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="31602-138">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="31602-138">Click New.</span></span>
3. <span data-ttu-id="31602-139">Verwenden Sie das Feld "Typ", um zusammenhängende Fragen zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="31602-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="31602-140">Sie können Kontrollkästchen, alternative Schaltflächen oder Kombinationsfelder für Fragen mit vordefinierten Antworten als Eingabetypen verwenden.</span><span class="sxs-lookup"><span data-stu-id="31602-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="31602-141">Wählen Sie im Feld "Eingabetyp" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="31602-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="31602-142">Geben Sie im Feld "Antwortgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="31602-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="31602-143">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="31602-143">In the Text field, type a value.</span></span>

