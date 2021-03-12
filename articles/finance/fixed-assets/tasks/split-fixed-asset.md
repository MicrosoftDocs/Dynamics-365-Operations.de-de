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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75938e6fdf5fd8f10ac9719fc449a586c08d06b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975940"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="6606a-103">Anlage teilen</span><span class="sxs-lookup"><span data-stu-id="6606a-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6606a-104">In diesem Abschnitt wird erläutert, wie Sie einen Prozentsatz eines Anlagenbuchs in ein neues Anlagenbuch aufteilen.</span><span class="sxs-lookup"><span data-stu-id="6606a-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="6606a-105">Dabei werden die "Buchhalterrolle" und die USMF-Demodaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="6606a-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="6606a-106">Neue Anlage erstellen</span><span class="sxs-lookup"><span data-stu-id="6606a-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="6606a-107">Wechseln Sie im Navigationsbereich zu **Module \> Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="6606a-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="6606a-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6606a-108">Select **New**.</span></span>
3. <span data-ttu-id="6606a-109">Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="6606a-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="6606a-110">Notieren Sie sich die Anlagennummer, die später im Teilungsprozess zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="6606a-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="6606a-111">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6606a-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="6606a-112">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="6606a-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="6606a-113">Anlage teilen</span><span class="sxs-lookup"><span data-stu-id="6606a-113">Split a fixed asset</span></span>

<span data-ttu-id="6606a-114">Bevor ein vollständig abgeschriebener Vermögenswert aufgeteilt wird, sollte der Status des Anlagenbuchs manuell von **Geschlossen** auf **Öffnen** geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6606a-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="6606a-115">Dieser Schritt ist erforderlich, da der Buchstatus **offen** sein muss, wenn Sie Transaktionen für den Vermögenswert buchen müssen (z. B. für einen Veräußerungsverkauf).</span><span class="sxs-lookup"><span data-stu-id="6606a-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="6606a-116">Sie müssen auch die **Mehrere Transaktionen innerhalb eines Belegs erlauben**-Parameter auf der **Allgemeines**-Registerkarte der **Hauptbuchparameter**-Seite aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6606a-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="6606a-117">Führen Sie die folgenden Schritte aus, um die Anlage zu teilen, nachdem der Status des Anlagenbuches geändert wurde und mehrere Transaktionen innerhalb eines Belegs zulässig waren.</span><span class="sxs-lookup"><span data-stu-id="6606a-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="6606a-118">Suchen und wählen Sie in der Liste die Verknüpfung der zu teilenden Anlage.</span><span class="sxs-lookup"><span data-stu-id="6606a-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="6606a-119">Wählen Sie **Bücher**.</span><span class="sxs-lookup"><span data-stu-id="6606a-119">Select **Books**.</span></span> <span data-ttu-id="6606a-120">Wählen Sie das Buch aus, um die neue Anlage aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="6606a-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="6606a-121">Wählen Sie **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="6606a-121">Select **Functions**.</span></span>
4. <span data-ttu-id="6606a-122">Wählen Sie **Anlage teilen**.</span><span class="sxs-lookup"><span data-stu-id="6606a-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="6606a-123">Geben Sie im Feld **Zu Anlage** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6606a-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="6606a-124">Wählen Sie im Feld **Zum Buch** die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6606a-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6606a-125">Geben Sie im Feld **Transaktionsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="6606a-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="6606a-126">Geben Sie im Feld **Prozent** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="6606a-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="6606a-127">Geben Sie im Feld **Journalname** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6606a-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="6606a-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6606a-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="6606a-129">Die Erfassungstransaktion buchen</span><span class="sxs-lookup"><span data-stu-id="6606a-129">Post the journal transaction</span></span>

1. <span data-ttu-id="6606a-130">Gehen Sie im Navigationsbereich zu **Module \> Anlage \> Journalbuchungen \> Anlagenbuchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="6606a-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="6606a-131">Wählen Sie in der Liste die Erfassung aus, die mit dem Teilungsprozess erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6606a-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="6606a-132">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="6606a-132">Select **Lines**.</span></span>

    - <span data-ttu-id="6606a-133">Überprüfen Sie die erstellten Erfassungspositionen.</span><span class="sxs-lookup"><span data-stu-id="6606a-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="6606a-134">Eine "Anschaffungsänderungstransaktion" wird für die ursprüngliche Anlage erstellt, um den Wert um den Prozentsatz zu verringern, der im Teilungsprozess angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6606a-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="6606a-135">Eine "Anschaffungstransaktion" wird für die neue Anlage für denselben Betrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="6606a-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="6606a-136">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="6606a-136">Select **Post**.</span></span>
