--- 
title: "Strukturen für erweiterte Regeln erstellen und zuweisen"
description: "Dieser Aufgabenleitfaden führt Sie durch das Erstellen und Zuweisen einer erweiterten Regelstruktur zu einer Kontostruktur."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="c5edc-103">Strukturen für erweiterte Regeln erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="c5edc-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5edc-104">Dieser Aufgabenleitfaden führt Sie durch das Erstellen und Zuweisen einer erweiterten Regelstruktur zu einer Kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="c5edc-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="c5edc-105">Dieser Leitfaden verwendet das Demounternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="c5edc-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="c5edc-106">Struktur für erweiterte Regeln erstellen</span><span class="sxs-lookup"><span data-stu-id="c5edc-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="c5edc-107">Wechseln Sie zu "Hauptbuch" > "Kontenplan" > "Strukturen" > "Erweiterte Regelstrukturen".</span><span class="sxs-lookup"><span data-stu-id="c5edc-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="c5edc-108">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5edc-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="c5edc-109">Geben Sie im Feld "Erweiterte Regelstruktur" einen Namen für die Regelstruktur ein.</span><span class="sxs-lookup"><span data-stu-id="c5edc-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="c5edc-110">Geben Sie im Feld "Beschreibung" einen Wert ein, um die Struktur zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c5edc-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="c5edc-111">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c5edc-111">Click OK.</span></span>
6. <span data-ttu-id="c5edc-112">Klicken Sie auf "Segment hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c5edc-112">Click Add segment.</span></span>
7. <span data-ttu-id="c5edc-113">Wählen Sie eine Segmentliste eine Finanzdimension aus.</span><span class="sxs-lookup"><span data-stu-id="c5edc-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="c5edc-114">Beispielsweise "Shop".</span><span class="sxs-lookup"><span data-stu-id="c5edc-114">For example, Store.</span></span>  
8. <span data-ttu-id="c5edc-115">Klicken Sie auf "Segment hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c5edc-115">Click Add segment.</span></span>
9. <span data-ttu-id="c5edc-116">Klicken Sie in der Liste auf den Link zur erweiterten Regelstruktur, um sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c5edc-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="c5edc-117">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5edc-117">Click Activate.</span></span>
11. <span data-ttu-id="c5edc-118">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5edc-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="c5edc-119">Anwenden einer erweiterten Regelstruktur auf eine Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="c5edc-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="c5edc-120">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="c5edc-120">Close the form.</span></span>
2. <span data-ttu-id="c5edc-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c5edc-121">Close the page.</span></span>
3. <span data-ttu-id="c5edc-122">Wechseln Sie zu Hauptbuch > Kontenplan > Strukturen > Kontostrukturen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c5edc-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="c5edc-123">Wählen Sie in der Liste die Kontostruktur aus, auf die Sie die erweiterte Regel anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c5edc-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="c5edc-124">Klicken Sie auf den Namen der Kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="c5edc-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="c5edc-125">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="c5edc-125">Click Edit.</span></span>
    * <span data-ttu-id="c5edc-126">Sie können auch auf "Erweiterte Regeln" klicken und die Kontostruktur im Entwurfsmodus einfügen.</span><span class="sxs-lookup"><span data-stu-id="c5edc-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="c5edc-127">Klicken Sie auf "Erweiterte Regeln".</span><span class="sxs-lookup"><span data-stu-id="c5edc-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="c5edc-128">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5edc-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="c5edc-129">Geben Sie im Feld "Erweiterte Regeln" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c5edc-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="c5edc-130">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c5edc-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="c5edc-131">Klicken Sie auf Erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5edc-131">Click Create.</span></span>
12. <span data-ttu-id="c5edc-132">Klicken Sie auf "Neue Kriterien hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c5edc-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="c5edc-133">Wählen Sie im Feld "Wo" "Hauptkonto" oder "Finanzdimension" aus.</span><span class="sxs-lookup"><span data-stu-id="c5edc-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="c5edc-134">Wählen Sie im Feld "Operator" eine Option aus (z. B., "liegt zwischen" und "schließt ein").</span><span class="sxs-lookup"><span data-stu-id="c5edc-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="c5edc-135">Geben Sie im Feld "Wert" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c5edc-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="c5edc-136">Geben Sie im Feld "bis" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c5edc-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="c5edc-137">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c5edc-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="c5edc-138">Wählen Sie in der Liste die erweiterte Regelstruktur aus, die Sie verwenden möchten, wenn das eingegebene Kriterium erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="c5edc-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="c5edc-139">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5edc-139">Click Add.</span></span>
20. <span data-ttu-id="c5edc-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c5edc-140">Close the page.</span></span>
21. <span data-ttu-id="c5edc-141">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5edc-141">Click Activate.</span></span>
22. <span data-ttu-id="c5edc-142">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5edc-142">Click Activate.</span></span>


