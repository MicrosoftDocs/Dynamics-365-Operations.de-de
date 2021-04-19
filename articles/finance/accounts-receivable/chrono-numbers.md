---
title: Chronologisches Nummerieren von Dokumenten und Belegen
description: In diesem Thema wird erläutert, wie Sie chronologische Nummern für geeignete Dokumente und zugehörige Belege einrichten und verwenden.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838860"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="642ee-103">Chronologisches Nummerieren von Dokumenten und Belegen</span><span class="sxs-lookup"><span data-stu-id="642ee-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="642ee-104">In einigen Ländern ist es gesetzlich vorgeschrieben, Dokumente und zugehörige Belege in chronologischer Reihenfolge zu nummerieren.</span><span class="sxs-lookup"><span data-stu-id="642ee-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="642ee-105">Die Chronologie muss durch Perioden unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="642ee-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="642ee-106">Alle Nummern, die zu früheren Perioden gehören, müssen kleiner sein als die Zahlen, die zu späteren Perioden gehören.</span><span class="sxs-lookup"><span data-stu-id="642ee-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="642ee-107">Um diese Anforderung zu erfüllen, wurde eine chronologische Nummerierungsfunktion implementiert.</span><span class="sxs-lookup"><span data-stu-id="642ee-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="642ee-108">In diesem Thema wird erläutert, wie Sie chronologische Nummern für geeignete Dokumente und zugehörige Belege konfigurieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="642ee-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="642ee-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="642ee-109">Prerequisites</span></span>

<span data-ttu-id="642ee-110">Aktivieren Sie im Arbeitsbereich „Funktionsverwaltung“ die Funktion **Chronologische Nummerierung**:</span><span class="sxs-lookup"><span data-stu-id="642ee-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="642ee-111">Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="642ee-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="642ee-112">Die chronologische Nummerierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="642ee-112">Configure chronological numbering</span></span>

<span data-ttu-id="642ee-113">Die chronologische Nummerierung betrifft die folgenden Dokumente.</span><span class="sxs-lookup"><span data-stu-id="642ee-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="642ee-114">**Debitorenkonten**</span><span class="sxs-lookup"><span data-stu-id="642ee-114">**Accounts receivable**</span></span>
- <span data-ttu-id="642ee-115">Debitorenrechnung</span><span class="sxs-lookup"><span data-stu-id="642ee-115">Customer invoice</span></span>
- <span data-ttu-id="642ee-116">Debitorenrechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-116">Customer invoice voucher</span></span>
- <span data-ttu-id="642ee-117">Verkaufsgutschrift</span><span class="sxs-lookup"><span data-stu-id="642ee-117">Sales credit note</span></span>
- <span data-ttu-id="642ee-118">Verkaufsgutschriftbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-118">Sales credit note voucher</span></span>
- <span data-ttu-id="642ee-119">Freitextrechnung</span><span class="sxs-lookup"><span data-stu-id="642ee-119">Free text invoice</span></span>
- <span data-ttu-id="642ee-120">Freitext-Rechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-120">Free text invoice voucher</span></span>
- <span data-ttu-id="642ee-121">Freitext-Gutschrift</span><span class="sxs-lookup"><span data-stu-id="642ee-121">Free text credit note</span></span>
- <span data-ttu-id="642ee-122">Freitext-Gutschriftbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-122">Free text credit note voucher</span></span>
- <span data-ttu-id="642ee-123">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="642ee-123">Packing slip</span></span>
- <span data-ttu-id="642ee-124">Lieferscheinbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-124">Packing slip voucher</span></span>
- <span data-ttu-id="642ee-125">Lieferschein-Korrekturbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="642ee-126">Zinsrechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-126">Interest note voucher</span></span>
- <span data-ttu-id="642ee-127">Mahnschreibenbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-127">Collection letter voucher</span></span>

