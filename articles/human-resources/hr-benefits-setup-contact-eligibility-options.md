---
title: Berechtigungsoptionen für persönliche Kontakte konfigurieren
description: Konfigurieren Sie Berechtigungsoptionen für persönliche Kontakte in Microsoft Dynamics 365 Human Resources. Persönliche Kontakte können Begünstigte oder Unterhaltsberechtigte sein.
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
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009169"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="fd430-104">Berechtigungsoptionen für persönliche Kontakte konfigurieren</span><span class="sxs-lookup"><span data-stu-id="fd430-104">Configure personal contact eligibility options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="fd430-105">In diesem Artikel erfahren Sie, wie Sie Typen für persönliche Kontakte für die Verwendung von Vorteilen in Microsoft Dynamics 365 Human Resources konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fd430-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="fd430-106">Persönliche Kontakte können Begünstigte oder Unterhaltsberechtigte sein.</span><span class="sxs-lookup"><span data-stu-id="fd430-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="fd430-107">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsoptionen für persönliche Kontakte**.</span><span class="sxs-lookup"><span data-stu-id="fd430-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="fd430-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fd430-108">Select **New**.</span></span>

3. <span data-ttu-id="fd430-109">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="fd430-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="fd430-110">Feld</span><span class="sxs-lookup"><span data-stu-id="fd430-110">Field</span></span> | <span data-ttu-id="fd430-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd430-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="fd430-112">**Berechtigungsoption**</span><span class="sxs-lookup"><span data-stu-id="fd430-112">**Eligibility option**</span></span> | <span data-ttu-id="fd430-113">Ein eindeutiger Name oder Code der Berechtigungsoption zur Identifizierung der Berechtigungsoption.</span><span class="sxs-lookup"><span data-stu-id="fd430-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="fd430-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd430-114">**Description**</span></span> | <span data-ttu-id="fd430-115">Eine kurze Beschreibung der Berechtigungsoption.</span><span class="sxs-lookup"><span data-stu-id="fd430-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="fd430-116">**Berechtigungscode für Kontakt**</span><span class="sxs-lookup"><span data-stu-id="fd430-116">**Contact eligibility code**</span></span> | <span data-ttu-id="fd430-117">Der Systemcode, der die persönliche Berechtigungsoption am besten beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fd430-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="fd430-118">Sie haben folgende Auswahlmöglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="fd430-118">You can choose from:</span></span> <ul><li><span data-ttu-id="fd430-119">Beziehung</span><span class="sxs-lookup"><span data-stu-id="fd430-119">Relationship</span></span></li><li><span data-ttu-id="fd430-120">Student</span><span class="sxs-lookup"><span data-stu-id="fd430-120">Student</span></span></li><li><span data-ttu-id="fd430-121">Überschüssige abhängige Person</span><span class="sxs-lookup"><span data-stu-id="fd430-121">Overage dependent</span></span></li><li><span data-ttu-id="fd430-122">Überaltertes, deaktiviertes abhängiges Objekt</span><span class="sxs-lookup"><span data-stu-id="fd430-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="fd430-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="fd430-123">**Status**</span></span> | <span data-ttu-id="fd430-124">Der Status der Berechtigungsoption.</span><span class="sxs-lookup"><span data-stu-id="fd430-124">The status of the eligibility option.</span></span> <span data-ttu-id="fd430-125">Wenn der Status für eine Berechtigungsoption auf inaktiv gesetzt ist, können Sie diese Berechtigungsoption für persönliche Kontakte nicht auswählen.</span><span class="sxs-lookup"><span data-stu-id="fd430-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="fd430-126">**Beziehung**</span><span class="sxs-lookup"><span data-stu-id="fd430-126">**Relationship**</span></span> | <span data-ttu-id="fd430-127">Gibt die Beziehung zwischen dem persönlichen Kontakt und dem Mitarbeiter an.</span><span class="sxs-lookup"><span data-stu-id="fd430-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="fd430-128">Dieses Feld ist nur aktiv, wenn der Kontaktberechtigungscode auf „Beziehung“ gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="fd430-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="fd430-129">**Alter**</span><span class="sxs-lookup"><span data-stu-id="fd430-129">**Age**</span></span> | <span data-ttu-id="fd430-130">Das maximale Alter eines berechtigten persönlichen Kontakts für den Vorteilsplan.</span><span class="sxs-lookup"><span data-stu-id="fd430-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="fd430-131">Dieses Feld ist nur aktiv, wenn Sie eine Beziehung auswählen.</span><span class="sxs-lookup"><span data-stu-id="fd430-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="fd430-132">Dieses Alter wird mit dem berechneten Alter des persönlichen Kontakts verglichen.</span><span class="sxs-lookup"><span data-stu-id="fd430-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="fd430-133">Das berechnete Alter ist: (Dispositionsdatum – Geburtsdatum des persönlichen Kontakts / 365).</span><span class="sxs-lookup"><span data-stu-id="fd430-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="fd430-134">Diese Zahl ist immer eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="fd430-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="fd430-135">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fd430-135">Select **Save**.</span></span> 
