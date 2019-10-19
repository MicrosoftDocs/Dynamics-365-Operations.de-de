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
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177879"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="7d873-103">Anlage teilen</span><span class="sxs-lookup"><span data-stu-id="7d873-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d873-104">In diesem Abschnitt wird erläutert, wie Sie einen Prozentsatz eines Anlagenbuchs in ein neues Anlagenbuch aufteilen.</span><span class="sxs-lookup"><span data-stu-id="7d873-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="7d873-105">Dabei werden die "Buchhalterrolle" und die USMF-Demodaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d873-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="7d873-106">Neue Anlage erstellen</span><span class="sxs-lookup"><span data-stu-id="7d873-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="7d873-107">Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Anlagen > Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="7d873-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="7d873-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7d873-108">Select **New**.</span></span>
3. <span data-ttu-id="7d873-109">Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7d873-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="7d873-110">Notieren Sie sich die Anlagennummer, die später im Teilungsprozess zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="7d873-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="7d873-111">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7d873-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7d873-112">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="7d873-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="7d873-113">Anlage teilen</span><span class="sxs-lookup"><span data-stu-id="7d873-113">Split a fixed asset</span></span>
1. <span data-ttu-id="7d873-114">Suchen und wählen Sie in der Liste die Verknüpfung der zu teilenden Anlage.</span><span class="sxs-lookup"><span data-stu-id="7d873-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="7d873-115">Wählen Sie **Bücher**.</span><span class="sxs-lookup"><span data-stu-id="7d873-115">Select **Books**.</span></span> <span data-ttu-id="7d873-116">Wählen Sie das Buch aus, um die neue Anlage aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="7d873-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="7d873-117">Wählen Sie **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="7d873-117">Select **Functions**.</span></span>
4. <span data-ttu-id="7d873-118">Wählen Sie **Anlage teilen**.</span><span class="sxs-lookup"><span data-stu-id="7d873-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="7d873-119">Geben Sie im Feld **Zu Anlage** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7d873-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="7d873-120">Wählen Sie im Feld **Zum Buch** die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d873-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7d873-121">Geben Sie im Feld **Transaktionsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="7d873-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="7d873-122">Geben Sie im Feld **Prozent** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7d873-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="7d873-123">Geben Sie im Feld **Journalname** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7d873-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="7d873-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d873-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="7d873-125">Die Erfassungstransaktion buchen</span><span class="sxs-lookup"><span data-stu-id="7d873-125">Post the journal transaction</span></span>
1. <span data-ttu-id="7d873-126">Gehen Sie im Navigationsbereich zu **Module > Anlage > Journalbuchungen > Anlagenbuchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="7d873-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="7d873-127">Wählen Sie in der Liste die Erfassung aus, die mit dem Teilungsprozess erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d873-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="7d873-128">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="7d873-128">Select **Lines**.</span></span>

    - <span data-ttu-id="7d873-129">Überprüfen Sie die erstellten Erfassungspositionen.</span><span class="sxs-lookup"><span data-stu-id="7d873-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="7d873-130">Eine "Anschaffungsänderungstransaktion" wird für die ursprüngliche Anlage erstellt, um den Wert um den Prozentsatz zu verringern, der im Teilungsprozess angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7d873-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="7d873-131">Eine "Anschaffungstransaktion" wird für die neue Anlage für denselben Betrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="7d873-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="7d873-132">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="7d873-132">Select **Post**.</span></span>

