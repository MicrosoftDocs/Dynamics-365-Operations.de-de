--- 
title: Erstellen von Abgrenzungsschemata
description: "Dieser Aufgabenleitfaden führt Sie durch die Erstellung eines Abgrenzungsschemas."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="ce060-103">Erstellen von Abgrenzungsschemata</span><span class="sxs-lookup"><span data-stu-id="ce060-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce060-104">Dieser Aufgabenleitfaden führt Sie durch die Erstellung eines Abgrenzungsschemas.</span><span class="sxs-lookup"><span data-stu-id="ce060-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="ce060-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce060-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ce060-106">Wechseln Sie zu "Hauptbuch" > "Journaleinrichtung" > "Abgrenzungsschemas".</span><span class="sxs-lookup"><span data-stu-id="ce060-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="ce060-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ce060-107">Click New.</span></span>
3. <span data-ttu-id="ce060-108">Geben Sie im Feld "Abgrenzungskennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ce060-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="ce060-109">Geben Sie im Feld "Beschreibung des Abgrenzungsschemas" eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="ce060-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="ce060-110">Geben Sie im Feld "Soll" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="ce060-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="ce060-111">Das Hauptkonto ersetzt das Sollhauptkonto auf der Erfassungsbelegposition und es wird auch für die Rückbuchung der Stundung auf Grundlage die Sachkontoabgrenzungsbuchungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce060-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="ce060-112">Geben Sie im Feld "Haben" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="ce060-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="ce060-113">Das Hauptkonto ersetzt das Habenhauptkonto auf der Erfassungsbelegposition und es wird auch für die Rückbuchung der Stundung auf Grundlage die Sachkontoabgrenzungsbuchungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce060-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="ce060-114">Wählen Sie im Feld "Beleg", wie der spezifischen Beleg festgelegt werden soll, wenn die Buchungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ce060-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="ce060-115">Geben Sie im Feld "Beschreibung" einen Wert ein, um die Buchungen zu beschreiben, die gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ce060-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="ce060-116">Wählen Sie im Feld "Periodenhäufigkeit" aus, wie häufig die Buchungen erfolgen sollen.</span><span class="sxs-lookup"><span data-stu-id="ce060-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="ce060-117">Geben Sie im Feld "Anzahl der Vorkommen nach Periode" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ce060-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="ce060-118">Wählen Sie im Feld "Transaktionen buchen" wann die Buchungen gebucht werden sollen (z. b. monatlich).</span><span class="sxs-lookup"><span data-stu-id="ce060-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


