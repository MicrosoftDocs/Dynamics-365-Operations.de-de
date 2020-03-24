---
title: Abzüge konfigurieren
description: Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5287161f352b386ae4e13067f40228d7c1bce62
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092728"
---
# <a name="configure-deductions"></a><span data-ttu-id="2f78e-103">Abzüge konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2f78e-103">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2f78e-104">Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist.</span><span class="sxs-lookup"><span data-stu-id="2f78e-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="2f78e-105">Abzüge haben ein Gültigkeitsdatum, sodass Sie einen historischen Datensatz der Abzugsinformationen führen können.</span><span class="sxs-lookup"><span data-stu-id="2f78e-105">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="2f78e-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abzüge**.</span><span class="sxs-lookup"><span data-stu-id="2f78e-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="2f78e-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="2f78e-107">Select **New**.</span></span>

3. <span data-ttu-id="2f78e-108">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="2f78e-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="2f78e-109">Feld</span><span class="sxs-lookup"><span data-stu-id="2f78e-109">Field</span></span> | <span data-ttu-id="2f78e-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f78e-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2f78e-111">Abzug</span><span class="sxs-lookup"><span data-stu-id="2f78e-111">Deduction</span></span> | <span data-ttu-id="2f78e-112">Eine eindeutige ID, mit der der Vorteilsabzug identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2f78e-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="2f78e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f78e-113">Description</span></span> | <span data-ttu-id="2f78e-114">Eine Beschreibung für den Abzug.</span><span class="sxs-lookup"><span data-stu-id="2f78e-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="2f78e-115">Gültig</span><span class="sxs-lookup"><span data-stu-id="2f78e-115">Effective</span></span> | <span data-ttu-id="2f78e-116">Das Startdatum.</span><span class="sxs-lookup"><span data-stu-id="2f78e-116">The start date.</span></span> <span data-ttu-id="2f78e-117">Das aktuelle Systemdatum ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="2f78e-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="2f78e-118">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="2f78e-118">Expiration</span></span> | <span data-ttu-id="2f78e-119">Das Enddatum.</span><span class="sxs-lookup"><span data-stu-id="2f78e-119">The end date.</span></span> <span data-ttu-id="2f78e-120">Der Standardwert lautet 31.12.2154 (stellvertretend für „endet nie“).</span><span class="sxs-lookup"><span data-stu-id="2f78e-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="2f78e-121">Überschrift</span><span class="sxs-lookup"><span data-stu-id="2f78e-121">Heading</span></span> | <span data-ttu-id="2f78e-122">Der Überschriftencode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2f78e-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="2f78e-123">Dies wird verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f78e-123">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="2f78e-124">Referenz für Lohnabzüge des Mitarbeiters</span><span class="sxs-lookup"><span data-stu-id="2f78e-124">Employee payroll deduction reference</span></span> | <span data-ttu-id="2f78e-125">Der Abzugscode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn Vergütungen für die Lohnabrechnung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2f78e-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="2f78e-126">Betragsüberschrift</span><span class="sxs-lookup"><span data-stu-id="2f78e-126">Amount heading</span></span> | <span data-ttu-id="2f78e-127">Der Überschriftencode aus dem Lohnsystem, den dieser Abzugsbetrag für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2f78e-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="2f78e-128">Dies wird normalerweise verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f78e-128">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="2f78e-129">Löschen möglich</span><span class="sxs-lookup"><span data-stu-id="2f78e-129">Can delete</span></span> | <span data-ttu-id="2f78e-130">Gibt an, ob ein exportierter Wert von Dynamics 365 for Finance and Operations dazu führen kann, dass der Wert im Lohnsystem gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="2f78e-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="2f78e-131">Gekoppelte Spalten</span><span class="sxs-lookup"><span data-stu-id="2f78e-131">Paired columns</span></span> | <span data-ttu-id="2f78e-132">Gibt an, ob Überschrift und Abzugsbetrag in gekoppelten benachbarten Spalten an das Lohnsystem exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2f78e-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="2f78e-133">Gültigkeitsdatum ändern</span><span class="sxs-lookup"><span data-stu-id="2f78e-133">Change effective date</span></span> | <span data-ttu-id="2f78e-134">Datum, zu dem die Änderung des Vorteilsabzugs gültig wird.</span><span class="sxs-lookup"><span data-stu-id="2f78e-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="2f78e-135">An diesem Datum ändert das System automatisch den Vergütungsabzug und aktualisiert alle Vorteilspläne, die mit diesem Abzug verbunden sind, solange Sie die Verarbeitung von aktualisierten Abzugsänderungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f78e-135">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="2f78e-136">Abzugsänderung abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="2f78e-136">Deduction change completed</span></span> | <span data-ttu-id="2f78e-137">Das Kontrollkästchen „Abzugsänderung abgeschlossen“ wird automatisch aktiviert, sobald die Änderungen des Vorteilsabzugs durch die Verarbeitung von aktualisierten Abzugsänderungen abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="2f78e-137">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="2f78e-138">Um Änderungen an der Vorteilssatzeinstellung zu verfolgen und beizubehalten, wählen Sie **Aktionen** und dann **Versionen verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="2f78e-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="2f78e-139">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2f78e-139">Select **Save**.</span></span> 
