---
title: Mehrwertsteuerbuchungen in Dokumenten erstellen
description: Mehrwertsteuer zu Dokumenten wird berechnet, indem eine "Mehrwertsteuergruppe" und eine "Artikel-Mehrwertsteuergruppe" auf Dokumentpositionen bereitgestellt werden.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc4b5c31d9a478a5226ae6b5e8c776de3b661dd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144834"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="97425-103">Mehrwertsteuerbuchungen in Dokumenten erstellen</span><span class="sxs-lookup"><span data-stu-id="97425-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97425-104">Mehrwertsteuer zu Dokumenten wird berechnet, indem eine "Mehrwertsteuergruppe" und eine "Artikel-Mehrwertsteuergruppe" auf Dokumentpositionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="97425-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="97425-105">Diese werden standardmäßig aus Masterdaten bereitgestellt, sie können aber bei Bedarf manuell geändert werden.</span><span class="sxs-lookup"><span data-stu-id="97425-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="97425-106">Die berechnete Mehrwertsteuer kann auf einer Positions und einer Dokumentebene überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="97425-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="97425-107">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="97425-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="97425-108">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="97425-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="97425-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="97425-109">Click New.</span></span>
3. <span data-ttu-id="97425-110">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="97425-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="97425-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="97425-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="97425-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="97425-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="97425-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="97425-113">Click OK.</span></span>
7. <span data-ttu-id="97425-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="97425-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="97425-115">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="97425-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="97425-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="97425-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="97425-117">Geben Sie im Feld "Einzelpreis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="97425-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="97425-118">Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="97425-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="97425-119">Klicken Sie auf die Registerkarte Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="97425-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="97425-120">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="97425-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="97425-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="97425-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="97425-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="97425-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="97425-123">Klicken Sie auf "Finanzdaten".</span><span class="sxs-lookup"><span data-stu-id="97425-123">Click Financials.</span></span>
17. <span data-ttu-id="97425-124">Klicken Sie auf "Mehrwertsteuer".</span><span class="sxs-lookup"><span data-stu-id="97425-124">Click Sales tax.</span></span>
18. <span data-ttu-id="97425-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="97425-125">Click OK.</span></span>
19. <span data-ttu-id="97425-126">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="97425-126">Click Add line.</span></span>
20. <span data-ttu-id="97425-127">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="97425-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="97425-128">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="97425-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="97425-129">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="97425-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="97425-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="97425-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="97425-131">Geben Sie im Feld "Einzelpreis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="97425-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="97425-132">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="97425-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="97425-133">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="97425-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="97425-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="97425-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="97425-135">Klicken Sie im Aktivitätsbereich auf "Verkaufen".</span><span class="sxs-lookup"><span data-stu-id="97425-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="97425-136">Klicken Sie auf "Mehrwertsteuer".</span><span class="sxs-lookup"><span data-stu-id="97425-136">Click Sales tax.</span></span>
30. <span data-ttu-id="97425-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="97425-137">Click OK.</span></span>

