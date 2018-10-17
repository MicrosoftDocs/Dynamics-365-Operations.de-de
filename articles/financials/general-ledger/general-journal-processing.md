---
title: Allgemeine Erfassungsverarbeitung
description: "Dieses Thema beschreibt Fähigkeiten in Microsoft Dynamics 365 for Finance and Operations, mit denen die allgemeine Erfassungsverarbeitung einfacher wird und die auch helfen sicherzustellen, dass die korrekten Daten erfasst und die interne Steuerung nicht beeinträchtigt werden."
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf744bc41ffcca6d029da5dd2031ada607a0109b
ms.openlocfilehash: e77aafafed5c972a6ad8c064107306d3ebde0b79
ms.contentlocale: de-de
ms.lasthandoff: 09/24/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="4ce0d-103">Allgemeine Erfassungsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="4ce0d-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ce0d-104">Dieses Thema beschreibt Fähigkeiten in Microsoft Dynamics 365 for Finance and Operations, mit denen die allgemeine Erfassungsverarbeitung einfacher wird und die auch helfen sicherzustellen, dass die korrekten Daten erfasst und die interne Steuerung nicht beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-104">This topic describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="4ce0d-105">Journale</span><span class="sxs-lookup"><span data-stu-id="4ce0d-105">Journal names</span></span>

<span data-ttu-id="4ce0d-106">Einer der wichtigsten Bereiche einrichten ist Journale.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="4ce0d-107">Es empfiehlt sich, bestimmte Journale für jeden Zweck, wie Abgrenzungsregulierung Fehlerkorrektur Intercompany, und zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="4ce0d-108">Sie können jedes Journal anpassen, mit deren Hilfe, Dateneingabe für jeden Zweck einfach und sicherstellen zu machen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="4ce0d-109">Auf der Seite **Journale** können Sie folgende Elemente einrichten:</span><span class="sxs-lookup"><span data-stu-id="4ce0d-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="4ce0d-110">**Workflowgenehmigung** - Definieren Sie Journal-Workflows, die basierend auf Kriterien wie „Gesamt“ oder „Betrag“ Wesentlichkeitsgrenzen für Überprüfung- und Genehmigungsschritte festlegen, um die interne Kontrolle zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="4ce0d-111">Sie richten Workflows für die allgemeinen Erfassungen auf der Seite **Hauptbuchworkflows** ein.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="4ce0d-112">**Standardwerte** – Wählen Sie Standardwerte für Gegenkonten, Währung und Finanzdimensionen aus.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="4ce0d-113">**Erfassungssteuerung** – Richten Sie Einschränkungen für den Unternehmens- und Kontotyp und die Segmentwerte ein.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="4ce0d-114">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="4ce0d-114">**Examples**</span></span>

