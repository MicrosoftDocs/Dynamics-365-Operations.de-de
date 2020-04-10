---
title: Erstellen Sie ein Originalbudget und machen Sie dann vorläufige Budgeteinträge im öffentlichen Sektor rückgängig
description: Wenn Sie einen Budgeteintrag erstellen und die Budgetmodell- und Dimensionswerte verwenden, die vorläufige Budgetbeträge enthalten, dann werden die vorläufigen Budgetbeträge rückgängig gemacht.
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
ms.openlocfilehash: 32d89216d49a743729de8910f738276cbddcd8bb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144553"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="3406b-103">Erstellen Sie ein Originalbudget und machen Sie dann vorläufige Budgeteinträge im öffentlichen Sektor rückgängig</span><span class="sxs-lookup"><span data-stu-id="3406b-103">Create an original budget and then reverse preliminary budget entries in the public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3406b-104">Wenn Sie einen Budgeteintrag erstellen und die Budgetmodell- und Dimensionswerte verwenden, die vorläufige Budgetbeträge enthalten, dann werden die vorläufigen Budgetbeträge rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="3406b-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="3406b-105">Diese Prozedur wurde unter Verwendung der PSUS-Vorführungsunternehmensdaten in der Partition "Öffentlicher Sektor" erstellt.</span><span class="sxs-lookup"><span data-stu-id="3406b-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="3406b-106">Wechseln Sie zu "Budgetierung" > "Budgetregistereinträge".</span><span class="sxs-lookup"><span data-stu-id="3406b-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="3406b-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3406b-107">Click New.</span></span>
3. <span data-ttu-id="3406b-108">Klicken Sie im Feld "Budgetmodell" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3406b-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3406b-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="3406b-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3406b-110">Klicken Sie im Feld "Budgetcode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3406b-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3406b-111">Klicken Sie in der Liste auf "Ursprüngliches Budget".</span><span class="sxs-lookup"><span data-stu-id="3406b-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="3406b-112">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="3406b-112">Click Save.</span></span>
8. <span data-ttu-id="3406b-113">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="3406b-113">Click Add line.</span></span>
9. <span data-ttu-id="3406b-114">Optional: Wenn Sie das Datum im Kopfbereich ändern möchten, geben Sie ein neues Datum.</span><span class="sxs-lookup"><span data-stu-id="3406b-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="3406b-115">Dieses Datum bestimmt den Finanzzeitraum, für den das Budget erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="3406b-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="3406b-116">Klicken Sie im Feld "Kontenstruktur" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3406b-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="3406b-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="3406b-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="3406b-118">Geben Sie im Feld "Dimensionswerte" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="3406b-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="3406b-119">Geben Sie im Feld "Betrag" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="3406b-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="3406b-120">Klicken Sie im Feld "Währung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3406b-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="3406b-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3406b-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="3406b-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="3406b-122">Click Save.</span></span>
17. <span data-ttu-id="3406b-123">Klicken Sie auf "Budgetsalden aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="3406b-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="3406b-124">Optional: Sie können die Option "Vorläufiges Budget rückgängig machen" auswählen.</span><span class="sxs-lookup"><span data-stu-id="3406b-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="3406b-125">Beachten Sie, dass Sie alle vorläufigen Budgeteinträge rückgängig machen können, oder nur die vorläufigen Budgeteinträge, die den Budgetcode haben, den Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="3406b-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="3406b-126">Um eine optionale Auswahl zu treffen, klicken Sie auf das Entsperren-Symbol am oberen Seitenrand.</span><span class="sxs-lookup"><span data-stu-id="3406b-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="3406b-127">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3406b-127">Click Update.</span></span>

