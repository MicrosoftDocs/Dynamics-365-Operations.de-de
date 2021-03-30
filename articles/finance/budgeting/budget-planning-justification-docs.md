---
title: Budgetplanungs-Begründungsdokumente
description: Begründungsdokumente ermöglichen eine Erläuterung für diese Anfordern eines Budgets, um zu erläutern bereit, warum ein bestimmtes Budget erforderlich ist.
author: panolte
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8754c017a966cb1d11a72d6f8a80e1088aeb9100
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210312"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="09ae3-103">Budgetplanungs-Begründungsdokumente</span><span class="sxs-lookup"><span data-stu-id="09ae3-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09ae3-104">Begründungsdokumente ermöglichen eine Erläuterung für diese Anfordern eines Budgets, um zu erläutern bereit, warum ein bestimmtes Budget erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="09ae3-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="09ae3-105">Eine Budgetplanvorlage wird vom Budget-Manager in Microsoft Word erstellt und zum aktuellen Budgetplanungsprozess hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="09ae3-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="09ae3-106">Budgeteigentümer können die Vorlage öffnen und dann die Daten automatisch in Word auf der Grundlage ihrer Budgetanforderung ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="09ae3-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="09ae3-107">Sie können zusätzliche Text oder Daten vor dem Speichern anfügen und Ihre personalisierten  Begründungsdokument im Budgetplan hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="09ae3-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="09ae3-108">Microsoft Dynamics Office-Add-In für Microsoft Word einrichten</span><span class="sxs-lookup"><span data-stu-id="09ae3-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="09ae3-109">Öffnen Sie ein neues Microsoft Word-Dokument.</span><span class="sxs-lookup"><span data-stu-id="09ae3-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="09ae3-110">Klicken Sie auf **Einfügen** auf dem Menüband und dann auf **Shop**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="09ae3-111">Suchen Sie nach Microsoft Dynamics Office Add-in, und klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="09ae3-112">In Word im rechten Bereich, klicken  Sie auf **Serverinformationen hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="09ae3-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="09ae3-113">Geben Sie die URL des Server ein und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="09ae3-114">Definieren der Begründungsvorlage in Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="09ae3-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="09ae3-115">Klicken Sie auf **Entwurf** im Microsoft Dynamics Office-Add-In, nachdem Sie sich angemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="09ae3-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="09ae3-116">Für Kopfdaten verwenden Sie die Schaltfläche **Felder hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="09ae3-117">Wählen Sie die Entitätsdatenquelle von BudgetPlanJustification aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="09ae3-118">**Hinweis:** Diese Entität ist für alle Begründungsdokumente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09ae3-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="09ae3-119">Andere Entitäten können verwendet werden, aber der Upload zurück an Microsoft Dynamics 365 Finance schlägt fehl, wenn diese Entität nicht einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="09ae3-119">Other entities can be used but the upload back to Microsoft Dynamics 365 Finance will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="09ae3-120">Fügen Sie BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter und DocumentNumber Bezeichnungen und Werte im Word-Dokument hinzu.</span><span class="sxs-lookup"><span data-stu-id="09ae3-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="09ae3-121">**Hinweis**: Sie können eigene benutzerdefinierten Beschriftungen verwenden, statt die Standardetiketts, sofern erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09ae3-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="09ae3-122">Klicken Sie **Fertig**, um den Kopfbereich abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="09ae3-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="09ae3-123">Für Positionsebenedetail von Budgetplanbeträgen, klicken Sie auf **Tabelle hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="09ae3-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="09ae3-124">Wählen Sie die Entitätsdatenquelle von BudgetPlanJustification aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="09ae3-125">Hinzufügen von Feldern für EffectiveDate, ScenarioName, AccountDisplayValue und AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="09ae3-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="09ae3-126">**Hinweis:** Wenn Kommentare verfügbar sind und innerhalb der einzelnen Budgetplanpositionen hinzugefügt werden, können diese in Tabelle hier hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="09ae3-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="09ae3-127">Fügen Sie alle zusätzlichen Anweisungen hinzu, wie Endbenutzer bereitzustellen, und führen Sie eine erforderliche Formatierung oder das Formatieren des Dokuments aus.</span><span class="sxs-lookup"><span data-stu-id="09ae3-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="09ae3-128">Speichern Sie das Dokument lokal auf Ihrem Computer und schließen Sie die Datei, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="09ae3-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="09ae3-129">Richten Sie den Budgetplanungsprozess ein, den Sie mit der Begründungsvorlage verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="09ae3-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="09ae3-130">Gehen Sie zu **Planung** &gt; **Einstellungen** &gt; **Budgetplanung** &gt; **Begründungsdokumentvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-130">Go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="09ae3-131">Klicken Sie auf **Neu**, und navigieren Sie zu Ihrem neu erstellten Microsoft Word-Dokument.</span><span class="sxs-lookup"><span data-stu-id="09ae3-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="09ae3-132">Vorlagenname und Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="09ae3-132">Enter a template display name and description.</span></span> <span data-ttu-id="09ae3-133">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-133">Click **OK**.</span></span>
4.  <span data-ttu-id="09ae3-134">Navigieren Sie zu **Budgetierung** &gt; **Einrichtung** &gt; **Budget** **Planung** &gt; **Butgetplanungsprozess**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="09ae3-135">Wählen Sie den Prozess aus, in dem die Begründungsvorlage verwendet werden soll, und klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="09ae3-136">Wählen Sie im Feld **Begründungsdokumentvorlage** die geeignete Vorlage aus und speichern Sie diese.</span><span class="sxs-lookup"><span data-stu-id="09ae3-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="09ae3-137">Bearbeiten und speichern Sie personalisierte Begründungsdokumente</span><span class="sxs-lookup"><span data-stu-id="09ae3-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="09ae3-138">Erstellen Sie einen neuen Budgetplan oder öffnen Sie einen vorhandenen Budgetplan.</span><span class="sxs-lookup"><span data-stu-id="09ae3-138">Create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="09ae3-139">Im Dropdownmenü **Begründung** wählen Sie **Neue Begründung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="09ae3-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="09ae3-140">Nachdem Sie die Details ausgefüllt haben, laden Sie das personalisierte Dokument aus dem Dropdownmenü **Begründung** hoch.</span><span class="sxs-lookup"><span data-stu-id="09ae3-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]