---
title: Neuerungen und Änderungen in Dynamics 365 Talent (31. Juli 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83f3339e6cea1448f5b257acf602fe5ca3449555
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010244"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-30-2019"></a><span data-ttu-id="08146-103">Neuerungen und Änderungen in Dynamics 365 Talent (30. Juli 2019)</span><span class="sxs-lookup"><span data-stu-id="08146-103">What's new or changed in Dynamics 365 Talent (July 30, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="08146-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="08146-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="08146-105">Änderungen in Attract</span><span class="sxs-lookup"><span data-stu-id="08146-105">Changes in Attract</span></span>
<span data-ttu-id="08146-106">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="08146-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="08146-107">Änderungen in Onboard</span><span class="sxs-lookup"><span data-stu-id="08146-107">Changes in Onboard</span></span>
<span data-ttu-id="08146-108">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="08146-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="08146-109">Core HR-Änderungen</span><span class="sxs-lookup"><span data-stu-id="08146-109">Changes in Core HR</span></span>
<span data-ttu-id="08146-110">Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2409.</span><span class="sxs-lookup"><span data-stu-id="08146-110">Changes described in this section apply to build number 8.1.2409.</span></span>


### <a name="region-support-for-canada-and-southeast-asia"></a><span data-ttu-id="08146-111">Regionssupport für Kanada und Südostasien</span><span class="sxs-lookup"><span data-stu-id="08146-111">Region support for Canada and Southeast Asia</span></span>

<span data-ttu-id="08146-112">Wir freuen uns anzukündigen, dass Kanada- und Südostasien nun für Talent am 1. August 2019 verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="08146-112">We are pleased to announce that Canada and Southeast Asia regions will be available for Talent on August 1, 2019.</span></span> <span data-ttu-id="08146-113">Mit dieser Änderung können Umgebungen in kanadischen asiatischen Regionen erstellen, und alle Talentdaten werden nur innerhalb dieser Standorte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="08146-113">With this change, you can create environments in the Canadian and Asian regions, and all Talent data will be maintained solely within those locations.</span></span> <span data-ttu-id="08146-114">Sie können eine Umgebung in diesen neuen Regionen erstellen, indem Sie die elektronische Adresse im neuen Umgebungsdialogfeld auswählen und diese Umgebung verwenden, um Talent in LCS wie unter [Talent bereitstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) beschrieben nutzen</span><span class="sxs-lookup"><span data-stu-id="08146-114">You can create an environment in these new regions by selecting the location in the New Environment dialog and use that environment to provision Talent in LCS as described in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="08146-115">Datenmigration vorhandener Projekte aus anderen Regionen in kanadische und asiatische Regionen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08146-115">Data migration of existing projects from other regions to the Canadian and Asian regions is not supported.</span></span> <span data-ttu-id="08146-116">Nur neue Projekte können zu den neuen unterstützten Regionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="08146-116">Only new projects can be provisioned to the these new supported regions.</span></span>

### <a name="new-active-positions-list-page"></a><span data-ttu-id="08146-117">Neue aktive Positionslistenseite</span><span class="sxs-lookup"><span data-stu-id="08146-117">New Active positions list page</span></span>

<span data-ttu-id="08146-118">Die Optionen für positionsbasierte Listen enthalten nun: **Alle Positionen**, **Aktive Positionen**, **Offene Positionen** und **Inaktive Positionen**.</span><span class="sxs-lookup"><span data-stu-id="08146-118">The options for position-based lists now include: **All positions**, **Active positions**, **Open positions**, and **Inactive positions**.</span></span> <span data-ttu-id="08146-119">Die Listenseite neue **Aktive Positionen** zeigt nur die Positionen an, offen oder besetzt, die zum aktuellen Datum aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="08146-119">The new **Active positions** list page displays only those positions, open or filled, that are active as of the current date.</span></span> 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a><span data-ttu-id="08146-120">Ermöglichen Sie den Kursteilnehmer, offenen Kursen hinzugefügt zu werden</span><span class="sxs-lookup"><span data-stu-id="08146-120">Allow course participants to be added to open courses</span></span>

<span data-ttu-id="08146-121">Die Änderungen dieser Woche beheben ein Problem, bei dem nur Direktunterstellte für offene Kurse erfasst werden können.</span><span class="sxs-lookup"><span data-stu-id="08146-121">This week's changes correct an issue where only direct reports can be registered for open courses.</span></span>

### <a name="fte-analysis-displaying-incorrect-fte-number"></a><span data-ttu-id="08146-122">FTE-Analyse, die falsche FTE-Nummer anzeigt</span><span class="sxs-lookup"><span data-stu-id="08146-122">FTE Analysis displaying incorrect FTE number</span></span>

<span data-ttu-id="08146-123">**FTE-Analyse** ist auf der Registerkarte **Analyse** von **Personalführung** korrigiert worden.</span><span class="sxs-lookup"><span data-stu-id="08146-123">**FTE analysis** has been corrected in the **Analytics** tab of **Personnel management**.</span></span>

### <a name="final-comments-label-translation"></a><span data-ttu-id="08146-124">Abschließende Kommentarbeschriftungsübersetzung</span><span class="sxs-lookup"><span data-stu-id="08146-124">Final comments label translation</span></span>

<span data-ttu-id="08146-125">Das Feld **Abschließende Kommentare** wird nun in der Prüfungsform übersetzt.</span><span class="sxs-lookup"><span data-stu-id="08146-125">The **Final comments** label is now translated in the review form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="08146-126">Vorschau</span><span class="sxs-lookup"><span data-stu-id="08146-126">In preview</span></span>

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a><span data-ttu-id="08146-127">Vorschaufunktionen werden nur in den Sandkasteninstanzen aktiviert</span><span class="sxs-lookup"><span data-stu-id="08146-127">Preview features are enabled only in sandbox instances</span></span>

<span data-ttu-id="08146-128">Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** ist.</span><span class="sxs-lookup"><span data-stu-id="08146-128">When you provision a new instance of Talent, you can specify whether the instance type is **Production** or **Sandbox**.</span></span> <span data-ttu-id="08146-129">Die Instanzen vom **Sandkasten** Typ ermöglichen ein frühzeitiges Testen neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="08146-129">Instances of the **Sandbox** type allow for early testing of new features.</span></span> <span data-ttu-id="08146-130">Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="08146-130">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="08146-131">Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="08146-131">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

<span data-ttu-id="08146-132">Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="08146-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

### <a name="view-extended-information-for-performance-in-manager-self-service"></a><span data-ttu-id="08146-133">Anzeigen von erweiterten Informationen, um die Leistung im Manager Self-Service zu melden</span><span class="sxs-lookup"><span data-stu-id="08146-133">View extended information for performance in manager self-service</span></span>

<span data-ttu-id="08146-134">Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen.</span><span class="sxs-lookup"><span data-stu-id="08146-134">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="08146-135">Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen.</span><span class="sxs-lookup"><span data-stu-id="08146-135">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="08146-136">Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft.</span><span class="sxs-lookup"><span data-stu-id="08146-136">In addition, direct managers and their employees can maintain and update performance journals to help ensure that the performance review process goes smoothly.</span></span> <span data-ttu-id="08146-137">Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="08146-137">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>
