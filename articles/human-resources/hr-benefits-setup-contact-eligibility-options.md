---
title: Berechtigungsoptionen für persönliche Kontakte konfigurieren
description: Konfigurieren Sie Berechtigungsoptionen für persönliche Kontakte in Microsoft Dynamics 365 Human Resources. Persönliche Kontakte können Begünstigte oder Unterhaltsberechtigte sein.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 68364b0cc1c579a3ee9813474c9d3f6e4df1c05d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430761"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="53c9b-104">Berechtigungsoptionen für persönliche Kontakte konfigurieren</span><span class="sxs-lookup"><span data-stu-id="53c9b-104">Configure personal contact eligibility options</span></span>

<span data-ttu-id="53c9b-105">In diesem Artikel erfahren Sie, wie Sie Typen für persönliche Kontakte für die Verwendung von Vorteilen in Microsoft Dynamics 365 Human Resources konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="53c9b-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="53c9b-106">Persönliche Kontakte können Begünstigte oder Unterhaltsberechtigte sein.</span><span class="sxs-lookup"><span data-stu-id="53c9b-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="53c9b-107">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsoptionen für persönliche Kontakte**.</span><span class="sxs-lookup"><span data-stu-id="53c9b-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="53c9b-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="53c9b-108">Select **New**.</span></span>

3. <span data-ttu-id="53c9b-109">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="53c9b-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="53c9b-110">Feld</span><span class="sxs-lookup"><span data-stu-id="53c9b-110">Field</span></span> | <span data-ttu-id="53c9b-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53c9b-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="53c9b-112">**Berechtigungsoption**</span><span class="sxs-lookup"><span data-stu-id="53c9b-112">**Eligibility option**</span></span> | <span data-ttu-id="53c9b-113">Ein eindeutiger Name oder Code der Berechtigungsoption zur Identifizierung der Berechtigungsoption.</span><span class="sxs-lookup"><span data-stu-id="53c9b-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="53c9b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53c9b-114">**Description**</span></span> | <span data-ttu-id="53c9b-115">Eine kurze Beschreibung der Berechtigungsoption.</span><span class="sxs-lookup"><span data-stu-id="53c9b-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="53c9b-116">**Berechtigungscode für Kontakt**</span><span class="sxs-lookup"><span data-stu-id="53c9b-116">**Contact eligibility code**</span></span> | <span data-ttu-id="53c9b-117">Der Systemcode, der die persönliche Berechtigungsoption am besten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="53c9b-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="53c9b-118">Sie haben folgende Auswahlmöglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="53c9b-118">You can choose from:</span></span> <ul><li><span data-ttu-id="53c9b-119">Beziehung</span><span class="sxs-lookup"><span data-stu-id="53c9b-119">Relationship</span></span></li><li><span data-ttu-id="53c9b-120">Student</span><span class="sxs-lookup"><span data-stu-id="53c9b-120">Student</span></span></li><li><span data-ttu-id="53c9b-121">Überschüssige abhängige Person</span><span class="sxs-lookup"><span data-stu-id="53c9b-121">Overage dependent</span></span></li><li><span data-ttu-id="53c9b-122">Überaltertes, deaktiviertes abhängiges Objekt</span><span class="sxs-lookup"><span data-stu-id="53c9b-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="53c9b-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="53c9b-123">**Status**</span></span> | <span data-ttu-id="53c9b-124">Der Status der Berechtigungsoption.</span><span class="sxs-lookup"><span data-stu-id="53c9b-124">The status of the eligibility option.</span></span> <span data-ttu-id="53c9b-125">Wenn der Status für eine Berechtigungsoption auf inaktiv gesetzt ist, können Sie diese Berechtigungsoption für persönliche Kontakte nicht auswählen.</span><span class="sxs-lookup"><span data-stu-id="53c9b-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="53c9b-126">**Beziehung**</span><span class="sxs-lookup"><span data-stu-id="53c9b-126">**Relationship**</span></span> | <span data-ttu-id="53c9b-127">Gibt die Beziehung zwischen dem persönlichen Kontakt und dem Mitarbeiter an.</span><span class="sxs-lookup"><span data-stu-id="53c9b-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="53c9b-128">Dieses Feld ist nur aktiv, wenn der Kontaktberechtigungscode auf „Beziehung“ gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="53c9b-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="53c9b-129">**Alter**</span><span class="sxs-lookup"><span data-stu-id="53c9b-129">**Age**</span></span> | <span data-ttu-id="53c9b-130">Das maximale Alter eines berechtigten persönlichen Kontakts für den Vorteilsplan.</span><span class="sxs-lookup"><span data-stu-id="53c9b-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="53c9b-131">Dieses Feld ist nur aktiv, wenn Sie eine Beziehung auswählen.</span><span class="sxs-lookup"><span data-stu-id="53c9b-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="53c9b-132">Dieses Alter wird mit dem berechneten Alter des persönlichen Kontakts verglichen.</span><span class="sxs-lookup"><span data-stu-id="53c9b-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="53c9b-133">Das berechnete Alter ist: (Dispositionsdatum – Geburtsdatum des persönlichen Kontakts / 365).</span><span class="sxs-lookup"><span data-stu-id="53c9b-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="53c9b-134">Diese Zahl ist immer eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="53c9b-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="53c9b-135">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="53c9b-135">Select **Save**.</span></span> 
