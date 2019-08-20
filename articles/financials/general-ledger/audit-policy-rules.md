---
title: Überwachungsrichtlinienregeln
description: Mithilfe von Überwachungsrichtlinien kann zur Sicherheit überprüft werden, ob Spesenabrechnungen, Kreditorenrechnungen und Bestellungen den von Ihnen erstellten Richtlinienregeln entsprechen. Alle Regeln, die einer Überwachungsrichtlinie zugeordnet sind, werden nach einem von Ihnen angegeben Zeitplan im Stapelverarbeitungsmodus ausgeführt.  Jede Richtlinienregel ist eine Instanz eines Richtlinienregeltyps. Für jeden Richtlinienregeltyp kann jeweils nur eine Richtlinienregel aktiv sein.
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de6406029aa88424863dd9a47505f5b3ad27f237
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839592"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="5c2fa-106">Überwachungsrichtlinienregeln</span><span class="sxs-lookup"><span data-stu-id="5c2fa-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c2fa-107">Mithilfe von Überwachungsrichtlinien kann zur Sicherheit überprüft werden, ob Spesenabrechnungen, Kreditorenrechnungen und Bestellungen den von Ihnen erstellten Richtlinienregeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="5c2fa-108">Alle Regeln, die einer Überwachungsrichtlinie zugeordnet sind, werden nach einem von Ihnen angegeben Zeitplan im Stapelverarbeitungsmodus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="5c2fa-109">Jede Richtlinienregel ist eine Instanz eines Richtlinienregeltyps.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="5c2fa-110">Für jeden Richtlinienregeltyp kann jeweils nur eine Richtlinienregel aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="5c2fa-111">Abfragen und Abfragetypen</span><span class="sxs-lookup"><span data-stu-id="5c2fa-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="5c2fa-112">Beim Erstellen einer Überwachungsrichtlinie wird zuerst ein Richtlinienregeltyp ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="5c2fa-113">Mit dem Richtlinienregeltyp wird die Entwicklungsumgebungsabfrage angegeben, die als Ausgangspunkt für die Erstellung der Richtlinienregel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="5c2fa-114">Zudem wird der Abfragetyp für die Richtlinienregel angegeben.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="5c2fa-115">Mit der Abfrage wird das Quelldokument bestimmt, das die Richtlinienregel überprüft.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="5c2fa-116">Außerdem werden die Felder im Quelldokument angegeben, das die juristische Person identifiziert, sowie das Feld mit dem Datum, das bei der Auswahl der zu überwachenden Dokumente verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="5c2fa-117">Der Abfragetyp steuert die Standardfelder auf der Abfrageseite und der Seite "Überwachungsrichtlinienregel".</span><span class="sxs-lookup"><span data-stu-id="5c2fa-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="5c2fa-118">In der folgenden Tabelle werden die für Überwachungsrichtlinien verfügbaren Abfragetypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c2fa-119">Abfragetyp</span><span class="sxs-lookup"><span data-stu-id="5c2fa-119">Query type</span></span></th>
<th><span data-ttu-id="5c2fa-120">Verwendungszweck</span><span class="sxs-lookup"><span data-stu-id="5c2fa-120">Purpose</span></span></th>
<th><span data-ttu-id="5c2fa-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5c2fa-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c2fa-122">Bedingt</span><span class="sxs-lookup"><span data-stu-id="5c2fa-122">Conditional</span></span></td>
<td><span data-ttu-id="5c2fa-123">Überprüfen der Attribute des Quelldokuments auf angegebene Werte.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c2fa-124">Zusammenführen</span><span class="sxs-lookup"><span data-stu-id="5c2fa-124">Aggregate</span></span></td>
<td><span data-ttu-id="5c2fa-125">Überprüfen mehrerer Quelldokumente oder Quelldokumentpositionen auf eine Richtlinienregel durch Aggregieren numerischer Werte.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c2fa-126">Musteraufnahme</span><span class="sxs-lookup"><span data-stu-id="5c2fa-126">Sampling</span></span></td>
<td><span data-ttu-id="5c2fa-127">Zufällige Auswahl eines angegebenen Prozentsatzes an Quelldokumenten zur Überprüfung auf Richtlinienverletzungen.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="5c2fa-128">Wenn Sie diese Option auswählen, verwenden Sie die Seite "Überwachungsrichtlinienregel", mit der Sie den Prozentsatz der Dokumente für die zufällige Auswahl zur Überwachung angeben können.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c2fa-129">Duplizieren</span><span class="sxs-lookup"><span data-stu-id="5c2fa-129">Duplicate</span></span></td>
<td><span data-ttu-id="5c2fa-130">Überprüfen der Quelldokumente auf doppelte Einträge in angegebenen Feldern.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="5c2fa-131">Wenn Sie diese Option auswählen, verwenden Sie die Seite "Überwachungsrichtlinienregel", mit der Sie die Anzahl der Tage angeben können, die dem Startdatum des Datumsbereichs für die Dokumentauswahl bei der Überprüfung auf doppelte Einträge hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c2fa-132">Listensuche</span><span class="sxs-lookup"><span data-stu-id="5c2fa-132">List search</span></span></td>
<td><span data-ttu-id="5c2fa-133">Überprüfen der Quelldokumente auf bestimmte Entitäten.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="5c2fa-134">Das überwachte Dokument wird durch das Stammdokument der Abfrage definiert.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="5c2fa-135">Die Abfrage muss eine Listenabfrage sein, die eine Referenz zur dirpartytable-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="5c2fa-136">Diese Option kann nur mit den folgenden Entwicklungsumgebungsabfragen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="5c2fa-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="5c2fa-137"><span class="ui">AuditPolicyExpenseList</span> (Spesenabrechnung - überwachte Mitarbeiter)</span><span class="sxs-lookup"><span data-stu-id="5c2fa-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="5c2fa-138"><span class="ui">AuditPolicyPurchList</span> (Bestellung - überwachte Kreditoren)</span><span class="sxs-lookup"><span data-stu-id="5c2fa-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="5c2fa-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Kreditorenrechnung - überwachte Kreditoren)</span><span class="sxs-lookup"><span data-stu-id="5c2fa-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="5c2fa-140">Geben Sie bei Auswahl dieser Option die überwachten Entitäten auf der Seite "Überwachungsrichtlinienregel" an.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c2fa-141">Schlüsselwortsuche</span><span class="sxs-lookup"><span data-stu-id="5c2fa-141">Keyword search</span></span></td>
<td><span data-ttu-id="5c2fa-142">Überprüfen von Quelldokumenten auf bestimmte Wörter.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="5c2fa-143">Geben Sie bei Auswahl dieser Option die zu suchenden Wörter auf der Seite "Überwachungsrichtlinienregel" ein.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="5c2fa-144">Die Seite "Überwachungsrichtlinienregel" enthält auch Optionen, mit denen Sie die Tabellen und Felder angeben können, die auf die eingegebenen Wörter überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="5c2fa-145">Allgemeine Parameter</span><span class="sxs-lookup"><span data-stu-id="5c2fa-145">Common parameters</span></span>
<span data-ttu-id="5c2fa-146">Alle Richtlinienregeln für eine bestimmte Überwachungsrichtlinie besitzen dieselben Stapelverarbeitungsparameter und denselben Datumsbereich für die Dokumentauswahl.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="5c2fa-147">Diese Parameter werden auf der Seite "Zusätzliche Optionen" für die Richtlinie angegeben.</span><span class="sxs-lookup"><span data-stu-id="5c2fa-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="5c2fa-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5c2fa-148">Additional resources</span></span>
--------

<span data-ttu-id="5c2fa-149">[Überwachungsrichtlinienverletzungen und - anfragen](audit-policy-violations-cases.md)
[Definieren Sie Überwachungsrichtlinien für Quelldokumente](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="5c2fa-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>


