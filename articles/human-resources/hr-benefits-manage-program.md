---
title: Definieren und verwalten eines Vorteilprogramms
description: Die Personalverwaltung stellt eine Reihe von Tools bereit, die verwendet werden können, um Vorteile, Abzüge und die Vergütungspläne der Arbeitskräfte einzurichten und zu verwalten, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet. Dieser Artikel bietet Informationen dazu, wie Vorteile eingerichtet und verwaltet werden.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 646fc03dcacced6a9a6ae8bb373c5a2d915c243a
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465077"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="c74c7-104">Definieren und Verwalten eines Vergütungsprogramms</span><span class="sxs-lookup"><span data-stu-id="c74c7-104">Define and manage a benefits program</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c74c7-105">Die Personalverwaltung stellt eine Reihe von Tools bereit, die verwendet werden können, um Vorteile, Abzüge und die Vergütungspläne der Arbeitskräfte einzurichten und zu verwalten, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c74c7-105">Human Resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="c74c7-106">Dieser Artikel bietet Informationen dazu, wie Vorteile eingerichtet und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c74c7-106">This article provides information about how to set up and manage benefits.</span></span>

## <a name="benefit-setup"></a><span data-ttu-id="c74c7-107">Vorteile einrichten</span><span class="sxs-lookup"><span data-stu-id="c74c7-107">Benefit setup</span></span>

