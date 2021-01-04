---
title: Organisationshierarchie in Dataverse
description: In diesem Thema wird die Integration von Organisationsdaten zwischen Finance and Operations Apps und Dataverse beschrieben.
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
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680071"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="b82b6-103">Organisationshierarchie in Dataverse</span><span class="sxs-lookup"><span data-stu-id="b82b6-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b82b6-104">Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="b82b6-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="b82b6-105">Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="b82b6-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="b82b6-106">Obwohl es in Dataverse nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös.</span><span class="sxs-lookup"><span data-stu-id="b82b6-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="b82b6-107">Im Rahmen der Dataverse-Integration wird die Datenstruktur der Organisationshierarchie zu Dataverse hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b82b6-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="b82b6-108">Datenfluss</span><span class="sxs-lookup"><span data-stu-id="b82b6-108">Data flow</span></span>

<span data-ttu-id="b82b6-109">Ein Geschäftsökosystem, das aus Finance and Operations Apps und Dataverse besteht, wird weiterhin eine Organisationshierarchie haben.</span><span class="sxs-lookup"><span data-stu-id="b82b6-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="b82b6-110">Diese Organisationshierarchie basiert auf Finance and Operations Apps, wird aber in Dataverse zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b82b6-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="b82b6-111">Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Dataverse als unidirektionaler Datenfluss von Finance and Operations Apps nach Dataverse verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="b82b6-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Architekturabbildung](media/dual-write-data-flow.png)

<span data-ttu-id="b82b6-113">Tabellenzuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung von Finance and Operations-Apps zu Dataverse verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b82b6-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="b82b6-114">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b82b6-114">Templates</span></span>

<span data-ttu-id="b82b6-115">Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen.</span><span class="sxs-lookup"><span data-stu-id="b82b6-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="b82b6-116">Wie die folgende Tabelle zeigt, wird eine Sammlung von Tabellenzuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="b82b6-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="b82b6-117">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="b82b6-117">Finance and Operations apps</span></span> | <span data-ttu-id="b82b6-118">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="b82b6-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="b82b6-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b82b6-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="b82b6-120">Organisationshierarchiezwecke</span><span class="sxs-lookup"><span data-stu-id="b82b6-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="b82b6-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="b82b6-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="b82b6-122">Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“.</span><span class="sxs-lookup"><span data-stu-id="b82b6-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="b82b6-123">Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="b82b6-123">Organization hierarchy type</span></span> | <span data-ttu-id="b82b6-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="b82b6-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="b82b6-125">Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Entität „Organisationshierarchietyp“.</span><span class="sxs-lookup"><span data-stu-id="b82b6-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="b82b6-126">Organisationshierarchie – veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="b82b6-126">Organization hierarchy - published</span></span> | <span data-ttu-id="b82b6-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="b82b6-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="b82b6-128">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Veröffentlichte Organisationshierarchie“.</span><span class="sxs-lookup"><span data-stu-id="b82b6-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="b82b6-129">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="b82b6-129">Operating unit</span></span> | <span data-ttu-id="b82b6-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="b82b6-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="b82b6-131">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="b82b6-131">Legal entities</span></span> | <span data-ttu-id="b82b6-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="b82b6-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="b82b6-133">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="b82b6-133">Legal entities</span></span> | <span data-ttu-id="b82b6-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="b82b6-134">cdm_companies</span></span> | <span data-ttu-id="b82b6-135">Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen).</span><span class="sxs-lookup"><span data-stu-id="b82b6-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="b82b6-136">Interne Organisation</span><span class="sxs-lookup"><span data-stu-id="b82b6-136">Internal Organization</span></span>

<span data-ttu-id="b82b6-137">Interne Organisationsinformationen in Dataverse stammen aus zwei Tabellen, **Organisationseinheit** und **Juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="b82b6-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
