---
title: Anlage teilen
description: In diesem Abschnitt wird erläutert, wie Sie einen Prozentsatz eines Anlagenbuchs in ein neues Anlagenbuch aufteilen.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138114"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="fe28d-103">Anlage teilen</span><span class="sxs-lookup"><span data-stu-id="fe28d-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe28d-104">In diesem Abschnitt wird erläutert, wie Sie einen Prozentsatz eines Anlagenbuchs in ein neues Anlagenbuch aufteilen.</span><span class="sxs-lookup"><span data-stu-id="fe28d-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="fe28d-105">Dabei werden die "Buchhalterrolle" und die USMF-Demodaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe28d-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="fe28d-106">Neue Anlage erstellen</span><span class="sxs-lookup"><span data-stu-id="fe28d-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="fe28d-107">Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Anlagen > Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="fe28d-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="fe28d-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fe28d-108">Select **New**.</span></span>
3. <span data-ttu-id="fe28d-109">Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fe28d-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="fe28d-110">Notieren Sie sich die Anlagennummer, die später im Teilungsprozess zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="fe28d-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="fe28d-111">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fe28d-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="fe28d-112">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="fe28d-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="fe28d-113">Anlage teilen</span><span class="sxs-lookup"><span data-stu-id="fe28d-113">Split a fixed asset</span></span>
1. <span data-ttu-id="fe28d-114">Suchen und wählen Sie in der Liste die Verknüpfung der zu teilenden Anlage.</span><span class="sxs-lookup"><span data-stu-id="fe28d-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="fe28d-115">Wählen Sie **Bücher**.</span><span class="sxs-lookup"><span data-stu-id="fe28d-115">Select **Books**.</span></span> <span data-ttu-id="fe28d-116">Wählen Sie das Buch aus, um die neue Anlage aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="fe28d-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="fe28d-117">Wählen Sie **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="fe28d-117">Select **Functions**.</span></span>
4. <span data-ttu-id="fe28d-118">Wählen Sie **Anlage teilen**.</span><span class="sxs-lookup"><span data-stu-id="fe28d-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="fe28d-119">Geben Sie im Feld **Zu Anlage** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="fe28d-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="fe28d-120">Wählen Sie im Feld **Zum Buch** die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fe28d-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fe28d-121">Geben Sie im Feld **Transaktionsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="fe28d-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="fe28d-122">Geben Sie im Feld **Prozent** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="fe28d-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="fe28d-123">Geben Sie im Feld **Journalname** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="fe28d-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="fe28d-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe28d-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="fe28d-125">Die Erfassungstransaktion buchen</span><span class="sxs-lookup"><span data-stu-id="fe28d-125">Post the journal transaction</span></span>
1. <span data-ttu-id="fe28d-126">Gehen Sie im Navigationsbereich zu **Module > Anlage > Journalbuchungen > Anlagenbuchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="fe28d-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="fe28d-127">Wählen Sie in der Liste die Erfassung aus, die mit dem Teilungsprozess erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fe28d-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="fe28d-128">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="fe28d-128">Select **Lines**.</span></span>

    - <span data-ttu-id="fe28d-129">Überprüfen Sie die erstellten Erfassungspositionen.</span><span class="sxs-lookup"><span data-stu-id="fe28d-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="fe28d-130">Eine "Anschaffungsänderungstransaktion" wird für die ursprüngliche Anlage erstellt, um den Wert um den Prozentsatz zu verringern, der im Teilungsprozess angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fe28d-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="fe28d-131">Eine "Anschaffungstransaktion" wird für die neue Anlage für denselben Betrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="fe28d-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="fe28d-132">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="fe28d-132">Select **Post**.</span></span>

