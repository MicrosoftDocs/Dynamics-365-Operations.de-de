---
title: Abschreibungsvorschlag erstellen
description: In dieser Prozedur wird beschrieben, wie Abschreibungschargenvorschläge funktionieren und erläutert, wie Abschreibung für Anlagen vorgeschlagen wird.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07146adfe1ead2b6e06e3c323963f8c012381b76
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840000"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="076c0-103">Abschreibungsvorschlag erstellen</span><span class="sxs-lookup"><span data-stu-id="076c0-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="076c0-104">In dieser Prozedur wird beschrieben, wie Abschreibungschargenvorschläge funktionieren und erläutert, wie Abschreibung für Anlagen vorgeschlagen wird.</span><span class="sxs-lookup"><span data-stu-id="076c0-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="076c0-105">Bei dieser Aufgabe werden das Demo-Unternehmen USMF sowie die Buchhalterrolle verwendet.</span><span class="sxs-lookup"><span data-stu-id="076c0-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="076c0-106">Abschreibungsvorschlag erstellen</span><span class="sxs-lookup"><span data-stu-id="076c0-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="076c0-107">Wechseln Sie zu "Anlagen" > "Erfassungseinträge" > "Abschreibungsvorschlag" erstellen.</span><span class="sxs-lookup"><span data-stu-id="076c0-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="076c0-108">Klicken Sie im Feld "Erfassungsname" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="076c0-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="076c0-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="076c0-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="076c0-110">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="076c0-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="076c0-111">Wählen Sie die Option "Abschreibung zusammenfassen" aus, um monatliche Abschreibungen in einer einzelnen Erfassungsposition zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="076c0-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="076c0-112">Ist also beispielsweise das Bis-Datum der 31. März 2015 ist, kann der folgende Buchungstext generiert werden: "Abschreibung seit 31. Januar 2015."</span><span class="sxs-lookup"><span data-stu-id="076c0-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="076c0-113">Das Feld Datum in den vorgeschlagenen Erfassungspositionen wird dann auf den 31. März 2015 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="076c0-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="076c0-114">Der Abschreibungsvorschlag kann nach Anlage, Anlagengruppe oder nach anderen Kriterien mithilfe der Option "Filter" gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="076c0-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="076c0-115">Wenn Sie das Formular "Anschaffungs- oder Abschreibungsvorschläge für Anlagen erstellen" verwenden, können Sie Abschreibung in Chargen vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="076c0-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="076c0-116">Dies wird für größere Vorschläge empfohlen, die mehr Systemressourcen verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="076c0-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="076c0-117">Wenn Sie die Chargenoption auswählen, können Sie weiterhin in diesem Zeitraum andere Aufgaben abschließen.</span><span class="sxs-lookup"><span data-stu-id="076c0-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="076c0-118">Wenn Sie Abschreibung auf diese Weise vorschlagen, wird die Abschreibung für Wertmodelle für Anlagen berechnet.</span><span class="sxs-lookup"><span data-stu-id="076c0-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="076c0-119">Klicken Sie auf "Erfassung erstellen".</span><span class="sxs-lookup"><span data-stu-id="076c0-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="076c0-120">Abschreibungseinträge prüfen</span><span class="sxs-lookup"><span data-stu-id="076c0-120">Review depreciation entries</span></span>
1. <span data-ttu-id="076c0-121">Wechseln Sie zu "Anlagen" > "Journaleinträge" > "Anlagenerfassung".</span><span class="sxs-lookup"><span data-stu-id="076c0-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="076c0-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="076c0-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="076c0-123">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="076c0-123">Click Lines.</span></span>
4. <span data-ttu-id="076c0-124">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="076c0-124">Click Post.</span></span>

