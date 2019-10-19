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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182024"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="fca4c-103">Organisationshierarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fca4c-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="fca4c-104">Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="fca4c-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="fca4c-105">Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="fca4c-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="fca4c-106">Obwohl es in Common Data Service nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös.</span><span class="sxs-lookup"><span data-stu-id="fca4c-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="fca4c-107">Im Rahmen der Common Data Service-Integration wird die Datenstruktur der Organisationshierarchie zu Common Data Service hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fca4c-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="fca4c-108">Datenfluss</span><span class="sxs-lookup"><span data-stu-id="fca4c-108">Data flow</span></span>

<span data-ttu-id="fca4c-109">Ein Geschäftsökosystem, das aus Finance and Operations-Apps and Common Data Service besteht, wird weiterhin eine Organisationshierarchie haben.</span><span class="sxs-lookup"><span data-stu-id="fca4c-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="fca4c-110">Diese Organisationshierarchie basiert auf Finance and Operations-Apps, wird aber in Common Data Service zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="fca4c-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="fca4c-111">Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Common Data Service als unidirektionaler Datenfluss von Finance and Operations-Apps nach Common Data Service verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="fca4c-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Architekturabbildung](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="fca4c-113">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="fca4c-113">Templates</span></span>

<span data-ttu-id="fca4c-114">Entitätszuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung von Daten aus Finance and Operations-Apps nach Common Data Service verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fca4c-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="fca4c-115">Zweck der internen Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="fca4c-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="fca4c-116">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“ von Finance and Operations nach anderen Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="fca4c-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="fca4c-117">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-117">Source field</span></span> | <span data-ttu-id="fca4c-118">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="fca4c-118">Map type</span></span> | <span data-ttu-id="fca4c-119">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-119">Destination field</span></span>
---|---|---
<span data-ttu-id="fca4c-120">HIERARCHIETYP</span><span class="sxs-lookup"><span data-stu-id="fca4c-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="fca4c-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="fca4c-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="fca4c-122">HIERARCHIETYP</span><span class="sxs-lookup"><span data-stu-id="fca4c-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="fca4c-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fca4c-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="fca4c-124">HIERARCHIEZWECK</span><span class="sxs-lookup"><span data-stu-id="fca4c-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="fca4c-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="fca4c-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="fca4c-126">UNVERÄNDERLICH</span><span class="sxs-lookup"><span data-stu-id="fca4c-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="fca4c-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="fca4c-127">msdyn\_immutable</span></span>
<span data-ttu-id="fca4c-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="fca4c-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="fca4c-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="fca4c-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="fca4c-130">Interner Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="fca4c-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="fca4c-131">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Organisationshierarchietyp“ von Finance and Operations nach anderen Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="fca4c-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="fca4c-132">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-132">Source field</span></span> | <span data-ttu-id="fca4c-133">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="fca4c-133">Map type</span></span> | <span data-ttu-id="fca4c-134">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-134">Destination field</span></span>
---|---|---
<span data-ttu-id="fca4c-135">NAME</span><span class="sxs-lookup"><span data-stu-id="fca4c-135">NAME</span></span> | \> | <span data-ttu-id="fca4c-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fca4c-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="fca4c-137">Interner Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="fca4c-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="fca4c-138">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Veröffentlichte Organisationshierarchie“ von Finance and Operations nach anderen Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="fca4c-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="fca4c-139">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-139">Source field</span></span> | <span data-ttu-id="fca4c-140">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="fca4c-140">Map type</span></span> | <span data-ttu-id="fca4c-141">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-141">Destination field</span></span>
---|---|---
<span data-ttu-id="fca4c-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="fca4c-142">VALIDTO</span></span> | \> | <span data-ttu-id="fca4c-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="fca4c-143">msdyn\_validto</span></span>
<span data-ttu-id="fca4c-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="fca4c-144">VALIDFROM</span></span> | \> | <span data-ttu-id="fca4c-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="fca4c-145">msdyn\_validfrom</span></span>
<span data-ttu-id="fca4c-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="fca4c-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="fca4c-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="fca4c-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="fca4c-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fca4c-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="fca4c-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="fca4c-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="fca4c-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fca4c-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="fca4c-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="fca4c-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="fca4c-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="fca4c-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="fca4c-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fca4c-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="fca4c-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fca4c-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="fca4c-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="fca4c-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="fca4c-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fca4c-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="fca4c-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="fca4c-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="fca4c-158">Interne Organisation</span><span class="sxs-lookup"><span data-stu-id="fca4c-158">Internal Organization</span></span>

