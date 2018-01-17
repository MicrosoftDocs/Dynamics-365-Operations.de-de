---
title: Nummernkreise
description: "Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Bezeichnern für Masterdatensätze und Buchungsdatensätze, die Bezeichner benötigen."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: e978519a86e32d4440b7c0562c4c5069c001ce81
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---

# <a name="number-sequences"></a><span data-ttu-id="59aa2-103">Nummernkreise</span><span class="sxs-lookup"><span data-stu-id="59aa2-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="59aa2-104">Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Bezeichnern für Masterdatensätze und Buchungsdatensätze, die Bezeichner benötigen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="59aa2-105">Ein Masterdatensatz oder Buchungsdatensatz, der eine Kennung erfordert, wird als *Referenz* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="59aa2-106">Bevor neue Datensätze für eine Referenz erstellt werden können, muss ein Nummernkreis eingerichtet und der Referenz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="59aa2-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="59aa2-107">Es wird empfohlen, die Seiten in **Organisationsverwaltung** zum Einrichten von Nummernkreisen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="59aa2-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="59aa2-108">Wenn modulspezifische Einstellungen erforderlich sind, können Sie die Seite Parameter in einem Modul verwenden, um Nummernkreise für die Referenzen in diesem Modul anzugeben.</span><span class="sxs-lookup"><span data-stu-id="59aa2-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="59aa2-109">Sie können beispielsweise in **Debitoren** und **Kreditoren** Nummernkreisgruppen einrichten, um bestimmten Debitoren oder Kreditoren bestimmte Nummernkreise zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="59aa2-110">Wenn Sie einen Nummernkreis einrichten, müssen Sie einen Bereich angeben, der definiert, welche Organisation den Nummernkreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="59aa2-111">Der Bereich kann **Gemeinsam genutzt**, **Unternehmen**, **Juristische Person** oder **Organisationseinheit** sein.</span><span class="sxs-lookup"><span data-stu-id="59aa2-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="59aa2-112">Die Bereiche **Juristische Person** und **Unternehmen** können auch mit **Steuerkalenderperiode** kombiniert werden, um noch spezifischere Nummernkreise zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="59aa2-113">Nummernkreisformate werden aus Segmenten gebildet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="59aa2-114">Nummernkreise, die einen anderen Bereich als **Gemeinsam genutzt** besitzen, können Segmente enthalten, die dem Bereich entsprechen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="59aa2-115">Ein Nummernkreis mit dem Bereich **Juristische Person** kann beispielsweise ein Segment für juristische Personen enthalten.</span><span class="sxs-lookup"><span data-stu-id="59aa2-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="59aa2-116">Durch Einfügen eines Bereichssegments in das Nummernkreisformat können Sie den Bereich eines bestimmten Datensatzes anhand seiner Nummer feststellen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="59aa2-117">Neben den Segmenten, die Bereichen entsprechen, können Nummernkreisformate die Segmente **Konstante** und **Alphanumerische Segmente** enthalten.</span><span class="sxs-lookup"><span data-stu-id="59aa2-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="59aa2-118">Ein Segment vom Typ **Konstante** enthält eine Gruppe von Buchstaben, Zahlen oder Symbolen, die unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="59aa2-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="59aa2-119">Ein Segment vom Typ **Alphanumerisch** enthält eine Gruppe von Buchstaben oder Zahlen, die jedes Mal schrittweise erhöht werden, wenn eine Nummer aus dem Nummernkreis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59aa2-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="59aa2-120">Verwenden Sie ein Nummernzeichen (\#) zur Angabe inkrementeller Nummern und ein kaufmännisches Und-Zeichen zur Angabe inkrementeller Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="59aa2-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="59aa2-121">Mit dem Format \#\#\#\#\#\_2017 wird beispielsweise der Nummernkreis 00001\_2017, 00002\_2017 usw. erstellt.</span><span class="sxs-lookup"><span data-stu-id="59aa2-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="59aa2-122">Nummernkreisbeispiele</span><span class="sxs-lookup"><span data-stu-id="59aa2-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="59aa2-123">Die folgenden Beispiele zeigen, wie Segmente verwendet werden, um Nummernkreisformate zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="59aa2-124">Insbesondere verdeutlichen die Beispiele, welche Auswirkungen das Verwenden von Bereichssegmenten hat.</span><span class="sxs-lookup"><span data-stu-id="59aa2-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="59aa2-125">Spesenabrechnungsnummern</span><span class="sxs-lookup"><span data-stu-id="59aa2-125">Expense report numbers</span></span>

