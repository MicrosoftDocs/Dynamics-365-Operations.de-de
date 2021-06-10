---
title: Abzüge konfigurieren
description: Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fac1624ce3a88b9fb4adcf303860e82f9d9165b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055555"
---
# <a name="configure-deductions"></a><span data-ttu-id="bed44-103">Abzüge konfigurieren</span><span class="sxs-lookup"><span data-stu-id="bed44-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bed44-104">Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist.</span><span class="sxs-lookup"><span data-stu-id="bed44-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="bed44-105">Abzüge haben ein Gültigkeitsdatum, damit Sie einen historischen Datensatz der Abzugsinformationen führen können.</span><span class="sxs-lookup"><span data-stu-id="bed44-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="bed44-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abzüge**.</span><span class="sxs-lookup"><span data-stu-id="bed44-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="bed44-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="bed44-107">Select **New**.</span></span>

3. <span data-ttu-id="bed44-108">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="bed44-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bed44-109">Feld</span><span class="sxs-lookup"><span data-stu-id="bed44-109">Field</span></span> | <span data-ttu-id="bed44-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bed44-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bed44-111">**Abzug**</span><span class="sxs-lookup"><span data-stu-id="bed44-111">**Deduction**</span></span> | <span data-ttu-id="bed44-112">Eine eindeutige ID, mit der der Vorteilsabzug identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="bed44-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="bed44-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bed44-113">**Description**</span></span> | <span data-ttu-id="bed44-114">Eine Beschreibung für den Abzug.</span><span class="sxs-lookup"><span data-stu-id="bed44-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="bed44-115">**Gültig**</span><span class="sxs-lookup"><span data-stu-id="bed44-115">**Effective**</span></span> | <span data-ttu-id="bed44-116">Das Startdatum.</span><span class="sxs-lookup"><span data-stu-id="bed44-116">The start date.</span></span> <span data-ttu-id="bed44-117">Das aktuelle Systemdatum ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="bed44-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="bed44-118">**Ablaufdatum**</span><span class="sxs-lookup"><span data-stu-id="bed44-118">**Expiration**</span></span> | <span data-ttu-id="bed44-119">Das Enddatum.</span><span class="sxs-lookup"><span data-stu-id="bed44-119">The end date.</span></span> <span data-ttu-id="bed44-120">Der Standardwert lautet 31.12.2154 (stellvertretend für „endet nie“).</span><span class="sxs-lookup"><span data-stu-id="bed44-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="bed44-121">**Überschrift**</span><span class="sxs-lookup"><span data-stu-id="bed44-121">**Heading**</span></span> | <span data-ttu-id="bed44-122">Der Überschriftencode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="bed44-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="bed44-123">Diese wird verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="bed44-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="bed44-124">**Referenz für Lohnabzüge des Mitarbeiters**</span><span class="sxs-lookup"><span data-stu-id="bed44-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="bed44-125">Der Abzugscode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn Vergütungen für die Lohnabrechnung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="bed44-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="bed44-126">**Betragsüberschrift**</span><span class="sxs-lookup"><span data-stu-id="bed44-126">**Amount heading**</span></span> | <span data-ttu-id="bed44-127">Der Überschriftencode aus dem Lohnsystem, den dieser Abzugsbetrag für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="bed44-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="bed44-128">Diese wird normalerweise verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="bed44-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="bed44-129">**Löschen möglich**</span><span class="sxs-lookup"><span data-stu-id="bed44-129">**Can delete**</span></span> | <span data-ttu-id="bed44-130">Gibt an, ob ein exportierter Wert von Dynamics 365 for Finance and Operations dazu führen kann, dass der Wert im Lohnsystem gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="bed44-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="bed44-131">**Gekoppelte Spalten**</span><span class="sxs-lookup"><span data-stu-id="bed44-131">**Paired columns**</span></span> | <span data-ttu-id="bed44-132">Gibt an, ob Überschrift und Abzugsbetrag in gekoppelten benachbarten Spalten an das Lohnsystem exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bed44-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="bed44-133">**Gültigkeitsdatum ändern**</span><span class="sxs-lookup"><span data-stu-id="bed44-133">**Change effective date**</span></span> | <span data-ttu-id="bed44-134">Datum, zu dem die Änderung des Vorteilsabzugs gültig wird.</span><span class="sxs-lookup"><span data-stu-id="bed44-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="bed44-135">An diesem Datum ändert das System automatisch den Vergütungsabzug und aktualisiert alle Vorteilspläne, die mit diesem Abzug verbunden sind, solange Sie die Verarbeitung von **Aktualisierten Abzugsänderungen** ausführen.</span><span class="sxs-lookup"><span data-stu-id="bed44-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="bed44-136">**Abzugsänderung abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="bed44-136">**Deduction change completed**</span></span> | <span data-ttu-id="bed44-137">Das Kontrollkästchen **Abzugsänderung abgeschlossen** wird automatisch aktiviert, sobald die Änderungen des Vorteilsabzugs durch die Verarbeitung von aktualisierten Abzugsänderungen abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="bed44-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="bed44-138">Um Änderungen an der Vorteilssatzeinstellung zu verfolgen und beizubehalten, wählen Sie **Aktionen** und dann **Versionen verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="bed44-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="bed44-139">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bed44-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]