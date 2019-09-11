---
title: Integrierte Standorte und Lagerorte
description: In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations und Common Data Service beschrieben.
author: benebotg
manager: AnnBe
ms.date: 15/8/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 3ee5192138374c58df9f9cfc033503d200356771
ms.sourcegitcommit: 559637f30037f6b52ebc4d4c13d0ecec46d4a051
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2019
ms.locfileid: "1920700"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="aeab5-103">Integrierte Standorte und Lagerorte</span><span class="sxs-lookup"><span data-stu-id="aeab5-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="aeab5-104">In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations und Common Data Service beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aeab5-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="aeab5-105">Betriebsstandorte und Lagerorte sind allgemeine Konzepte in einer Lieferketten-Verwaltungsanwendung.</span><span class="sxs-lookup"><span data-stu-id="aeab5-105">Operational sites and warehouses are common concepts in a supply chain management application.</span></span> <span data-ttu-id="aeab5-106">Sie werden verwendet, um die Lieferkette des Unternehmens zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="aeab5-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="aeab5-107">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="aeab5-107">Templates</span></span>

<span data-ttu-id="aeab5-108">Bei der Integration in Common Data Service sind diese Konzepte und all ihre zugehörigen Informationen in Common Data Service mithilfe der Standort- und Lagerortdatenentitäten in der folgenden Tabelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aeab5-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="aeab5-109">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="aeab5-109">Finance and Operations</span></span>  | <span data-ttu-id="aeab5-110">Customer Engagement-Anwendung</span><span class="sxs-lookup"><span data-stu-id="aeab5-110">Customer Engagement application</span></span>
--------------------------|---------------------------------
<span data-ttu-id="aeab5-111">Websites</span><span class="sxs-lookup"><span data-stu-id="aeab5-111">Sites</span></span>                     | <span data-ttu-id="aeab5-112">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="aeab5-112">msdyn_operationalsites</span></span>
<span data-ttu-id="aeab5-113">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="aeab5-113">Warehouses</span></span>                | <span data-ttu-id="aeab5-114">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="aeab5-114">warehouses</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="operational-sites"></a><span data-ttu-id="aeab5-115">Betriebsstandorte</span><span class="sxs-lookup"><span data-stu-id="aeab5-115">Operational sites</span></span>

<span data-ttu-id="aeab5-116">Die Betriebsstandorte sind in Common Data Service mithilfe der folgenden Zuordnungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aeab5-116">The operational sites are available in Common Data Service using the following mappings.</span></span>

