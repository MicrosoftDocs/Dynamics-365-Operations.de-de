---
title: Abdeckungsoptionen erstellen
description: Abdeckungsoptionen in Microsoft Dynamics 365 Human Resources sind Deckungsgrade für die Wahl eines Teilnehmers in einem Leistungsplan oder -programm.
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
ms.openlocfilehash: 2e1d5fc80d93e41626da8eb5bdf8f389fb0bd531
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466181"
---
# <a name="create-coverage-options"></a><span data-ttu-id="9cd99-103">Abdeckungsoptionen erstellen</span><span class="sxs-lookup"><span data-stu-id="9cd99-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9cd99-104">Abdeckungsoptionen in Microsoft Dynamics 365 Human Resources sind Deckungsgrade für die Wahl eines Teilnehmers in einem Leistungsplan oder -programm.</span><span class="sxs-lookup"><span data-stu-id="9cd99-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="9cd99-105">Zu den Deckungsoptionen könnten beispielsweise gehören **Nur für Mitarbeiter** für einen medizinischen Plan oder **2x Gehalt** für eine Lebensversicherung.</span><span class="sxs-lookup"><span data-stu-id="9cd99-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="9cd99-106">Nach der Definition können Sie die Optionen für die Leistungsdeckung wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="9cd99-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="9cd99-107">Sie können eine Option einem oder mehreren Plänen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="9cd99-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="9cd99-108">Nachdem Sie die Abdeckungsoptionen definiert haben, hängen Sie die Abdeckungsoptionen an einen Vorteilsplantyp an.</span><span class="sxs-lookup"><span data-stu-id="9cd99-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="9cd99-109">Der Plantyp wird dann einem Vorteilsplan oder ‑programm zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9cd99-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="9cd99-110">Abdeckungsoptionen, die einem Plantyp zugeordnet sind, sind für alle Pläne verfügbar, die mit diesem Plantyp erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9cd99-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="9cd99-111">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abdeckungsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="9cd99-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="9cd99-112">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9cd99-112">Select **New**.</span></span>

