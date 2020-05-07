---
title: Erweiterte Verträge für Abrechnung nach Arbeitsstatus erstellen
description: In diesem Thema wird erläutert, wie Sie Projektverträge erstellen, damit Sie Rechnungen für Debitoren basierend auf einem Prozentsatz der abgeschlossenen Arbeit erstellen können.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282827"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="9d8b2-103">Erweiterte Verträge für Abrechnung nach Arbeitsstatus erstellen</span><span class="sxs-lookup"><span data-stu-id="9d8b2-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d8b2-104">In diesem Thema wird erläutert, wie Sie Projektverträge erstellen, damit Sie für Debitoren Rechnungen basierend auf einem Prozentsatz der abgeschlossenen Arbeit erstellen können.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="9d8b2-105">Rechnungsbeträge für die Arbeitsbudgetkategorien, die Sie für das Projekt eingerichtet haben, werden automatisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="9d8b2-106">Der Zeitpunkt für die Rechnung wird bei der Vertragsverhandlung mit dem Debitor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="9d8b2-107">Richten Sie mithilfe der Prozeduren in diesem Thema einen Vertrag, ein zugehöriges Projekt und die Fakturierungsregeln ein, mit denen die Rechnungsbeträge für die eingerichteten Arbeitsbudgetkategorien des Projekts berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="9d8b2-108">Nachdem Sie den Vertrag und das Projekt erstellt haben, können Sie die Details des Projekts einrichten.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="9d8b2-109">Sie können beispielsweise Aktivitäten definieren und dem Projekt Arbeitskräfte zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="9d8b2-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9d8b2-110">Example</span></span>

<span data-ttu-id="9d8b2-111">Ihre Organisation ist eine Softwareentwicklungsfirma.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-111">Your organization is a software development firm.</span></span> <span data-ttu-id="9d8b2-112">Sie vereinbaren, für eine Gesamtgebühr von 20.000 Euro ein Lohnbuchhaltungspaket für einen Debitor zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="9d8b2-113">Ihre Organisation sagt zu, dem Debitor eine Rechnung auszustellen, sobald bestimmte Prozentsätze des Projekts abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="9d8b2-114">Sie richten die folgenden Projektkategorien für die Arbeit ein, damit Sie sie im Abrechnungsprozess verwenden können:</span><span class="sxs-lookup"><span data-stu-id="9d8b2-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="9d8b2-115">Beratung</span><span class="sxs-lookup"><span data-stu-id="9d8b2-115">Consulting</span></span>
- <span data-ttu-id="9d8b2-116">Entwurf</span><span class="sxs-lookup"><span data-stu-id="9d8b2-116">Design</span></span>
- <span data-ttu-id="9d8b2-117">Installation</span><span class="sxs-lookup"><span data-stu-id="9d8b2-117">Installation</span></span>

<span data-ttu-id="9d8b2-118">Sie richten außerdem Fakturierungsregeln ein, durch die die Rechnungsbeträge für den abgeschlossenen Prozentsatz der Arbeit in jeder Kategorie automatisch berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="9d8b2-119">Der Budget-Manager erstellt ein Budget für die Projektkategorien.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="9d8b2-120">Der Betrag der abgeschlossenen Arbeit wird automatisch als Prozentsatz der tatsächlichen Arbeit im Vergleich zu den budgetierten Beträgen berechnet.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9d8b2-121">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9d8b2-121">Prerequisites</span></span>

<span data-ttu-id="9d8b2-122">Bevor Sie ein Projekt erstellen, das Fakturierungsregeln verwendet, müssen Sie die Nummernkreise für Fakturierungsregeln sowie eine Gebührenerfassung einrichten, mit der Abrechnungen nach Arbeitsstatus gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="9d8b2-123">Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Einrichtung** \> **Projektverwaltungs- und Buchhaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="9d8b2-124">Richten Sie auf der Seite **Projektverwaltungs- und Buchhaltungsparameter** auf der Registerkarte **Nummernkreise** den Nummernkreis ein, den Sie beim Erstellen von Fakturierungsregeln verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="9d8b2-125">Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Erfassungen** \> **Gebühr**.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="9d8b2-126">Wählen Sie auf der Seite **Gebührenerfassung** die Option **Neu** aus und geben Sie den Erfassungsnamen ein.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="9d8b2-127">Erstellen eines Vertrags für die Abrechnung nach Arbeitsstatus</span><span class="sxs-lookup"><span data-stu-id="9d8b2-127">Create a contract for progress billings</span></span>

