---
title: Erstellen eines vorläufigen Budgets für den "Öffentlichen Sektor"
description: Sie können vorläufige Budgetregistereinträge für ein bestimmtes Budgetmodell und Dimensionswerte erstellen.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 800b7009f023bd2a0d8437b81d82c0e9de770841
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174373"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="ae047-103">Erstellen eines vorläufigen Budgets für den "Öffentlichen Sektor"</span><span class="sxs-lookup"><span data-stu-id="ae047-103">Create a preliminary budget for Public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae047-104">Sie können vorläufige Budgetregistereinträge für ein bestimmtes Budgetmodell und Dimensionswerte erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae047-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="ae047-105">Nachdem das tatsächliche Budget genehmigt wurde, können Sie ursprüngliche Budgetregistereinträge mit erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae047-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="ae047-106">Diese Prozedur wurde unter Verwendung der PSUS-Vorführungsunternehmensdaten in der Partition "Öffentlicher Sektor" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ae047-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="ae047-107">Wechseln Sie zu "Budgetierung" > "Budgetregistereinträge".</span><span class="sxs-lookup"><span data-stu-id="ae047-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="ae047-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ae047-108">Click New.</span></span>
3. <span data-ttu-id="ae047-109">Klicken Sie im Feld "Budgetmodell" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae047-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ae047-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ae047-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ae047-111">Klicken Sie im Feld "Budgetcode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae047-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ae047-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ae047-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ae047-113">Klicken Sie im Feld "Ursachencode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae047-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ae047-114">Klicken Sie in der Liste auf den gewünschten Datensatz.</span><span class="sxs-lookup"><span data-stu-id="ae047-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="ae047-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ae047-115">Click Save.</span></span>
10. <span data-ttu-id="ae047-116">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="ae047-116">Click Add line.</span></span>
    * <span data-ttu-id="ae047-117">Optional: Wenn Sie das Datum im Kopfbereich ändern möchten, geben Sie ein neues Datum.</span><span class="sxs-lookup"><span data-stu-id="ae047-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="ae047-118">Dieses Datum bestimmt den Finanzzeitraum, für den das Budget erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="ae047-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="ae047-119">Wenn Sie den Aufgabenleitfaden anzeigt, um andere Felder auszufüllen, klicken Sie oben auf der Seite auf "Entsperren.</span><span class="sxs-lookup"><span data-stu-id="ae047-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="ae047-120">Klicken Sie im Feld "Kontenstruktur" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae047-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="ae047-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ae047-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="ae047-122">Geben Sie im Feld "Dimensionswerte" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="ae047-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="ae047-123">Geben Sie im Feld "Betrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ae047-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="ae047-124">Sie können auch einen Betragstyp eingeben.</span><span class="sxs-lookup"><span data-stu-id="ae047-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="ae047-125">Klicken Sie im Feld "Währung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae047-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="ae047-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ae047-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ae047-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ae047-127">Click Save.</span></span>
18. <span data-ttu-id="ae047-128">Klicken Sie auf "Budgetsalden aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="ae047-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="ae047-129">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ae047-129">Click Update.</span></span>
    * <span data-ttu-id="ae047-130">Um die Ergebnisse der Aktualisierung anzuzeigen, klicken Sie auf der blauen Leiste auf "Meldungsdetails".</span><span class="sxs-lookup"><span data-stu-id="ae047-130">To see the results of the update, click Message details on the blue bar.</span></span>  

