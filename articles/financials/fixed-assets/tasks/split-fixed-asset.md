---
title: Eine Anlage splitten
description: In dieser Aufgabenanleitung wird ein Prozentanteil eines Anlagenbuches zu einem neuen Anlagenbuch aufgeteilt.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566891"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="0d12f-103">Eine Anlage splitten</span><span class="sxs-lookup"><span data-stu-id="0d12f-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d12f-104">In dieser Aufgabenanleitung wird ein Prozentanteil eines Anlagenbuches zu einem neuen Anlagenbuch aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="0d12f-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="0d12f-105">Dabei werden die "Buchhalterrolle" und die USMF-Demodaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d12f-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="0d12f-106">Neue Anlage erstellen</span><span class="sxs-lookup"><span data-stu-id="0d12f-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="0d12f-107">Wechseln Sie zu Anlagen > Anlagen > Anlagen.</span><span class="sxs-lookup"><span data-stu-id="0d12f-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="0d12f-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0d12f-108">Click New.</span></span>
3. <span data-ttu-id="0d12f-109">Geben Sie im Feld "Anlagengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0d12f-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="0d12f-110">Notieren Sie sich die Anlagennummer, die später im Teilungsprozess zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="0d12f-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="0d12f-111">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0d12f-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0d12f-112">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="0d12f-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="0d12f-113">Eine Anlage splitten</span><span class="sxs-lookup"><span data-stu-id="0d12f-113">Split a fixed asset</span></span>
1. <span data-ttu-id="0d12f-114">Suchen Sie in der Liste die zu teilende Anlage und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="0d12f-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="0d12f-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0d12f-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0d12f-116">Klicken Sie auf Bücher.</span><span class="sxs-lookup"><span data-stu-id="0d12f-116">Click Books.</span></span>
    * <span data-ttu-id="0d12f-117">Wählen Sie das Buch aus, um die neue Anlage aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="0d12f-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="0d12f-118">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0d12f-118">Click Functions.</span></span>
5. <span data-ttu-id="0d12f-119">Klicken Sie auf "Anlage aufteilen".</span><span class="sxs-lookup"><span data-stu-id="0d12f-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="0d12f-120">Geben Sie im Feld "Zielanlage" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0d12f-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="0d12f-121">Klicken Sie im Feld An Buch auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0d12f-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0d12f-122">Geben Sie im Feld "Transaktionsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0d12f-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="0d12f-123">Geben Sie im Feld "Prozent" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0d12f-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="0d12f-124">Geben Sie im Feld 'Journal' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0d12f-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="0d12f-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0d12f-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="0d12f-126">Die Erfassungstransaktion buchen</span><span class="sxs-lookup"><span data-stu-id="0d12f-126">Post the journal transaction</span></span>
1. <span data-ttu-id="0d12f-127">Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".</span><span class="sxs-lookup"><span data-stu-id="0d12f-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="0d12f-128">Wählen Sie in der Liste die Erfassung aus, die mit dem Teilungsprozess erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0d12f-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="0d12f-129">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="0d12f-129">Click Lines.</span></span>
    * <span data-ttu-id="0d12f-130">Überprüfen Sie die erstellten Erfassungspositionen.</span><span class="sxs-lookup"><span data-stu-id="0d12f-130">Verify the journal lines created.</span></span>  <span data-ttu-id="0d12f-131">Eine "Anschaffungsänderungstransaktion" wird für die ursprüngliche Anlage erstellt, um den Wert um den Prozentsatz zu verringern, der im Teilungsprozess angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d12f-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="0d12f-132">Eine "Anschaffungstransaktion" wird für die neue Anlage für denselben Betrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d12f-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="0d12f-133">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="0d12f-133">Click Post.</span></span>

