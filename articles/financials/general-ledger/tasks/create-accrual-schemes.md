---
title: Erstellen von Abgrenzungsschemata
description: Dieser Aufgabenleitfaden führt Sie durch die Erstellung eines Abgrenzungsschemas.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce96ccfb0dc3e4a723af967147dae93772c5b44f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355287"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="6b79b-103">Erstellen von Abgrenzungsschemata</span><span class="sxs-lookup"><span data-stu-id="6b79b-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b79b-104">Dieser Aufgabenleitfaden führt Sie durch die Erstellung eines Abgrenzungsschemas.</span><span class="sxs-lookup"><span data-stu-id="6b79b-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="6b79b-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b79b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6b79b-106">Wechseln Sie zu "Hauptbuch" > "Journaleinrichtung" > "Abgrenzungsschemas".</span><span class="sxs-lookup"><span data-stu-id="6b79b-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="6b79b-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6b79b-107">Click New.</span></span>
3. <span data-ttu-id="6b79b-108">Geben Sie im Feld "Abgrenzungskennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6b79b-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="6b79b-109">Geben Sie im Feld "Beschreibung des Abgrenzungsschemas" eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="6b79b-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="6b79b-110">Geben Sie im Feld "Soll" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="6b79b-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="6b79b-111">Das Hauptkonto ersetzt das Sollhauptkonto auf der Erfassungsbelegposition und es wird auch für die Rückbuchung der Stundung auf Grundlage die Sachkontoabgrenzungsbuchungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b79b-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="6b79b-112">Geben Sie im Feld "Haben" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="6b79b-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="6b79b-113">Das Hauptkonto ersetzt das Habenhauptkonto auf der Erfassungsbelegposition und es wird auch für die Rückbuchung der Stundung auf Grundlage die Sachkontoabgrenzungsbuchungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b79b-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="6b79b-114">Wählen Sie im Feld "Beleg", wie der spezifischen Beleg festgelegt werden soll, wenn die Buchungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="6b79b-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="6b79b-115">Geben Sie im Feld "Beschreibung" einen Wert ein, um die Buchungen zu beschreiben, die gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="6b79b-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="6b79b-116">Wählen Sie im Feld "Periodenhäufigkeit" aus, wie häufig die Buchungen erfolgen sollen.</span><span class="sxs-lookup"><span data-stu-id="6b79b-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="6b79b-117">Geben Sie im Feld "Anzahl der Vorkommen nach Periode" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="6b79b-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="6b79b-118">Wählen Sie im Feld "Transaktionen buchen" wann die Buchungen gebucht werden sollen (z. b. monatlich).</span><span class="sxs-lookup"><span data-stu-id="6b79b-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>

