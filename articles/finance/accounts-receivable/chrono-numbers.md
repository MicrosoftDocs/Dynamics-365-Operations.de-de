---
title: Chronologisches Nummerieren von Dokumenten und Belegen
description: In diesem Thema wird erläutert, wie Sie chronologische Nummern für geeignete Dokumente und zugehörige Belege einrichten und verwenden.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104387"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="341ec-103">Chronologisches Nummerieren von Dokumenten und Belegen</span><span class="sxs-lookup"><span data-stu-id="341ec-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="341ec-104">In einigen Ländern ist es gesetzlich vorgeschrieben, Dokumente und zugehörige Belege in chronologischer Reihenfolge zu nummerieren.</span><span class="sxs-lookup"><span data-stu-id="341ec-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="341ec-105">Die Chronologie muss durch Perioden unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="341ec-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="341ec-106">Alle Nummern, die zu früheren Perioden gehören, müssen kleiner sein als die Zahlen, die zu späteren Perioden gehören.</span><span class="sxs-lookup"><span data-stu-id="341ec-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="341ec-107">Um diese Anforderung zu erfüllen, wurde eine chronologische Nummerierungsfunktion implementiert.</span><span class="sxs-lookup"><span data-stu-id="341ec-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="341ec-108">In diesem Thema wird erläutert, wie Sie chronologische Nummern für geeignete Dokumente und zugehörige Belege konfigurieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="341ec-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="341ec-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="341ec-109">Prerequisites</span></span>

<span data-ttu-id="341ec-110">Aktivieren Sie im Arbeitsbereich „Funktionsverwaltung“ die Funktion **Chronologische Nummerierung**:</span><span class="sxs-lookup"><span data-stu-id="341ec-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="341ec-111">Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="341ec-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="341ec-112">Die chronologische Nummerierung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="341ec-112">Configure chronological numbering</span></span>

<span data-ttu-id="341ec-113">Die chronologische Nummerierung betrifft die folgenden Dokumente.</span><span class="sxs-lookup"><span data-stu-id="341ec-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="341ec-114">**Debitorenkonten**</span><span class="sxs-lookup"><span data-stu-id="341ec-114">**Accounts receivable**</span></span>
- <span data-ttu-id="341ec-115">Debitorenrechnung</span><span class="sxs-lookup"><span data-stu-id="341ec-115">Customer invoice</span></span>
- <span data-ttu-id="341ec-116">Debitorenrechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-116">Customer invoice voucher</span></span>
- <span data-ttu-id="341ec-117">Verkaufsgutschrift</span><span class="sxs-lookup"><span data-stu-id="341ec-117">Sales credit note</span></span>
- <span data-ttu-id="341ec-118">Verkaufsgutschriftbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-118">Sales credit note voucher</span></span>
- <span data-ttu-id="341ec-119">Freitextrechnung</span><span class="sxs-lookup"><span data-stu-id="341ec-119">Free text invoice</span></span>
- <span data-ttu-id="341ec-120">Freitext-Rechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-120">Free text invoice voucher</span></span>
- <span data-ttu-id="341ec-121">Freitext-Gutschrift</span><span class="sxs-lookup"><span data-stu-id="341ec-121">Free text credit note</span></span>
- <span data-ttu-id="341ec-122">Freitext-Gutschriftbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-122">Free text credit note voucher</span></span>
- <span data-ttu-id="341ec-123">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="341ec-123">Packing slip</span></span>
- <span data-ttu-id="341ec-124">Lieferscheinbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-124">Packing slip voucher</span></span>
- <span data-ttu-id="341ec-125">Lieferschein-Korrekturbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="341ec-126">Zinsrechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-126">Interest note voucher</span></span>
- <span data-ttu-id="341ec-127">Mahnschreibenbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-127">Collection letter voucher</span></span>

