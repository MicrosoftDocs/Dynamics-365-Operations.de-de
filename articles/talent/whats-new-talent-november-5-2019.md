---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (5. November 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48de07178acfaccf11e0a02b2848bf24e6ccc117
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896772"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a><span data-ttu-id="226e1-103">Neuerungen oder Änderungen in Dynamics 365 Talent (5. November 2019)</span><span class="sxs-lookup"><span data-stu-id="226e1-103">What's new or changed in Dynamics 365 Talent (November 5, 2019)</span></span>

<span data-ttu-id="226e1-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="226e1-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="226e1-105">Änderungen in Attract</span><span class="sxs-lookup"><span data-stu-id="226e1-105">Changes in Attract</span></span>

<span data-ttu-id="226e1-106">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="226e1-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="226e1-107">Änderungen in Onboard</span><span class="sxs-lookup"><span data-stu-id="226e1-107">Changes in Onboard</span></span>

<span data-ttu-id="226e1-108">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="226e1-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="226e1-109">Core HR-Änderungen</span><span class="sxs-lookup"><span data-stu-id="226e1-109">Changes in Core HR</span></span>

<span data-ttu-id="226e1-110">Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2598.</span><span class="sxs-lookup"><span data-stu-id="226e1-110">Changes described in this section apply to build number 8.1.2598.</span></span> <span data-ttu-id="226e1-111">Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="226e1-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="copy-a-core-hr-instance"></a><span data-ttu-id="226e1-112">Kopieren einer Core HR-Instanz</span><span class="sxs-lookup"><span data-stu-id="226e1-112">Copy a Core HR instance</span></span>

<span data-ttu-id="226e1-113">In der aktuellen Version können Sie mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Talent: Core HR-Datenbank in eine Sandbox-Umgebung kopieren.</span><span class="sxs-lookup"><span data-stu-id="226e1-113">In this week's release, you can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Talent: Core HR database to a sandbox environment.</span></span> <span data-ttu-id="226e1-114">Wenn Sie eine andere Sandbox-Umgebung haben, können Sie die Datenbank auch aus dieser Umgebung in eine bestimmte Sandbox-Umgebung kopieren.</span><span class="sxs-lookup"><span data-stu-id="226e1-114">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span> <span data-ttu-id="226e1-115">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="226e1-115">For more information, see:</span></span>

- <span data-ttu-id="226e1-116">[Breiteres Umgebungsmanagement](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) im Dynamics 365: 2019 Release Wave 2 Plan</span><span class="sxs-lookup"><span data-stu-id="226e1-116">[Broader environment management](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) in the Dynamics 365: 2019 release wave 2 plan</span></span>

- <span data-ttu-id="226e1-117">[Kopieren einer Core HR-Instanz](hr-copy-instance.md) in der Talentdokumentation</span><span class="sxs-lookup"><span data-stu-id="226e1-117">[Copy a Core HR instance](hr-copy-instance.md) in Talent documentation</span></span>

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a><span data-ttu-id="226e1-118">Common Data Service Integration Batchjobs werden nicht erstellt, wenn die Common Data Service Integration aktiviert ist (388030).</span><span class="sxs-lookup"><span data-stu-id="226e1-118">Common Data Service integration batch jobs aren't created when Common Data Service integration is enabled (388030)</span></span>

<span data-ttu-id="226e1-119">Diese Änderung erstellt Batch-Jobs für die Common Data Service-Integration, wenn sie aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="226e1-119">This change will create batch jobs for Common Data Service integration when it's enabled.</span></span>

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a><span data-ttu-id="226e1-120">Die HcmPersonImageEntity ändert die Größe des Personenbildes beim Hochladen nicht (369469).</span><span class="sxs-lookup"><span data-stu-id="226e1-120">The HcmPersonImageEntity doesn't resize the person image when uploaded (369469)</span></span>

<span data-ttu-id="226e1-121">Die Veröffentlichung dieser Woche ändert die Größe der Bilder, um die Leistung beim Import über die Datenverwaltung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="226e1-121">This week's release changes how images are resized for better performance when imported through data management.</span></span>

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a><span data-ttu-id="226e1-122">Das Datum der Verfügbarkeit für die Zuordnung einer Position kann vor dem Aktivierungsdatum (340103) liegen.</span><span class="sxs-lookup"><span data-stu-id="226e1-122">A position's Available for assignment date can be earlier than the Activation date (340103)</span></span>

<span data-ttu-id="226e1-123">Bei dieser Änderung erscheint eine Warnung, wenn Sie ein **Verfügbar für Zuordnungsdatum** auswählen, das vor dem **Aktivierungsdatum** der Position liegt.</span><span class="sxs-lookup"><span data-stu-id="226e1-123">With this change, a warning will appear if you select an **Available for assignment date** that's earlier than the position's **Activation date**.</span></span>

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a><span data-ttu-id="226e1-124">Es kann kein Vergütungsänderungsantrag im Employee Self-Service für schrittbasierte Pläne erstellt werden (376872).</span><span class="sxs-lookup"><span data-stu-id="226e1-124">Can't create a compensation change request in employee self-service for step-based plans (376872)</span></span>

<span data-ttu-id="226e1-125">Diese Freigabe behebt ein Problem bei der Beantragung von Vergütungsänderungen durch die Mitarbeiter-Self-Service für stufenbasierte Pläne.</span><span class="sxs-lookup"><span data-stu-id="226e1-125">This release corrects an issue when requesting compensation changes through employee self-service for step-based plans.</span></span> 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a><span data-ttu-id="226e1-126">Der Begründungscode wird nicht mit Common Data Service synchronisiert, wenn die Beschreibung länger als 30 Zeichen ist, Core HR erlaubt 60 (352682).</span><span class="sxs-lookup"><span data-stu-id="226e1-126">Reason code doesn't sync to Common Data Service if the description is longer than 30 characters, Core HR allows 60 (352682)</span></span>

<span data-ttu-id="226e1-127">mit dieser Änderung werden Differenzcodes mit mehr als 30 Zeichen in Common Data Service aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="226e1-127">with this change, reason codes with more than 30 characters will be updated in Common Data Service.</span></span> <span data-ttu-id="226e1-128">Änderungen in Common Data Service werden auch in Talent berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="226e1-128">Changes made in Common Data Service will also be reflected back in Talent.</span></span>

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a><span data-ttu-id="226e1-129">Adressintegration von Talent zu Finance and Operations (351961)</span><span class="sxs-lookup"><span data-stu-id="226e1-129">Address integration from Talent to Finance and Operations (351961)</span></span>

<span data-ttu-id="226e1-130">Diese Version behebt ein Problem, bei dem in Talent aktualisierte Adressen nicht in Finance and Operations aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="226e1-130">This release fixes an issue where addresses updated in Talent weren't updating in Finance and Operations.</span></span> <span data-ttu-id="226e1-131">Änderungen an Adressblöcken werden nun aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="226e1-131">Changes to address blocks will now update.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="226e1-132">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="226e1-132">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="226e1-133">Leistungsbeurteilungen drucken</span><span class="sxs-lookup"><span data-stu-id="226e1-133">Print performance reviews</span></span>

<span data-ttu-id="226e1-134">Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.</span><span class="sxs-lookup"><span data-stu-id="226e1-134">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="226e1-135">Arbeitsbereich für die Funktionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="226e1-135">Feature management workspace</span></span>

<span data-ttu-id="226e1-136">Funktionen werden in jeder Version hinzugefügt und aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="226e1-136">Features are added and updated in every release.</span></span> <span data-ttu-id="226e1-137">Die Funktionsverwaltungserfahrung bietet einen Arbeitsbereich, in dem Sie eine Liste mit Funktionen anzeigen können, die in jeder Version geliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="226e1-137">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="226e1-138">Standardmäßig sind neue Funktionen ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="226e1-138">By default, new features are turned off.</span></span> <span data-ttu-id="226e1-139">Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="226e1-139">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="226e1-140">Weitere Informationen über die Änderungen, die in der Funktionsverwaltung enthalten sind, finden Sie unter [Überblick über die Funktionsverwaltung](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="226e1-140">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
