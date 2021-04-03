---
title: Vorteilspläne für Arbeitskräfte erstellen
description: Sie können Vorteilspläne für Arbeitskräfte in Microsoft Dynamics 365 Human Resources erstellen, um Vorteilspläne für Mitarbeiter auszuwählen und die Auswahl der Vorteilspläne zu bestätigen.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ac357bbef4bf84b9eaf153834bc7a609240c45e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464225"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="1df6a-103">Vorteilspläne für Arbeitskräfte erstellen</span><span class="sxs-lookup"><span data-stu-id="1df6a-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1df6a-104">Sie können Vorteilspläne für Arbeitskräfte in Microsoft Dynamics 365 Human Resources erstellen, um Vorteilspläne für Mitarbeiter auszuwählen und die Auswahl der Vorteilspläne zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="1df6a-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="1df6a-105">In der Regel wählen Mitarbeiter Vorteilspläne selbst aus, indem sie Mitarbeiter-Self-Service verwenden. Anschließend bestätigt ein Vorteilsadministrator die Auswahl.</span><span class="sxs-lookup"><span data-stu-id="1df6a-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="1df6a-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Vorteilspläne für Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="1df6a-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="1df6a-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1df6a-107">Select **New**.</span></span>

3. <span data-ttu-id="1df6a-108">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="1df6a-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1df6a-109">Feld</span><span class="sxs-lookup"><span data-stu-id="1df6a-109">Field</span></span> | <span data-ttu-id="1df6a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1df6a-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1df6a-111">Periode</span><span class="sxs-lookup"><span data-stu-id="1df6a-111">Period</span></span> | <span data-ttu-id="1df6a-112">Gibt eine Vorteilsperiode an, die zum Filtern der Pläne im Inforegister „Pläne“ verwendet werden soll. Filtern Sie die Pläne, um eine Teilmenge aller Plandatensätze auszuwählen, damit Sie die Teilmenge bestätigen können.</span><span class="sxs-lookup"><span data-stu-id="1df6a-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="1df6a-113">Wählen Sie beispielsweise eine von Ihnen erstellte Periode mit dem Namen 2015 aus, um alle ausgewählten Vorteilsregistrierungsanmeldungen für 2015 zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="1df6a-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="1df6a-114">Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="1df6a-114">Worker</span></span> | <span data-ttu-id="1df6a-115">Gibt eine Arbeitskraft an, die zum Filtern der Pläne im Inforegister „Pläne“ verwendet werden soll. Filtern Sie die Pläne, um eine Teilmenge aller Plandatensätze auszuwählen, damit Sie die Teilmenge bestätigen können.</span><span class="sxs-lookup"><span data-stu-id="1df6a-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="1df6a-116">Juristische Person</span><span class="sxs-lookup"><span data-stu-id="1df6a-116">Legal entity</span></span> | <span data-ttu-id="1df6a-117">Gibt eine juristische Perso nan, die zum Filtern der Pläne im Inforegister „Pläne“ verwendet werden soll. Filtern Sie die Pläne, um eine Teilmenge aller Plandatensätze auszuwählen, damit Sie die Teilmenge bestätigen können.</span><span class="sxs-lookup"><span data-stu-id="1df6a-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="1df6a-118">Abdeckungsoption</span><span class="sxs-lookup"><span data-stu-id="1df6a-118">Coverage option</span></span> | <span data-ttu-id="1df6a-119">Gibt eine Abdeckungsoption an, die zum Filtern der Pläne im Inforegister „Pläne“ verwendet werden soll. Filtern Sie die Pläne, um eine Teilmenge aller Plandatensätze auszuwählen, damit Sie die Teilmenge bestätigen können.</span><span class="sxs-lookup"><span data-stu-id="1df6a-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="1df6a-120">Standard</span><span class="sxs-lookup"><span data-stu-id="1df6a-120">Default</span></span> | <span data-ttu-id="1df6a-121">Filtert die Vorteilspläne basierend darauf, ob es sich um einen Standardplan handelt.</span><span class="sxs-lookup"><span data-stu-id="1df6a-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="1df6a-122">Filtern Sie die Pläne, um eine Teilmenge aller Plandatensätze auszuwählen, damit Sie die Teilmenge bestätigen können.</span><span class="sxs-lookup"><span data-stu-id="1df6a-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="1df6a-123">Status</span><span class="sxs-lookup"><span data-stu-id="1df6a-123">Status</span></span> | <span data-ttu-id="1df6a-124">Filtert Vorteilspläne basierend auf ihrem Status.</span><span class="sxs-lookup"><span data-stu-id="1df6a-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="1df6a-125">Filtern Sie die Pläne, um eine Teilmenge aller Plandatensätze auszuwählen, damit Sie die Teilmenge bestätigen können.</span><span class="sxs-lookup"><span data-stu-id="1df6a-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="1df6a-126">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="1df6a-126">Confirmation</span></span> | <span data-ttu-id="1df6a-127">Gibt den Bestätigungsstatus an, der zum Filtern der Pläne im Inforegister „Pläne“ verwendet werden soll. Filtern Sie die Pläne, um eine Teilmenge aller Plandatensätze auszuwählen, damit Sie die Teilmenge bestätigen können.</span><span class="sxs-lookup"><span data-stu-id="1df6a-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="1df6a-128">Aufhebung</span><span class="sxs-lookup"><span data-stu-id="1df6a-128">Cancellation</span></span> | <span data-ttu-id="1df6a-129">Gibt den Stornierungsstatus an, der zum Filtern der Pläne im Inforegister „Pläne“ verwendet werden soll. Filtern Sie die Pläne, um eine Teilmenge aller Plandatensätze auszuwählen, damit Sie die Teilmenge bestätigen können.</span><span class="sxs-lookup"><span data-stu-id="1df6a-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="1df6a-130">Filter für Gültigkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="1df6a-130">Effective date filter</span></span> | <span data-ttu-id="1df6a-131">Filtert die Pläne danach, ob sie abgelaufen, aktiv oder in Zukunft aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="1df6a-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="1df6a-132">Aktivieren Sie die Kontrollkästchen der entsprechenden Pläne, die im Inforegister „Pläne“ angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1df6a-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="1df6a-133">Planwechsel</span><span class="sxs-lookup"><span data-stu-id="1df6a-133">Plans</span></span> | <span data-ttu-id="1df6a-134">Das Inforegister „Pläne“ enthält die Pläne, die den von Ihnen angegebenen Filterkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1df6a-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="1df6a-135">Die relevanten Konfigurationsoptionen, die von HR-Mitarbeitern festgelegt wurden, und die von Mitarbeitern ausgewählten Registrierungsanmeldungen sind in jeder Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="1df6a-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="1df6a-136">Das Feld „Qualifiziert“ gibt an, ob ein Validierungskonflikt mit der Planauswahl vorliegt.</span><span class="sxs-lookup"><span data-stu-id="1df6a-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="1df6a-137">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1df6a-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]