<span data-ttu-id="642ee-128">**Kreditorenkonten**</span><span class="sxs-lookup"><span data-stu-id="642ee-128">**Accounts payable**</span></span>
- <span data-ttu-id="642ee-129">Rechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-129">Invoice voucher</span></span>
- <span data-ttu-id="642ee-130">Gutschriftbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-130">Credit note voucher</span></span>
- <span data-ttu-id="642ee-131">Produktzugangsbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-131">Product receipt voucher</span></span>

<span data-ttu-id="642ee-132">**Projektverwaltung**</span><span class="sxs-lookup"><span data-stu-id="642ee-132">**Project management**</span></span>
- <span data-ttu-id="642ee-133">Rechnung</span><span class="sxs-lookup"><span data-stu-id="642ee-133">Invoice</span></span>
- <span data-ttu-id="642ee-134">Rechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-134">Invoice voucher</span></span>
- <span data-ttu-id="642ee-135">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="642ee-135">Credit note</span></span>
- <span data-ttu-id="642ee-136">Gutschriftbeleg</span><span class="sxs-lookup"><span data-stu-id="642ee-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="642ee-137">Nummernkreise definieren</span><span class="sxs-lookup"><span data-stu-id="642ee-137">Define number sequences</span></span>

<span data-ttu-id="642ee-138">Rufen Sie zur Definition von Nummernkreisen **Organisationsverwaltung** > **Nummernkreise** > **Nummernkreise** auf.</span><span class="sxs-lookup"><span data-stu-id="642ee-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="642ee-139">Sie können beliebig viele Nummernkreise definieren, um die betroffenen Perioden für die erforderlichen Dokumente abzudecken.</span><span class="sxs-lookup"><span data-stu-id="642ee-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="642ee-140">Geben Sie für jeden Nummernkreis ein Unternehmen an.</span><span class="sxs-lookup"><span data-stu-id="642ee-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="642ee-141">Die Segmente der Nummernkreise müssen so definiert werden, dass sie eine chronologische Reihenfolge für Perioden liefern.</span><span class="sxs-lookup"><span data-stu-id="642ee-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="642ee-142">Beispielsweise können die Segmentnamen ein spezielles Präfix enthalten, das eine bestimmte Periode identifiziert.</span><span class="sxs-lookup"><span data-stu-id="642ee-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Nummernkreiseinrichtung](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="642ee-144">Nummernkreisgruppen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="642ee-144">Configure number sequence groups</span></span>

<span data-ttu-id="642ee-145">Rufen Sie **Debitorenkonten** > **Einrichtung** > **Debitorenkontenparameter** auf, um Nummernkreisgruppen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="642ee-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="642ee-146">Definieren Sie auf der Registerkarte **Nummernkreise** so viele Nummernkreisgruppen, wie erforderlich sind, um die betroffenen Perioden abzudecken.</span><span class="sxs-lookup"><span data-stu-id="642ee-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="642ee-147">Wählen Sie für jede Gruppe im Abschnitt **Referenz** eine der unterstützten Dokumentreferenzen aus, und beziehen Sie sich im Feld **Nummernkreiscode** auf einen Nummernkreis, der zuvor für die zugehörige Periode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="642ee-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Nummernkreisgruppeneinrichtung](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="642ee-149">Konfigurieren Sie in ähnlicher Weise Nummernkreisgruppen in **Kreditorenkonten**- und **Projektverwaltung und -buchhaltung**-Modulen.</span><span class="sxs-lookup"><span data-stu-id="642ee-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="642ee-150">Nummernkreisgruppen chronologisch konfigurieren</span><span class="sxs-lookup"><span data-stu-id="642ee-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="642ee-151">Rufen Sie **Organisationsverwaltung** > **Nummernkreise** > **Chronologische Nummernkreisgruppen** auf, um die Chronologie der Nummernkreisgruppen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="642ee-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="642ee-152">Definieren Sie die Anwendbarkeitsbedingungen für Nummernkreisgruppen.</span><span class="sxs-lookup"><span data-stu-id="642ee-152">Define the applicability conditions for number sequence groups.</span></span>

