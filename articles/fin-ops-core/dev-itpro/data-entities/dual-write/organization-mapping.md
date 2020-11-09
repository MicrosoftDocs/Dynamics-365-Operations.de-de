---
title: Organisationshierarchie in Common Data Service
description: In diesem Thema wird die Integration von Organisationsdaten zwischen Finance and Operations Apps und Common Data Service beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000733"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="d1864-103">Organisationshierarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d1864-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1864-104">Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="d1864-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="d1864-105">Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="d1864-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="d1864-106">Obwohl es in Common Data Service nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös.</span><span class="sxs-lookup"><span data-stu-id="d1864-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="d1864-107">Im Rahmen der Common Data Service-Integration wird die Datenstruktur der Organisationshierarchie zu Common Data Service hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d1864-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="d1864-108">Datenfluss</span><span class="sxs-lookup"><span data-stu-id="d1864-108">Data flow</span></span>

<span data-ttu-id="d1864-109">Ein Geschäftsökosystem, das aus Finance and Operations Apps und Common Data Service besteht, wird weiterhin eine Organisationshierarchie haben.</span><span class="sxs-lookup"><span data-stu-id="d1864-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="d1864-110">Diese Organisationshierarchie basiert auf Finance and Operations Apps, wird aber in Common Data Service zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="d1864-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="d1864-111">Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Common Data Service als unidirektionaler Datenfluss von Finance and Operations Apps nach Common Data Service verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="d1864-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Architekturabbildung](media/dual-write-data-flow.png)

<span data-ttu-id="d1864-113">Entitätszuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung Finance and Operations Apps zu Common Data Service  verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d1864-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="d1864-114">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="d1864-114">Templates</span></span>

<span data-ttu-id="d1864-115">Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen.</span><span class="sxs-lookup"><span data-stu-id="d1864-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="d1864-116">Wie die folgende Tabelle zeigt, darstellt, wird eine Sammlung von Entitätszuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d1864-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="d1864-117">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="d1864-117">Finance and Operations apps</span></span> | <span data-ttu-id="d1864-118">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="d1864-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="d1864-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1864-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="d1864-120">Organisationshierarchiezwecke</span><span class="sxs-lookup"><span data-stu-id="d1864-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="d1864-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="d1864-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="d1864-122">Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“.</span><span class="sxs-lookup"><span data-stu-id="d1864-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="d1864-123">Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="d1864-123">Organization hierarchy type</span></span> | <span data-ttu-id="d1864-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="d1864-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="d1864-125">Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Entität „Organisationshierarchietyp“.</span><span class="sxs-lookup"><span data-stu-id="d1864-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="d1864-126">Organisationshierarchie – veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="d1864-126">Organization hierarchy - published</span></span> | <span data-ttu-id="d1864-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="d1864-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="d1864-128">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Veröffentlichte Organisationshierarchie“.</span><span class="sxs-lookup"><span data-stu-id="d1864-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="d1864-129">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="d1864-129">Operating unit</span></span> | <span data-ttu-id="d1864-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d1864-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="d1864-131">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="d1864-131">Legal entities</span></span> | <span data-ttu-id="d1864-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d1864-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="d1864-133">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="d1864-133">Legal entities</span></span> | <span data-ttu-id="d1864-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="d1864-134">cdm_companies</span></span> | <span data-ttu-id="d1864-135">Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen).</span><span class="sxs-lookup"><span data-stu-id="d1864-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="d1864-136">Interne Organisation</span><span class="sxs-lookup"><span data-stu-id="d1864-136">Internal Organization</span></span>

<span data-ttu-id="d1864-137">Informationen zur internen Organisation in Common Data Service stammen aus zwei Entitäten, **Organisationseinheit** und **juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="d1864-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