<span data-ttu-id="341ec-128">**Kreditorenkonten**</span><span class="sxs-lookup"><span data-stu-id="341ec-128">**Accounts payable**</span></span>
- <span data-ttu-id="341ec-129">Rechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-129">Invoice voucher</span></span>
- <span data-ttu-id="341ec-130">Gutschriftbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-130">Credit note voucher</span></span>
- <span data-ttu-id="341ec-131">Produktzugangsbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-131">Product receipt voucher</span></span>

<span data-ttu-id="341ec-132">**Projektverwaltung**</span><span class="sxs-lookup"><span data-stu-id="341ec-132">**Project management**</span></span>
- <span data-ttu-id="341ec-133">Rechnung</span><span class="sxs-lookup"><span data-stu-id="341ec-133">Invoice</span></span>
- <span data-ttu-id="341ec-134">Rechnungsbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-134">Invoice voucher</span></span>
- <span data-ttu-id="341ec-135">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="341ec-135">Credit note</span></span>
- <span data-ttu-id="341ec-136">Gutschriftbeleg</span><span class="sxs-lookup"><span data-stu-id="341ec-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="341ec-137">Nummernkreise definieren</span><span class="sxs-lookup"><span data-stu-id="341ec-137">Define number sequences</span></span>

<span data-ttu-id="341ec-138">Rufen Sie zur Definition von Nummernkreisen **Organisationsverwaltung** > **Nummernkreise** > **Nummernkreise** auf.</span><span class="sxs-lookup"><span data-stu-id="341ec-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="341ec-139">Sie können beliebig viele Nummernkreise definieren, um die betroffenen Perioden für die erforderlichen Dokumente abzudecken.</span><span class="sxs-lookup"><span data-stu-id="341ec-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="341ec-140">Geben Sie für jeden Nummernkreis ein Unternehmen an.</span><span class="sxs-lookup"><span data-stu-id="341ec-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="341ec-141">Die Segmente der Nummernkreise müssen so definiert werden, dass sie eine chronologische Reihenfolge für Perioden liefern.</span><span class="sxs-lookup"><span data-stu-id="341ec-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="341ec-142">Beispielsweise können die Segmentnamen ein spezielles Präfix enthalten, das eine bestimmte Periode identifiziert.</span><span class="sxs-lookup"><span data-stu-id="341ec-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Nummernkreiseinrichtung](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="341ec-144">Nummernkreisgruppen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="341ec-144">Configure number sequence groups</span></span>

<span data-ttu-id="341ec-145">Rufen Sie **Debitorenkonten** > **Einrichtung** > **Debitorenkontenparameter** auf, um Nummernkreisgruppen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="341ec-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="341ec-146">Definieren Sie auf der Registerkarte **Nummernkreise** so viele Nummernkreisgruppen, wie erforderlich sind, um die betroffenen Perioden abzudecken.</span><span class="sxs-lookup"><span data-stu-id="341ec-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="341ec-147">Wählen Sie für jede Gruppe im Abschnitt **Referenz** eine der unterstützten Dokumentreferenzen aus, und beziehen Sie sich im Feld **Nummernkreiscode** auf einen Nummernkreis, der zuvor für die zugehörige Periode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="341ec-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Nummernkreisgruppeneinrichtung](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="341ec-149">Konfigurieren Sie in ähnlicher Weise Nummernkreisgruppen in **Kreditorenkonten**- und **Projektverwaltung und -buchhaltung**-Modulen.</span><span class="sxs-lookup"><span data-stu-id="341ec-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="341ec-150">Nummernkreisgruppen chronologisch konfigurieren</span><span class="sxs-lookup"><span data-stu-id="341ec-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="341ec-151">Rufen Sie **Organisationsverwaltung** > **Nummernkreise** > **Chronologische Nummernkreisgruppen** auf, um die Chronologie der Nummernkreisgruppen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="341ec-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="341ec-152">Definieren Sie die Anwendbarkeitsbedingungen für Nummernkreisgruppen.</span><span class="sxs-lookup"><span data-stu-id="341ec-152">Define the applicability conditions for number sequence groups.</span></span>

