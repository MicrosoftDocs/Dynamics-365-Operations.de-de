---
title: Einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen erstellen
description: Erstellen Sie einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen, um Urlaubsanforderungen in Dynamics 365 Human Resources konsistent zu kaufen und zu verkaufen.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d490e0c36ea0e854c5d7afc5b3bf75f6b65e542c
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712595"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="ce67f-103">Einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="ce67f-103">Create a buy and sell leave request workflow</span></span>

<span data-ttu-id="ce67f-104">Sie können in Dynamics 365 Human Resources einen Workflow erstellen, um Ihre Käufe und Verkäufe von Urlaubsanforderungen konsistent zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ce67f-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="ce67f-105">Ein Workflow zum **Kaufen und Verkaufen von Urlaub** ermöglicht Ihnen:</span><span class="sxs-lookup"><span data-stu-id="ce67f-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="ce67f-106">Aufgaben definieren</span><span class="sxs-lookup"><span data-stu-id="ce67f-106">Define tasks</span></span>
- <span data-ttu-id="ce67f-107">Bestimmen, wer die Aufgaben ausführen muss</span><span class="sxs-lookup"><span data-stu-id="ce67f-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="ce67f-108">Geben Sie an, wer Anforderungen genehmigen oder ablehnen kann</span><span class="sxs-lookup"><span data-stu-id="ce67f-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="ce67f-109">Einen Workflow zum Kaufen und Verkaufen von Urlaubsanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="ce67f-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="ce67f-110">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="ce67f-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ce67f-111">Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter Workflows**.</span><span class="sxs-lookup"><span data-stu-id="ce67f-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="ce67f-112">Wählen Sie **Neu** aus, und dann wählen Sie **Urlaubsanforderung kaufen und verkaufen** aus.</span><span class="sxs-lookup"><span data-stu-id="ce67f-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="ce67f-113">Wenn die Nachricht **Diese Datei öffnen?** erscheint, wählen Sie **Öffnen** und melden sich mit Ihren Unternehmensdaten an.</span><span class="sxs-lookup"><span data-stu-id="ce67f-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="ce67f-114">Verwenden Sie den Workflow-Editor, um einen Workflow für Ihre Urlaubsanträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce67f-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="ce67f-115">Weitere Informationen zum Arbeiten mit Workflows finden Sie unter [Erstellen Sie eine Workflow-Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="ce67f-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="ce67f-116">Datenelemente des Urlaubs- und Abwesenheitsanforderungs-Workflows</span><span class="sxs-lookup"><span data-stu-id="ce67f-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="ce67f-117">Mit den folgenden Datenelementen können Sie in Workflows bedingte oder automatische Genehmigungen zum Kauf und Verkauf von Urlaubsanforderungen erstellen:</span><span class="sxs-lookup"><span data-stu-id="ce67f-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="ce67f-118">**Betrag**</span><span class="sxs-lookup"><span data-stu-id="ce67f-118">**Amount**</span></span>
- <span data-ttu-id="ce67f-119">**Richtlinie zum Kauf und Verkauf von Urlaub**</span><span class="sxs-lookup"><span data-stu-id="ce67f-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="ce67f-120">**Firma**</span><span class="sxs-lookup"><span data-stu-id="ce67f-120">**Company**</span></span>
- <span data-ttu-id="ce67f-121">**Erstellt von**</span><span class="sxs-lookup"><span data-stu-id="ce67f-121">**Created by**</span></span>
- <span data-ttu-id="ce67f-122">**Datum und Uhrzeit der Erstellung**</span><span class="sxs-lookup"><span data-stu-id="ce67f-122">**Created date and time**</span></span>
- <span data-ttu-id="ce67f-123">**Enddatum**</span><span class="sxs-lookup"><span data-stu-id="ce67f-123">**End date**</span></span>
- <span data-ttu-id="ce67f-124">**Urlaubstyp**</span><span class="sxs-lookup"><span data-stu-id="ce67f-124">**Leave type**</span></span>
- <span data-ttu-id="ce67f-125">**Geändert von**</span><span class="sxs-lookup"><span data-stu-id="ce67f-125">**Modified by**</span></span>
- <span data-ttu-id="ce67f-126">**Änderungsdatum und -uhrzeit**</span><span class="sxs-lookup"><span data-stu-id="ce67f-126">**Modified date and time**</span></span>
- <span data-ttu-id="ce67f-127">**Anforderungskennung**</span><span class="sxs-lookup"><span data-stu-id="ce67f-127">**Request ID**</span></span>
- <span data-ttu-id="ce67f-128">**Startdatum**</span><span class="sxs-lookup"><span data-stu-id="ce67f-128">**Start date**</span></span>
- <span data-ttu-id="ce67f-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="ce67f-129">**Status**</span></span> 
- <span data-ttu-id="ce67f-130">**Übermittlungsdatum**</span><span class="sxs-lookup"><span data-stu-id="ce67f-130">**Submission date**</span></span>
- <span data-ttu-id="ce67f-131">**Übermittelt von**</span><span class="sxs-lookup"><span data-stu-id="ce67f-131">**Submitted by**</span></span>
- <span data-ttu-id="ce67f-132">**Übermittelt von der Personalverwaltung**</span><span class="sxs-lookup"><span data-stu-id="ce67f-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="ce67f-133">**Übermittelt vom Manager**</span><span class="sxs-lookup"><span data-stu-id="ce67f-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="ce67f-134">**Übermittelt im Auftrag von**</span><span class="sxs-lookup"><span data-stu-id="ce67f-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="ce67f-135">**Worker**</span><span class="sxs-lookup"><span data-stu-id="ce67f-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="ce67f-136">Workflowbeispiele</span><span class="sxs-lookup"><span data-stu-id="ce67f-136">Workflow examples</span></span>

<span data-ttu-id="ce67f-137">Diese Beispiele zeigen, wie Sie mithilfe dieser Datenelemente verschiedene Typen von Workflowbedingungen erstellen können:</span><span class="sxs-lookup"><span data-stu-id="ce67f-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="ce67f-138">Verwenden Sie **Übermittelt von der Personalverwaltung** und **Übermittelt vom Manager** in einer automatischen Aktivität zum automatischen Genehmigen des Kaufs und Verkaufs von Urlaubsanforderungen, die diese Rollen im Auftrag von Mitarbeitern übermitteln.</span><span class="sxs-lookup"><span data-stu-id="ce67f-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="ce67f-139">Weitere Informationen über automatische Aktivitäten finden Sie unter [Genehmigungsprozesse in einem Workflow konfigurieren](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="ce67f-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="ce67f-140">Verwenden Sie **Urlaubstyp** in einer bedingten Anweisung oder einer automatischen Aktivität, um zu steuern, wie der Workflow Anforderungen mit bestimmten Abwesenheitstypen weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="ce67f-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce67f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce67f-141">See also</span></span>

[<span data-ttu-id="ce67f-142">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="ce67f-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="ce67f-143">Kauf- und Verkaufsurlaubsrichtlinien verwalten</span><span class="sxs-lookup"><span data-stu-id="ce67f-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)

