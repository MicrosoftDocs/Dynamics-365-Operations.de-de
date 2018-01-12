---
title: "Arbeitsbereich für die Bankverwaltung"
description: "Dieses Thema enthält Informationen zum Bankwesen-Arbeitsbereich. Der Arbeitsbereich zeigt Informationen hinsichtlich der Bankkonten des Unternehmens und enthält eine Zusammenfassungsansicht und eine Analyseseite. Die Zusammenfassungsansicht zeigt Übersichtskacheln, Bankkontoinformationen, ein Saldodiagramm und zugehörige Informationen an. Die Analyseseite verwendet die Funktionen von Microsoft Power BI, um grafische Elemente hinsichtlich der Bankkontosalden anzuzeigen."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: a090d5deef80260858413fa49011b983c6bf4b20
ms.contentlocale: de-de
ms.lasthandoff: 01/12/2018

---
# <a name="bank-management-workspace"></a><span data-ttu-id="c988f-106">Arbeitsbereich für die Bankverwaltung</span><span class="sxs-lookup"><span data-stu-id="c988f-106">Bank management workspace</span></span>

<span data-ttu-id="c988f-107">Der Arbeitsbereich **Bankwesen** zeigt Informationen bezüglich der Bankkonten des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="c988f-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="c988f-108">Der Arbeitsbereich umfasst eine Ansicht **Zusammenfassung** und eine Seite **Analyse**.</span><span class="sxs-lookup"><span data-stu-id="c988f-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="c988f-109">Die **Zusammenfassungsansicht** zeigt Übersichtskacheln, Bankkontoinformationen, ein Saldodiagramm und zugehörige Informationen an.</span><span class="sxs-lookup"><span data-stu-id="c988f-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="c988f-110">Die **Analyseseite** verwendet die Funktionen von Microsoft Power BI, um grafische Elemente hinsichtlich der Bankkontosalden anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c988f-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="c988f-111">Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="c988f-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="c988f-112">Summe</span><span class="sxs-lookup"><span data-stu-id="c988f-112">Summary</span></span>

<span data-ttu-id="c988f-113">Die Kacheln im Abschnitt **Zusammenfassung** bieten einen Überblick der Bankkonten und schnellen Zugriff auf Seiten, die Sie am häufigsten verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="c988f-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="c988f-114">Die Bankabstimmungsinformationen sind für die erweiterten Bankabstimmungsfunktionen spezifisch.</span><span class="sxs-lookup"><span data-stu-id="c988f-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="c988f-115">Informationen sind nur für die Bankkonten enthalten, bei denen die Option **Erweiterte Bankabstimmung** auf **Ja** auf der Seite **Bankkonto** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c988f-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="c988f-116">Im Abschnitt **Zusammenfassung** können Sie elektronische Bankdateien für Bankkonten für alle juristischen Person importieren.</span><span class="sxs-lookup"><span data-stu-id="c988f-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="c988f-117">Bankkonten</span><span class="sxs-lookup"><span data-stu-id="c988f-117">Bank accounts</span></span>

<span data-ttu-id="c988f-118">Jedes Bankkonto bei der juristischen Person wird als eine Karte im Abschnitt **Bankkonten** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c988f-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="c988f-119">Der aktuelle Saldo wird angezeigt und Sie können Detailinformationen zu den Buchungen anzeigen, aus denen dieser zusammengefasste Saldobetrag besteht.</span><span class="sxs-lookup"><span data-stu-id="c988f-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="c988f-120">Für den Betrag **Transferbuchungen** können Sie auch Detailinformationen zu den Buchungen anzeigen, aus denen dieser zusammengefasste Betrag besteht.</span><span class="sxs-lookup"><span data-stu-id="c988f-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="c988f-121">Transferbuchungen sind alle ausstehende Buchungen, die bereits mithilfe der Transferfunktionen ausgeführt wurden, aber noch nicht verrechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c988f-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="c988f-122">Der Betrag **Ausstehender Saldo** ist der aktuelle Saldos minus der Transfer- oder ausstehenden Buchungen.</span><span class="sxs-lookup"><span data-stu-id="c988f-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="c988f-123">Die Karte zeigt außerdem an, wann das Bankkonto zuletzt abgestimmt wurde.</span><span class="sxs-lookup"><span data-stu-id="c988f-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="c988f-124">Diese Informationen werden nur angezeigt, wenn die erweiterte Bankabstimmung für das Bankkonto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c988f-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="c988f-125">Bilanz</span><span class="sxs-lookup"><span data-stu-id="c988f-125">Balance</span></span>

