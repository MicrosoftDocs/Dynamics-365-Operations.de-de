---
title: Abdeckungsoptionen erstellen
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009092"
---
# <a name="create-coverage-options"></a><span data-ttu-id="51563-102">Abdeckungsoptionen erstellen</span><span class="sxs-lookup"><span data-stu-id="51563-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="51563-103">Abdeckungsoptionen in Microsoft Dynamics 365 Human Resources sind die Abdeckungsgrade für die Wahl eines Teilnehmers in einem Vorteilsplan oder ‑programm, z. B. „Nur Mitarbeiter“ für einen Krankenversicherungsplan oder „2x Gehalt“ für einen Lebensversicherungsplan.</span><span class="sxs-lookup"><span data-stu-id="51563-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="51563-104">Nach der Definition sind die Optionen der Vorteilsabdeckung wiederverwendbar und Sie können eine Option mit einem oder mehreren Plänen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="51563-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="51563-105">Wenn die Abdeckungsoptionen definiert sind, hängen Sie die Abdeckungsoptionen an einen Vorteilsplantyp an.</span><span class="sxs-lookup"><span data-stu-id="51563-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="51563-106">Der Plantyp wird dann einem Vorteilsplan oder ‑programm zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="51563-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="51563-107">Abdeckungsoptionen, die einem Plantyp zugeordnet sind, stehen für alle Pläne zur Verfügung, die mit diesem Plantyp erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="51563-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="51563-108">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abdeckungsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="51563-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="51563-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="51563-109">Select **New**.</span></span>