![Chronologische Nummerneinrichtung](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="341ec-154">Feld</span><span class="sxs-lookup"><span data-stu-id="341ec-154">Field</span></span>            | <span data-ttu-id="341ec-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="341ec-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="341ec-156">In Kraft</span><span class="sxs-lookup"><span data-stu-id="341ec-156">Effective</span></span>  | <span data-ttu-id="341ec-157">Das Startdatum der Anwendbarkeit der Nummernkreisgruppe.</span><span class="sxs-lookup"><span data-stu-id="341ec-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="341ec-158">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="341ec-158">Expiration</span></span>      | <span data-ttu-id="341ec-159">Das Enddatum der Anwendbarkeit der Nummernkreisgruppe.</span><span class="sxs-lookup"><span data-stu-id="341ec-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="341ec-160">Wenn kein Enddatum eingesetzt wird, wählen Sie **Niemals** aus.</span><span class="sxs-lookup"><span data-stu-id="341ec-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="341ec-161">Nummernkreisgruppe</span><span class="sxs-lookup"><span data-stu-id="341ec-161">Number sequence group</span></span> | <span data-ttu-id="341ec-162">Nummernkreisgruppe, mit der während der Periode Dokumentnummern generiert werden.</span><span class="sxs-lookup"><span data-stu-id="341ec-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="341ec-163">Ursprüngliche Nummernkreisgruppe</span><span class="sxs-lookup"><span data-stu-id="341ec-163">Original number sequence group</span></span> | <span data-ttu-id="341ec-164">Dieser Nummernkreisgruppencode wird zum zusätzlichen Filtern für Fälle verwendet, in denen Dokumenten bereits eine bestimmte *permanente* Nummernkreisgruppe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="341ec-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="341ec-165">Ein leerer Wert wird als bestimmter Wert betrachtet.</span><span class="sxs-lookup"><span data-stu-id="341ec-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="341ec-166">Wenn Sie eine vorläufig zugewiesene Gruppe ignorieren müssen, verwenden Sie für dieses Setup die Option **Standard**.</span><span class="sxs-lookup"><span data-stu-id="341ec-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="341ec-167">Standard</span><span class="sxs-lookup"><span data-stu-id="341ec-167">Default</span></span> | <span data-ttu-id="341ec-168">Wenn diese Option aktiviert ist, ignoriert das System die vorläufig zugewiesene Dokumentnummernkreisgruppe und verwendet nur die Start- und Enddaten der Perioden für die Anwendbarkeitsanalyse.</span><span class="sxs-lookup"><span data-stu-id="341ec-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="341ec-169">Bei Deaktivierung verwendet das System die vollständige Kombination **Gültig** + **Ablaufdatum** + **Ursprüngliche Nummernkreisgruppe** als Auswahl.</span><span class="sxs-lookup"><span data-stu-id="341ec-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="341ec-170">Dokumentbuchung</span><span class="sxs-lookup"><span data-stu-id="341ec-170">Document posting</span></span>
<span data-ttu-id="341ec-171">Wenn Sie ein Dokument buchen, wird dem Dokument die entsprechende Nummernkreisgruppe basierend auf dem Buchungsdatum des Dokuments zugewiesen und anschließend zum Generieren einer Dokumentnummer basierend auf dem erkannten Nummernkreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="341ec-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="341ec-172">Das System gibt eine Meldung zur Zuweisung der Nummernkreisgruppen aus.</span><span class="sxs-lookup"><span data-stu-id="341ec-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumentnummer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="341ec-174">Für einige Länder gibt es bereits eine spezifische Logik für die Nummerierung von Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="341ec-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="341ec-175">In diesem Fall überschreibt die länderspezifische Logik die Funktion **Chronologische Nummerierung**.</span><span class="sxs-lookup"><span data-stu-id="341ec-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>