<span data-ttu-id="59aa2-126">Im folgenden Beispiel werden Spesenabrechnungsnummern für die juristische Person mit dem Titel **CS** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="59aa2-127">**Bereich:** Reisekosten und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59aa2-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="59aa2-128">**Referenz:** Ausgaben-Berichtsnummer</span><span class="sxs-lookup"><span data-stu-id="59aa2-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="59aa2-129">**Umfang:** Juristische Person</span><span class="sxs-lookup"><span data-stu-id="59aa2-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="59aa2-130">**Juristische Person:**CS</span><span class="sxs-lookup"><span data-stu-id="59aa2-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="59aa2-131">Segmente</span><span class="sxs-lookup"><span data-stu-id="59aa2-131">Segments</span></span>  | <span data-ttu-id="59aa2-132">Segmenttyp</span><span class="sxs-lookup"><span data-stu-id="59aa2-132">Segment type</span></span> | <span data-ttu-id="59aa2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="59aa2-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="59aa2-134">Segment 1</span><span class="sxs-lookup"><span data-stu-id="59aa2-134">Segment 1</span></span> | <span data-ttu-id="59aa2-135">Juristische Person</span><span class="sxs-lookup"><span data-stu-id="59aa2-135">Legal entity</span></span> | <span data-ttu-id="59aa2-136">CS</span><span class="sxs-lookup"><span data-stu-id="59aa2-136">CS</span></span>        |
| <span data-ttu-id="59aa2-137">Segment 2</span><span class="sxs-lookup"><span data-stu-id="59aa2-137">Segment 2</span></span> | <span data-ttu-id="59aa2-138">Konstante</span><span class="sxs-lookup"><span data-stu-id="59aa2-138">Constant</span></span>     | <span data-ttu-id="59aa2-139">-SPESEN-</span><span class="sxs-lookup"><span data-stu-id="59aa2-139">-EXPENSE-</span></span> |
| <span data-ttu-id="59aa2-140">Segment 3</span><span class="sxs-lookup"><span data-stu-id="59aa2-140">Segment 3</span></span> | <span data-ttu-id="59aa2-141">Alphanumerisch</span><span class="sxs-lookup"><span data-stu-id="59aa2-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="59aa2-142">**Beispiel für formatierte Nummer**: CS-SPESEN-0039</span><span class="sxs-lookup"><span data-stu-id="59aa2-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="59aa2-143">Sie können ein ähnliches Nummernkreisformat für andere juristische Personen einrichten.</span><span class="sxs-lookup"><span data-stu-id="59aa2-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="59aa2-144">Beispiel: Wenn Sie für eine juristische Person namens **RW** nur den Wert des Segments für die juristische Person ändern, lautet die formatierte Nummer RW-SPESEN-0039.</span><span class="sxs-lookup"><span data-stu-id="59aa2-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="59aa2-145">Sie können auch das gesamte Nummernkreisformat für andere juristische Personen ändern.</span><span class="sxs-lookup"><span data-stu-id="59aa2-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="59aa2-146">Sie können beispielsweise das Bereichssegment für die juristische Person auslassen, um eine formatierte Nummer zu erstellen, beispielsweise SPESEN-0001.</span><span class="sxs-lookup"><span data-stu-id="59aa2-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="59aa2-147">Auftragsnummern</span><span class="sxs-lookup"><span data-stu-id="59aa2-147">Sales order numbers</span></span>

<span data-ttu-id="59aa2-148">Im folgenden Beispiel werden Auftragsnummern für die Unternehmenskennung **CEU** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="59aa2-149">**Bereich:** Verkäufe</span><span class="sxs-lookup"><span data-stu-id="59aa2-149">**Area:** Sales</span></span> 
- <span data-ttu-id="59aa2-150">**Referenz:**Verkaufsauftrag</span><span class="sxs-lookup"><span data-stu-id="59aa2-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="59aa2-151">**Umfang:** Unternehmen</span><span class="sxs-lookup"><span data-stu-id="59aa2-151">**Scope:** Company</span></span> 
- <span data-ttu-id="59aa2-152">**Unternehmen:** CEU</span><span class="sxs-lookup"><span data-stu-id="59aa2-152">**Company:** CEU</span></span>

