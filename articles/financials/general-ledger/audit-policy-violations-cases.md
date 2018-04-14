---
title: "Überwachungsrichtlinienverletzungen und -anfragen"
description: "Der Artikel beschrieben, wie Überwachungsanfragen aus den Verletzungen von Überwachungsrichtlinienregeln generiert werden. Er umfasst außerdem Informationen zu den verschiedenen Methoden, die Überwachungsrichtlinien für den Datumsbereich für die Dokumentauswahl verwenden."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c44beba51538184c062b53d643bda98de3d752b4
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="d1524-104">Überwachungsrichtlinienverletzungen und -anfragen</span><span class="sxs-lookup"><span data-stu-id="d1524-104">Audit policy violations and cases</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d1524-105">Der Artikel beschrieben, wie Überwachungsanfragen aus den Verletzungen von Überwachungsrichtlinienregeln generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1524-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="d1524-106">Er umfasst außerdem Informationen zu den verschiedenen Methoden, die Überwachungsrichtlinien für den Datumsbereich für die Dokumentauswahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1524-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="d1524-107">Generieren von Überwachungsanfragen</span><span class="sxs-lookup"><span data-stu-id="d1524-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="d1524-108">Mithilfe von Überwachungsrichtlinien werden Spesenabrechnungen, Bestellungen und Kreditorenrechnungen ermittelt, die den von Ihnen als Überwachungsrichtlinienregeln definierten und konfigurierten Geschäftsregeln widersprechen.</span><span class="sxs-lookup"><span data-stu-id="d1524-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="d1524-109">Überwachungsrichtlinien werden im Stapelverarbeitungsmodus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1524-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="d1524-110">Wenn Sie eine Überwachungsrichtlinie ausführen, werden alle Regeln der Richtlinie gleichzeitig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1524-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="d1524-111">Jede Richtlinienregel wertet eine Reihe von Dokumenten aus.</span><span class="sxs-lookup"><span data-stu-id="d1524-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="d1524-112">Die Richtlinienregel wählt die Dokumente aus, die sich im Datumsbereich für die Dokumentauswahl befinden und den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d1524-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="d1524-113">Mit einer Richtlinienregel können z. B. Spesenabrechnungen ausgewählt werden, die Mahlzeiten für über 50,00 EUR enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1524-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="d1524-114">Mit einer anderen Richtlinienregel können Kreditorenrechnungen ausgewählt werden, die an einen bestimmten Kreditor zu zahlen sind.</span><span class="sxs-lookup"><span data-stu-id="d1524-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="d1524-115">Für jedes Dokument, das in der Gruppe ausgewählt wird, wird ein Verstoß generiert.</span><span class="sxs-lookup"><span data-stu-id="d1524-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="d1524-116">Bei diesem Verstoß wird in einem Datensatz aufgezeichnet, dass ein bestimmtes Dokument (z. B. Rechnung 12345) der Richtlinienregel nicht entspricht.</span><span class="sxs-lookup"><span data-stu-id="d1524-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="d1524-117">Dabei werden mehrere Datensätze für Überwachungsverstöße gruppiert und Überwachungsanfragen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d1524-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="d1524-118">Anfragen für die einzelnen Überwachungsrichtlinien werden standardmäßig nach der Überwachungsrichtlinienregel gruppiert.</span><span class="sxs-lookup"><span data-stu-id="d1524-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="d1524-119">Wenn Sie es bevorzugen, können Sie andere Gruppierungskriterien auswählen, indem Sie die Seite **Anfragegruppierungskriterien** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1524-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="d1524-120">Sie können z. B. Ausgabenkopfdaten nach Projektkennung und Kreditorenrechnungen nach Kreditorenkonto gruppieren.</span><span class="sxs-lookup"><span data-stu-id="d1524-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="d1524-121">In diesem Fall werden alle Verstöße im Hinblick auf Ausgabenkopfdaten mit der gleichen Projektkennung in derselben Anfrage und alle Kreditorenrechnungsverstöße mit dem gleichen Kreditorenkonto in derselben Anfrage gruppiert.</span><span class="sxs-lookup"><span data-stu-id="d1524-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="d1524-122">Hinweis: Bei Überwachungsrichtlinienregeln, die auf dem **Duplizieren**-Abfragetyp basieren, werden Verstöße nicht nach Richtlinienregel oder nach den Kriterien gruppiert, die auf der Seite **Anfragegruppierungskriterien** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1524-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="d1524-123">Die Gruppierung richtet sich stattdessen nach den in die Überwachungsrichtlinienregel integrierten Kriterien.</span><span class="sxs-lookup"><span data-stu-id="d1524-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="d1524-124">Wenn beispielsweise eine Richtlinienregel Spesenrechnungen auf doppelte Ausgaben auswertet, bei denen Betrag, Händlerkennung und Datum übereinstimmen, stellen alle Ausgaben mit denselben Werten in diesen Feldern eine Anfrage dar.</span><span class="sxs-lookup"><span data-stu-id="d1524-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="d1524-125">Alle Ausgaben, die verschiedene Werte besitzen, sind getrennte Anfragen.</span><span class="sxs-lookup"><span data-stu-id="d1524-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="d1524-126">Nachdem die Überwachungsanfragen generiert wurden, werden sie mit den üblichen Prozessen der Anfrageverwaltung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d1524-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="d1524-127">Datumsbereich für die Dokumentauswahl</span><span class="sxs-lookup"><span data-stu-id="d1524-127">Document selection date ranges</span></span>
<span data-ttu-id="d1524-128">Beim Ausführen einer Überwachungsrichtlinie wählt jede Richtlinienregel Dokumente vom angegebenen Typ aus, die ein Datum aus dem Datumsbereich für die Dokumentauswahl aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d1524-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="d1524-129">Der Datumsbereich für die Dokumentauswahl wird auf der Seite **Zusätzliche Optionen** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d1524-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="d1524-130">Vielen Dokumenten sind mehrere Datumsangaben zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d1524-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="d1524-131">Das Datumsfeld, das der Überwachungsrichtlinienregel verwendet, wird auf der Seite **Richtlinienregeltyp** angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1524-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="d1524-132">Nachfolgend werden einige andere Methoden aufgeführt, auf die eine Überwachungsrichtlinie den Datumsbereich für die Dokumentauswahl verwendet:</span><span class="sxs-lookup"><span data-stu-id="d1524-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="d1524-133">In der Richtlinie wird die Version jeder Richtlinienregel verwendet, die am letzten Tag des Datumsbereichs für die Dokumentauswahl gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d1524-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="d1524-134">Sie können die Gültigkeitsdaten der einzelnen Richtlinienregeln auf der Listenseite **Überwachungsrichtlinien** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d1524-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="d1524-135">In der Richtlinie werden die Organisationsknoten verwendet, die der Richtlinie am letzten Tag des Datumsbereichs für die Dokumentauswahl zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d1524-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="d1524-136">Auf der Listenseite **Überwachungsrichtlinien** werden nur die Organisationsknoten angezeigt, die der Richtlinie gegenwärtig zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d1524-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="d1524-137">Für auf dem Abfragetyp **Listensuche** basierende Richtlinienregeln wertet die Richtlinie Dokumente für überwachte Entitäten aus, die am letzten Tag des Datumsbereichs für die Dokumentauswahl gültig sind.</span><span class="sxs-lookup"><span data-stu-id="d1524-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="d1524-138">Weitere Informationen zu den [Richtlinienregeltypen](audit-policy-rules.md) finden Sie unter .</span><span class="sxs-lookup"><span data-stu-id="d1524-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>




