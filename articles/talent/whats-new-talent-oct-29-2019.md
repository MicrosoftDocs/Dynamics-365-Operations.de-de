---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (29. Oktober 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897441"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="202b2-103">Neuerungen oder Änderungen in Dynamics 365 Talent (29. Oktober 2019)</span><span class="sxs-lookup"><span data-stu-id="202b2-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

<span data-ttu-id="202b2-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="202b2-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="202b2-105">Änderungen in Attract</span><span class="sxs-lookup"><span data-stu-id="202b2-105">Changes in Attract</span></span>

<span data-ttu-id="202b2-106">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="202b2-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="202b2-107">Änderungen in Onboard</span><span class="sxs-lookup"><span data-stu-id="202b2-107">Changes in Onboard</span></span>

<span data-ttu-id="202b2-108">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="202b2-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="202b2-109">Core HR-Änderungen</span><span class="sxs-lookup"><span data-stu-id="202b2-109">Changes in Core HR</span></span>

<span data-ttu-id="202b2-110">Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="202b2-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="202b2-111">Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="202b2-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="202b2-112">Löschparteien ohne Rollen sollten standardmäßig eingeschaltet sein (371233).</span><span class="sxs-lookup"><span data-stu-id="202b2-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="202b2-113">Wenn Sie eine neue Umgebung in Talent bereitstellen, ist **Partner löschen, wenn keine Rollen vorhanden sind** standardmäßig eingeschaltet.</span><span class="sxs-lookup"><span data-stu-id="202b2-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="202b2-114">Wenn Sie einen Mitarbeiter löschen, wird die mit dem Mitarbeiter verbundene Partei nur dann entfernt, wenn diese Einstellung eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="202b2-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="202b2-115">Diese Änderung begrenzt doppelte Datensätze im globalen Adressbuch, wenn Sie Mitarbeiter importieren, ändern oder reimportieren müssen.</span><span class="sxs-lookup"><span data-stu-id="202b2-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="202b2-116">Entwürfe und stornierte Urlaubsanträge sollten in Common Data Service (376999) gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="202b2-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="202b2-117">Mit dieser Änderung können Sie nun in Common Data Service Urlaubsanträge mit dem Status **Entwurf** oder **Storniert** löschen.</span><span class="sxs-lookup"><span data-stu-id="202b2-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="202b2-118">Zusätzliche Listenwerte in benutzerdefinierten Feldern werden nach dem Klicken auf Übernehmen im Formular Benutzerdefinierte Felder (379599) nicht in Common Data Service angezeigt.</span><span class="sxs-lookup"><span data-stu-id="202b2-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="202b2-119">Wenn Sie neue Listenwerte zu einem bestehenden benutzerdefinierten Feld hinzufügen, das bereits mit Common Data Service synchronisiert wurde, sind sie nun im Gemeinsamen Datenservice verfügbar, nachdem Sie Ihre Änderungen im Formular **Benutzerdefinierte Felder** übernommen haben.</span><span class="sxs-lookup"><span data-stu-id="202b2-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="202b2-120">Anwendung von Onboarding-Checklisten bei mehr als einer Beschäftigung in allen Rechtspersonen (371270)</span><span class="sxs-lookup"><span data-stu-id="202b2-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="202b2-121">In der Freigabe dieser Woche können Sie Checklisten auf Mitarbeiter mit mehr als einer Beschäftigung in **Arbeiterformular > Checklisten** anwenden.</span><span class="sxs-lookup"><span data-stu-id="202b2-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="202b2-122">Die Vorschau der Vorteile der offenen Registrierung wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="202b2-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="202b2-123">In Verbindung mit unserer Ankündigung in der Rubrik [Strategische Investitionen in Core HR fördern die operative Exzellenz](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) Blog-Post, hat Microsoft die Vorteile der offenen Registrierungsfunktion aus der öffentlichen Vorschau entfernt.</span><span class="sxs-lookup"><span data-stu-id="202b2-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="202b2-124">Neue Funktionen werden in Zukunft veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="202b2-124">New functionality will be released in the future.</span></span> <span data-ttu-id="202b2-125">Die produktive Nutzung der Vorteile der offenen Registrierungsfunktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="202b2-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="202b2-126">Bald verfügbar</span><span class="sxs-lookup"><span data-stu-id="202b2-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="202b2-127">Leistungsbeurteilungen drucken</span><span class="sxs-lookup"><span data-stu-id="202b2-127">Print performance reviews</span></span>

<span data-ttu-id="202b2-128">Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.</span><span class="sxs-lookup"><span data-stu-id="202b2-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="202b2-129">Arbeitsbereich für die Funktionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="202b2-129">Feature management workspace</span></span>

<span data-ttu-id="202b2-130">Funktionen werden in jeder Version hinzugefügt und aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="202b2-130">Features are added and updated in every release.</span></span> <span data-ttu-id="202b2-131">Die Funktionsverwaltungserfahrung bietet einen Arbeitsbereich, in dem Sie eine Liste mit Funktionen anzeigen können, die in jeder Version geliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="202b2-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="202b2-132">Standardmäßig sind neue Funktionen ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="202b2-132">By default, new features are turned off.</span></span> <span data-ttu-id="202b2-133">Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="202b2-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="202b2-134">Weitere Informationen über die Änderungen, die in der Funktionsverwaltung enthalten sind, finden Sie unter [Überblick über die Funktionsverwaltung](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="202b2-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
