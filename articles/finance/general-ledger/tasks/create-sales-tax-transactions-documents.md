---
title: Mehrwertsteuerbuchungen in Dokumenten erstellen
description: Mehrwertsteuer zu Dokumenten wird berechnet, indem eine "Mehrwertsteuergruppe" und eine "Artikel-Mehrwertsteuergruppe" auf Dokumentpositionen bereitgestellt werden.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 061949dedde763c188e13c07cec750895cbef175
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836984"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="b8d71-103">Mehrwertsteuerbuchungen in Dokumenten erstellen</span><span class="sxs-lookup"><span data-stu-id="b8d71-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8d71-104">Mehrwertsteuer zu Dokumenten wird berechnet, indem eine "Mehrwertsteuergruppe" und eine "Artikel-Mehrwertsteuergruppe" auf Dokumentpositionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8d71-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="b8d71-105">Diese werden standardmäßig aus Masterdaten bereitgestellt, sie können aber bei Bedarf manuell geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b8d71-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="b8d71-106">Die berechnete Mehrwertsteuer kann auf einer Positions und einer Dokumentebene überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="b8d71-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="b8d71-107">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8d71-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b8d71-108">Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="b8d71-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b8d71-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b8d71-109">Click New.</span></span>
3. <span data-ttu-id="b8d71-110">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8d71-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b8d71-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b8d71-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b8d71-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8d71-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b8d71-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b8d71-113">Click OK.</span></span>
7. <span data-ttu-id="b8d71-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8d71-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b8d71-115">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8d71-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b8d71-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8d71-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b8d71-117">Geben Sie im Feld "Einzelpreis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b8d71-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="b8d71-118">Erweitern oder reduzieren Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="b8d71-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="b8d71-119">Klicken Sie auf die Registerkarte Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b8d71-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="b8d71-120">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8d71-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b8d71-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b8d71-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b8d71-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8d71-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b8d71-123">Klicken Sie auf "Finanzdaten".</span><span class="sxs-lookup"><span data-stu-id="b8d71-123">Click Financials.</span></span>
17. <span data-ttu-id="b8d71-124">Klicken Sie auf "Mehrwertsteuer".</span><span class="sxs-lookup"><span data-stu-id="b8d71-124">Click Sales tax.</span></span>
18. <span data-ttu-id="b8d71-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b8d71-125">Click OK.</span></span>
19. <span data-ttu-id="b8d71-126">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b8d71-126">Click Add line.</span></span>
20. <span data-ttu-id="b8d71-127">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8d71-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="b8d71-128">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8d71-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="b8d71-129">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b8d71-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="b8d71-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8d71-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="b8d71-131">Geben Sie im Feld "Einzelpreis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b8d71-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="b8d71-132">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b8d71-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="b8d71-133">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b8d71-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="b8d71-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8d71-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="b8d71-135">Klicken Sie im Aktivitätsbereich auf "Verkaufen".</span><span class="sxs-lookup"><span data-stu-id="b8d71-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="b8d71-136">Klicken Sie auf "Mehrwertsteuer".</span><span class="sxs-lookup"><span data-stu-id="b8d71-136">Click Sales tax.</span></span>
30. <span data-ttu-id="b8d71-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b8d71-137">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]