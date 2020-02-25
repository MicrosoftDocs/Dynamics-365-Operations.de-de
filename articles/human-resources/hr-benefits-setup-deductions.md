---
title: Abzüge konfigurieren
description: ''
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009168"
---
# <a name="configure-deductions"></a><span data-ttu-id="e15a4-102">Abzüge konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e15a4-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e15a4-103">Verwenden Sie Abzüge in Microsoft Dynamics 365 Human Resources, um zu bestimmen, wie viel ggf. für jeden Vorteil vom Lohnscheck eines Mitarbeiters abzuziehen ist.</span><span class="sxs-lookup"><span data-stu-id="e15a4-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="e15a4-104">Abzüge haben ein Gültigkeitsdatum, sodass Sie einen historischen Datensatz der Abzugsinformationen führen können.</span><span class="sxs-lookup"><span data-stu-id="e15a4-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="e15a4-105">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abzüge**.</span><span class="sxs-lookup"><span data-stu-id="e15a4-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="e15a4-106">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e15a4-106">Select **New**.</span></span>

3. <span data-ttu-id="e15a4-107">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="e15a4-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e15a4-108">Feld</span><span class="sxs-lookup"><span data-stu-id="e15a4-108">Field</span></span> | <span data-ttu-id="e15a4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e15a4-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e15a4-110">Abzug</span><span class="sxs-lookup"><span data-stu-id="e15a4-110">Deduction</span></span> | <span data-ttu-id="e15a4-111">Eine eindeutige ID, mit der der Vorteilsabzug identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e15a4-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="e15a4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e15a4-112">Description</span></span> | <span data-ttu-id="e15a4-113">Eine Beschreibung für den Abzug.</span><span class="sxs-lookup"><span data-stu-id="e15a4-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="e15a4-114">Gültig</span><span class="sxs-lookup"><span data-stu-id="e15a4-114">Effective</span></span> | <span data-ttu-id="e15a4-115">Das Startdatum.</span><span class="sxs-lookup"><span data-stu-id="e15a4-115">The start date.</span></span> <span data-ttu-id="e15a4-116">Das aktuelle Systemdatum ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="e15a4-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="e15a4-117">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="e15a4-117">Expiration</span></span> | <span data-ttu-id="e15a4-118">Das Enddatum.</span><span class="sxs-lookup"><span data-stu-id="e15a4-118">The end date.</span></span> <span data-ttu-id="e15a4-119">Der Standardwert lautet 31.12.2154 (stellvertretend für „endet nie“).</span><span class="sxs-lookup"><span data-stu-id="e15a4-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="e15a4-120">Überschrift</span><span class="sxs-lookup"><span data-stu-id="e15a4-120">Heading</span></span> | <span data-ttu-id="e15a4-121">Der Überschriftencode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e15a4-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="e15a4-122">Dies wird verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e15a4-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="e15a4-123">Referenz für Lohnabzüge des Mitarbeiters</span><span class="sxs-lookup"><span data-stu-id="e15a4-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="e15a4-124">Der Abzugscode aus dem Lohnsystem, den dieser Abzug für den Mitarbeiteranteil des Abzugs verwendet, wenn Vergütungen für die Lohnabrechnung verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e15a4-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="e15a4-125">Betragsüberschrift</span><span class="sxs-lookup"><span data-stu-id="e15a4-125">Amount heading</span></span> | <span data-ttu-id="e15a4-126">Der Überschriftencode aus dem Lohnsystem, den dieser Abzugsbetrag für den Mitarbeiteranteil des Abzugs verwendet, wenn die Vorteile für den Lohn verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e15a4-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="e15a4-127">Dies wird normalerweise verwendet, wenn Sie einen Drittanbieter für die Lohnabrechnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e15a4-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="e15a4-128">Löschen möglich</span><span class="sxs-lookup"><span data-stu-id="e15a4-128">Can delete</span></span> | <span data-ttu-id="e15a4-129">Gibt an, ob ein exportierter Wert von Dynamics 365 for Finance and Operations dazu führen kann, dass der Wert im Lohnsystem gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="e15a4-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="e15a4-130">Gekoppelte Spalten</span><span class="sxs-lookup"><span data-stu-id="e15a4-130">Paired columns</span></span> | <span data-ttu-id="e15a4-131">Gibt an, ob Überschrift und Abzugsbetrag in gekoppelten benachbarten Spalten an das Lohnsystem exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e15a4-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="e15a4-132">Gültigkeitsdatum ändern</span><span class="sxs-lookup"><span data-stu-id="e15a4-132">Change effective date</span></span> | <span data-ttu-id="e15a4-133">Datum, zu dem die Änderung des Vorteilsabzugs gültig wird.</span><span class="sxs-lookup"><span data-stu-id="e15a4-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="e15a4-134">An diesem Datum ändert das System automatisch den Vergütungsabzug und aktualisiert alle Vorteilspläne, die mit diesem Abzug verbunden sind, solange Sie die Verarbeitung von aktualisierten Abzugsänderungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="e15a4-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="e15a4-135">Abzugsänderung abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="e15a4-135">Deduction change completed</span></span> | <span data-ttu-id="e15a4-136">Das Kontrollkästchen „Abzugsänderung abgeschlossen“ wird automatisch aktiviert, sobald die Änderungen des Vorteilsabzugs durch die Verarbeitung von aktualisierten Abzugsänderungen abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="e15a4-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="e15a4-137">Um Änderungen an der Vorteilssatzeinstellung zu verfolgen und beizubehalten, wählen Sie **Aktionen** und dann **Versionen verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="e15a4-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="e15a4-138">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e15a4-138">Select **Save**.</span></span> 
