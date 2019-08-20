---
title: Geschäftsjahr abschließen
description: Dieses Verfahren führt Sie durch den Jahresabschlussprozess, der Salden in ein neues Geschäftsjahr übertragen.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c12f0842f6e8edf3b51d12d0e008eb09acf8c374
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834925"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="34957-103">Geschäftsjahr abschließen</span><span class="sxs-lookup"><span data-stu-id="34957-103">Close the fiscal year</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34957-104">Dieses Verfahren führt Sie durch den Jahresabschlussprozess, der Salden in ein neues Geschäftsjahr übertragen.</span><span class="sxs-lookup"><span data-stu-id="34957-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="34957-105">Prüfen von Parameter für Jahresabschlüsse</span><span class="sxs-lookup"><span data-stu-id="34957-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="34957-106">Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Sachkonto-Einstellungen > Hauptbuchparameter**.</span><span class="sxs-lookup"><span data-stu-id="34957-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="34957-107">Erweitern Sie den Abschnitt **Geschäftsjahresschluss**.</span><span class="sxs-lookup"><span data-stu-id="34957-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="34957-108">Wählen Sie „Ja“ oder „Nein“ für die Option **Jahresabschlussbuchungen bei Umbuchung löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="34957-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="34957-109">Wenn das Geschäftsjahr bereits geschlossen wurde und der Jahresendabschluss erneut ausgeführt wird, ist diese Einstellung wichtig.</span><span class="sxs-lookup"><span data-stu-id="34957-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="34957-110">Wenn sie auf "Ja" festgelegt ist, wird der Beleg für den früheren Jahresabschluss gelöscht und ein neuer Beleg wird für alle Kontoenanfangssalden erstellt.</span><span class="sxs-lookup"><span data-stu-id="34957-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="34957-111">Wenn er auf "Nein" festgelegt ist, bleibt der vorherige Beleg bestehen und ein neuer Beleg wird nur für Regulierungseinträge erstellt, die nach dem letzten Jahresabschluss gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="34957-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="34957-112">Wählen Sie „Ja“ oder „Nein“ für die Option **Abschlussbuchungen bei Umbuchung erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="34957-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="34957-113">Bei "Ja" werden zwei Buchungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="34957-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="34957-114">Ein Beleg wird im abgeschlossenen Geschäftsjahr erstellt, um die Salden von GuV-Sachkonten auf Null zu setzen und ein zweiter Beleg wird im folgenden Geschäftsjahre für die Anfangssalden erstellt.</span><span class="sxs-lookup"><span data-stu-id="34957-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="34957-115">Bei "Nein" wird ein einzelner Belegt im folgenden Geschäftsjahre für die Anfangssalden erstellt.</span><span class="sxs-lookup"><span data-stu-id="34957-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="34957-116">Wählen Sie „Ja“ oder „Nein“ für die Option **Geschäftsjahresstatus auf dauerhaft abgeschlossen festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="34957-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="34957-117">Bei "Ja" wird der Geschäftsjahrsstatus auf "Dauerhaft geschlossen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="34957-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="34957-118">Da ein dauerhaft geschlossenes Jahr nicht erneut geöffnet werden kann, sollten Sie diese Option auf "Nein" festlegen.</span><span class="sxs-lookup"><span data-stu-id="34957-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="34957-119">Wählen Sie „Ja“ oder „Nein“ für die Option zur **manuellen Eingabe einer Belegnummer im Rahmen des Jahresabschlussprozesses** aus.</span><span class="sxs-lookup"><span data-stu-id="34957-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="34957-120">Bei "Ja" muss manuell eine Belegnummer im Rahmen des Jahresabschlussprozesses eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="34957-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="34957-121">Ein Nummernkreis wird nicht verwendet, um die Belegnummer zu generieren.</span><span class="sxs-lookup"><span data-stu-id="34957-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="34957-122">Es ist eine bewährte Verfahrensweise, dieses auf "Ja" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="34957-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="34957-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="34957-123">Close the page.</span></span>
8. <span data-ttu-id="34957-124">Wechseln Sie zu **Hauptbuch > Zeitraum geschlossen > Jahresabschluss**.</span><span class="sxs-lookup"><span data-stu-id="34957-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="34957-125">Klicken Sie auf **Neu**, um eine Jahresabschlussvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34957-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="34957-126">Eine Vorlage kann für eine Gruppe von juristischen Personen erstellt werden, für die der Jahresabschluss ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34957-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="34957-127">Diese Vorlage kann Jahr für Jahr wiederverwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34957-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="34957-128">Geben Sie im Feld **Gruppenname** einen Namen für die Jahresabschlussvorlage ein.</span><span class="sxs-lookup"><span data-stu-id="34957-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="34957-129">Wählen Sie im Feld **Steuerkalender** das Geschäftsjahr aus, für das die Vorlage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="34957-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="34957-130">Nur die juristischen Personen, die dasselbe Geschäftsjahr verwenden, können im in der Jahresabschlussvorlage gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="34957-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="34957-131">Dies liegt daran, dass der Jahresabschluss über die Auswahl eines Geschäftsjahrs statt eines Datums durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34957-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="34957-132">Klicken Sie im **Aktivitätsbereich** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="34957-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="34957-133">Klicken Sie im Abschnitt **Juristische Personen** auf **Hinzufügen**, um die juristischen Personen für diese Vorlage auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="34957-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="34957-134">Juristische Personen können hinzugefügt werden, indem entweder die juristischen Personen auswählen werden oder indem eine Organisationshierarchie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="34957-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="34957-135">Nur juristischen Personen mit einer Organisationshierarchie mit demselben Steuerkalender werden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="34957-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="34957-136">Wählen Sie die juristischen Personen oder die Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="34957-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="34957-137">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="34957-137">Click **OK**.</span></span>
16. <span data-ttu-id="34957-138">Wählen Sie „Ja“ oder „Nein“ unter **Bilanzdimensionen übertragen**.</span><span class="sxs-lookup"><span data-stu-id="34957-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="34957-139">Es ist eine bewährte Verfahrensweise, diese Option für Bilanzkonten auf „Ja“ festzulegen.</span><span class="sxs-lookup"><span data-stu-id="34957-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="34957-140">Dies erhält die Finanzdimensionen in gebuchte Posten bei wenn die Anfangssalden für die Bilanzkonten manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="34957-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="34957-141">Bei GuV-Konten können Sie auswählen, das die Finanzdimensionen erhalten bleiben (Alle schließen), wenn die Salden zu den nicht ausgeschütteten Gewinnen verschoben werden, oder Sie können alle Finanzdimensionen durch einen anderen Dimensionswert ersetzen (Einzeln abschließen).</span><span class="sxs-lookup"><span data-stu-id="34957-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="34957-142">Wenn Sie "Einzeln abschließen" auswählen, können Sie einen bestimmten Dimensionswert für jede Dimension definieren oder diesen frei lassen.</span><span class="sxs-lookup"><span data-stu-id="34957-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="34957-143">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="34957-143">Click **Save**.</span></span>
18. <span data-ttu-id="34957-144">Starten Sie den Jahresabschluss über **Geschäftsjahresabschluss ausführen** im **Aktivitätsbereich**.</span><span class="sxs-lookup"><span data-stu-id="34957-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="34957-145">Der Jahresabschluss wird für die ausgewählte Vorlage ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34957-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="34957-146">Wählen Sie alle oder einige juristischen Personen aus der Vorlage, für die der Jahresabschluss ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34957-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="34957-147">Beim ersten Ausführen des Jahresabschlusses führen die meisten Organisationen den Jahresabschluss für alle juristischen Personen innerhalb der Vorlage aus, um Startsalden zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="34957-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="34957-148">Werden danach Regulierungseinträge vorgenommen, können Sie den Jahresabschluss nur für die juristischen Personen ausführen, die Regulierungen haben.</span><span class="sxs-lookup"><span data-stu-id="34957-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="34957-149">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="34957-149">Click **OK**.</span></span>
21. <span data-ttu-id="34957-150">Wählen Sie das Geschäftsjahr aus, für die der Jahresabschluss ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34957-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="34957-151">Geben Sie im Feld **Beleg** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="34957-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="34957-152">Es ist eine bewährte Verfahrensweise, das Geschäftsjahr in die Belegnummer einzubeziehen, um den erstellten Jahresabschlussbeleg einfacher zu finden.</span><span class="sxs-lookup"><span data-stu-id="34957-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="34957-153">Die Standardwerte für den als Stapelverarbeitung auszuführenden Jahresabschluss.</span><span class="sxs-lookup"><span data-stu-id="34957-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="34957-154">Es ist eine bewährte Verfahrensweise für Prozesse mit langer Laufzeit, diese im Stapelverarbeitungsmodus auszuführen.</span><span class="sxs-lookup"><span data-stu-id="34957-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="34957-155">Dies ist in der Regel einer dieser Prozesse. Daher wird er standardmäßig im Stapelbearbeitungsmodus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34957-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="34957-156">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="34957-156">Click **OK**.</span></span>

