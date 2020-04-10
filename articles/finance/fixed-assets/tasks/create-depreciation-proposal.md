---
title: Abschreibungsvorschlag erstellen
description: In diesem Thema wird beschrieben, wie Abschreibungschargenvorschläge arbeiten und erläutert, wie Abschreibung für Anlagen vorgeschlagen werden.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 07337063c01f146c72ca6d9e0f9096907cdc9638
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142822"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="eee35-103">Abschreibungsvorschlag erstellen</span><span class="sxs-lookup"><span data-stu-id="eee35-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eee35-104">In diesem Thema wird beschrieben, wie Abschreibungschargenvorschläge arbeiten und erläutert, wie Abschreibung für Anlagen vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="eee35-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="eee35-105">Bei dieser Aufgabe werden das Demo-Unternehmen USMF sowie die Buchhalterrolle verwendet.</span><span class="sxs-lookup"><span data-stu-id="eee35-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="eee35-106">Abschreibungsvorschlag erstellen</span><span class="sxs-lookup"><span data-stu-id="eee35-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="eee35-107">Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Journaleinträge > Abschreibungsvorschlag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="eee35-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="eee35-108">Wählen Sie im Feld **Name der Erfassung** eine Option in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="eee35-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="eee35-109">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="eee35-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="eee35-110">Wählen Sie die Option **Abschreibung zusammenfassen** aus, um monatliche Abschreibungen in einer einzelnen Erfassungsposition zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="eee35-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="eee35-111">Ist also beispielsweise das Bis-Datum der 31. März 2015, kann der folgende Buchungstext generiert werden: Abschreibung seit 31. Januar 2015.</span><span class="sxs-lookup"><span data-stu-id="eee35-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="eee35-112">Das Feld **Datum** in den vorgeschlagenen Erfassungspositionen wird dann auf den 31. März 2015 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eee35-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="eee35-113">Der Abschreibungsvorschlag kann nach Anlage, Anlagengruppe oder nach anderen Kriterien mithilfe der Option **Filter** gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="eee35-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="eee35-114">Wenn Sie das Formular **Anschaffungs- oder Abschreibungsvorschläge für Anlagen erstellen** verwenden, können Sie Abschreibung in Chargen vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="eee35-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="eee35-115">Dies wird für größere Vorschläge empfohlen, die mehr Systemressourcen verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="eee35-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="eee35-116">Wenn Sie die Chargenoption auswählen, können Sie weiterhin in diesem Zeitraum andere Aufgaben abschließen.</span><span class="sxs-lookup"><span data-stu-id="eee35-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="eee35-117">Wenn Sie Abschreibung auf diese Weise vorschlagen, wird die Abschreibung für Wertmodelle für Anlagen berechnet.</span><span class="sxs-lookup"><span data-stu-id="eee35-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="eee35-118">Wählen Sie **Erfassung erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="eee35-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="eee35-119">Abschreibungseinträge prüfen</span><span class="sxs-lookup"><span data-stu-id="eee35-119">Review depreciation entries</span></span>
1. <span data-ttu-id="eee35-120">Gehen Sie im Navigationsbereich zu **Module > Anlage > Journalbuchungen > Anlagenbuchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="eee35-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="eee35-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="eee35-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eee35-122">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="eee35-122">Select **Lines**.</span></span>
4. <span data-ttu-id="eee35-123">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="eee35-123">Select **Post**.</span></span>

