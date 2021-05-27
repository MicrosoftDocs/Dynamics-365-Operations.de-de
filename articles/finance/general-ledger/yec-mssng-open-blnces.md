---
title: Fehlende Anfangssalden für den Jahresabschluss
description: In diesem Thema wird erläutert, warum beim Jahresabschluss möglicherweise Anfangssalden fehlen und wie diese Salden ggf. neu erstellt werden.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028565"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="9add9-103">Fehlende Anfangssalden für den Jahresabschluss</span><span class="sxs-lookup"><span data-stu-id="9add9-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9add9-104">In diesem Thema wird erläutert, warum beim Jahresabschluss möglicherweise Anfangssalden fehlen und wie diese Salden ggf. neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9add9-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="9add9-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="9add9-105">Symptom</span></span>

<span data-ttu-id="9add9-106">Warum gibt es nach dem Jahresabschluss des Hauptbuchs keine Anfangssalden?</span><span class="sxs-lookup"><span data-stu-id="9add9-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="9add9-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="9add9-107">Resolution</span></span>

<span data-ttu-id="9add9-108">Im Folgenden finden Sie die zu prüfenden Elemente, wenn Sie ein Jahr im Hauptbuch abgeschlossen und dann eine Zwischenbilanz erstellt haben, bei der Anfangssalden für das nächste Geschäftsjahr nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9add9-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="9add9-109">Wenn das Feld **Vorherigen Abschluss rückgängig machen** auf **Ja** eingestellt ist, wird der vorherige Abschluss für das gleiche Geschäftsjahr rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="9add9-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="9add9-110">Beim Prozess des Rückgängigmachens werden alle Einträge der Abschluss- und Anfangssalden gelöscht, als wäre der Jahresendabschluss nie erfolgt.</span><span class="sxs-lookup"><span data-stu-id="9add9-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="9add9-111">Belege werden ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9add9-111">The vouchers are also deleted.</span></span> <span data-ttu-id="9add9-112">Der Jahresendabschlussprozess wird nicht automatisch erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9add9-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="9add9-113">Vielmehr muss der Vorgang manuell erneut gestartet werden, wobei die Option **Vorherigen Abschluss rückgängig machen** auf **Nein** aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9add9-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="9add9-114">Dieses Szenario wird im FAQ-Thema zum Jahresabschluss behandelt.</span><span class="sxs-lookup"><span data-stu-id="9add9-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="9add9-115">Weitere Informationen finden Sie unter [Häufig gestellte Fragen zu Aktivitäten am Jahresende](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="9add9-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="9add9-116">Symptom</span><span class="sxs-lookup"><span data-stu-id="9add9-116">Symptom</span></span>

<span data-ttu-id="9add9-117">Ich habe den Jahresabschluss durchgeführt, während die Option **Vorherigen Abschluss rückgängig machen** auf **Nein** festgelegt war, und ich habe noch keine Anfangssalden für mein Geschäftsjahr.</span><span class="sxs-lookup"><span data-stu-id="9add9-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="9add9-118">Lösung</span><span class="sxs-lookup"><span data-stu-id="9add9-118">Resolution</span></span>

<span data-ttu-id="9add9-119">Prüfen Sie zunächst den Status des Stapelverarbeitungsauftrags.</span><span class="sxs-lookup"><span data-stu-id="9add9-119">First check the status of the batch job.</span></span> <span data-ttu-id="9add9-120">Der Jahresabschluss umfasst eine Reihe separater Aufgaben. Der wichtigste Schritt ist jedoch der Stapelverarbeitungsauftrag mit der Aufgabenbeschreibung **Schritt 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="9add9-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="9add9-121">Während dieses Schritts erfolgt die Buchung der Primobuchungen und optional der Abschlussbuchungen im Hauptbuch.</span><span class="sxs-lookup"><span data-stu-id="9add9-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="9add9-122">[![Historie der Stapelverarbeitungen](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="9add9-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="9add9-123">Wenn dieser Schritt erfolgreich beendet wurde jedoch keine Anfangssalden auf der Seite **Zwischenbilanzermittlung** (**Hauptbuch > Abfragen und Berichte > Zwischenbilanz**) angezeigt werden, überprüfen Sie die Ergebnisse des Stapelverarbeitungsauftrags zum Jahresabschluss, um festzustellen, ob der Schritt „Salden neu erstellen“ erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9add9-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="9add9-124">[![Ergebnisse des Stapelverarbeitungsauftrags zum Jahresabschluss](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="9add9-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="9add9-125">Wenn dieser Schritt aus irgendeinem Grund fehlgeschlagen ist, wurden die Primobuchungen (und optional Abschlussbuchungen) wahrscheinlich erfolgreich gebucht.</span><span class="sxs-lookup"><span data-stu-id="9add9-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="9add9-126">Sie können überprüfen, ob die Hauptbuchbuchungen erfolgreich auf der Seite **Belegbuchungsabfrage** gebucht wurden, indem Sie die Belegnummer und das Datum angeben, die im Dialogfeld zum Jahresabschluss für das Jahr angegeben sind, das Sie abgeschlossen haben (**Hauptbuch > Abfragen und Berichte > Belegbuchungen**).</span><span class="sxs-lookup"><span data-stu-id="9add9-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="9add9-127">[![Belegbuchungsabfrage](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="9add9-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="9add9-128">Wenn die Eröffnungsbelege (und optional Abschlussbelege) vorhanden sind, müssen Sie den Jahresabschluss nicht erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="9add9-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="9add9-129">Informationen zum weiteren Vorgehen finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="9add9-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="9add9-130">Symptom</span><span class="sxs-lookup"><span data-stu-id="9add9-130">Symptom</span></span>

<span data-ttu-id="9add9-131">Der Schritt „Salden neu erstellen“ beim Jahresabschluss ist fehlgeschlagen. Muss ich den gesamten Jahresabschlussprozess erneut ausführen?</span><span class="sxs-lookup"><span data-stu-id="9add9-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="9add9-132">Lösung</span><span class="sxs-lookup"><span data-stu-id="9add9-132">Resolution</span></span>

<span data-ttu-id="9add9-133">Der Schritt „Salden neu erstellen“ aktualisiert die Hauptbuchsalden, die beim Generieren der Zwischenbilanzermittlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9add9-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="9add9-134">Dies ist der letzte Schritt im Jahresabschlussprozess.</span><span class="sxs-lookup"><span data-stu-id="9add9-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="9add9-135">Wenn dieser Schritt der einzige Schritt ist, der fehlgeschlagen ist, wurden die Hauptbuchbuchungen erfolgreich gebucht.</span><span class="sxs-lookup"><span data-stu-id="9add9-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="9add9-136">Sie müssen den Jahresendabschluss nicht erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="9add9-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="9add9-137">Sie können den Prozess ausführen, um die Salden manuell über die Seite **Finanzdimensionssätze** (**Hauptbuch > Kontenplan > Dimensionen > Finanzdimensionssätze**) neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9add9-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="9add9-138">[![Schaltfläche „Salden neu erstellen“ auf der Seite „Finanzdimensionssätze“](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="9add9-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="9add9-139">Wenn die Verarbeitung dieses Schritts lange dauert, empfehlen wir, die bewährten Methoden für Finanzdimensionssätze zu überprüfen, wie unter [Bewährte Methoden für die Aktualisierung von Finanzdimensionssätzen](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9add9-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

