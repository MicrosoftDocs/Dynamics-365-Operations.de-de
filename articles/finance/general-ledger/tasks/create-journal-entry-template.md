---
title: Erstellen von Journaleinträgen mithilfe einer Vorlage
description: Gebuchte Erfassungsbelege können als Belegvorlagen gespeichert und in einem neuen Erfassungsbeleg angewendet werden.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3843c165b3fc3030a937ec47a1439b1c1b36206d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216497"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="9166b-103">Erstellen von Journaleinträgen mithilfe einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="9166b-103">Create a journal entry using template</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9166b-104">Gebuchte Erfassungsbelege können als Belegvorlagen gespeichert und in einem neuen Erfassungsbeleg angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9166b-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="9166b-105">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="9166b-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="9166b-106">Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Journaleinträge > Allgemeine Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="9166b-106">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="9166b-107">Klicken Sie im **Aktivitätsbereich** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="9166b-107">On the **Action pane**, click **New**.</span></span> <span data-ttu-id="9166b-108">Diese Prozedur beginnt, indem Sie einen Erfassungsbeleg erstellen und buchen, aber jeder bereits gebuchte Erfassungsbeleg kann als Vorlage gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9166b-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
3. <span data-ttu-id="9166b-109">Klicken Sie im Feld **Name** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9166b-109">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9166b-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9166b-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9166b-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9166b-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9166b-112">Klicken Sie auf **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="9166b-112">Click **Lines**.</span></span>
7. <span data-ttu-id="9166b-113">Geben Sie im Feld **Kontenart** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9166b-113">In the **Account type** field, type a value.</span></span>
8. <span data-ttu-id="9166b-114">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9166b-114">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="9166b-115">Geben Sie im Feld **Soll** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9166b-115">In the **Debit** field, type a value.</span></span>
10. <span data-ttu-id="9166b-116">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="9166b-116">Click **New**.</span></span>
11. <span data-ttu-id="9166b-117">Geben Sie im Feld **Kontenart** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9166b-117">In the **Account type** field, type a value.</span></span>
12. <span data-ttu-id="9166b-118">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9166b-118">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="9166b-119">Geben Sie im Feld **Soll** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9166b-119">In the **Debit** field, type a value.</span></span>
14. <span data-ttu-id="9166b-120">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="9166b-120">Click **New**.</span></span>
14. <span data-ttu-id="9166b-121">Geben Sie im Feld **Konto** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="9166b-121">In the **Account** field, specify the desired values.</span></span>
15. <span data-ttu-id="9166b-122">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9166b-122">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="9166b-123">Geben Sie im Feld **Gutschrift** einen Wert ein, um den Beleg auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="9166b-123">In the **Credit** field, type a value to balance the voucher.</span></span>
17. <span data-ttu-id="9166b-124">Klicken Sie im **Aktivitätsbereich** auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="9166b-124">On the **Action pane**, click **Post**.</span></span>
18. <span data-ttu-id="9166b-125">Klicken Sie auf **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="9166b-125">Click **Functions**.</span></span>
19. <span data-ttu-id="9166b-126">Klicken Sie auf **Belegvorlage speichern**.</span><span class="sxs-lookup"><span data-stu-id="9166b-126">Click **Save voucher** template.</span></span>
20. <span data-ttu-id="9166b-127">Bei dieser Prozedur wird ein Typ **Prozentvorlage** angenommen.</span><span class="sxs-lookup"><span data-stu-id="9166b-127">This procedure assumes a **Percent Template** type.</span></span> <span data-ttu-id="9166b-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9166b-128">Click OK.</span></span>
    - <span data-ttu-id="9166b-129">Prozent: Die Beträge im Beleg werden in Prozentsatzfaktoren konvertiert, wodurch jeder Betrag angewendet werden kann, wenn die Vorlage „Beleg“ ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="9166b-129">Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>
    - <span data-ttu-id="9166b-130">Betrag: Die tatsächlichen Beträge werden gespeichert und angewendet.</span><span class="sxs-lookup"><span data-stu-id="9166b-130">Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="9166b-131">Klicken Sie auf **Allgemeine Erfassungen**.</span><span class="sxs-lookup"><span data-stu-id="9166b-131">Click **General journals**.</span></span>
22. <span data-ttu-id="9166b-132">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="9166b-132">Click **New**.</span></span>
23. <span data-ttu-id="9166b-133">Klicken Sie im Feld **Name** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9166b-133">In the **Name** field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="9166b-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="9166b-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="9166b-135">Klicken Sie auf **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="9166b-135">Click **Lines**.</span></span>
26. <span data-ttu-id="9166b-136">Klicken Sie auf **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="9166b-136">Click **Functions**.</span></span>
27. <span data-ttu-id="9166b-137">Klicken Sie auf **Belegvorlage auswählen**.</span><span class="sxs-lookup"><span data-stu-id="9166b-137">Click **Select voucher template**.</span></span>
28. <span data-ttu-id="9166b-138">Suchen Sie die Vorlage, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="9166b-138">Find the template that you created earlier.</span></span> <span data-ttu-id="9166b-139">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9166b-139">Click **OK**.</span></span> <span data-ttu-id="9166b-140">Sie müssen möglicherweise auf **Vorheriger Schritt** klicken und dann die richtige Vorlage auswählen, wenn andere Vorlagen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9166b-140">You may need to click **Previous step** and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="9166b-141">Geben Sie im Feld **Betrag** den Betrag ein, der auf den Beleg angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9166b-141">In the **Amount** field, enter the amount to be applied to the voucher.</span></span> <span data-ttu-id="9166b-142">Das Feld **Betrag** wird nur angezeigt, wenn die Belegvorlage vom Typ „Prozent“ ist.</span><span class="sxs-lookup"><span data-stu-id="9166b-142">The **Amount** field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="9166b-143">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9166b-143">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]