<span data-ttu-id="c74c7-108">Damit eine Arbeitskraft für Vorteile registriert werden kann, müssen Sie die Elemente jedes Vorteils erstellen.</span><span class="sxs-lookup"><span data-stu-id="c74c7-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="c74c7-109">Diese Elemente kombinieren ähnliche Vorteilspläne und definieren Standardeinstellungen, wie Rabattsätze und Buchhaltungsdetails.</span><span class="sxs-lookup"><span data-stu-id="c74c7-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="c74c7-110">Viele dieser Einstellungen können angepasst werden, wenn Arbeitskräfte später für den Vorteil registriert werden.</span><span class="sxs-lookup"><span data-stu-id="c74c7-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="c74c7-111">Für jeden Vorteilsplan kann eine Organisation mehrere Registrierungssoptionen anbieten, oder eine Arbeitskraft kann die Registrierung für den Plan erlassen.</span><span class="sxs-lookup"><span data-stu-id="c74c7-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="c74c7-112">[![Vorteilsprozessfluss](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="c74c7-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="c74c7-113">Vergütungselemente</span><span class="sxs-lookup"><span data-stu-id="c74c7-113">Benefit elements</span></span>

<span data-ttu-id="c74c7-114">Bevor Sie damit beginnen, Vorteile zu erstellen und Arbeitskräfte dafür zu registrieren, müssen Sie die Elemente definieren, die einen Vorteil ausmachen: den Typ, den Plan und die Optionen.</span><span class="sxs-lookup"><span data-stu-id="c74c7-114">Before you begin to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="c74c7-115">**Typ** – Eine Reihe von Plänen für einen speziellen Vorteil, wie z. B. "Gesundheitsleistungen" oder "freies Parken".</span><span class="sxs-lookup"><span data-stu-id="c74c7-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="c74c7-116">**Plan** – Eine bestimmter Vorteil, der von einem externen Anbieter bezogen wird.</span><span class="sxs-lookup"><span data-stu-id="c74c7-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="c74c7-117">**Option** – Die Dispositionsebenen, z. B. "nur Mitarbeiter" oder "Mitarbeiter und Ehepartner".</span><span class="sxs-lookup"><span data-stu-id="c74c7-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="c74c7-118">Für jeden Vorteilstyp, wie Augen- oder Zahnmedizin, kann eine Organisation den Arbeitskräften eine oder mehrere Pläne anbieten.</span><span class="sxs-lookup"><span data-stu-id="c74c7-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="c74c7-119">Für jeden Plan kann die Organisation unterschiedliche Optionen anbieten.</span><span class="sxs-lookup"><span data-stu-id="c74c7-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="c74c7-120">So können Arbeitskräfte z. B. Zusatzlebensversicherungsschutz zum einfachen, doppelten oder dreifachen jährlichen Gehalt kaufen.</span><span class="sxs-lookup"><span data-stu-id="c74c7-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="c74c7-121">Jede Kombination eines Plans und der Optionen wird zu einem Vorteil, für den die Arbeitskräfte sich registrieren können.</span><span class="sxs-lookup"><span data-stu-id="c74c7-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="c74c7-122">[![Vergütungsplan](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="c74c7-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="c74c7-123">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="c74c7-123">Eligibility</span></span>
<span data-ttu-id="c74c7-124">Viele Faktoren bestimmen die Eignung der Arbeitskraft für unterschiedliche Arten von Vorteil, die ein Arbeitgeber anbietet.</span><span class="sxs-lookup"><span data-stu-id="c74c7-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="c74c7-125">Wenn Sie einen Vorteil in Dynamics 365 Human Resources erstellen, können Sie den Typ der Berechtigung festlegen, der für diesen Vorteil gilt.</span><span class="sxs-lookup"><span data-stu-id="c74c7-125">When you create a benefit in Dynamics 365 Human Resources, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="c74c7-126">Sie können einen Vorteilskatalogs für alle Arbeitskräfte erstellen.</span><span class="sxs-lookup"><span data-stu-id="c74c7-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="c74c7-127">Beispiel sind Parkausweise, die einige Unternehmen allen Mitarbeitern als sonstiger Vorteil bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c74c7-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="c74c7-128">Wenn Sie diesen Vorteil erstellen, legen Sie die Berechtigung auf **Alle Arbeitskräfte sind berechtigt** fest.</span><span class="sxs-lookup"><span data-stu-id="c74c7-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="c74c7-129">Für andere Vorteile wie Schmuck und Steuerabgaben, Eignung gilt nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c74c7-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="c74c7-130">Wenn Sie diese Arten von Vergütung erstellen, setzen Sie die Berechtigung auf **Berechtigungsprozess umgehen**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="c74c7-131">Schließlich kann Vorteilseignung regelbasiert sein.</span><span class="sxs-lookup"><span data-stu-id="c74c7-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="c74c7-132">Beispielsweise ein Unternehmen bietet zwei Typen Lebensversicherungsvorteil Mitarbeitern anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c74c7-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="c74c7-133">Exekutivmitarbeiter sind für eine Lebenversicherung freigegeben, für alle anderen Vollzeitangestellten für die andere Lebenversicherung freigegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c74c7-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="c74c7-134">In Human Resources können Sie eine Vorteilsberechtigungsregel erstellen, um alle Exekutivmitarbeiter zu finden und eine Regel, um alle Vollzeitmitarbeiter zu finden. Sie können diese Regeln anschließend auf den entsprechenden Vorteil anwenden.</span><span class="sxs-lookup"><span data-stu-id="c74c7-134">In Human Resources, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="c74c7-135">Registrierung</span><span class="sxs-lookup"><span data-stu-id="c74c7-135">Enrollment</span></span>
<span data-ttu-id="c74c7-136">Nachdem Sie die Vorteile erstellt haben, die Ihre Organisation anbietet und die Berechtigung festgelegt haben, können Sie die Arbeitskräfte für Vorteile registrieren.</span><span class="sxs-lookup"><span data-stu-id="c74c7-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="c74c7-137">Sie können eine einzelne Arbeitskraft für Vorteile registrieren, oder Sie können in einen einzelnen Prozesses viele Arbeitskräfte für mindestens einen Vorteilen registrieren.</span><span class="sxs-lookup"><span data-stu-id="c74c7-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="c74c7-138">Manchmal beendet eine Organisation das Angebot eines bestimmten Vorteils.</span><span class="sxs-lookup"><span data-stu-id="c74c7-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="c74c7-139">In diesem Fall müssen Sie den Vorteil und die Arbeitskräfte aktualisieren, die registriert werden.</span><span class="sxs-lookup"><span data-stu-id="c74c7-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="c74c7-140">Massenvorteilsablauf ermöglicht es Ihnen, das Ablaufdatum eines Vorteils und der Registrierung für die Arbeitskräfte zu ändern, die gleichzeitig für diesen Vorteil registriert sind.</span><span class="sxs-lookup"><span data-stu-id="c74c7-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="c74c7-141">Sie können auch mehrere Arbeitskräfte auswählen, die für einen Vorteil registriert sind und das Enddatum der Disposition ändern.</span><span class="sxs-lookup"><span data-stu-id="c74c7-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="c74c7-142">Ebenso können Sie mit der Massenvorteilserweiterung das Ablaufdatum eines Vorteils und der Arbeitskraftregistrierungen für diesen Vorteil verlängern, wenn Sie beschließen, einen Vorteil länger anzubieten, als ursprünglich geplant.</span><span class="sxs-lookup"><span data-stu-id="c74c7-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]