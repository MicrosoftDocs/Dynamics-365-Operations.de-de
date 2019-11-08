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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572448"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="eb600-103">Organisationshierarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="eb600-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="eb600-104">Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="eb600-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="eb600-105">Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="eb600-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="eb600-106">Obwohl es in Common Data Service nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös.</span><span class="sxs-lookup"><span data-stu-id="eb600-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="eb600-107">Im Rahmen der Common Data Service-Integration wird die Datenstruktur der Organisationshierarchie zu Common Data Service hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="eb600-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="eb600-108">Datenfluss</span><span class="sxs-lookup"><span data-stu-id="eb600-108">Data flow</span></span>

<span data-ttu-id="eb600-109">Ein Geschäftsökosystem, das aus Finance and Operations-Apps and Common Data Service besteht, wird weiterhin eine Organisationshierarchie haben.</span><span class="sxs-lookup"><span data-stu-id="eb600-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="eb600-110">Diese Organisationshierarchie basiert auf Finance and Operations-Apps, wird aber in Common Data Service zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="eb600-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="eb600-111">Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Common Data Service als unidirektionaler Datenfluss von Finance and Operations-Apps nach Common Data Service verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="eb600-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Architekturabbildung](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="eb600-113">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="eb600-113">Templates</span></span>

<span data-ttu-id="eb600-114">Entitätszuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung von Daten aus Finance and Operations-Apps nach Common Data Service verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eb600-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="eb600-115">Zweck der internen Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="eb600-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="eb600-116">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“ von Finance and Operations nach anderen Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="eb600-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="eb600-117">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-117">Source field</span></span> | <span data-ttu-id="eb600-118">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="eb600-118">Map type</span></span> | <span data-ttu-id="eb600-119">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-119">Destination field</span></span>
---|---|---
<span data-ttu-id="eb600-120">HIERARCHIETYP</span><span class="sxs-lookup"><span data-stu-id="eb600-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="eb600-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="eb600-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="eb600-122">HIERARCHIETYP</span><span class="sxs-lookup"><span data-stu-id="eb600-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="eb600-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="eb600-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="eb600-124">HIERARCHIEZWECK</span><span class="sxs-lookup"><span data-stu-id="eb600-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="eb600-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="eb600-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="eb600-126">UNVERÄNDERLICH</span><span class="sxs-lookup"><span data-stu-id="eb600-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="eb600-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="eb600-127">msdyn\_immutable</span></span>
<span data-ttu-id="eb600-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="eb600-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="eb600-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="eb600-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="eb600-130">Interner Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="eb600-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="eb600-131">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Organisationshierarchietyp“ von Finance and Operations nach anderen Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="eb600-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="eb600-132">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-132">Source field</span></span> | <span data-ttu-id="eb600-133">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="eb600-133">Map type</span></span> | <span data-ttu-id="eb600-134">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-134">Destination field</span></span>
---|---|---
<span data-ttu-id="eb600-135">NAME</span><span class="sxs-lookup"><span data-stu-id="eb600-135">NAME</span></span> | \> | <span data-ttu-id="eb600-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="eb600-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="eb600-137">Interner Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="eb600-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="eb600-138">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Veröffentlichte Organisationshierarchie“ von Finance and Operations nach anderen Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="eb600-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="eb600-139">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-139">Source field</span></span> | <span data-ttu-id="eb600-140">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="eb600-140">Map type</span></span> | <span data-ttu-id="eb600-141">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-141">Destination field</span></span>
---|---|---
<span data-ttu-id="eb600-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="eb600-142">VALIDTO</span></span> | \> | <span data-ttu-id="eb600-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="eb600-143">msdyn\_validto</span></span>
<span data-ttu-id="eb600-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="eb600-144">VALIDFROM</span></span> | \> | <span data-ttu-id="eb600-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="eb600-145">msdyn\_validfrom</span></span>
<span data-ttu-id="eb600-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="eb600-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="eb600-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="eb600-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="eb600-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="eb600-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="eb600-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="eb600-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="eb600-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="eb600-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="eb600-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="eb600-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="eb600-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="eb600-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="eb600-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="eb600-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="eb600-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="eb600-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="eb600-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="eb600-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="eb600-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="eb600-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="eb600-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="eb600-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="eb600-158">Interne Organisation</span><span class="sxs-lookup"><span data-stu-id="eb600-158">Internal Organization</span></span>