![Chronologische Nummerneinrichtung](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="642ee-154">Feld</span><span class="sxs-lookup"><span data-stu-id="642ee-154">Field</span></span>            | <span data-ttu-id="642ee-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642ee-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="642ee-156">In Kraft</span><span class="sxs-lookup"><span data-stu-id="642ee-156">Effective</span></span>  | <span data-ttu-id="642ee-157">Das Startdatum der Anwendbarkeit der Nummernkreisgruppe.</span><span class="sxs-lookup"><span data-stu-id="642ee-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="642ee-158">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="642ee-158">Expiration</span></span>      | <span data-ttu-id="642ee-159">Das Enddatum der Anwendbarkeit der Nummernkreisgruppe.</span><span class="sxs-lookup"><span data-stu-id="642ee-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="642ee-160">Wenn kein Enddatum eingesetzt wird, wählen Sie **Niemals** aus.</span><span class="sxs-lookup"><span data-stu-id="642ee-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="642ee-161">Nummernkreisgruppe</span><span class="sxs-lookup"><span data-stu-id="642ee-161">Number sequence group</span></span> | <span data-ttu-id="642ee-162">Nummernkreisgruppe, mit der während der Periode Dokumentnummern generiert werden.</span><span class="sxs-lookup"><span data-stu-id="642ee-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="642ee-163">Ursprüngliche Nummernkreisgruppe</span><span class="sxs-lookup"><span data-stu-id="642ee-163">Original number sequence group</span></span> | <span data-ttu-id="642ee-164">Dieser Nummernkreisgruppencode wird zum zusätzlichen Filtern für Fälle verwendet, in denen Dokumenten bereits eine bestimmte *permanente* Nummernkreisgruppe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="642ee-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="642ee-165">Ein leerer Wert wird als bestimmter Wert betrachtet.</span><span class="sxs-lookup"><span data-stu-id="642ee-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="642ee-166">Wenn Sie eine vorläufig zugewiesene Gruppe ignorieren müssen, verwenden Sie für dieses Setup die Option **Standard**.</span><span class="sxs-lookup"><span data-stu-id="642ee-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="642ee-167">Standard</span><span class="sxs-lookup"><span data-stu-id="642ee-167">Default</span></span> | <span data-ttu-id="642ee-168">Wenn diese Option aktiviert ist, ignoriert das System die vorläufig zugewiesene Dokumentnummernkreisgruppe und verwendet nur die Start- und Enddaten der Perioden für die Anwendbarkeitsanalyse.</span><span class="sxs-lookup"><span data-stu-id="642ee-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="642ee-169">Bei Deaktivierung verwendet das System die vollständige Kombination **Gültig** + **Ablaufdatum** + **Ursprüngliche Nummernkreisgruppe** als Auswahl.</span><span class="sxs-lookup"><span data-stu-id="642ee-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="642ee-170">Dokumentbuchung</span><span class="sxs-lookup"><span data-stu-id="642ee-170">Document posting</span></span>
<span data-ttu-id="642ee-171">Wenn Sie ein Dokument buchen, wird dem Dokument die entsprechende Nummernkreisgruppe basierend auf dem Buchungsdatum des Dokuments zugewiesen und anschließend zum Generieren einer Dokumentnummer basierend auf dem erkannten Nummernkreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="642ee-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="642ee-172">Das System gibt eine Meldung zur Zuweisung der Nummernkreisgruppen aus.</span><span class="sxs-lookup"><span data-stu-id="642ee-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumentnummer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="642ee-174">Für einige Länder gibt es bereits eine spezifische Logik für die Nummerierung von Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="642ee-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="642ee-175">In diesem Fall überschreibt die länderspezifische Logik die Funktion **Chronologische Nummerierung**.</span><span class="sxs-lookup"><span data-stu-id="642ee-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
