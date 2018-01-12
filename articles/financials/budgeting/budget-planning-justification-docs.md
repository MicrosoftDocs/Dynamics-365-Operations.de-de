---
title: "Budgetplanungs-Begründungsdokumente"
description: "Begründungsdokumente ermöglichen eine Erläuterung für diese Anfordern eines Budgets, um zu erläutern bereit, warum ein bestimmtes Budget erforderlich ist."
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 18bed103c40ed41427b97748b33362415ef9fea3
ms.contentlocale: de-de
ms.lasthandoff: 01/12/2018

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="8b73a-103">Budgetplanungs-Begründungsdokumente</span><span class="sxs-lookup"><span data-stu-id="8b73a-103">Budget planning justification documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8b73a-104">Begründungsdokumente ermöglichen eine Erläuterung für diese Anfordern eines Budgets, um zu erläutern bereit, warum ein bestimmtes Budget erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8b73a-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="8b73a-105">Eine Budgetplanvorlage wird vom Budget-Manager in Microsoft Word erstellt und zum aktuellen Budgetplanungsprozess hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b73a-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="8b73a-106">Budgeteigentümer können die Vorlage öffnen und dann die Daten automatisch in Word auf der Grundlage ihrer Budgetanforderung ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="8b73a-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="8b73a-107">Sie können zusätzliche Text oder Daten vor dem Speichern anfügen und Ihre personalisierten  Begründungsdokument im Budgetplan hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8b73a-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="8b73a-108">Einstellung von Microsoft Dynamics Add-In für Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="8b73a-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="8b73a-109">Ein neues Microsoft Word-Dokument öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b73a-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="8b73a-110">Klicken Sie auf **Einfügen** auf dem Menüband und dann auf **Shop**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="8b73a-111">Suchen Sie nach Microsoft Dynamics Office Add-in und klicken auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="8b73a-112">In Word im rechten Bereich, klicken  Sie auf **Serverinformationen hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="8b73a-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="8b73a-113">Geben Sie die URL des Server ein und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="8b73a-114">Definieren Sie die Begründungsvorlage in Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="8b73a-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="8b73a-115">Klicken Sie auf **Entwurf** -im Microsoft Dynamics Office Add-In, nachdem Sie sich angemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="8b73a-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="8b73a-116">Für Kopfdaten verwenden Sie die Schaltfläche **Felder hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="8b73a-117">Wählen Sie die Entitätsdatenquelle von BudgetPlanJustification aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="8b73a-118">**Hinweis:** Diese Entität ist für alle Begründungsdokumente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8b73a-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="8b73a-119">Andere Entitäten können verwendet werden, aber der Upload zurück an der Enterprise edition von Microsoft Dynamics 365 for Finance and Operations schlägt fehl, wenn diese Entität nicht einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="8b73a-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="8b73a-120">Fügen Sie BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter und DocumentNumber Bezeichnungen und Werte im Word-Dokument hinzu.</span><span class="sxs-lookup"><span data-stu-id="8b73a-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="8b73a-121">**Hinweis**: Sie können eigene benutzerdefinierten Beschriftungen verwenden, statt die Standardetiketts, sofern erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8b73a-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="8b73a-122">Klicken Sie **Fertig**, um den Kopfbereich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8b73a-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="8b73a-123">Für Positionsebenedetail von Budgetplanbeträgen, klicken Sie auf **Tabelle hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="8b73a-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="8b73a-124">Wählen Sie die Entitätsdatenquelle von BudgetPlanJustification aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="8b73a-125">Hinzufügen von Feldern für EffectiveDate, ScenarioName, AccountDisplayValue und AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="8b73a-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="8b73a-126">**Hinweis:** Wenn Kommentare verfügbar sind und innerhalb der einzelnen Budgetplanpositionen hinzugefügt werden, können diese in Tabelle hier hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8b73a-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="8b73a-127">Fügen Sie alle zusätzlichen Anweisungen hinzu, wie Endbenutzer bereitzustellen, und führen Sie eine erforderliche Formatierung oder das Formatieren des Dokuments aus.</span><span class="sxs-lookup"><span data-stu-id="8b73a-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="8b73a-128">Speichern Sie das Dokument lokal auf Ihrem Computer und schließen Sie die Datei, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="8b73a-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="8b73a-129">Richten Sie den Budgetplanungsprozess ein, den Sie mit der Begründungsvorlage verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8b73a-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="8b73a-130">In Finance and Operations gehen Sie zu **Planung** &gt; **Einstellungen** &gt; **Budgetplanung** &gt; **Begründungsdokumentvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="8b73a-131">Klicken Sie auf **Neu** und durchsuchen Sie Ihre neu erstellten Microsoft Word-Dokumente.</span><span class="sxs-lookup"><span data-stu-id="8b73a-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="8b73a-132">Vorlagenname und Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="8b73a-132">Enter a template display name and description.</span></span> <span data-ttu-id="8b73a-133">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-133">Click **OK**.</span></span>
4.  <span data-ttu-id="8b73a-134">Navigieren Sie zu **Budgetierung** &gt; **Einrichtung** &gt; **Budget** **Planung** &gt; **Butgetplanungsprozess**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="8b73a-135">Wählen Sie den Prozess aus, in dem die Begründungsvorlage verwendet werden soll, und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="8b73a-136">Wählen Sie im Feld **Begründungsdokumentvorlage** die geeignete Vorlage aus und speichern Sie diese.</span><span class="sxs-lookup"><span data-stu-id="8b73a-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="8b73a-137">Bearbeiten und speichern Sie personalisierte Begründungsdokumente</span><span class="sxs-lookup"><span data-stu-id="8b73a-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="8b73a-138">In Finance and Operations erstellen Sie einen neuen Budgetplan oder öffnen Sie einen vorhandenen Budgetplan.</span><span class="sxs-lookup"><span data-stu-id="8b73a-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="8b73a-139">Im Dropdownmenü **Begründung** wählen Sie **Neue Begründung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="8b73a-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="8b73a-140">Nachdem Sie die Details ausgefüllt haben, laden Sie das personalisierte Dokument aus dem Dropdownmenü **Begründung** hoch.</span><span class="sxs-lookup"><span data-stu-id="8b73a-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>





