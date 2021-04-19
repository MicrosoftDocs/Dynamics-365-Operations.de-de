---
title: Strukturen für erweiterte Regeln erstellen und zuweisen
description: In diesem Thema wird erläutert, wie Sie eine erweiterte Regelstruktur erstellen und einer Kontostruktur zuweisen.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b81e3cc169bf0164af0b9c4de4faeb936df6784
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837056"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="11ad5-103">Strukturen für erweiterte Regeln erstellen und zuweisen</span><span class="sxs-lookup"><span data-stu-id="11ad5-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11ad5-104">In diesem Thema wird erläutert, wie Sie eine erweiterte Regelstruktur erstellen und einer Kontostruktur zuweisen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="11ad5-105">Dieser Leitfaden verwendet das Demounternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="11ad5-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="11ad5-106">Struktur für erweiterte Regeln erstellen</span><span class="sxs-lookup"><span data-stu-id="11ad5-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="11ad5-107">Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Strukturen > Erweiterte Regelstrukturen**.</span><span class="sxs-lookup"><span data-stu-id="11ad5-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="11ad5-108">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="11ad5-109">Geben Sie im Feld **Erweiterte Regelstruktur** einen Namen zur Beschreibung der Regelstruktur ein.</span><span class="sxs-lookup"><span data-stu-id="11ad5-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="11ad5-110">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="11ad5-110">Select **OK**.</span></span>
5. <span data-ttu-id="11ad5-111">Wählen Sie **Segment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="11ad5-112">Wählen Sie eine Segmentliste eine Finanzdimension aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="11ad5-113">Zum Beispiel **Shop**.</span><span class="sxs-lookup"><span data-stu-id="11ad5-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="11ad5-114">Wählen Sie **Segment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="11ad5-115">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="11ad5-116">Anwenden einer erweiterten Regelstruktur auf eine Kontostruktur</span><span class="sxs-lookup"><span data-stu-id="11ad5-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="11ad5-117">Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Strukturen > Kontostrukturen konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="11ad5-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="11ad5-118">Wählen Sie in der Liste die Kontostruktur aus, auf die Sie die erweiterte Regel anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="11ad5-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="11ad5-119">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-119">Select **Edit**.</span></span> <span data-ttu-id="11ad5-120">Sie können auch **Erweiterte Regeln** auswählen. Sie werden dann aufgefordert, die Kontostruktur im **Entwurfsmodus** einzufügen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="11ad5-121">Wählen Sie **Erweiterte Regeln** aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="11ad5-122">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="11ad5-123">Geben Sie im Feld **Erweiterte Regel** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11ad5-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="11ad5-124">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11ad5-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="11ad5-125">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-125">Select **Create**.</span></span>
9. <span data-ttu-id="11ad5-126">Wählen Sie **Neue Kriterien hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="11ad5-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="11ad5-127">Wählen Sie im Feld **Wo** das Hauptkonto oder eine Finanzdimension aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="11ad5-128">Wählen Sie im Feld **Operator** eine Option aus (z. B. **ist zwischen** und **enthält**).</span><span class="sxs-lookup"><span data-stu-id="11ad5-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="11ad5-129">Geben Sie im Feld **Wert** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11ad5-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="11ad5-130">Geben Sie im Feld **Bis** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11ad5-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="11ad5-131">Wählen Sie **Hinzufügen**, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="11ad5-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="11ad5-132">Wählen Sie in der Liste die erweiterte Regelstruktur aus, die Sie verwenden möchten, wenn das eingegebene Kriterium erfüllt wird.</span><span class="sxs-lookup"><span data-stu-id="11ad5-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="11ad5-133">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-133">Select **Add**.</span></span>
17. <span data-ttu-id="11ad5-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="11ad5-134">Close the page.</span></span>
18. <span data-ttu-id="11ad5-135">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="11ad5-135">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]