3. <span data-ttu-id="9cd99-113">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="9cd99-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9cd99-114">Feld</span><span class="sxs-lookup"><span data-stu-id="9cd99-114">Field</span></span> | <span data-ttu-id="9cd99-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cd99-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9cd99-116">**Abdeckungsoption**</span><span class="sxs-lookup"><span data-stu-id="9cd99-116">**Coverage option**</span></span> | <span data-ttu-id="9cd99-117">Ein eindeutiger Name für die Abdeckungsoption.</span><span class="sxs-lookup"><span data-stu-id="9cd99-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="9cd99-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9cd99-118">**Description**</span></span> | <span data-ttu-id="9cd99-119">Eine Beschreibung der Abdeckungsoption.</span><span class="sxs-lookup"><span data-stu-id="9cd99-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="9cd99-120">**Abdeckungscode**</span><span class="sxs-lookup"><span data-stu-id="9cd99-120">**Coverage code**</span></span> | <span data-ttu-id="9cd99-121">Abdeckungscodes weisen Mindest‑ und Höchstbeträge für jede berechtigten abgedeckten Personentyp zu.</span><span class="sxs-lookup"><span data-stu-id="9cd99-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="9cd99-122">Ein Abdeckungscode gibt an, wer abgedeckt ist oder was die zulässige Abdeckungssumme für einen Plantyp ist.</span><span class="sxs-lookup"><span data-stu-id="9cd99-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="9cd99-123">Sie können die Abdeckungssumme als Dollarbetrag oder als Prozentsatz ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="9cd99-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="9cd99-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9cd99-124">For example:</span></span></br></br><span data-ttu-id="9cd99-125">- **MA+1** – Um qualifiziert zu sein, muss für den Mitarbeiter ein Unterhaltsberechtigter ausgewählt sein (wenn mehr als einer ausgewählt ist, sind sie nicht mehr qualifiziert).</span><span class="sxs-lookup"><span data-stu-id="9cd99-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="9cd99-126">- **MA+Familie** – Um qualifiziert zu sein, müssen für den Mitarbeiter mindestens zwei Unterhaltsberechtigte ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="9cd99-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="9cd99-127">**Maximale Anzahl**</span><span class="sxs-lookup"><span data-stu-id="9cd99-127">**Maximum number**</span></span> | <span data-ttu-id="9cd99-128">Die Höchstzahl der Unterhaltsberechtigten.</span><span class="sxs-lookup"><span data-stu-id="9cd99-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="9cd99-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="9cd99-129">**Status**</span></span> | <span data-ttu-id="9cd99-130">Der Status der Abdeckungsoption.</span><span class="sxs-lookup"><span data-stu-id="9cd99-130">The status of the coverage option.</span></span> <span data-ttu-id="9cd99-131">Wenn der Status der Abdeckungsoption auf „Inaktiv“ gesetzt ist, kann die Abdeckungsoption für die Plantypen nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="9cd99-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="9cd99-132">**Prozentsatz**</span><span class="sxs-lookup"><span data-stu-id="9cd99-132">**Percent**</span></span> | <span data-ttu-id="9cd99-133">Der Prozentbetrag.</span><span class="sxs-lookup"><span data-stu-id="9cd99-133">The percent amount.</span></span> <span data-ttu-id="9cd99-134">Dieses Feld ist nur aktiv, wenn im Feld „Abdeckungscode“ die Option „%% x Gehalt“ ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="9cd99-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="9cd99-135">**Divisor**</span><span class="sxs-lookup"><span data-stu-id="9cd99-135">**Divisor**</span></span> | <span data-ttu-id="9cd99-136">Der Divisor, der für die Berechnung verwendet werden soll, wenn Sie den Abdeckungscode „%% x Gehalt“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="9cd99-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="9cd99-137">**Mindestprozentsatz**</span><span class="sxs-lookup"><span data-stu-id="9cd99-137">**Percent minimum**</span></span> | <span data-ttu-id="9cd99-138">Der minimale Prozentsatz, wenn Sie den Abdeckungscode „Prozent“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="9cd99-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="9cd99-139">**Maximaler Prozentsatz**</span><span class="sxs-lookup"><span data-stu-id="9cd99-139">**Percent maximum**</span></span> | <span data-ttu-id="9cd99-140">Der maximale Prozentsatz, wenn Sie den Abdeckungscode „Prozent“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="9cd99-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="9cd99-141">Fügen Sie unter **Berechtigungsoptionen für persönliche Kontakte** jeder Abdeckungsoption die entsprechende Berechtigungsoption für persönliche Kontakte hinzu.</span><span class="sxs-lookup"><span data-stu-id="9cd99-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="9cd99-142">Geben Sie unter **Self-Service** Werte für die folgenden Felder ein:</span><span class="sxs-lookup"><span data-stu-id="9cd99-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="9cd99-143">Feld</span><span class="sxs-lookup"><span data-stu-id="9cd99-143">Field</span></span> | <span data-ttu-id="9cd99-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cd99-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9cd99-145">**Mitarbeiterbeitragsbetrag zulassen**</span><span class="sxs-lookup"><span data-stu-id="9cd99-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="9cd99-146">Gibt an, ob Mitarbeiter den Beitragsbetrag für den Vorteils-Self-Service ändern dürfen, wenn sie Vorteile auswählen.</span><span class="sxs-lookup"><span data-stu-id="9cd99-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="9cd99-147">Wenn Sie dieses Kontrollkästchen aktivieren, berechnet das System die Vorteilsplanparameter basierend auf dem Beitragsbetrag, den der Mitarbeiter beim Vorteils-Self-Service eingibt.</span><span class="sxs-lookup"><span data-stu-id="9cd99-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="9cd99-148">**Mitarbeiterdeckungsbetrag zulassen**</span><span class="sxs-lookup"><span data-stu-id="9cd99-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="9cd99-149">Gibt an, ob Mitarbeiter den Abdeckungsbetrag für den Vorteils-Self-Service ändern dürfen, wenn sie Vorteile auswählen.</span><span class="sxs-lookup"><span data-stu-id="9cd99-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="9cd99-150">Wenn Sie dieses Kontrollkästchen aktivieren, berechnet das System die Vorteilsplanparameter basierend auf dem Abdeckungsbetrag, den der Mitarbeiter beim Mitarbeiter-Self-Service eingibt.</span><span class="sxs-lookup"><span data-stu-id="9cd99-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="9cd99-151">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="9cd99-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]