<span data-ttu-id="aeab5-117">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="aeab5-117">Source field</span></span> | <span data-ttu-id="aeab5-118">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="aeab5-118">Map type</span></span> | <span data-ttu-id="aeab5-119">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="aeab5-119">Destination field</span></span>
---|---|---
<span data-ttu-id="aeab5-120">SITENAME</span><span class="sxs-lookup"><span data-stu-id="aeab5-120">SITENAME</span></span> | >< | <span data-ttu-id="aeab5-121">msdyn_name</span><span class="sxs-lookup"><span data-stu-id="aeab5-121">msdyn_name</span></span>
<span data-ttu-id="aeab5-122">DEFAULTFINANCIALDIMENSIONVALUE</span><span class="sxs-lookup"><span data-stu-id="aeab5-122">DEFAULTFINANCIALDIMENSIONVALUE</span></span> | >< | <span data-ttu-id="aeab5-123">msdyn_defaultfinancialdimensionvalue</span><span class="sxs-lookup"><span data-stu-id="aeab5-123">msdyn_defaultfinancialdimensionvalue</span></span>
<span data-ttu-id="aeab5-124">DEFAULTINVENTORYSTATUSID</span><span class="sxs-lookup"><span data-stu-id="aeab5-124">DEFAULTINVENTORYSTATUSID</span></span> | >< | <span data-ttu-id="aeab5-125">msdyn_defaultinventorystatusid</span><span class="sxs-lookup"><span data-stu-id="aeab5-125">msdyn_defaultinventorystatusid</span></span>
<span data-ttu-id="aeab5-126">ISRECEIVINGWAREHOUSEOVERRIDEALLOWED</span><span class="sxs-lookup"><span data-stu-id="aeab5-126">ISRECEIVINGWAREHOUSEOVERRIDEALLOWED</span></span> | >< | <span data-ttu-id="aeab5-127">msdyn_isreceivingwarehouseoverrideallowed</span><span class="sxs-lookup"><span data-stu-id="aeab5-127">msdyn_isreceivingwarehouseoverrideallowed</span></span>
<span data-ttu-id="aeab5-128">SITEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-128">SITEID</span></span> | >< | <span data-ttu-id="aeab5-129">msdyn_siteid</span><span class="sxs-lookup"><span data-stu-id="aeab5-129">msdyn_siteid</span></span>
<span data-ttu-id="aeab5-130">SITENAME</span><span class="sxs-lookup"><span data-stu-id="aeab5-130">SITENAME</span></span> | >< | <span data-ttu-id="aeab5-131">msdyn_sitename</span><span class="sxs-lookup"><span data-stu-id="aeab5-131">msdyn_sitename</span></span>
<span data-ttu-id="aeab5-132">TAXBRANCHCODE</span><span class="sxs-lookup"><span data-stu-id="aeab5-132">TAXBRANCHCODE</span></span> | >< | <span data-ttu-id="aeab5-133">msdyn_taxbranchcode</span><span class="sxs-lookup"><span data-stu-id="aeab5-133">msdyn_taxbranchcode</span></span>
<span data-ttu-id="aeab5-134">FISCALESTABLISHMENTID</span><span class="sxs-lookup"><span data-stu-id="aeab5-134">FISCALESTABLISHMENTID</span></span> | >< | <span data-ttu-id="aeab5-135">msdyn_fiscalestablishmentid</span><span class="sxs-lookup"><span data-stu-id="aeab5-135">msdyn_fiscalestablishmentid</span></span>
<span data-ttu-id="aeab5-136">ISPRIMARYADDRESSASSIGNED</span><span class="sxs-lookup"><span data-stu-id="aeab5-136">ISPRIMARYADDRESSASSIGNED</span></span> | >< | <span data-ttu-id="aeab5-137">msdyn_isprimaryaddressassigned</span><span class="sxs-lookup"><span data-stu-id="aeab5-137">msdyn_isprimaryaddressassigned</span></span>
<span data-ttu-id="aeab5-138">PRIMARYADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="aeab5-138">PRIMARYADDRESSCITY</span></span> | >< | <span data-ttu-id="aeab5-139">msdyn_primaryaddresscity</span><span class="sxs-lookup"><span data-stu-id="aeab5-139">msdyn_primaryaddresscity</span></span>
<span data-ttu-id="aeab5-140">PRIMARYADDRESSCOUNTRYREGIONID</span><span class="sxs-lookup"><span data-stu-id="aeab5-140">PRIMARYADDRESSCOUNTRYREGIONID</span></span> | >< | <span data-ttu-id="aeab5-141">msdyn_primaryaddresscountryregionid</span><span class="sxs-lookup"><span data-stu-id="aeab5-141">msdyn_primaryaddresscountryregionid</span></span>
<span data-ttu-id="aeab5-142">PRIMARYADDRESSCOUNTYID</span><span class="sxs-lookup"><span data-stu-id="aeab5-142">PRIMARYADDRESSCOUNTYID</span></span> | >< | <span data-ttu-id="aeab5-143">msdyn_primaryaddresscountyid</span><span class="sxs-lookup"><span data-stu-id="aeab5-143">msdyn_primaryaddresscountyid</span></span>
<span data-ttu-id="aeab5-144">PRIMARYADDRESSDISTRICTNAME</span><span class="sxs-lookup"><span data-stu-id="aeab5-144">PRIMARYADDRESSDISTRICTNAME</span></span> | >< | <span data-ttu-id="aeab5-145">msdyn_primaryaddressdistrictname</span><span class="sxs-lookup"><span data-stu-id="aeab5-145">msdyn_primaryaddressdistrictname</span></span>
<span data-ttu-id="aeab5-146">PRIMARYADDRESSLATITUDE</span><span class="sxs-lookup"><span data-stu-id="aeab5-146">PRIMARYADDRESSLATITUDE</span></span> | >< | <span data-ttu-id="aeab5-147">msdyn_primaryaddresslatitude</span><span class="sxs-lookup"><span data-stu-id="aeab5-147">msdyn_primaryaddresslatitude</span></span>
<span data-ttu-id="aeab5-148">PRIMARYADDRESSLOCATIONROLES</span><span class="sxs-lookup"><span data-stu-id="aeab5-148">PRIMARYADDRESSLOCATIONROLES</span></span> | >< | <span data-ttu-id="aeab5-149">msdyn_primaryaddresslocationrole</span><span class="sxs-lookup"><span data-stu-id="aeab5-149">msdyn_primaryaddresslocationrole</span></span>
<span data-ttu-id="aeab5-150">PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE</span><span class="sxs-lookup"><span data-stu-id="aeab5-150">PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE</span></span> | >< | <span data-ttu-id="aeab5-151">msdyn_primaryaddresslocationsalestaxgroupcode</span><span class="sxs-lookup"><span data-stu-id="aeab5-151">msdyn_primaryaddresslocationsalestaxgroupcode</span></span>
<span data-ttu-id="aeab5-152">PRIMARYADDRESSLONGITUDE</span><span class="sxs-lookup"><span data-stu-id="aeab5-152">PRIMARYADDRESSLONGITUDE</span></span> | >< | <span data-ttu-id="aeab5-153">msdyn_primaryaddresslongitude</span><span class="sxs-lookup"><span data-stu-id="aeab5-153">msdyn_primaryaddresslongitude</span></span>
<span data-ttu-id="aeab5-154">PRIMARYADDRESSSTATEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-154">PRIMARYADDRESSSTATEID</span></span> | >< | <span data-ttu-id="aeab5-155">msdyn_primaryaddressstateid</span><span class="sxs-lookup"><span data-stu-id="aeab5-155">msdyn_primaryaddressstateid</span></span>
<span data-ttu-id="aeab5-156">PRIMARYADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="aeab5-156">PRIMARYADDRESSSTREET</span></span> | >< | <span data-ttu-id="aeab5-157">msdyn_primaryaddressstreet</span><span class="sxs-lookup"><span data-stu-id="aeab5-157">msdyn_primaryaddressstreet</span></span>
<span data-ttu-id="aeab5-158">PRIMARYADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="aeab5-158">PRIMARYADDRESSZIPCODE</span></span> | >< | <span data-ttu-id="aeab5-159">msdyn_primaryaddresszipcode</span><span class="sxs-lookup"><span data-stu-id="aeab5-159">msdyn_primaryaddresszipcode</span></span>
<span data-ttu-id="aeab5-160">PRIMARYADDRESSBUILDINGCOMPLIMENT</span><span class="sxs-lookup"><span data-stu-id="aeab5-160">PRIMARYADDRESSBUILDINGCOMPLIMENT</span></span> | >< | <span data-ttu-id="aeab5-161">msdyn_primaryaddressbuildingcompliment</span><span class="sxs-lookup"><span data-stu-id="aeab5-161">msdyn_primaryaddressbuildingcompliment</span></span>
<span data-ttu-id="aeab5-162">PRIMARYADDRESSCITYINKANA</span><span class="sxs-lookup"><span data-stu-id="aeab5-162">PRIMARYADDRESSCITYINKANA</span></span> | >< | <span data-ttu-id="aeab5-163">msdyn_primaryaddresscityinkana</span><span class="sxs-lookup"><span data-stu-id="aeab5-163">msdyn_primaryaddresscityinkana</span></span>
<span data-ttu-id="aeab5-164">PRIMARYADDRESSSTREETINKANA</span><span class="sxs-lookup"><span data-stu-id="aeab5-164">PRIMARYADDRESSSTREETINKANA</span></span> | >< | <span data-ttu-id="aeab5-165">msdyn_primaryaddressstreetinkana</span><span class="sxs-lookup"><span data-stu-id="aeab5-165">msdyn_primaryaddressstreetinkana</span></span>
<span data-ttu-id="aeab5-166">PRIMARYADDRESSDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aeab5-166">PRIMARYADDRESSDESCRIPTION</span></span> | >< | <span data-ttu-id="aeab5-167">msdyn_primaryaddressdescription</span><span class="sxs-lookup"><span data-stu-id="aeab5-167">msdyn_primaryaddressdescription</span></span>
<span data-ttu-id="aeab5-168">FORMATTEDPRIMARYADDRESS</span><span class="sxs-lookup"><span data-stu-id="aeab5-168">FORMATTEDPRIMARYADDRESS</span></span> | >< | <span data-ttu-id="aeab5-169">msdyn_formattedprimaryaddress</span><span class="sxs-lookup"><span data-stu-id="aeab5-169">msdyn_formattedprimaryaddress</span></span>
<span data-ttu-id="aeab5-170">WILLMASTERPLANNEDINTRASITEMOVEMENTSUSETRANSFERJOURNALS</span><span class="sxs-lookup"><span data-stu-id="aeab5-170">WILLMASTERPLANNEDINTRASITEMOVEMENTSUSETRANSFERJOURNALS</span></span> | >< | <span data-ttu-id="aeab5-171">msdyn_masterplannedusestransferjournal</span><span class="sxs-lookup"><span data-stu-id="aeab5-171">msdyn_masterplannedusestransferjournal</span></span>
<span data-ttu-id="aeab5-172">PRIMARYADDRESSPOSTBOX</span><span class="sxs-lookup"><span data-stu-id="aeab5-172">PRIMARYADDRESSPOSTBOX</span></span> | >< | <span data-ttu-id="aeab5-173">msdyn_primaryaddresspostbox</span><span class="sxs-lookup"><span data-stu-id="aeab5-173">msdyn_primaryaddresspostbox</span></span>
<span data-ttu-id="aeab5-174">PRIMARYADDRESSSTREETNUMBER</span><span class="sxs-lookup"><span data-stu-id="aeab5-174">PRIMARYADDRESSSTREETNUMBER</span></span> | >< | <span data-ttu-id="aeab5-175">msdyn_primaryaddressstreetnumber</span><span class="sxs-lookup"><span data-stu-id="aeab5-175">msdyn_primaryaddressstreetnumber</span></span>