<span data-ttu-id="fca4c-159">Informationen zur internen Organisation in Common Data Service stammen aus zwei Entitäten, **Organisationseinheit** und **juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="fca4c-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="fca4c-160">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="fca4c-160">Operating unit</span></span>

<span data-ttu-id="fca4c-161">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-161">Source field</span></span> | <span data-ttu-id="fca4c-162">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="fca4c-162">Map type</span></span> | <span data-ttu-id="fca4c-163">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-163">Destination field</span></span>
---|---|---
<span data-ttu-id="fca4c-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="fca4c-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="fca4c-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="fca4c-165">msdyn\_languageid</span></span>
<span data-ttu-id="fca4c-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="fca4c-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="fca4c-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="fca4c-167">msdyn\_namealias</span></span>
<span data-ttu-id="fca4c-168">NAME</span><span class="sxs-lookup"><span data-stu-id="fca4c-168">NAME</span></span> | \> | <span data-ttu-id="fca4c-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fca4c-169">msdyn\_name</span></span>
<span data-ttu-id="fca4c-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fca4c-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="fca4c-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="fca4c-171">msdyn\_partynumber</span></span>
<span data-ttu-id="fca4c-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="fca4c-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="fca4c-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="fca4c-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="fca4c-174">Juristische Person</span><span class="sxs-lookup"><span data-stu-id="fca4c-174">Legal entity</span></span>

<span data-ttu-id="fca4c-175">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-175">Source field</span></span> | <span data-ttu-id="fca4c-176">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="fca4c-176">Map type</span></span> | <span data-ttu-id="fca4c-177">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-177">Destination field</span></span>
---|---|---
<span data-ttu-id="fca4c-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="fca4c-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="fca4c-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="fca4c-179">msdyn\_namealias</span></span>
<span data-ttu-id="fca4c-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="fca4c-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="fca4c-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="fca4c-181">msdyn\_languageid</span></span>
<span data-ttu-id="fca4c-182">NAME</span><span class="sxs-lookup"><span data-stu-id="fca4c-182">NAME</span></span> | \> | <span data-ttu-id="fca4c-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fca4c-183">msdyn\_name</span></span>
<span data-ttu-id="fca4c-184">PARTEINUMMER</span><span class="sxs-lookup"><span data-stu-id="fca4c-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="fca4c-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="fca4c-185">msdyn\_partynumber</span></span>
<span data-ttu-id="fca4c-186">Kein</span><span class="sxs-lookup"><span data-stu-id="fca4c-186">none</span></span> | \>\> | <span data-ttu-id="fca4c-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="fca4c-187">msdyn\_type</span></span>
<span data-ttu-id="fca4c-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="fca4c-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="fca4c-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="fca4c-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="fca4c-190">Firma</span><span class="sxs-lookup"><span data-stu-id="fca4c-190">Company</span></span>

<span data-ttu-id="fca4c-191">Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen) zwischen Finance and Operations und anderen Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="fca4c-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="fca4c-192">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-192">Source field</span></span> | <span data-ttu-id="fca4c-193">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="fca4c-193">Map type</span></span> | <span data-ttu-id="fca4c-194">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="fca4c-194">Destination field</span></span>
---|---|---
<span data-ttu-id="fca4c-195">NAME</span><span class="sxs-lookup"><span data-stu-id="fca4c-195">NAME</span></span> | = | <span data-ttu-id="fca4c-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="fca4c-196">cdm\_name</span></span>
<span data-ttu-id="fca4c-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="fca4c-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="fca4c-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="fca4c-198">cdm\_companycode</span></span>