<span data-ttu-id="eb600-159">Informationen zur internen Organisation in Common Data Service stammen aus zwei Entitäten, **Organisationseinheit** und **juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="eb600-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="eb600-160">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="eb600-160">Operating unit</span></span>

<span data-ttu-id="eb600-161">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-161">Source field</span></span> | <span data-ttu-id="eb600-162">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="eb600-162">Map type</span></span> | <span data-ttu-id="eb600-163">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-163">Destination field</span></span>
---|---|---
<span data-ttu-id="eb600-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="eb600-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="eb600-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="eb600-165">msdyn\_languageid</span></span>
<span data-ttu-id="eb600-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="eb600-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="eb600-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="eb600-167">msdyn\_namealias</span></span>
<span data-ttu-id="eb600-168">NAME</span><span class="sxs-lookup"><span data-stu-id="eb600-168">NAME</span></span> | \> | <span data-ttu-id="eb600-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="eb600-169">msdyn\_name</span></span>
<span data-ttu-id="eb600-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="eb600-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="eb600-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="eb600-171">msdyn\_partynumber</span></span>
<span data-ttu-id="eb600-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="eb600-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="eb600-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="eb600-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="eb600-174">Juristische Person</span><span class="sxs-lookup"><span data-stu-id="eb600-174">Legal entity</span></span>

<span data-ttu-id="eb600-175">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-175">Source field</span></span> | <span data-ttu-id="eb600-176">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="eb600-176">Map type</span></span> | <span data-ttu-id="eb600-177">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-177">Destination field</span></span>
---|---|---
<span data-ttu-id="eb600-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="eb600-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="eb600-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="eb600-179">msdyn\_namealias</span></span>
<span data-ttu-id="eb600-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="eb600-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="eb600-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="eb600-181">msdyn\_languageid</span></span>
<span data-ttu-id="eb600-182">NAME</span><span class="sxs-lookup"><span data-stu-id="eb600-182">NAME</span></span> | \> | <span data-ttu-id="eb600-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="eb600-183">msdyn\_name</span></span>
<span data-ttu-id="eb600-184">PARTEINUMMER</span><span class="sxs-lookup"><span data-stu-id="eb600-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="eb600-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="eb600-185">msdyn\_partynumber</span></span>
<span data-ttu-id="eb600-186">Kein</span><span class="sxs-lookup"><span data-stu-id="eb600-186">none</span></span> | \>\> | <span data-ttu-id="eb600-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="eb600-187">msdyn\_type</span></span>
<span data-ttu-id="eb600-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="eb600-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="eb600-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="eb600-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="eb600-190">Firma</span><span class="sxs-lookup"><span data-stu-id="eb600-190">Company</span></span>

<span data-ttu-id="eb600-191">Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen) zwischen Finance and Operations und anderen Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="eb600-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="eb600-192">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-192">Source field</span></span> | <span data-ttu-id="eb600-193">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="eb600-193">Map type</span></span> | <span data-ttu-id="eb600-194">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="eb600-194">Destination field</span></span>
---|---|---
<span data-ttu-id="eb600-195">NAME</span><span class="sxs-lookup"><span data-stu-id="eb600-195">NAME</span></span> | = | <span data-ttu-id="eb600-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="eb600-196">cdm\_name</span></span>
<span data-ttu-id="eb600-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="eb600-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="eb600-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="eb600-198">cdm\_companycode</span></span>