| <span data-ttu-id="59aa2-153">Segmente</span><span class="sxs-lookup"><span data-stu-id="59aa2-153">Segments</span></span>  | <span data-ttu-id="59aa2-154">Segmenttyp</span><span class="sxs-lookup"><span data-stu-id="59aa2-154">Segment type</span></span> | <span data-ttu-id="59aa2-155">Wert</span><span class="sxs-lookup"><span data-stu-id="59aa2-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="59aa2-156">Segment 1</span><span class="sxs-lookup"><span data-stu-id="59aa2-156">Segment 1</span></span> | <span data-ttu-id="59aa2-157">Konstante</span><span class="sxs-lookup"><span data-stu-id="59aa2-157">Constant</span></span>     | <span data-ttu-id="59aa2-158">AU-</span><span class="sxs-lookup"><span data-stu-id="59aa2-158">SO-</span></span>      |
| <span data-ttu-id="59aa2-159">Segment 2</span><span class="sxs-lookup"><span data-stu-id="59aa2-159">Segment 2</span></span> | <span data-ttu-id="59aa2-160">Alphanumerisch</span><span class="sxs-lookup"><span data-stu-id="59aa2-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="59aa2-161">**Beispiel für formatierte Nummer**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="59aa2-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="59aa2-162">Auch wenn das Format kein Bereichssegment enthält, beginnt die Nummerierung für jede Unternehmenskennung erneut.</span><span class="sxs-lookup"><span data-stu-id="59aa2-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="59aa2-163">Wenn Sie dasselbe Format für alle Unternehmenskennungen verwenden, werden in allen Unternehmen dieselben Zahlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="59aa2-164">Beispielsweise wird in jedem Unternehmen die Auftragsnummer AU-0029 verwendet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="59aa2-165">Sie können auch das gesamte Nummernkreisformat für andere Unternehmenskennungen ändern.</span><span class="sxs-lookup"><span data-stu-id="59aa2-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="59aa2-166">Bestellanforderungsnummern</span><span class="sxs-lookup"><span data-stu-id="59aa2-166">Purchase requisition numbers</span></span>

<span data-ttu-id="59aa2-167">Im folgenden Beispiel werden Bestellanforderungsnummern organisationsweit verwendet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="59aa2-168">**Bereich:** Einkauf</span><span class="sxs-lookup"><span data-stu-id="59aa2-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="59aa2-169">**Referenz:** Einkaufspreis</span><span class="sxs-lookup"><span data-stu-id="59aa2-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="59aa2-170">**Umfang:** Geteilt</span><span class="sxs-lookup"><span data-stu-id="59aa2-170">**Scope:** Shared</span></span>