<span data-ttu-id="9d8b2-128">Gehen Sie folgendermaßen vor, um einen Projektvertrag für ein Festpreisprojekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="9d8b2-129">Sie erstellen eine Projektrechnung, wenn die Arbeit, die für das Projekt abgeschlossen ist, einen angegebenen Prozentsatz erreicht.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="9d8b2-130">Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Projekte** \> **Projektverträge**.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="9d8b2-131">Wählen Sie auf der Seite **Projektverträge** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="9d8b2-132">Legen Sie im Dialogfeld **Neuer Projektvertrag** die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="9d8b2-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="9d8b2-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="9d8b2-133">**Name**</span></span>
    - <span data-ttu-id="9d8b2-134">**Finanzierungstyp**</span><span class="sxs-lookup"><span data-stu-id="9d8b2-134">**Funding type**</span></span>
    - <span data-ttu-id="9d8b2-135">**Finanzierungsquelle**</span><span class="sxs-lookup"><span data-stu-id="9d8b2-135">**Funding source**</span></span>
    - <span data-ttu-id="9d8b2-136">**Verkaufswährung** – Standardmäßig wird diese Währung für Debitorenrechnungen verwendet, die dem Projektvertrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="9d8b2-137">Sie können die Verkaufswährung auf einer bestimmten Debitorenrechnung jedoch ändern.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="9d8b2-138">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-138">Select **OK**.</span></span> <span data-ttu-id="9d8b2-139">Die Informationen werden in den Kopf der Seite **Projektverträge** kopiert.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="9d8b2-140">Geben Sie auf der Seite **Projektverträge** den Rest der erforderlichen Informationen für das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="9d8b2-141">Erstellen eines Projekts für die Abrechnung nach Arbeitsstatus</span><span class="sxs-lookup"><span data-stu-id="9d8b2-141">Create a project for progress billings</span></span>

<span data-ttu-id="9d8b2-142">Gehen Sie folgendermaßen vor, um ein Projekt und alle Unterprojekte zu erstellen, die einem Projektvertrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="9d8b2-143">Wechseln Sie zu **Projektverwaltung und -verrechnung** \> **Projekte** \> **Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="9d8b2-144">Wählen Sie auf der Seite **Alle Projekte** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="9d8b2-145">Wählen Sie im Dialogfeld **Neues Projekt** im Feld **Projekttyp** die Option **Nach Aufwand** aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="9d8b2-146">Wählen Sie eine Projektgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-146">Select a project group.</span></span> <span data-ttu-id="9d8b2-147">Eine Projektgruppe definiert die Buchungsinformationen für die Projekte, die der Gruppe zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="9d8b2-148">Wählen Sie **Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-148">Select **Create project**.</span></span>
6. <span data-ttu-id="9d8b2-149">Legen Sie nach dem Erstellen des Projekts die Projektphase auf **In Bearbeitung** fest.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="9d8b2-150">Erstellen eines Budgets für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="9d8b2-150">Create a budget for a project</span></span>

<span data-ttu-id="9d8b2-151">Budgetkategorien werden verwendet, um die Rechnungsbeträge für den abgeschlossenen Prozentsatz der Arbeit für jede Kategorie automatisch zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="9d8b2-152">Gehen Sie folgendermaßen vor, um Budgetkategorien für die vorkalkulierten Kosten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="9d8b2-153">Wechseln Sie zu **Projektverwaltung und -verrechnung** \> **Projekte** \> **Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="9d8b2-154">Wählen Sie auf der Seite **Alle Projekte** das gewünschte Projekt aus und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="9d8b2-155">Wählen Sie auf der Seite**Projekte** im Aktionsbereich auf der Registerkarte **Plan** in der Gruppe **Budget** die Option **Projektbudget** aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="9d8b2-156">Geben Sie auf der Seite **Projektbudget** vorkalkulierte Kosten für jede Kategorie im Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="9d8b2-157">Erstellen der Fakturierungsregeln für die Abrechnung nach Arbeitsstatus</span><span class="sxs-lookup"><span data-stu-id="9d8b2-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="9d8b2-158">Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Projekte** \> **Projektverträge**.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="9d8b2-159">Wählen Sie auf der Seite **Projektverträge** einen Projektvertrag aus und öffnen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="9d8b2-160">Wählen Sie auf der Seite des Projektvertrags im Inforegister **Frakturierungsregeln** die Option **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="9d8b2-161">Wählen Sie auf der Seite **Fakturierungsregel** im Feld **Positionstyp** die Option **Status** aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="9d8b2-162">Geben Sie im Inforegister **Details der Fakturierungsregelpositionen** in das Feld **Vertragswert** den Gesamtwert des Vertrags ein.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="9d8b2-163">Wählen Sie im Feld **Kategorie** die Kategorie aus, in die die Gebührenbuchung gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="9d8b2-164">Wählen Sie im Feld **Projekt** das Projekt aus, für das diese Fakturierungsregel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="9d8b2-165">Optional: Weisen Sie die Fakturierungsregel zusätzlichen Projekten zu.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="9d8b2-166">Wählen Sie im Inforegister **Projekt** im Bereich **Verfügbare Projekte** ein Projekt aus und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach rechts, um das Projekt zum Abschnitt **Ausgewählte Projekte** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="9d8b2-167">Optional: Berechnen Sie den Prozentsatzbetrag, den der Debitor für die Zahlungen für eine Rechnung einbehält.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="9d8b2-168">Wählen Sie im Inforegister **Bedingungen für Einbehaltung der Zahlung** die Finanzierungsquelle aus. Wählen Sie anschließend im Feld **Prozentsatz der Einbehaltung** den Einbehaltungsprozentsatz aus.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="9d8b2-169">Wiederholen Sie diese Schritte, um weitere Fakturierungsregeln für den Projektvertrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d8b2-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
