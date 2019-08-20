---
title: Organisationshierarchie in Common Data Service
description: In diesem Thema wird die Integration von Organisationsdaten zwischen Finance and Operations und Common Data Service beschrieben.
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789193"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="3790b-103">Organisationshierarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3790b-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="3790b-104">Da Microsoft Dynamics 365 for Finance and Operations ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="3790b-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="3790b-105">Unternehmensfinanzen und Vorgänge können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="3790b-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="3790b-106">Obwohl es in Common Data Service nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös.</span><span class="sxs-lookup"><span data-stu-id="3790b-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="3790b-107">Im Rahmen der Common Data Service-Integration wird die Datenstruktur der Organisationshierarchie zu Common Data Service hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3790b-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="3790b-108">Datenfluss</span><span class="sxs-lookup"><span data-stu-id="3790b-108">Data flow</span></span>

<span data-ttu-id="3790b-109">Ein Geschäftsökosystem, das aus Finance and Operations and Common Data Service besteht, wird weiterhin eine Organisationshierarchie haben.</span><span class="sxs-lookup"><span data-stu-id="3790b-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="3790b-110">Diese Organisationshierarchie basiert auf Finance and Operations, wird aber in Common Data Service zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="3790b-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="3790b-111">Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Common Data Service als unidirektionaler Datenfluss von Finance and Operations nach Common Data Serviceverfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="3790b-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Architekturabbildung](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="3790b-113">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="3790b-113">Templates</span></span>

<span data-ttu-id="3790b-114">Entitätszuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung von Daten aus Finance and Operations nach Common Data Service verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3790b-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="3790b-115">Zweck der internen Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="3790b-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="3790b-116">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“ von Finance and Operations nach Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3790b-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="3790b-117">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-117">Source field</span></span> | <span data-ttu-id="3790b-118">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="3790b-118">Map type</span></span> | <span data-ttu-id="3790b-119">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-119">Destination field</span></span>
---|---|---
<span data-ttu-id="3790b-120">HIERARCHIETYP</span><span class="sxs-lookup"><span data-stu-id="3790b-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="3790b-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="3790b-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="3790b-122">HIERARCHIETYP</span><span class="sxs-lookup"><span data-stu-id="3790b-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="3790b-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="3790b-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="3790b-124">HIERARCHIEZWECK</span><span class="sxs-lookup"><span data-stu-id="3790b-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="3790b-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="3790b-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="3790b-126">UNVERÄNDERLICH</span><span class="sxs-lookup"><span data-stu-id="3790b-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="3790b-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="3790b-127">msdyn\_immutable</span></span>
<span data-ttu-id="3790b-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="3790b-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="3790b-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="3790b-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="3790b-130">Interner Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="3790b-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="3790b-131">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“ von Finance and Operations nach Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3790b-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="3790b-132">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-132">Source field</span></span> | <span data-ttu-id="3790b-133">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="3790b-133">Map type</span></span> | <span data-ttu-id="3790b-134">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-134">Destination field</span></span>
---|---|---
<span data-ttu-id="3790b-135">NAME</span><span class="sxs-lookup"><span data-stu-id="3790b-135">NAME</span></span> | \> | <span data-ttu-id="3790b-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="3790b-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="3790b-137">Interner Organisationshierarchietyp</span><span class="sxs-lookup"><span data-stu-id="3790b-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="3790b-138">Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Veröffentlichte Organisationshierarchie“ von Finance and Operations nach Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3790b-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="3790b-139">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-139">Source field</span></span> | <span data-ttu-id="3790b-140">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="3790b-140">Map type</span></span> | <span data-ttu-id="3790b-141">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-141">Destination field</span></span>
---|---|---
<span data-ttu-id="3790b-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="3790b-142">VALIDTO</span></span> | \> | <span data-ttu-id="3790b-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="3790b-143">msdyn\_validto</span></span>
<span data-ttu-id="3790b-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="3790b-144">VALIDFROM</span></span> | \> | <span data-ttu-id="3790b-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="3790b-145">msdyn\_validfrom</span></span>
<span data-ttu-id="3790b-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="3790b-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="3790b-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="3790b-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="3790b-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="3790b-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="3790b-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="3790b-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="3790b-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="3790b-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="3790b-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="3790b-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="3790b-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="3790b-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="3790b-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="3790b-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="3790b-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="3790b-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="3790b-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="3790b-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="3790b-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="3790b-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="3790b-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="3790b-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="3790b-158">Interne Organisation</span><span class="sxs-lookup"><span data-stu-id="3790b-158">Internal Organization</span></span>

