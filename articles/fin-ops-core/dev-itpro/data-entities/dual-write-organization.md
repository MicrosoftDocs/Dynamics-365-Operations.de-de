---
title: Organisationshierarchie in Common Data Service
description: In diesem Thema wird die Integration von Organisationsdaten zwischen Finance and Operations-Apps und Common Data Service beschrieben.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9efc63c385c31a6d8848d016c1a8689460908dcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769659"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="97414-103">Organisationshierarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="97414-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97414-104">Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="97414-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="97414-105">Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="97414-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="97414-106">Obwohl es in Common Data Service nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös.</span><span class="sxs-lookup"><span data-stu-id="97414-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="97414-107">Im Rahmen der Common Data Service-Integration wird die Datenstruktur der Organisationshierarchie zu Common Data Service hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="97414-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="97414-108">Datenfluss</span><span class="sxs-lookup"><span data-stu-id="97414-108">Data flow</span></span>

<span data-ttu-id="97414-109">Ein Geschäftsökosystem, das aus Finance and Operations-Apps and Common Data Service besteht, wird weiterhin eine Organisationshierarchie haben.</span><span class="sxs-lookup"><span data-stu-id="97414-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="97414-110">Diese Organisationshierarchie basiert auf Finance and Operations-Apps, wird aber in Common Data Service zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="97414-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="97414-111">Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Common Data Service als unidirektionaler Datenfluss von Finance and Operations-Apps nach Common Data Service verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="97414-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Architekturabbildung](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="97414-113">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="97414-113">Templates</span></span>

<span data-ttu-id="97414-114">Entitätszuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung von Daten aus Finance and Operations-Apps nach Common Data Service verfügbar.</span><span class="sxs-lookup"><span data-stu-id="97414-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="97414-115">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="97414-115">Templates</span></span>

<span data-ttu-id="97414-116">Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen.</span><span class="sxs-lookup"><span data-stu-id="97414-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="97414-117">Wie die folgende Tabelle zeigt, darstellt, wird eine Sammlung von Entitätszuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="97414-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="97414-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97414-118">Finance and Operations</span></span> | <span data-ttu-id="97414-119">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="97414-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="97414-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97414-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="97414-121">Organisationshierarchiezwecke</span><span class="sxs-lookup"><span data-stu-id="97414-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="97414-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="97414-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="97414-123">Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“.</span><span class="sxs-lookup"><span data-stu-id="97414-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="97414-124">Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="97414-124">Organization hierarchy type</span></span> | <span data-ttu-id="97414-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="97414-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="97414-126">Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Entität „Organisationshierarchietyp“.</span><span class="sxs-lookup"><span data-stu-id="97414-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="97414-127">Organisationshierarchie – veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="97414-127">Organization hierarchy - published</span></span> | <span data-ttu-id="97414-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="97414-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="97414-129">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Veröffentlichte Organisationshierarchie“.</span><span class="sxs-lookup"><span data-stu-id="97414-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="97414-130">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="97414-130">Operating unit</span></span> | <span data-ttu-id="97414-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="97414-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="97414-132">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="97414-132">Legal entities</span></span> | <span data-ttu-id="97414-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="97414-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="97414-134">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="97414-134">Legal entities</span></span> | <span data-ttu-id="97414-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="97414-135">cdm_companies</span></span> | <span data-ttu-id="97414-136">Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen).</span><span class="sxs-lookup"><span data-stu-id="97414-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](dual-write/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](dual-write/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](dual-write/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="97414-137">Interne Organisation</span><span class="sxs-lookup"><span data-stu-id="97414-137">Internal Organization</span></span>

<span data-ttu-id="97414-138">Informationen zur internen Organisation in Common Data Service stammen aus zwei Entitäten, **Organisationseinheit** und **juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="97414-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](dual-write/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-Companies.md)]