## <a name="warehouses"></a><span data-ttu-id="aeab5-176">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="aeab5-176">Warehouses</span></span>

<span data-ttu-id="aeab5-177">Die Lagerorte sind mithilfe der folgenden Zuordnungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aeab5-177">The warehouses are available using the following mappings.</span></span>

<span data-ttu-id="aeab5-178">Quellfeld</span><span class="sxs-lookup"><span data-stu-id="aeab5-178">Source field</span></span> | <span data-ttu-id="aeab5-179">Zuordnungstyp</span><span class="sxs-lookup"><span data-stu-id="aeab5-179">Map type</span></span> | <span data-ttu-id="aeab5-180">Zielfeld</span><span class="sxs-lookup"><span data-stu-id="aeab5-180">Destination field</span></span>
---|---|---
<span data-ttu-id="aeab5-181">DEFAULTCONTAINERTYPEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-181">DEFAULTCONTAINERTYPEID</span></span> | >> | <span data-ttu-id="aeab5-182">msdyn_defaultcontainertypeid</span><span class="sxs-lookup"><span data-stu-id="aeab5-182">msdyn_defaultcontainertypeid</span></span>
<span data-ttu-id="aeab5-183">AREITEMSCOVERAGEPLANNEDMANUALLY</span><span class="sxs-lookup"><span data-stu-id="aeab5-183">AREITEMSCOVERAGEPLANNEDMANUALLY</span></span> | >> | <span data-ttu-id="aeab5-184">msdyn_areitemscoverageplannedmanually</span><span class="sxs-lookup"><span data-stu-id="aeab5-184">msdyn_areitemscoverageplannedmanually</span></span>
<span data-ttu-id="aeab5-185">ARELABORSTANDARDSALLOWED</span><span class="sxs-lookup"><span data-stu-id="aeab5-185">ARELABORSTANDARDSALLOWED</span></span> | >> | <span data-ttu-id="aeab5-186">msdyn_arelaborstandardsallowed</span><span class="sxs-lookup"><span data-stu-id="aeab5-186">msdyn_arelaborstandardsallowed</span></span>
<span data-ttu-id="aeab5-187">PRIMARYADDRESSBUILDINGCOMPLIMENT</span><span class="sxs-lookup"><span data-stu-id="aeab5-187">PRIMARYADDRESSBUILDINGCOMPLIMENT</span></span> | >> | <span data-ttu-id="aeab5-188">msdyn_primaryaddressbuildingcompliment</span><span class="sxs-lookup"><span data-stu-id="aeab5-188">msdyn_primaryaddressbuildingcompliment</span></span>
<span data-ttu-id="aeab5-189">PRIMARYADDRESSPOSTBOX</span><span class="sxs-lookup"><span data-stu-id="aeab5-189">PRIMARYADDRESSPOSTBOX</span></span> | >> | <span data-ttu-id="aeab5-190">msdyn_primaryaddresspostbox</span><span class="sxs-lookup"><span data-stu-id="aeab5-190">msdyn_primaryaddresspostbox</span></span>
<span data-ttu-id="aeab5-191">PRIMARYADDRESSSTREETNUMBER</span><span class="sxs-lookup"><span data-stu-id="aeab5-191">PRIMARYADDRESSSTREETNUMBER</span></span> | >> | <span data-ttu-id="aeab5-192">msdyn_primaryaddressstreetnumber</span><span class="sxs-lookup"><span data-stu-id="aeab5-192">msdyn_primaryaddressstreetnumber</span></span>
<span data-ttu-id="aeab5-193">AREWAREHOUSELOCATIONCHECKDIGITSUNIQUE</span><span class="sxs-lookup"><span data-stu-id="aeab5-193">AREWAREHOUSELOCATIONCHECKDIGITSUNIQUE</span></span> | >> | <span data-ttu-id="aeab5-194">msdyn_arewarehouselocationcheckdigitsunique</span><span class="sxs-lookup"><span data-stu-id="aeab5-194">msdyn_arewarehouselocationcheckdigitsunique</span></span>
<span data-ttu-id="aeab5-195">INVENTORYCOUNTINGREASONCODEPOLICYNAME</span><span class="sxs-lookup"><span data-stu-id="aeab5-195">INVENTORYCOUNTINGREASONCODEPOLICYNAME</span></span> | >> | <span data-ttu-id="aeab5-196">msdyn_inventorycountingreasoncodepolicyname</span><span class="sxs-lookup"><span data-stu-id="aeab5-196">msdyn_inventorycountingreasoncodepolicyname</span></span>
<span data-ttu-id="aeab5-197">AUTOUPDATESHIPMENTRULE</span><span class="sxs-lookup"><span data-stu-id="aeab5-197">AUTOUPDATESHIPMENTRULE</span></span> | >> | <span data-ttu-id="aeab5-198">msdyn_autoupdateshipmentrule</span><span class="sxs-lookup"><span data-stu-id="aeab5-198">msdyn_autoupdateshipmentrule</span></span>
<span data-ttu-id="aeab5-199">WAREHOUSERELEASERESERVATIONREQUIREMENTRULE</span><span class="sxs-lookup"><span data-stu-id="aeab5-199">WAREHOUSERELEASERESERVATIONREQUIREMENTRULE</span></span> | >> | <span data-ttu-id="aeab5-200">msdyn_warehousereleasereservationrequirement</span><span class="sxs-lookup"><span data-stu-id="aeab5-200">msdyn_warehousereleasereservationrequirement</span></span>
<span data-ttu-id="aeab5-201">EXTERNALLYLOCATEDWAREHOUSEVENDORACCOUNTNUMBER</span><span class="sxs-lookup"><span data-stu-id="aeab5-201">EXTERNALLYLOCATEDWAREHOUSEVENDORACCOUNTNUMBER</span></span> | >> | <span data-ttu-id="aeab5-202">msdyn_externallylocatedwarehousevendoraccountnu</span><span class="sxs-lookup"><span data-stu-id="aeab5-202">msdyn_externallylocatedwarehousevendoraccountnu</span></span>
<span data-ttu-id="aeab5-203">INVENTORYSTATUSCHANGERESERVATIONREMOVALLEVEL</span><span class="sxs-lookup"><span data-stu-id="aeab5-203">INVENTORYSTATUSCHANGERESERVATIONREMOVALLEVEL</span></span> | >> | <span data-ttu-id="aeab5-204">msdyn_inventorystatuschangereservationremoval</span><span class="sxs-lookup"><span data-stu-id="aeab5-204">msdyn_inventorystatuschangereservationremoval</span></span>
<span data-ttu-id="aeab5-205">WAREHOUSEWORKPROCESSINGPOLICYNAME</span><span class="sxs-lookup"><span data-stu-id="aeab5-205">WAREHOUSEWORKPROCESSINGPOLICYNAME</span></span> | >> | <span data-ttu-id="aeab5-206">msdyn_warehouseworkprocessingpolicyname</span><span class="sxs-lookup"><span data-stu-id="aeab5-206">msdyn_warehouseworkprocessingpolicyname</span></span>
<span data-ttu-id="aeab5-207">ISFALLBACKWAREHOUSE</span><span class="sxs-lookup"><span data-stu-id="aeab5-207">ISFALLBACKWAREHOUSE</span></span> | >> | <span data-ttu-id="aeab5-208">msdyn_isfallbackwarehouse</span><span class="sxs-lookup"><span data-stu-id="aeab5-208">msdyn_isfallbackwarehouse</span></span>
<span data-ttu-id="aeab5-209">ISFINANCIALNEGATIVERETAILSTOREINVENTORYALLOWED</span><span class="sxs-lookup"><span data-stu-id="aeab5-209">ISFINANCIALNEGATIVERETAILSTOREINVENTORYALLOWED</span></span> | >> | <span data-ttu-id="aeab5-210">msdyn_financialnegativestoreinventoryallowed</span><span class="sxs-lookup"><span data-stu-id="aeab5-210">msdyn_financialnegativestoreinventoryallowed</span></span>
<span data-ttu-id="aeab5-211">ISPALLETMOVEMENTDURINGCYCLECOUNTINGALLOWED</span><span class="sxs-lookup"><span data-stu-id="aeab5-211">ISPALLETMOVEMENTDURINGCYCLECOUNTINGALLOWED</span></span> | >> | <span data-ttu-id="aeab5-212">msdyn_palletmovementduringcyclecountingallowed</span><span class="sxs-lookup"><span data-stu-id="aeab5-212">msdyn_palletmovementduringcyclecountingallowed</span></span>
<span data-ttu-id="aeab5-213">ISPHYSICALNEGATIVERETAILSTOREINVENTORYALLOWED</span><span class="sxs-lookup"><span data-stu-id="aeab5-213">ISPHYSICALNEGATIVERETAILSTOREINVENTORYALLOWED</span></span> | >> | <span data-ttu-id="aeab5-214">msdyn_physicalnegativestoreinventoryallowed</span><span class="sxs-lookup"><span data-stu-id="aeab5-214">msdyn_physicalnegativestoreinventoryallowed</span></span>
<span data-ttu-id="aeab5-215">ISREFILLEDFROMMAINWAREHOUSE</span><span class="sxs-lookup"><span data-stu-id="aeab5-215">ISREFILLEDFROMMAINWAREHOUSE</span></span> | >> | <span data-ttu-id="aeab5-216">msdyn_isrefilledfrommainwarehouse</span><span class="sxs-lookup"><span data-stu-id="aeab5-216">msdyn_isrefilledfrommainwarehouse</span></span>
<span data-ttu-id="aeab5-217">ISRETAILSTOREWAREHOUSE</span><span class="sxs-lookup"><span data-stu-id="aeab5-217">ISRETAILSTOREWAREHOUSE</span></span> | >> | <span data-ttu-id="aeab5-218">msdyn_isretailstorewarehouse</span><span class="sxs-lookup"><span data-stu-id="aeab5-218">msdyn_isretailstorewarehouse</span></span>
<span data-ttu-id="aeab5-219">MAINREFILLINGWAREHOUSEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-219">MAINREFILLINGWAREHOUSEID</span></span> | >> | <span data-ttu-id="aeab5-220">msdyn_mainrefillingwarehouseid.msdyn_warehouseid</span><span class="sxs-lookup"><span data-stu-id="aeab5-220">msdyn_mainrefillingwarehouseid.msdyn_warehouseid</span></span>
<span data-ttu-id="aeab5-221">MASTERPLANNINGWORKCALENDARDID</span><span class="sxs-lookup"><span data-stu-id="aeab5-221">MASTERPLANNINGWORKCALENDARDID</span></span> | >> | <span data-ttu-id="aeab5-222">msdyn_masterplanningworkcalendarid</span><span class="sxs-lookup"><span data-stu-id="aeab5-222">msdyn_masterplanningworkcalendarid</span></span>
<span data-ttu-id="aeab5-223">MAXIMUMBATCHPICKINGLISTQUANTITY</span><span class="sxs-lookup"><span data-stu-id="aeab5-223">MAXIMUMBATCHPICKINGLISTQUANTITY</span></span> | >> | <span data-ttu-id="aeab5-224">msdyn_maximumbatchpickinglistquantity</span><span class="sxs-lookup"><span data-stu-id="aeab5-224">msdyn_maximumbatchpickinglistquantity</span></span>
<span data-ttu-id="aeab5-225">MAXIMUMPICKINGLISTLINEQUANTITY</span><span class="sxs-lookup"><span data-stu-id="aeab5-225">MAXIMUMPICKINGLISTLINEQUANTITY</span></span> | >> | <span data-ttu-id="aeab5-226">msdyn_maximumpickinglistlinequantity</span><span class="sxs-lookup"><span data-stu-id="aeab5-226">msdyn_maximumpickinglistlinequantity</span></span>
<span data-ttu-id="aeab5-227">OPERATIONALSITEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-227">OPERATIONALSITEID</span></span> | >> | <span data-ttu-id="aeab5-228">msdyn_operationalsiteid.msdyn_siteid</span><span class="sxs-lookup"><span data-stu-id="aeab5-228">msdyn_operationalsiteid.msdyn_siteid</span></span>
<span data-ttu-id="aeab5-229">QUARANTINEWAREHOUSEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-229">QUARANTINEWAREHOUSEID</span></span> | >> | <span data-ttu-id="aeab5-230">msdyn_quarantinewarehouseid.msdyn_warehouseid</span><span class="sxs-lookup"><span data-stu-id="aeab5-230">msdyn_quarantinewarehouseid.msdyn_warehouseid</span></span>
<span data-ttu-id="aeab5-231">RETAILSTOREQUANTITYALLOCATIONREPLENISMENTRULEWEIGHT</span><span class="sxs-lookup"><span data-stu-id="aeab5-231">RETAILSTOREQUANTITYALLOCATIONREPLENISMENTRULEWEIGHT</span></span> | > | <span data-ttu-id="aeab5-232">msdyn_storeqtyallocationreplenishmentweight</span><span class="sxs-lookup"><span data-stu-id="aeab5-232">msdyn_storeqtyallocationreplenishmentweight</span></span>
<span data-ttu-id="aeab5-233">SHOULDWAREHOUSELOCATIONIDINCLUDEAISLEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-233">SHOULDWAREHOUSELOCATIONIDINCLUDEAISLEID</span></span> | >> | <span data-ttu-id="aeab5-234">msdyn_shouldwarehouselocationincludeaisleid</span><span class="sxs-lookup"><span data-stu-id="aeab5-234">msdyn_shouldwarehouselocationincludeaisleid</span></span>
<span data-ttu-id="aeab5-235">TRANSITWAREHOUSEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-235">TRANSITWAREHOUSEID</span></span> | >> | <span data-ttu-id="aeab5-236">msdyn_transitwarehouseid.msdyn_warehouseid</span><span class="sxs-lookup"><span data-stu-id="aeab5-236">msdyn_transitwarehouseid.msdyn_warehouseid</span></span>
<span data-ttu-id="aeab5-237">WAREHOUSEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-237">WAREHOUSEID</span></span> | >> | <span data-ttu-id="aeab5-238">msdyn_warehouseid</span><span class="sxs-lookup"><span data-stu-id="aeab5-238">msdyn_warehouseid</span></span>
<span data-ttu-id="aeab5-239">WAREHOUSELOCATIONIDBINIDFORMAT</span><span class="sxs-lookup"><span data-stu-id="aeab5-239">WAREHOUSELOCATIONIDBINIDFORMAT</span></span> | >> | <span data-ttu-id="aeab5-240">msdyn_warehouselocationidbinidformat</span><span class="sxs-lookup"><span data-stu-id="aeab5-240">msdyn_warehouselocationidbinidformat</span></span>
<span data-ttu-id="aeab5-241">WAREHOUSELOCATIONIDRACKIDFORMAT</span><span class="sxs-lookup"><span data-stu-id="aeab5-241">WAREHOUSELOCATIONIDRACKIDFORMAT</span></span> | >> | <span data-ttu-id="aeab5-242">msdyn_warehouselocationidrackidformat</span><span class="sxs-lookup"><span data-stu-id="aeab5-242">msdyn_warehouselocationidrackidformat</span></span>
<span data-ttu-id="aeab5-243">WAREHOUSELOCATIONIDSHELFIDFORMAT</span><span class="sxs-lookup"><span data-stu-id="aeab5-243">WAREHOUSELOCATIONIDSHELFIDFORMAT</span></span> | >> | <span data-ttu-id="aeab5-244">msdyn_warehouselocationidshelfidformat</span><span class="sxs-lookup"><span data-stu-id="aeab5-244">msdyn_warehouselocationidshelfidformat</span></span>
<span data-ttu-id="aeab5-245">WAREHOUSENAME</span><span class="sxs-lookup"><span data-stu-id="aeab5-245">WAREHOUSENAME</span></span> | >> | <span data-ttu-id="aeab5-246">msdyn_name</span><span class="sxs-lookup"><span data-stu-id="aeab5-246">msdyn_name</span></span>
<span data-ttu-id="aeab5-247">WAREHOUSENAME</span><span class="sxs-lookup"><span data-stu-id="aeab5-247">WAREHOUSENAME</span></span> | >> | <span data-ttu-id="aeab5-248">msdyn_warehousename</span><span class="sxs-lookup"><span data-stu-id="aeab5-248">msdyn_warehousename</span></span>
<span data-ttu-id="aeab5-249">WAREHOUSESPECIFICDEFAULTINVENTORYSTATUSID</span><span class="sxs-lookup"><span data-stu-id="aeab5-249">WAREHOUSESPECIFICDEFAULTINVENTORYSTATUSID</span></span> | >> | <span data-ttu-id="aeab5-250">msdyn_warehousespecificdefaultinventorystatusid</span><span class="sxs-lookup"><span data-stu-id="aeab5-250">msdyn_warehousespecificdefaultinventorystatusid</span></span>
<span data-ttu-id="aeab5-251">WAREHOUSETYPE</span><span class="sxs-lookup"><span data-stu-id="aeab5-251">WAREHOUSETYPE</span></span> | >> | <span data-ttu-id="aeab5-252">msdyn_warehousetype</span><span class="sxs-lookup"><span data-stu-id="aeab5-252">msdyn_warehousetype</span></span>
<span data-ttu-id="aeab5-253">ISPRIMARYADDRESSASSIGNED</span><span class="sxs-lookup"><span data-stu-id="aeab5-253">ISPRIMARYADDRESSASSIGNED</span></span> | >> | <span data-ttu-id="aeab5-254">msdyn_isprimaryaddressassigned</span><span class="sxs-lookup"><span data-stu-id="aeab5-254">msdyn_isprimaryaddressassigned</span></span>
<span data-ttu-id="aeab5-255">PRIMARYADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="aeab5-255">PRIMARYADDRESSCITY</span></span> | >> | <span data-ttu-id="aeab5-256">msdyn_primaryaddresscity</span><span class="sxs-lookup"><span data-stu-id="aeab5-256">msdyn_primaryaddresscity</span></span>
<span data-ttu-id="aeab5-257">PRIMARYADDRESSCOUNTRYREGIONID</span><span class="sxs-lookup"><span data-stu-id="aeab5-257">PRIMARYADDRESSCOUNTRYREGIONID</span></span> | >> | <span data-ttu-id="aeab5-258">msdyn_primaryaddresscountryregionid</span><span class="sxs-lookup"><span data-stu-id="aeab5-258">msdyn_primaryaddresscountryregionid</span></span>
<span data-ttu-id="aeab5-259">PRIMARYADDRESSCOUNTYID</span><span class="sxs-lookup"><span data-stu-id="aeab5-259">PRIMARYADDRESSCOUNTYID</span></span> | >> | <span data-ttu-id="aeab5-260">msdyn_primaryaddresscountyid</span><span class="sxs-lookup"><span data-stu-id="aeab5-260">msdyn_primaryaddresscountyid</span></span>
<span data-ttu-id="aeab5-261">PRIMARYADDRESSDISTRICTNAME</span><span class="sxs-lookup"><span data-stu-id="aeab5-261">PRIMARYADDRESSDISTRICTNAME</span></span> | >> | <span data-ttu-id="aeab5-262">msdyn_primaryaddressdistrictname</span><span class="sxs-lookup"><span data-stu-id="aeab5-262">msdyn_primaryaddressdistrictname</span></span>
<span data-ttu-id="aeab5-263">PRIMARYADDRESSLATITUDE</span><span class="sxs-lookup"><span data-stu-id="aeab5-263">PRIMARYADDRESSLATITUDE</span></span> | >> | <span data-ttu-id="aeab5-264">msdyn_primaryaddresslatitude</span><span class="sxs-lookup"><span data-stu-id="aeab5-264">msdyn_primaryaddresslatitude</span></span>
<span data-ttu-id="aeab5-265">PRIMARYADDRESSLONGITUDE</span><span class="sxs-lookup"><span data-stu-id="aeab5-265">PRIMARYADDRESSLONGITUDE</span></span> | >> | <span data-ttu-id="aeab5-266">msdyn_primaryaddresslongitude</span><span class="sxs-lookup"><span data-stu-id="aeab5-266">msdyn_primaryaddresslongitude</span></span>
<span data-ttu-id="aeab5-267">PRIMARYADDRESSLOCATIONROLES</span><span class="sxs-lookup"><span data-stu-id="aeab5-267">PRIMARYADDRESSLOCATIONROLES</span></span> | >> | <span data-ttu-id="aeab5-268">msdyn_primaryaddresslocationroles</span><span class="sxs-lookup"><span data-stu-id="aeab5-268">msdyn_primaryaddresslocationroles</span></span>
<span data-ttu-id="aeab5-269">PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE</span><span class="sxs-lookup"><span data-stu-id="aeab5-269">PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE</span></span> | >> | <span data-ttu-id="aeab5-270">msdyn_primaryaddresslocationsalestaxgroupcode</span><span class="sxs-lookup"><span data-stu-id="aeab5-270">msdyn_primaryaddresslocationsalestaxgroupcode</span></span>
<span data-ttu-id="aeab5-271">PRIMARYADDRESSSTATEID</span><span class="sxs-lookup"><span data-stu-id="aeab5-271">PRIMARYADDRESSSTATEID</span></span> | >> | <span data-ttu-id="aeab5-272">msdyn_primaryaddressstateid</span><span class="sxs-lookup"><span data-stu-id="aeab5-272">msdyn_primaryaddressstateid</span></span>
<span data-ttu-id="aeab5-273">PRIMARYADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="aeab5-273">PRIMARYADDRESSSTREET</span></span> | >> | <span data-ttu-id="aeab5-274">msdyn_primaryaddressstreet</span><span class="sxs-lookup"><span data-stu-id="aeab5-274">msdyn_primaryaddressstreet</span></span>
<span data-ttu-id="aeab5-275">PRIMARYADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="aeab5-275">PRIMARYADDRESSZIPCODE</span></span> | >> | <span data-ttu-id="aeab5-276">msdyn_primaryaddresszipcode</span><span class="sxs-lookup"><span data-stu-id="aeab5-276">msdyn_primaryaddresszipcode</span></span>
<span data-ttu-id="aeab5-277">EXTERNALLYLOCATEDWAREHOUSECUSTOMERACCOUNTNUMBER</span><span class="sxs-lookup"><span data-stu-id="aeab5-277">EXTERNALLYLOCATEDWAREHOUSECUSTOMERACCOUNTNUMBER</span></span> | >> | <span data-ttu-id="aeab5-278">msdyn_externallylocatedwarehousecustomeraccount</span><span class="sxs-lookup"><span data-stu-id="aeab5-278">msdyn_externallylocatedwarehousecustomeraccount</span></span>
<span data-ttu-id="aeab5-279">PRIMARYADDRESSCITYINKANA</span><span class="sxs-lookup"><span data-stu-id="aeab5-279">PRIMARYADDRESSCITYINKANA</span></span> | >> | <span data-ttu-id="aeab5-280">msdyn_primaryaddresscityinkana</span><span class="sxs-lookup"><span data-stu-id="aeab5-280">msdyn_primaryaddresscityinkana</span></span>
<span data-ttu-id="aeab5-281">PRIMARYADDRESSSTREETINKANA</span><span class="sxs-lookup"><span data-stu-id="aeab5-281">PRIMARYADDRESSSTREETINKANA</span></span> | >> | <span data-ttu-id="aeab5-282">msdyn_primaryaddressstreetinkana</span><span class="sxs-lookup"><span data-stu-id="aeab5-282">msdyn_primaryaddressstreetinkana</span></span>
<span data-ttu-id="aeab5-283">PRIMARYADDRESSDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aeab5-283">PRIMARYADDRESSDESCRIPTION</span></span> | >> | <span data-ttu-id="aeab5-284">msdyn_primaryaddressdescription</span><span class="sxs-lookup"><span data-stu-id="aeab5-284">msdyn_primaryaddressdescription</span></span>
<span data-ttu-id="aeab5-285">AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED</span><span class="sxs-lookup"><span data-stu-id="aeab5-285">AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED</span></span> | >> | <span data-ttu-id="aeab5-286">msdyn_uesadvancedwarehousemanagementprocesses</span><span class="sxs-lookup"><span data-stu-id="aeab5-286">msdyn_uesadvancedwarehousemanagementprocesses</span></span>
<span data-ttu-id="aeab5-287">AREPICKINGLISTSDELIVERYMODESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="aeab5-287">AREPICKINGLISTSDELIVERYMODESPECIFIC</span></span> | >> | <span data-ttu-id="aeab5-288">msdyn_arepickinglistsdeliverymodespecific</span><span class="sxs-lookup"><span data-stu-id="aeab5-288">msdyn_arepickinglistsdeliverymodespecific</span></span>
<span data-ttu-id="aeab5-289">AREPICKINGLISTSSHIPMENTSPECIFICONLY</span><span class="sxs-lookup"><span data-stu-id="aeab5-289">AREPICKINGLISTSSHIPMENTSPECIFICONLY</span></span> | >> | <span data-ttu-id="aeab5-290">msdyn_arepickinglistshipmentspecificonly</span><span class="sxs-lookup"><span data-stu-id="aeab5-290">msdyn_arepickinglistshipmentspecificonly</span></span>
<span data-ttu-id="aeab5-291">FORMATTEDPRIMARYADDRESS</span><span class="sxs-lookup"><span data-stu-id="aeab5-291">FORMATTEDPRIMARYADDRESS</span></span> | >> | <span data-ttu-id="aeab5-292">msdyn_formattedprimaryaddress</span><span class="sxs-lookup"><span data-stu-id="aeab5-292">msdyn_formattedprimaryaddress</span></span>
<span data-ttu-id="aeab5-293">ISBILLOFLADINGPRINTINGBEFORESHIPMENTCONFIRMATIONENABLED</span><span class="sxs-lookup"><span data-stu-id="aeab5-293">ISBILLOFLADINGPRINTINGBEFORESHIPMENTCONFIRMATIONENABLED</span></span> | >> | <span data-ttu-id="aeab5-294">msdyn_printbillofladingbeforeshipconfirmation</span><span class="sxs-lookup"><span data-stu-id="aeab5-294">msdyn_printbillofladingbeforeshipconfirmation</span></span>
<span data-ttu-id="aeab5-295">RAWMATERIALPICKINGINVENTORYISSUESTATUS</span><span class="sxs-lookup"><span data-stu-id="aeab5-295">RAWMATERIALPICKINGINVENTORYISSUESTATUS</span></span> | >> | <span data-ttu-id="aeab5-296">msdyn_rawmaterialpickinginventoryissuestatus</span><span class="sxs-lookup"><span data-stu-id="aeab5-296">msdyn_rawmaterialpickinginventoryissuestatus</span></span>
<span data-ttu-id="aeab5-297">WILLAUTOMATICLOADRELEASERESERVEINVENTORY</span><span class="sxs-lookup"><span data-stu-id="aeab5-297">WILLAUTOMATICLOADRELEASERESERVEINVENTORY</span></span> | >> | <span data-ttu-id="aeab5-298">msdyn_willautomaticloadreleaseinventory</span><span class="sxs-lookup"><span data-stu-id="aeab5-298">msdyn_willautomaticloadreleaseinventory</span></span>
<span data-ttu-id="aeab5-299">WILLINVENTORYSTATUSCHANGEREMOVEBLOCKING</span><span class="sxs-lookup"><span data-stu-id="aeab5-299">WILLINVENTORYSTATUSCHANGEREMOVEBLOCKING</span></span> | >> | <span data-ttu-id="aeab5-300">msdyn_willinventorystatuschangeremoveblocking</span><span class="sxs-lookup"><span data-stu-id="aeab5-300">msdyn_willinventorystatuschangeremoveblocking</span></span>
<span data-ttu-id="aeab5-301">WILLMANUALLOADRELEASERESERVEINVENTORY</span><span class="sxs-lookup"><span data-stu-id="aeab5-301">WILLMANUALLOADRELEASERESERVEINVENTORY</span></span> | >> | <span data-ttu-id="aeab5-302">msdyn_willmanualloadreleasereserveinventory</span><span class="sxs-lookup"><span data-stu-id="aeab5-302">msdyn_willmanualloadreleasereserveinventory</span></span>
<span data-ttu-id="aeab5-303">WILLORDERRELEASINGCONSOLIDATESHIPMENTS</span><span class="sxs-lookup"><span data-stu-id="aeab5-303">WILLORDERRELEASINGCONSOLIDATESHIPMENTS</span></span> | >> | <span data-ttu-id="aeab5-304">msdyn_willorderreleasingconsolidateshipments</span><span class="sxs-lookup"><span data-stu-id="aeab5-304">msdyn_willorderreleasingconsolidateshipments</span></span>
<span data-ttu-id="aeab5-305">WILLPRODUCTIONBOMSRESERVEWAREHOUSELEVELONLY</span><span class="sxs-lookup"><span data-stu-id="aeab5-305">WILLPRODUCTIONBOMSRESERVEWAREHOUSELEVELONLY</span></span> | >> | <span data-ttu-id="aeab5-306">msdyn_productionbomsreservewarehouselevel</span><span class="sxs-lookup"><span data-stu-id="aeab5-306">msdyn_productionbomsreservewarehouselevel</span></span>
<span data-ttu-id="aeab5-307">WILLSHIPPINGCANCELLATIONDECREMENTLOADQUANITY</span><span class="sxs-lookup"><span data-stu-id="aeab5-307">WILLSHIPPINGCANCELLATIONDECREMENTLOADQUANITY</span></span> | >> | <span data-ttu-id="aeab5-308">msdyn_shippingcanceldecrementloadquantity</span><span class="sxs-lookup"><span data-stu-id="aeab5-308">msdyn_shippingcanceldecrementloadquantity</span></span>
<span data-ttu-id="aeab5-309">WILLWAREHOUSELOCATIONIDINCLUDEBINIDBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="aeab5-309">WILLWAREHOUSELOCATIONIDINCLUDEBINIDBYDEFAULT</span></span> | >> | <span data-ttu-id="aeab5-310">msdyn_warehouselocationidincludeblindid</span><span class="sxs-lookup"><span data-stu-id="aeab5-310">msdyn_warehouselocationidincludeblindid</span></span>
<span data-ttu-id="aeab5-311">WILLWAREHOUSELOCATIONIDINCLUDERACKIDBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="aeab5-311">WILLWAREHOUSELOCATIONIDINCLUDERACKIDBYDEFAULT</span></span> | >> | <span data-ttu-id="aeab5-312">msdyn_warehouselocationincluderackidbydefault</span><span class="sxs-lookup"><span data-stu-id="aeab5-312">msdyn_warehouselocationincluderackidbydefault</span></span>
<span data-ttu-id="aeab5-313">WILLWAREHOUSELOCATIONIDINCLUDESHELFIDBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="aeab5-313">WILLWAREHOUSELOCATIONIDINCLUDESHELFIDBYDEFAULT</span></span> | >> | <span data-ttu-id="aeab5-314">msdyn_warehouselocationidincludeshelfid</span><span class="sxs-lookup"><span data-stu-id="aeab5-314">msdyn_warehouselocationidincludeshelfid</span></span>