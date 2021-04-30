---
title: Einen Urlaubsanforderungsworkflow erstellen
description: Erstellen Sie einen Workflow für Urlaubsanträge und Abwesenheitsanträge, um Urlaubsanträge in Dynamics 365 Human Resources konsistent zu verwalten.
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb726f37d25e782a90938b7794be6dea2c30a7d5
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890722"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="c847b-103">Einen Urlaubsanforderungsworkflow erstellen</span><span class="sxs-lookup"><span data-stu-id="c847b-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c847b-104">Sie können einen Workflow für Urlaubsanträge und Abwesenheitsanträge erstellen, um Urlaubsanträge in Dynamics 365 Human Resources konsistent zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c847b-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="c847b-105">Mit einem Workflow **Urlaub und Abwesenheit** können Sie:</span><span class="sxs-lookup"><span data-stu-id="c847b-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="c847b-106">Aufgaben definieren</span><span class="sxs-lookup"><span data-stu-id="c847b-106">Define tasks</span></span>
- <span data-ttu-id="c847b-107">Bestimmen, wer die Aufgaben ausführen muss</span><span class="sxs-lookup"><span data-stu-id="c847b-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="c847b-108">Geben Sie an, wer Anforderungen genehmigen oder ablehnen kann</span><span class="sxs-lookup"><span data-stu-id="c847b-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="c847b-109">Eine Urlaubs- und Abwesenheitsworkflowanfrage erstellen</span><span class="sxs-lookup"><span data-stu-id="c847b-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="c847b-110">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="c847b-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c847b-111">Unter **Einrichtung** wählen Sie **Personalverwaltungsparameter Workflows**.</span><span class="sxs-lookup"><span data-stu-id="c847b-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="c847b-112">Wählen Sie **Neu** und dann wählen Sie **Urlaubs- und Abwesenheitsantrag**.</span><span class="sxs-lookup"><span data-stu-id="c847b-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="c847b-113">Wenn die Nachricht **Diese Datei öffnen?** erscheint, wählen Sie **Öffnen** und melden sich mit Ihren Unternehmensdaten an.</span><span class="sxs-lookup"><span data-stu-id="c847b-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="c847b-114">Verwenden Sie den Workflow-Editor, um einen Workflow für Ihre Urlaubsanträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c847b-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="c847b-115">Weitere Informationen zum Arbeiten mit Workflows finden Sie unter [Erstellen Sie eine Workflow-Übersicht](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="c847b-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="c847b-116">Datenelemente des Urlaubs- und Abwesenheitsanforderungs-Workflows</span><span class="sxs-lookup"><span data-stu-id="c847b-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="c847b-117">Mit den folgenden Datenelementen können Sie in Workflows bedingte oder automatische Genehmigungen für Urlaubs- und Abwesenheitsanträge erstellen:</span><span class="sxs-lookup"><span data-stu-id="c847b-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="c847b-118">**Betrag**</span><span class="sxs-lookup"><span data-stu-id="c847b-118">**Amount**</span></span>
- <span data-ttu-id="c847b-119">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="c847b-119">**Comment**</span></span>
- <span data-ttu-id="c847b-120">**Firma**</span><span class="sxs-lookup"><span data-stu-id="c847b-120">**Company**</span></span>
- <span data-ttu-id="c847b-121">**Erstellt von**</span><span class="sxs-lookup"><span data-stu-id="c847b-121">**Created by**</span></span>
- <span data-ttu-id="c847b-122">**Erstellungsdatum und -uhrzeit**</span><span class="sxs-lookup"><span data-stu-id="c847b-122">**Created date and time**</span></span>
- <span data-ttu-id="c847b-123">**Enddatum**</span><span class="sxs-lookup"><span data-stu-id="c847b-123">**End date**</span></span>
- <span data-ttu-id="c847b-124">**Sonderurlaubstyp**</span><span class="sxs-lookup"><span data-stu-id="c847b-124">**Leave type**</span></span>
- <span data-ttu-id="c847b-125">**Geändert von**</span><span class="sxs-lookup"><span data-stu-id="c847b-125">**Modified by**</span></span>
- <span data-ttu-id="c847b-126">**Änderungsdatum und -uhrzeit**</span><span class="sxs-lookup"><span data-stu-id="c847b-126">**Modified date and time**</span></span>
- <span data-ttu-id="c847b-127">**Ursachencode**</span><span class="sxs-lookup"><span data-stu-id="c847b-127">**Reason code**</span></span>
- <span data-ttu-id="c847b-128">**Anforderungskennung**</span><span class="sxs-lookup"><span data-stu-id="c847b-128">**Request ID**</span></span>
- <span data-ttu-id="c847b-129">**Startdatum**</span><span class="sxs-lookup"><span data-stu-id="c847b-129">**Start date**</span></span>
- <span data-ttu-id="c847b-130">**Status**</span><span class="sxs-lookup"><span data-stu-id="c847b-130">**Status**</span></span> 
- <span data-ttu-id="c847b-131">**Übermittlungsdatum**</span><span class="sxs-lookup"><span data-stu-id="c847b-131">**Submission date**</span></span>
- <span data-ttu-id="c847b-132">**Übermittelt von**</span><span class="sxs-lookup"><span data-stu-id="c847b-132">**Submitted by**</span></span>
- <span data-ttu-id="c847b-133">**Übermittelt von der Personalverwaltung**</span><span class="sxs-lookup"><span data-stu-id="c847b-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="c847b-134">**Übermittelt vom Manager**</span><span class="sxs-lookup"><span data-stu-id="c847b-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="c847b-135">**Übermittelt im Auftrag von**</span><span class="sxs-lookup"><span data-stu-id="c847b-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="c847b-136">**Worker**</span><span class="sxs-lookup"><span data-stu-id="c847b-136">**Worker**</span></span>
- <span data-ttu-id="c847b-137">**Arbeitskrafttyp**</span><span class="sxs-lookup"><span data-stu-id="c847b-137">**Worker type**</span></span>

<span data-ttu-id="c847b-138">Diese Beispiele zeigen, wie Sie mithilfe dieser Datenelemente verschiedene Typen von Workflowbedingungen erstellen können:</span><span class="sxs-lookup"><span data-stu-id="c847b-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="c847b-139">Verwenden Sie den **Ursachencode** in einer bedingten Anweisung zur Weiterleitung von Krankmeldungn mit dem Ursachencode **Medizinische Behandlung** an die Personalverwaltung zur Genehmigung, während alle anderen Ursachencodes an den Manager weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c847b-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="c847b-140">Weitere Informationen zu bedingten Anweisungen finden Sie unter [Konfigurieren bedingter Entscheidungen in einem Workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c847b-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span></span> 

- <span data-ttu-id="c847b-141">Verwenden Sie **Übermittelt von der Personalverwaltung** und **Übermittelt vom Manager** in einer automatischen Aktivität zum automatischen Genehmigen von Abwesenheitsanträgen, die diese Rollen im Auftrag von Mitarbeitern übermitteln.</span><span class="sxs-lookup"><span data-stu-id="c847b-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="c847b-142">Weitere Informationen über automatische Aktivitäten finden Sie unter [Genehmigungsprozesse in einem Workflow konfigurieren](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c847b-142">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="c847b-143">Verwenden Sie **Urlaubstyp** in einer bedingten Anweisung oder einer automatischen Aktivität, um zu steuern, wie der Workflow Anforderungen mit bestimmten Abwesenheitstypen weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="c847b-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="c847b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c847b-144">See also</span></span>

- [<span data-ttu-id="c847b-145">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="c847b-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]