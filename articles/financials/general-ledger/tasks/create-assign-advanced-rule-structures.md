---
title: Strukturen für erweiterte Regeln erstellen und zuweisen
description: In diesem Thema wird erläutert, wie Sie eine erweiterte Regelstruktur erstellen und einer Kontostruktur zuweisen.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cff07c13553ea140f537160da7f93820d5e3f77a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834890"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="92e6b-103">Strukturen für erweiterte Regeln erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="92e6b-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92e6b-104">In diesem Thema wird erläutert, wie Sie eine erweiterte Regelstruktur erstellen und einer Kontostruktur zuweisen.</span><span class="sxs-lookup"><span data-stu-id="92e6b-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="92e6b-105">Dieser Leitfaden verwendet das Demounternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="92e6b-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="92e6b-106">Struktur für erweiterte Regeln erstellen</span><span class="sxs-lookup"><span data-stu-id="92e6b-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="92e6b-107">Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Strukturen > Erweiterte Regelstrukturen**.</span><span class="sxs-lookup"><span data-stu-id="92e6b-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="92e6b-108">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="92e6b-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="92e6b-109">Geben Sie im Feld **Erweiterte Regelstruktur** einen Namen zur Beschreibung der Regelstruktur ein.</span><span class="sxs-lookup"><span data-stu-id="92e6b-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="92e6b-110">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="92e6b-110">Select **OK**.</span></span>
5. <span data-ttu-id="92e6b-111">Wählen Sie **Segment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="92e6b-112">Wählen Sie eine Segmentliste eine Finanzdimension aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="92e6b-113">Zum Beispiel **Shop**.</span><span class="sxs-lookup"><span data-stu-id="92e6b-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="92e6b-114">Wählen Sie **Segment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="92e6b-115">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="92e6b-116">Anwenden einer erweiterten Regelstruktur auf eine Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="92e6b-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="92e6b-117">Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Strukturen > Kontostrukturen konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="92e6b-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="92e6b-118">Wählen Sie in der Liste die Kontostruktur aus, auf die Sie die erweiterte Regel anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="92e6b-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="92e6b-119">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-119">Select **Edit**.</span></span> <span data-ttu-id="92e6b-120">Sie können auch **Erweiterte Regeln** auswählen. Sie werden dann aufgefordert, die Kontostruktur im **Entwurfsmodus** einzufügen.</span><span class="sxs-lookup"><span data-stu-id="92e6b-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="92e6b-121">Wählen Sie **Erweiterte Regeln** aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="92e6b-122">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="92e6b-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="92e6b-123">Geben Sie im Feld **Erweiterte Regel** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="92e6b-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="92e6b-124">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="92e6b-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="92e6b-125">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-125">Select **Create**.</span></span>
9. <span data-ttu-id="92e6b-126">Wählen Sie **Neue Kriterien hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="92e6b-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="92e6b-127">Wählen Sie im Feld **Wo** das Hauptkonto oder eine Finanzdimension aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="92e6b-128">Wählen Sie im Feld **Operator** eine Option aus (z. B. **ist zwischen** und **enthält**).</span><span class="sxs-lookup"><span data-stu-id="92e6b-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="92e6b-129">Geben Sie im Feld **Wert** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="92e6b-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="92e6b-130">Geben Sie im Feld **Bis** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="92e6b-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="92e6b-131">Wählen Sie **Hinzufügen**, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="92e6b-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="92e6b-132">Wählen Sie in der Liste die erweiterte Regelstruktur aus, die Sie verwenden möchten, wenn das eingegebene Kriterium erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="92e6b-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="92e6b-133">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-133">Select **Add**.</span></span>
17. <span data-ttu-id="92e6b-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="92e6b-134">Close the page.</span></span>
18. <span data-ttu-id="92e6b-135">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="92e6b-135">Select **Activate**.</span></span>

