---
title: Allgemeine Erfassungsverarbeitung
description: "Dieser Artikel beschreibt die Funktionen in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edtion, mit denen die allgemeine Erfassung einfacher wird, und die auch helfen sicherzustellen, dass die korrekten Daten erfasst und die internen Kontrollen nicht beeinträchtigt werden."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 76386f7ab8033075f9db4cadc697f3a2a997163e
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="general-journal-processing"></a><span data-ttu-id="b95b0-103">Allgemeine Erfassungsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="b95b0-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b95b0-104">Dieser Artikel beschreibt die Funktionen in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edtion, mit denen die allgemeine Erfassung einfacher wird, und die auch helfen sicherzustellen, dass die korrekten Daten erfasst und die internen Kontrollen nicht beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="b95b0-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="b95b0-105">Journale</span><span class="sxs-lookup"><span data-stu-id="b95b0-105">Journal names</span></span>

<span data-ttu-id="b95b0-106">Einer der wichtigsten Bereiche einrichten ist Journale.</span><span class="sxs-lookup"><span data-stu-id="b95b0-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="b95b0-107">Es empfiehlt sich, bestimmte Journale für jeden Zweck, wie Abgrenzungsregulierung Fehlerkorrektur Intercompany, und zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b95b0-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="b95b0-108">Sie können jedes Journal anpassen, mit deren Hilfe, Dateneingabe für jeden Zweck einfach und sicherstellen zu machen.</span><span class="sxs-lookup"><span data-stu-id="b95b0-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="b95b0-109">Auf der Seite **Journale** können Sie folgende Elemente einrichten:</span><span class="sxs-lookup"><span data-stu-id="b95b0-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="b95b0-110">**Workflowgenehmigung** - Definieren Sie Journal-Workflows, die basierend auf Kriterien wie „Gesamt“ oder „Betrag“ Wesentlichkeitsgrenzen für Überprüfung- und Genehmigungsschritte festlegen, um die interne Kontrolle zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b95b0-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="b95b0-111">Sie richten Workflows für die allgemeinen Erfassungen auf der Seite **Hauptbuchworkflows** ein.</span><span class="sxs-lookup"><span data-stu-id="b95b0-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="b95b0-112">**Standardwerte** – Wählen Sie Standardwerte für Gegenkonten, Währung und Finanzdimensionen aus.</span><span class="sxs-lookup"><span data-stu-id="b95b0-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="b95b0-113">**Erfassungssteuerung** – Richten Sie Einschränkungen für den Unternehmens- und Kontotyp und die Segmentwerte ein.</span><span class="sxs-lookup"><span data-stu-id="b95b0-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="b95b0-114">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="b95b0-114">**Examples**</span></span>

