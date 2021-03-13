---
title: Abzüge konfigurieren
description: Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c84e44e784e18c82098d63909f198049ae5f995c
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112667"
---
# <a name="configure-deductions"></a><span data-ttu-id="9c759-103">Abzüge konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9c759-103">Configure deductions</span></span>

<span data-ttu-id="9c759-104">Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist.</span><span class="sxs-lookup"><span data-stu-id="9c759-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="9c759-105">Abzüge haben ein Gültigkeitsdatum, damit Sie einen historischen Datensatz der Abzugsinformationen führen können.</span><span class="sxs-lookup"><span data-stu-id="9c759-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="9c759-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abzüge**.</span><span class="sxs-lookup"><span data-stu-id="9c759-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="9c759-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9c759-107">Select **New**.</span></span>

3. <span data-ttu-id="9c759-108">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="9c759-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9c759-109">Feld</span><span class="sxs-lookup"><span data-stu-id="9c759-109">Field</span></span> | <span data-ttu-id="9c759-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c759-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9c759-111">**Abzug**</span><span class="sxs-lookup"><span data-stu-id="9c759-111">**Deduction**</span></span> | <span data-ttu-id="9c759-112">Eine eindeutige ID, mit der der Vorteilsabzug identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9c759-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="9c759-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c759-113">**Description**</span></span> | <span data-ttu-id="9c759-114">Eine Beschreibung für den Abzug.</span><span class="sxs-lookup"><span data-stu-id="9c759-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="9c759-115">**Gültig**</span><span class="sxs-lookup"><span data-stu-id="9c759-115">**Effective**</span></span> | <span data-ttu-id="9c759-116">Das Startdatum.</span><span class="sxs-lookup"><span data-stu-id="9c759-116">The start date.</span></span> <span data-ttu-id="9c759-117">Das aktuelle Systemdatum ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9c759-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="9c759-118">**Ablaufdatum**</span><span class="sxs-lookup"><span data-stu-id="9c759-118">**Expiration**</span></span> | <span data-ttu-id="9c759-119">Das Enddatum.</span><span class="sxs-lookup"><span data-stu-id="9c759-119">The end date.</span></span> <span data-ttu-id="9c759-120">Der Standardwert lautet 31.12.2154 (stellvertretend für „endet nie“).</span><span class="sxs-lookup"><span data-stu-id="9c759-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="9c759-121">**Überschrift**</span><span class="sxs-lookup"><span data-stu-id="9c759-121">**Heading**</span></span> | <span data-ttu-id="9c759-122">Der Überschriftencode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9c759-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="9c759-123">Diese wird verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c759-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="9c759-124">**Referenz für Lohnabzüge des Mitarbeiters**</span><span class="sxs-lookup"><span data-stu-id="9c759-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="9c759-125">Der Abzugscode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn Vergütungen für die Lohnabrechnung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9c759-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="9c759-126">**Betragsüberschrift**</span><span class="sxs-lookup"><span data-stu-id="9c759-126">**Amount heading**</span></span> | <span data-ttu-id="9c759-127">Der Überschriftencode aus dem Lohnsystem, den dieser Abzugsbetrag für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9c759-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="9c759-128">Diese wird normalerweise verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c759-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="9c759-129">**Löschen möglich**</span><span class="sxs-lookup"><span data-stu-id="9c759-129">**Can delete**</span></span> | <span data-ttu-id="9c759-130">Gibt an, ob ein exportierter Wert von Dynamics 365 for Finance and Operations dazu führen kann, dass der Wert im Lohnsystem gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="9c759-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="9c759-131">**Gekoppelte Spalten**</span><span class="sxs-lookup"><span data-stu-id="9c759-131">**Paired columns**</span></span> | <span data-ttu-id="9c759-132">Gibt an, ob Überschrift und Abzugsbetrag in gekoppelten benachbarten Spalten an das Lohnsystem exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c759-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="9c759-133">**Gültigkeitsdatum ändern**</span><span class="sxs-lookup"><span data-stu-id="9c759-133">**Change effective date**</span></span> | <span data-ttu-id="9c759-134">Datum, zu dem die Änderung des Vorteilsabzugs gültig wird.</span><span class="sxs-lookup"><span data-stu-id="9c759-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="9c759-135">An diesem Datum ändert das System automatisch den Vergütungsabzug und aktualisiert alle Vorteilspläne, die mit diesem Abzug verbunden sind, solange Sie die Verarbeitung von **Aktualisierten Abzugsänderungen** ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c759-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="9c759-136">**Abzugsänderung abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="9c759-136">**Deduction change completed**</span></span> | <span data-ttu-id="9c759-137">Das Kontrollkästchen **Abzugsänderung abgeschlossen** wird automatisch aktiviert, sobald die Änderungen des Vorteilsabzugs durch die Verarbeitung von aktualisierten Abzugsänderungen abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="9c759-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="9c759-138">Um Änderungen an der Vorteilssatzeinstellung zu verfolgen und beizubehalten, wählen Sie **Aktionen** und dann **Versionen verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="9c759-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="9c759-139">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="9c759-139">Select **Save**.</span></span> 