3. <span data-ttu-id="51563-110">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="51563-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="51563-111">Feld</span><span class="sxs-lookup"><span data-stu-id="51563-111">Field</span></span> | <span data-ttu-id="51563-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51563-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="51563-113">**Abdeckungsoption**</span><span class="sxs-lookup"><span data-stu-id="51563-113">**Coverage option**</span></span> | <span data-ttu-id="51563-114">Ein eindeutiger Name für die Abdeckungsoption.</span><span class="sxs-lookup"><span data-stu-id="51563-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="51563-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51563-115">**Description**</span></span> | <span data-ttu-id="51563-116">Eine Beschreibung der Abdeckungsoption.</span><span class="sxs-lookup"><span data-stu-id="51563-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="51563-117">**Abdeckungscode**</span><span class="sxs-lookup"><span data-stu-id="51563-117">**Coverage code**</span></span> | <span data-ttu-id="51563-118">Abdeckungscodes weisen Mindest‑ und Höchstbeträge für jede berechtigten abgedeckten Personentyp zu.</span><span class="sxs-lookup"><span data-stu-id="51563-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="51563-119">Ein Abdeckungscode gibt an, wer abgedeckt ist oder was die zulässige Abdeckungssumme für einen Plantyp ist.</span><span class="sxs-lookup"><span data-stu-id="51563-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="51563-120">Sie können die Abdeckungssumme als Dollarbetrag oder als Prozentsatz ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="51563-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="51563-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="51563-121">For example:</span></span></br></br><span data-ttu-id="51563-122">- **MA+1** – Um qualifiziert zu sein, muss für den Mitarbeiter ein Unterhaltsberechtigter ausgewählt sein (wenn mehr als einer ausgewählt ist, sind sie nicht mehr qualifiziert).</span><span class="sxs-lookup"><span data-stu-id="51563-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="51563-123">- **MA+Familie** – Um qualifiziert zu sein, müssen für den Mitarbeiter mindestens zwei Unterhaltsberechtigte ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="51563-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="51563-124">**Maximale Anzahl**</span><span class="sxs-lookup"><span data-stu-id="51563-124">**Maximum number**</span></span> | <span data-ttu-id="51563-125">Die Höchstzahl der Unterhaltsberechtigten.</span><span class="sxs-lookup"><span data-stu-id="51563-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="51563-126">**Status**</span><span class="sxs-lookup"><span data-stu-id="51563-126">**Status**</span></span> | <span data-ttu-id="51563-127">Der Status der Abdeckungsoption.</span><span class="sxs-lookup"><span data-stu-id="51563-127">The status of the coverage option.</span></span> <span data-ttu-id="51563-128">Wenn der Status der Abdeckungsoption auf „Inaktiv“ gesetzt ist, kann die Abdeckungsoption für die Plantypen nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="51563-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="51563-129">**Prozentsatz**</span><span class="sxs-lookup"><span data-stu-id="51563-129">**Percent**</span></span> | <span data-ttu-id="51563-130">Der Prozentbetrag.</span><span class="sxs-lookup"><span data-stu-id="51563-130">The percent amount.</span></span> <span data-ttu-id="51563-131">Dieses Feld ist nur aktiv, wenn im Feld „Abdeckungscode“ die Option „%% x Gehalt“ ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="51563-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="51563-132">**Divisor**</span><span class="sxs-lookup"><span data-stu-id="51563-132">**Divisor**</span></span> | <span data-ttu-id="51563-133">Der Divisor, der für die Berechnung verwendet werden soll, wenn Sie den Abdeckungscode „%% x Gehalt“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="51563-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="51563-134">**Mindestprozentsatz**</span><span class="sxs-lookup"><span data-stu-id="51563-134">**Percent minimum**</span></span> | <span data-ttu-id="51563-135">Der minimale Prozentsatz, wenn Sie den Abdeckungscode „Prozent“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="51563-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="51563-136">**Maximaler Prozentsatz**</span><span class="sxs-lookup"><span data-stu-id="51563-136">**Percent maximum**</span></span> | <span data-ttu-id="51563-137">Der maximale Prozentsatz, wenn Sie den Abdeckungscode „Prozent“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="51563-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="51563-138">Fügen Sie unter **Berechtigungsoptionen für persönliche Kontakte** jeder Abdeckungsoption die entsprechende Berechtigungsoption für persönliche Kontakte hinzu.</span><span class="sxs-lookup"><span data-stu-id="51563-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="51563-139">Geben Sie unter **Self-Service** Werte für die folgenden Felder ein:</span><span class="sxs-lookup"><span data-stu-id="51563-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="51563-140">Feld</span><span class="sxs-lookup"><span data-stu-id="51563-140">Field</span></span> | <span data-ttu-id="51563-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51563-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="51563-142">**Mitarbeiterbeitragsbetrag zulassen**</span><span class="sxs-lookup"><span data-stu-id="51563-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="51563-143">Gibt an, ob Mitarbeiter den Beitragsbetrag für den Vorteils-Self-Service ändern dürfen, wenn sie Vorteile auswählen.</span><span class="sxs-lookup"><span data-stu-id="51563-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="51563-144">Wenn Sie dieses Kontrollkästchen aktivieren, berechnet das System die Vorteilsplanparameter basierend auf dem Beitragsbetrag, den der Mitarbeiter beim Vorteils-Self-Service eingibt.</span><span class="sxs-lookup"><span data-stu-id="51563-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="51563-145">**Mitarbeiterdeckungsbetrag zulassen**</span><span class="sxs-lookup"><span data-stu-id="51563-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="51563-146">Gibt an, ob Mitarbeiter den Abdeckungsbetrag für den Vorteils-Self-Service ändern dürfen, wenn sie Vorteile auswählen.</span><span class="sxs-lookup"><span data-stu-id="51563-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="51563-147">Wenn Sie dieses Kontrollkästchen aktivieren, berechnet das System die Vorteilsplanparameter basierend auf dem Abdeckungsbetrag, den der Mitarbeiter beim Mitarbeiter-Self-Service eingibt.</span><span class="sxs-lookup"><span data-stu-id="51563-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="51563-148">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="51563-148">Select **Save**.</span></span> 