<span data-ttu-id="b95b0-115">Ein Journal kann nur für Regulierungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b95b0-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="b95b0-116">In diesem Fall können Sie angeben, dass nur die **Sachkonto**-Kontenart für alle Unternehmen gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b95b0-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="b95b0-117">[![Erfassungssteuerungs-Kontotypen](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="b95b0-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="b95b0-118">Ein Journal kann nur für ein bestimmtes Segment oder für einen Bereich für Hauptkonten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b95b0-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="b95b0-119">[![Erfassungssteuerungssegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="b95b0-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="b95b0-120">Die Option **Automatische Rückbuchung** ist nur in allgemeinen Erfassungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b95b0-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="b95b0-121">Beispiel: Sie haben eine Abgrenzungsregulierung, in der das eigentliche Dokument noch nicht verarbeitet wurde, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b95b0-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="b95b0-122">[![Erfassungsrücksetzung](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="b95b0-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="b95b0-123">Rückbuchung allgemeine Erfassung Das Microsoft Excel-Add-in für Journaleinträge bietet eine weitere Ebene der Automatisierung und erleichtert die Dateneingabe.</span><span class="sxs-lookup"><span data-stu-id="b95b0-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="b95b0-124">Die **Positionen in Excel öffnen**-Aktivität ist auf den Seiten **Allgemeine Erfassung** und **Alle Journale** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b95b0-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="b95b0-125">Auf der Seite **Periodische Erfassungen** können Sie wiederholende Erfassungen einrichten, um die Erfassungsverarbeitung zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="b95b0-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="b95b0-126">Belegvorlagen können jederzeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="b95b0-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="b95b0-127">Auf der Seite **Allgemeine Erfassungen** finden Sie die Aktivitäten **Speichern** und **Belegvorlage auswählen** auf der Seite **Alle Journale** unter **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="b95b0-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="b95b0-128">Verwandte Einstellung</span><span class="sxs-lookup"><span data-stu-id="b95b0-128">Related setup</span></span>
<span data-ttu-id="b95b0-129">Die folgende Einstellung ist für allgemeine Erfassungen nicht spezifisch, sorgt aber dafür, dass die Dateneingabe richtig und einfach ist.</span><span class="sxs-lookup"><span data-stu-id="b95b0-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="b95b0-130">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="b95b0-130">Main account</span></span>

<span data-ttu-id="b95b0-131">Die Hauptkontoeinstellung stellt viele Optionen zum Verarbeiten der allgemeinen Erfassung bereit:</span><span class="sxs-lookup"><span data-stu-id="b95b0-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="b95b0-132">**SOLL/HABEN-Anforderung** - Verwenden Sie diese Option, wenn ein Hauptkonto auf Soll- oder Habenbuchungen beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="b95b0-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="b95b0-133">Die Einstellung wird überprüft, wenn eine Erfassung geprüft oder gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="b95b0-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="b95b0-134">**Standardgegenkonto**</span><span class="sxs-lookup"><span data-stu-id="b95b0-134">**Default offset account**</span></span>
-   <span data-ttu-id="b95b0-135">**Unterbrochen** – Aussetzen eines Hauptkontos für die Dateneingabe für alle Unternehmen oder für ein bestimmtes Unternehmen bzw. bestimmte juristische Personen</span><span class="sxs-lookup"><span data-stu-id="b95b0-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="b95b0-136">**Keine manuellen Eingaben zulassen** – Verhindert, dass Benutzer in Erfassungen manuell einen Wert für dieses Konto eingeben</span><span class="sxs-lookup"><span data-stu-id="b95b0-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="b95b0-137">**Standard-Währung/Währung prüfen**</span><span class="sxs-lookup"><span data-stu-id="b95b0-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="b95b0-138">**Juristische Person überschreibt** - Diese Einstellung ist spezifisch für das definierte Unternehmen/die definierte juristische Person:</span><span class="sxs-lookup"><span data-stu-id="b95b0-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="b95b0-139">**Standard-MwSt/MwSt prüfen**</span><span class="sxs-lookup"><span data-stu-id="b95b0-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="b95b0-140">**Standarddimension** – **Nicht fixiert** oder **Fester Wert**</span><span class="sxs-lookup"><span data-stu-id="b95b0-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="b95b0-141">**Fester Wert** unterstützt, dass alle Buchungen für dieses Hauptkonto immer einen beliebigen Dimensionswert verwenden, der als **Fest** eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="b95b0-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="b95b0-142">**Buchungsprüfung**</span><span class="sxs-lookup"><span data-stu-id="b95b0-142">**Posting validation**</span></span>
    -   <span data-ttu-id="b95b0-143">**Benutzervalidierung** - Diese Option regelt, welche Benutzer auf ein Hauptkonto buchen dürfen.</span><span class="sxs-lookup"><span data-stu-id="b95b0-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="b95b0-144">**Überprüfung des Buchungstyps** – Diese Option regelt, welche Buchungsarten für ein Hauptkonto zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b95b0-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="b95b0-145">Buchhaltungsstrukturen und Strukturen für erweiterte Regeln</span><span class="sxs-lookup"><span data-stu-id="b95b0-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="b95b0-146">Buchhaltungsstrukturen und Strukturen für erweiterte Regeln sind sehr wichtig, um sicherzustellen, dass die Daten, die für die Finanzberichterstellung und die Leistungsnachverfolgung erforderlich sind, während der allgemeinen Erfassungsverarbeitung und in allen Dokumentationen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="b95b0-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="b95b0-147">Mit Buchhaltungsstrukturen und Strukturen für erweiterten Regeln können Sie die Dateneingabeerfahrung anpassen.</span><span class="sxs-lookup"><span data-stu-id="b95b0-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="b95b0-148">Sie können die Dateneingabe nur für Finanzdimensionen zulassen, die in jeder Situation relevant sind. Sie können auch die Anforderung erzwingen, dass erforderliche und korrekte Daten immer erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="b95b0-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="b95b0-149">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b95b0-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="b95b0-150">[Kontenplan planen](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="b95b0-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="b95b0-151">Erweiterte Regeln für Erfassungen erstellen</span><span class="sxs-lookup"><span data-stu-id="b95b0-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="b95b0-152">Journaleinträge mithilfe einer Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="b95b0-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="b95b0-153">Erfassungen erstellen und validieren</span><span class="sxs-lookup"><span data-stu-id="b95b0-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="b95b0-154">Periodische Erfassungen veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="b95b0-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="b95b0-155">Sachkonto-Zuordnungserfassung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="b95b0-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