| <span data-ttu-id="59aa2-171">Segmente</span><span class="sxs-lookup"><span data-stu-id="59aa2-171">Segments</span></span>  | <span data-ttu-id="59aa2-172">Segmenttyp</span><span class="sxs-lookup"><span data-stu-id="59aa2-172">Segment type</span></span> | <span data-ttu-id="59aa2-173">Wert</span><span class="sxs-lookup"><span data-stu-id="59aa2-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="59aa2-174">Segment 1</span><span class="sxs-lookup"><span data-stu-id="59aa2-174">Segment 1</span></span> | <span data-ttu-id="59aa2-175">Konstante</span><span class="sxs-lookup"><span data-stu-id="59aa2-175">Constant</span></span>     | <span data-ttu-id="59aa2-176">BestAnf</span><span class="sxs-lookup"><span data-stu-id="59aa2-176">Req</span></span>      |
| <span data-ttu-id="59aa2-177">Segment 2</span><span class="sxs-lookup"><span data-stu-id="59aa2-177">Segment 2</span></span> | <span data-ttu-id="59aa2-178">Alphanumerisch</span><span class="sxs-lookup"><span data-stu-id="59aa2-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="59aa2-179">**Beispiel für formatierte Nummer**: Req0052</span><span class="sxs-lookup"><span data-stu-id="59aa2-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="59aa2-180">Da der Umfang **Geteilt** ist, wird das Nummernsequenzformat in der gesamten Organisation verwendet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="59aa2-181">Sie können für verschiedene Bereiche der Organisation nicht verschiedene Nummernkreisformate verwenden.</span><span class="sxs-lookup"><span data-stu-id="59aa2-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="59aa2-182">Leistungsüberlegungen für Nummernkreise</span><span class="sxs-lookup"><span data-stu-id="59aa2-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="59aa2-183">Berücksichtigen Sie vor dem Einrichten von Nummernkreisen die folgenden Informationen, die Aufschluss darüber eben, wie sich die Konfiguration von Nummernkreisen auf die Systemleistung auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="59aa2-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="59aa2-184">Fortlaufende bzw. nicht fortlaufende Nummernkreise</span><span class="sxs-lookup"><span data-stu-id="59aa2-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="59aa2-185">Nummernkreise können fortlaufend bzw. nicht fortlaufend sein.</span><span class="sxs-lookup"><span data-stu-id="59aa2-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="59aa2-186">Bei einem fortlaufenden Nummernkreis werden keine Zahlen übersprungen, aber Zahlen werden ggf. nicht sequentiell verwendet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="59aa2-187">Zahlen aus einem nicht fortlaufenden Nummernkreis werden sequenziell verwendet, aber der Nummernkreis kann Zahlen überspringen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="59aa2-188">Beispiel: Ein Benutzer storniert eine Buchung. In diesem Fall wird eine Nummer generiert, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="59aa2-189">In einem fortlaufenden Nummernkreis wird diese Nummer später recycelt.</span><span class="sxs-lookup"><span data-stu-id="59aa2-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="59aa2-190">In einem nicht fortlaufenden Nummernkreis wird diese Nummer nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="59aa2-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="59aa2-191">Fortlaufende Nummernkreise sind normalerweise für externe Dokumente erforderlich, beispielsweise für Bestellungen, Aufträge und Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="59aa2-192">Fortlaufende Nummernkreise können sich jedoch negativ auf die Antwortzeiten des Systems auswirken, da das System jedes Mal, wenn ein Dokument oder ein Datensatz angelegt wird, eine Nummer aus der Datenbank anfordern muss.</span><span class="sxs-lookup"><span data-stu-id="59aa2-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="59aa2-193">Wenn Sie einen nicht fortlaufenden Nummernkreis verwenden, können Sie auf der Seite **Nummernkreise** auf dem Inforegister **Leistung** die Option **Vorabzuordnung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="59aa2-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="59aa2-194">Wenn Sie eine Menge von vorab zugeordneten Nummern angegeben, wählt das System diese Nummern aus und speichert sie im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="59aa2-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="59aa2-195">Neue Nummern werden nur aus der Datenbank angefordert, nachdem die vorab zugewiesenen Nummern verbraucht wurden.</span><span class="sxs-lookup"><span data-stu-id="59aa2-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="59aa2-196">Sofern nicht vorgeschrieben ist, fortlaufende Nummernkreise zu verwenden, wird empfohlen, aus Leistungsgründen nicht fortlaufende Nummernkreise zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="59aa2-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="59aa2-197">Automatische Bereinigung von Nummernkreisen</span><span class="sxs-lookup"><span data-stu-id="59aa2-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="59aa2-198">Bei einem Stromausfall, Anwendungsfehler oder einem anderen unerwarteten Problem kann das System die Nummern für fortlaufende Nummernkreise nicht automatisch recyceln.</span><span class="sxs-lookup"><span data-stu-id="59aa2-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="59aa2-199">Sie können den Bereinigungsprozess manuell oder automatisch ausführen, um die verloren gegangenen Nummern wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="59aa2-200">Berücksichtigen Sie aber die Serverauslastung, wenn Sie den Bereinigungsprozess planen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="59aa2-201">Es wird empfohlen, die Bereinigung außerhalb der Spitzenzeiten als Stapelverarbeitungslauf auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59aa2-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