<span data-ttu-id="c988f-126">Das **Saldo**-Diagramm zeigt historische Saldoinformationen für das Bankkonto an, das im **Bankkonten**-Abschnitt ausgewählt wurde, oder eine Übersicht der historischen Saldoinformationen für alle Bankkonten bei der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="c988f-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="c988f-127">Diese Informationen sind für verschiedene Zeiträume verfügbar: die aktuelle Woche, den aktuellen Monat, das aktuelle Jahr, die letzten fünf Jahre und alle Zeiträume (der vollständige Verlauf des Bankkontos).</span><span class="sxs-lookup"><span data-stu-id="c988f-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="c988f-128">Wenn Sie das **Saldo**-Diagramm für ein einzelnes Bankkonto anzeigen, werden die historischen Salden in der Bankkontowährung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c988f-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="c988f-129">Wenn Sie das Saldo-Diagramm aller Bankkonten der juristischen Person anzeigen, werden die historischen Salden in der Buchhaltungswährung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c988f-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="c988f-130">Informationen dazu, wann die Daten zuletzt aktualisiert wurden, werden am Anfang des Diagramms angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c988f-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="c988f-131">Sie können die Daten bei Bedarf aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c988f-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="c988f-132">Zugehörige Informationen</span><span class="sxs-lookup"><span data-stu-id="c988f-132">Related information</span></span>

<span data-ttu-id="c988f-133">Aus dem Abschnitt **Zugehörige Informationen** können Sie die Seite **Allgemeine Erfassung** öffnen, um Banküberweisungen abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c988f-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="c988f-134">Sie können die Seiten **Bankbuchungen** und **Transferbuchungen** auch schnell öffnen.</span><span class="sxs-lookup"><span data-stu-id="c988f-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="c988f-135">Analyseansicht</span><span class="sxs-lookup"><span data-stu-id="c988f-135">Analytics view</span></span>

<span data-ttu-id="c988f-136">Die Seite **Analyse** enthält wichtige Metriken zu Bankkonten im aktuellen Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="c988f-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="c988f-137">Die folgenden Visualisierungen sind auf der Seite verfügbar:</span><span class="sxs-lookup"><span data-stu-id="c988f-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="c988f-138">Gesamter Banksaldo in der Systemwährung</span><span class="sxs-lookup"><span data-stu-id="c988f-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="c988f-139">Saldo nach juristischer Person</span><span class="sxs-lookup"><span data-stu-id="c988f-139">Balance by legal entity</span></span>
-   <span data-ttu-id="c988f-140">Vergleich des heutigen Ist-Saldos gegenüber des geplanten Saldos in Bankkontowährung</span><span class="sxs-lookup"><span data-stu-id="c988f-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="c988f-141">Saldo nach Bankkonto</span><span class="sxs-lookup"><span data-stu-id="c988f-141">Balance by bank account</span></span>
-   <span data-ttu-id="c988f-142">Saldo in Währung</span><span class="sxs-lookup"><span data-stu-id="c988f-142">Balance by currency</span></span>

<span data-ttu-id="c988f-143">Sie können die Bankanalyse für alle Unternehmen im Arbeitsbereich **Bargeldüberblick – alle Unternehmen** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c988f-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span>