<span data-ttu-id="3790b-159">Informationen zur internen Organisation in Common Data Service stammen aus zwei auf Finance and Operations-Entitäten, **Organisationseinheit** und **juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="3790b-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="3790b-160">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="3790b-160">Operating unit</span></span>

<span data-ttu-id="3790b-161">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-161">Source field</span></span> | <span data-ttu-id="3790b-162">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="3790b-162">Map type</span></span> | <span data-ttu-id="3790b-163">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-163">Destination field</span></span>
---|---|---
<span data-ttu-id="3790b-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="3790b-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="3790b-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="3790b-165">msdyn\_languageid</span></span>
<span data-ttu-id="3790b-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="3790b-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="3790b-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="3790b-167">msdyn\_namealias</span></span>
<span data-ttu-id="3790b-168">NAME</span><span class="sxs-lookup"><span data-stu-id="3790b-168">NAME</span></span> | \> | <span data-ttu-id="3790b-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="3790b-169">msdyn\_name</span></span>
<span data-ttu-id="3790b-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="3790b-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="3790b-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="3790b-171">msdyn\_partynumber</span></span>
<span data-ttu-id="3790b-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="3790b-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="3790b-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="3790b-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="3790b-174">Juristische Person</span><span class="sxs-lookup"><span data-stu-id="3790b-174">Legal entity</span></span>

<span data-ttu-id="3790b-175">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-175">Source field</span></span> | <span data-ttu-id="3790b-176">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="3790b-176">Map type</span></span> | <span data-ttu-id="3790b-177">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-177">Destination field</span></span>
---|---|---
<span data-ttu-id="3790b-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="3790b-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="3790b-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="3790b-179">msdyn\_namealias</span></span>
<span data-ttu-id="3790b-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="3790b-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="3790b-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="3790b-181">msdyn\_languageid</span></span>
<span data-ttu-id="3790b-182">NAME</span><span class="sxs-lookup"><span data-stu-id="3790b-182">NAME</span></span> | \> | <span data-ttu-id="3790b-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="3790b-183">msdyn\_name</span></span>
<span data-ttu-id="3790b-184">PARTEINUMMER</span><span class="sxs-lookup"><span data-stu-id="3790b-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="3790b-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="3790b-185">msdyn\_partynumber</span></span>
<span data-ttu-id="3790b-186">Kein</span><span class="sxs-lookup"><span data-stu-id="3790b-186">none</span></span> | \>\> | <span data-ttu-id="3790b-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="3790b-187">msdyn\_type</span></span>
<span data-ttu-id="3790b-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="3790b-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="3790b-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="3790b-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="3790b-190">Firma</span><span class="sxs-lookup"><span data-stu-id="3790b-190">Company</span></span>

<span data-ttu-id="3790b-191">Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen) zwischen Finance and Operations and Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3790b-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="3790b-192">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-192">Source field</span></span> | <span data-ttu-id="3790b-193">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="3790b-193">Map type</span></span> | <span data-ttu-id="3790b-194">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="3790b-194">Destination field</span></span>
---|---|---
<span data-ttu-id="3790b-195">NAME</span><span class="sxs-lookup"><span data-stu-id="3790b-195">NAME</span></span> | = | <span data-ttu-id="3790b-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="3790b-196">cdm\_name</span></span>
<span data-ttu-id="3790b-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="3790b-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="3790b-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="3790b-198">cdm\_companycode</span></span>