<span data-ttu-id="4ce0d-115">Ein Journal kann nur für Regulierungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="4ce0d-116">In diesem Fall können Sie angeben, dass nur die **Sachkonto**-Kontenart für alle Unternehmen gültig ist.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="4ce0d-117">[![Erfassungssteuerungs-Kontotypen](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="4ce0d-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="4ce0d-118">Ein Journal kann nur für ein bestimmtes Segment oder für einen Bereich für Hauptkonten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="4ce0d-119">[![Erfassungssteuerungssegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="4ce0d-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="4ce0d-120">Die Option **Automatische Rückbuchung** ist nur in allgemeinen Erfassungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="4ce0d-121">Beispiel: Sie haben eine Abgrenzungsregulierung, in der das eigentliche Dokument noch nicht verarbeitet wurde, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="4ce0d-122">[![Erfassungsrücksetzung](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="4ce0d-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="4ce0d-123">Rückbuchung allgemeine Erfassung Das Microsoft Excel-Add-in für Journaleinträge bietet eine weitere Ebene der Automatisierung und erleichtert die Dateneingabe.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="4ce0d-124">Die **Positionen in Excel öffnen**-Aktivität ist auf den Seiten **Allgemeine Erfassung** und **Alle Journale** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="4ce0d-125">Auf der Seite **Periodische Erfassungen** können Sie wiederholende Erfassungen einrichten, um die Erfassungsverarbeitung zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="4ce0d-126">Belegvorlagen können jederzeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="4ce0d-127">Auf der Seite **Allgemeine Erfassungen** finden Sie die Aktivitäten **Speichern** und **Belegvorlage auswählen** auf der Seite **Alle Journale** unter **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="4ce0d-128">Verwandte Einstellung</span><span class="sxs-lookup"><span data-stu-id="4ce0d-128">Related setup</span></span>
<span data-ttu-id="4ce0d-129">Die folgende Einstellung ist für die allgemeine Erfassungen nicht spezifisch, sorgt aber dafür, dass die Dateneingabe richtig und einfach ist.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="4ce0d-130">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="4ce0d-130">Main account</span></span>

<span data-ttu-id="4ce0d-131">Die Hauptkontoeinstellung stellt viele Optionen zum Verarbeiten der allgemeinen Erfassung bereit:</span><span class="sxs-lookup"><span data-stu-id="4ce0d-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="4ce0d-132">**SOLL/HABEN-Anforderung** - Verwenden Sie diese Option, wenn ein Hauptkonto auf Soll- oder Habenbuchungen beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="4ce0d-133">Die Einstellung wird überprüft, wenn eine Erfassung geprüft oder gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="4ce0d-134">**Standardgegenkonto**</span><span class="sxs-lookup"><span data-stu-id="4ce0d-134">**Default offset account**</span></span>
-   <span data-ttu-id="4ce0d-135">**Unterbrochen** – Aussetzen eines Hauptkontos für die Dateneingabe für alle Unternehmen oder für ein bestimmtes Unternehmen bzw. bestimmte juristische Personen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="4ce0d-136">**Keine manuellen Eingaben zulassen** – Verhindert, dass Benutzer in Erfassungen manuell einen Wert für dieses Konto eingeben</span><span class="sxs-lookup"><span data-stu-id="4ce0d-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="4ce0d-137">**Standard-Währung/Währung prüfen**</span><span class="sxs-lookup"><span data-stu-id="4ce0d-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="4ce0d-138">**Juristische Person überschreibt** - Diese Einstellung ist spezifisch für das definierte Unternehmen/die definierte juristische Person:</span><span class="sxs-lookup"><span data-stu-id="4ce0d-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="4ce0d-139">**Standard-MwSt/MwSt prüfen**</span><span class="sxs-lookup"><span data-stu-id="4ce0d-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="4ce0d-140">**Standarddimension** – **Nicht fixiert** oder **Fester Wert**</span><span class="sxs-lookup"><span data-stu-id="4ce0d-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="4ce0d-141">**Fester Wert** unterstützt, dass sämtliche Buchungen für dieses Hauptkonto immer einen beliebigen Dimensionswert verwenden, der als **Fest** eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="4ce0d-142">**Buchungsprüfung**</span><span class="sxs-lookup"><span data-stu-id="4ce0d-142">**Posting validation**</span></span>
    -   <span data-ttu-id="4ce0d-143">**Benutzervalidierung** - Diese Option regelt, welche Benutzer auf ein Hauptkonto buchen dürfen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="4ce0d-144">**Überprüfung des Buchungstyps** – Diese Option regelt, welche Buchungsarten für ein Hauptkonto zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="4ce0d-145">Buchhaltungsstrukturen und Strukturen für erweiterte Regeln</span><span class="sxs-lookup"><span data-stu-id="4ce0d-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="4ce0d-146">Buchhaltungsstrukturen und Strukturen für die erweiterten Regeln sind sehr wichtig, um sicherzustellen, dass die Daten, die für die Finanzberichterstellung und die Leistungsnachverfolgung erforderlich sind, während der allgemeinen Erfassungsverarbeitung und in allen Dokumentationen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="4ce0d-147">Mit Buchhaltungsstrukturen und Strukturen für erweiterten Regeln können Sie die Dateneingabeerfahrung anpassen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="4ce0d-148">Sie können die Dateneingabe nur für Finanzdimensionen zulassen, die in jeder Situation relevant sind. Sie können auch die Anforderung erzwingen, dass die erforderlichen und korrekte  Daten immer erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="4ce0d-149">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4ce0d-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="4ce0d-150">[Kontenplan planen](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="4ce0d-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="4ce0d-151">Erweiterte Regeln für Erfassungen erstellen</span><span class="sxs-lookup"><span data-stu-id="4ce0d-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="4ce0d-152">Journaleinträge mithilfe einer Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="4ce0d-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="4ce0d-153">Erfassungen erstellen und validieren</span><span class="sxs-lookup"><span data-stu-id="4ce0d-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="4ce0d-154">Periodische Erfassungen buchen</span><span class="sxs-lookup"><span data-stu-id="4ce0d-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="4ce0d-155">Sachkonto-Zuordnungserfassung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="4ce0d-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="4ce0d-156">Buchung simulieren</span><span class="sxs-lookup"><span data-stu-id="4ce0d-156">Simulate posting</span></span>
<span data-ttu-id="4ce0d-157">Sie können **Buchung simulieren** im Menü **Überprüfen** für die meisten Erfassungen finden.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="4ce0d-158">Wenn Sie eine Erfassung mit der Funktion **Überprüfen** prüft das System die Erfassung für bestimmte Fehlerbedingungen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="4ce0d-159">Wenn Sie die Funktion **Buchung simulieren** verwenden, führt das System alle gleichen Prozessen aus, die während des Buchens durchgeführt werden, ohne die Erfassung zu buchen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="4ce0d-160">Sie können die Verbuchungsmeldungen, die angezeigt werden, überprüfen, die Fehler beheben, die Sie finden und dann das Menü **Buchen** klicken, um die Erfassung zu buchen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-160">You can then review the posting messages that are displayed, fix any errors that you find, and then click the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="4ce0d-161">**Buchen simulieren** ist nicht verfügbar für Stapelverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="4ce0d-162">Allerdings ist ein Code vorhanden, um die Buchung in Chargen zu simulieren und Entwickler können den Code erweitern, um diese Funktionen ergänzen.</span><span class="sxs-lookup"><span data-stu-id="4ce0d-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  

