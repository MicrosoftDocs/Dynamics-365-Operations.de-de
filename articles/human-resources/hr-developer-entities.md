---
title: Dataverse-Tabellen
description: Microsoft Dynamics 365 Human Resources verwendet Dataverse, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054355"
---
# <a name="dataverse-tables"></a><span data-ttu-id="7d8e2-103">Dataverse-Tabellen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7d8e2-104">Microsoft Dynamics 365 Human Resources verwendet Dataverse, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="7d8e2-105">Human Resources-Entitäten entsprechen Dataverse-Tabellen.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="7d8e2-106">Weitere Informationen zu Dataverse (früher Common Data Service) und Terminologie-Updates finden Sie unter [Was ist Microsoft Dataverse ?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="7d8e2-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="7d8e2-107">Die folgenden Dataverse-Tabellen sind basierend auf Human Resources-Entitäten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="7d8e2-108">Vorteilstabellen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-108">Benefit tables</span></span>

| <span data-ttu-id="7d8e2-109">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-109">Name</span></span> | <span data-ttu-id="7d8e2-110">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-111">Vorteilsberechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="7d8e2-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="7d8e2-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="7d8e2-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="7d8e2-113">Berechnungshäufigkeit Lohnperiode für Vergütungen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="7d8e2-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="7d8e2-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="7d8e2-115">Vergütungsberechnungssatz</span><span class="sxs-lookup"><span data-stu-id="7d8e2-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="7d8e2-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="7d8e2-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="7d8e2-117">Vergütungsberechnungssatz-Detail</span><span class="sxs-lookup"><span data-stu-id="7d8e2-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="7d8e2-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="7d8e2-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="7d8e2-119">Vergütungsoption</span><span class="sxs-lookup"><span data-stu-id="7d8e2-119">Benefit Option</span></span> | <span data-ttu-id="7d8e2-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="7d8e2-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="7d8e2-121">Vergütungsplan</span><span class="sxs-lookup"><span data-stu-id="7d8e2-121">Benefit Plan</span></span> | <span data-ttu-id="7d8e2-122">cdm_benefitplan (Nicht aktiviert für benutzerdefinierte Feldunterstützung)</span><span class="sxs-lookup"><span data-stu-id="7d8e2-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="7d8e2-123">Vergütungstyp</span><span class="sxs-lookup"><span data-stu-id="7d8e2-123">Benefit Type</span></span> | <span data-ttu-id="7d8e2-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="7d8e2-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="7d8e2-125">Tabellen von Geschäftsprozessaufgaben</span><span class="sxs-lookup"><span data-stu-id="7d8e2-125">Business process tasks tables</span></span>

| <span data-ttu-id="7d8e2-126">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-126">Name</span></span> | <span data-ttu-id="7d8e2-127">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-128">Geschäftsprozesskalender</span><span class="sxs-lookup"><span data-stu-id="7d8e2-128">Business Process Calendar</span></span> | <span data-ttu-id="7d8e2-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="7d8e2-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="7d8e2-130">Zuweisung der Geschäftsprozessgruppe</span><span class="sxs-lookup"><span data-stu-id="7d8e2-130">Business Process Group Assignment</span></span> | <span data-ttu-id="7d8e2-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="7d8e2-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="7d8e2-132">Geschäftsprozessbibliothek-Aufgabengruppe</span><span class="sxs-lookup"><span data-stu-id="7d8e2-132">Business Process Library Task Group</span></span> | <span data-ttu-id="7d8e2-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="7d8e2-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="7d8e2-134">Geschäftsprozessphase</span><span class="sxs-lookup"><span data-stu-id="7d8e2-134">Business Process Stage</span></span> | <span data-ttu-id="7d8e2-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="7d8e2-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="7d8e2-136">Kopfzeile der Prüflistenvorlage</span><span class="sxs-lookup"><span data-stu-id="7d8e2-136">Checklist Template Header</span></span> | <span data-ttu-id="7d8e2-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="7d8e2-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="7d8e2-138">Prüflistenvorlagen-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7d8e2-138">Checklist Template Task</span></span> | <span data-ttu-id="7d8e2-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="7d8e2-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="7d8e2-140">Vergütungstabellen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-140">Compensation tables</span></span>

| <span data-ttu-id="7d8e2-141">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-141">Name</span></span> | <span data-ttu-id="7d8e2-142">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-143">Plan mit fester Vergütung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="7d8e2-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="7d8e2-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="7d8e2-145">Vergütungsraster</span><span class="sxs-lookup"><span data-stu-id="7d8e2-145">Compensation Grid</span></span> | <span data-ttu-id="7d8e2-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="7d8e2-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="7d8e2-147">Vergütungsstufe</span><span class="sxs-lookup"><span data-stu-id="7d8e2-147">Compensation Level</span></span> | <span data-ttu-id="7d8e2-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="7d8e2-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="7d8e2-149">Häufigkeit der Vergütungszahlung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="7d8e2-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="7d8e2-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="7d8e2-151">Vergütungsreferenzpunkten einrichten</span><span class="sxs-lookup"><span data-stu-id="7d8e2-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="7d8e2-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="7d8e2-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="7d8e2-153">Vergütungsreferenzpunktzeile einrichten</span><span class="sxs-lookup"><span data-stu-id="7d8e2-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="7d8e2-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="7d8e2-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="7d8e2-155">Vergütungsregion</span><span class="sxs-lookup"><span data-stu-id="7d8e2-155">Compensation Region</span></span> | <span data-ttu-id="7d8e2-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="7d8e2-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="7d8e2-157">Vergütungsstruktur</span><span class="sxs-lookup"><span data-stu-id="7d8e2-157">Compensation Structure</span></span> | <span data-ttu-id="7d8e2-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="7d8e2-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="7d8e2-159">Variabler Plan für Vergütung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-159">Compensation Variable Plan</span></span> | <span data-ttu-id="7d8e2-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="7d8e2-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="7d8e2-161">Variable Planstufe für Vergütung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="7d8e2-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="7d8e2-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="7d8e2-163">Plantyp für variable Vergütung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="7d8e2-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="7d8e2-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="7d8e2-165">Ereignis für feste Vergütung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-165">Fixed Compensation Event</span></span> | <span data-ttu-id="7d8e2-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="7d8e2-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="7d8e2-167">Übertragungsregel</span><span class="sxs-lookup"><span data-stu-id="7d8e2-167">Vesting Rule</span></span> | <span data-ttu-id="7d8e2-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="7d8e2-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="7d8e2-169">Feste Arbeitskraftvergütung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="7d8e2-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="7d8e2-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="7d8e2-171">Organisationstabellen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-171">Organization tables</span></span>

| <span data-ttu-id="7d8e2-172">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-172">Name</span></span> | <span data-ttu-id="7d8e2-173">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-174">Abteilung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-174">Department</span></span> | <span data-ttu-id="7d8e2-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="7d8e2-175">cdm_department</span></span> |
| <span data-ttu-id="7d8e2-176">Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-176">Employment</span></span> | <span data-ttu-id="7d8e2-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="7d8e2-177">cdm_employment</span></span> |
| <span data-ttu-id="7d8e2-178">Firma</span><span class="sxs-lookup"><span data-stu-id="7d8e2-178">Company</span></span> | <span data-ttu-id="7d8e2-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="7d8e2-179">cdm_company</span></span> |
| <span data-ttu-id="7d8e2-180">Auftrag</span><span class="sxs-lookup"><span data-stu-id="7d8e2-180">Job</span></span> | <span data-ttu-id="7d8e2-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="7d8e2-181">cdm_job</span></span> |
| <span data-ttu-id="7d8e2-182">Stellenfunktion</span><span class="sxs-lookup"><span data-stu-id="7d8e2-182">Job Function</span></span> | <span data-ttu-id="7d8e2-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="7d8e2-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="7d8e2-184">Position</span><span class="sxs-lookup"><span data-stu-id="7d8e2-184">Job Position</span></span> | <span data-ttu-id="7d8e2-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="7d8e2-185">cdm_jobposition</span></span> |
| <span data-ttu-id="7d8e2-186">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="7d8e2-186">Position Type</span></span> | <span data-ttu-id="7d8e2-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="7d8e2-187">cdm_positiontype</span></span> |
| <span data-ttu-id="7d8e2-188">Arbeitskraftzuweisung für die Position</span><span class="sxs-lookup"><span data-stu-id="7d8e2-188">Position Worker Assignment</span></span> | <span data-ttu-id="7d8e2-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="7d8e2-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="7d8e2-190">Positionsdimension</span><span class="sxs-lookup"><span data-stu-id="7d8e2-190">Job Position Dimension</span></span> | <span data-ttu-id="7d8e2-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="7d8e2-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="7d8e2-192">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="7d8e2-192">Job Type</span></span> | <span data-ttu-id="7d8e2-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="7d8e2-193">cdm_jobtype</span></span> |
| <span data-ttu-id="7d8e2-194">Sprache</span><span class="sxs-lookup"><span data-stu-id="7d8e2-194">Language</span></span> | <span data-ttu-id="7d8e2-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="7d8e2-195">cdm_language</span></span> |
| <span data-ttu-id="7d8e2-196">Titel</span><span class="sxs-lookup"><span data-stu-id="7d8e2-196">Title</span></span> | <span data-ttu-id="7d8e2-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="7d8e2-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="7d8e2-198">Finanzielle Dimensionen für **Positionstyp**, **Arbeitskraftzuweisung für die Position**, und **Beschäftigung** bieten eine einseitige Integration in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="7d8e2-199">Aktualisierungen der Finanzdimensionen werden derzeit nicht synchronisiert von Dataverse zu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d8e2-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="7d8e2-200">Tabelle „Urlaub und Abwesenheit“</span><span class="sxs-lookup"><span data-stu-id="7d8e2-200">Leave and absence tables</span></span>

| <span data-ttu-id="7d8e2-201">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-201">Name</span></span> | <span data-ttu-id="7d8e2-202">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-203">Urlaubsbankbuchung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-203">Leave Bank Transaction</span></span> | <span data-ttu-id="7d8e2-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="7d8e2-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="7d8e2-205">Urlaubsregistrierung</span><span class="sxs-lookup"><span data-stu-id="7d8e2-205">Leave Enrollment</span></span> | <span data-ttu-id="7d8e2-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="7d8e2-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="7d8e2-207">Urlaubsplan</span><span class="sxs-lookup"><span data-stu-id="7d8e2-207">Leave Plan</span></span> | <span data-ttu-id="7d8e2-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="7d8e2-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="7d8e2-209">Urlaubsantrag</span><span class="sxs-lookup"><span data-stu-id="7d8e2-209">Leave Request</span></span> | <span data-ttu-id="7d8e2-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="7d8e2-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="7d8e2-211">Urlaubsantragdetail</span><span class="sxs-lookup"><span data-stu-id="7d8e2-211">Leave Request Detail</span></span> | <span data-ttu-id="7d8e2-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="7d8e2-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="7d8e2-213">Urlaubstyp</span><span class="sxs-lookup"><span data-stu-id="7d8e2-213">Leave Type</span></span> | <span data-ttu-id="7d8e2-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="7d8e2-214">cdm_leavetype</span></span> |
| <span data-ttu-id="7d8e2-215">Ursachencode für Abwesenheitstyp</span><span class="sxs-lookup"><span data-stu-id="7d8e2-215">Leave Type Reason Code</span></span> | <span data-ttu-id="7d8e2-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="7d8e2-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="7d8e2-217">Lohntabellen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-217">Payroll tables</span></span>

| <span data-ttu-id="7d8e2-218">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-218">Name</span></span> | <span data-ttu-id="7d8e2-219">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-220">Lohnzyklus</span><span class="sxs-lookup"><span data-stu-id="7d8e2-220">Pay Cycle</span></span> | <span data-ttu-id="7d8e2-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-221">cdm_paycycle</span></span> |
| <span data-ttu-id="7d8e2-222">Lohnperiode</span><span class="sxs-lookup"><span data-stu-id="7d8e2-222">Pay Period</span></span> | <span data-ttu-id="7d8e2-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="7d8e2-223">cdm_payperiod</span></span> |
| <span data-ttu-id="7d8e2-224">Lohneinkommenscode</span><span class="sxs-lookup"><span data-stu-id="7d8e2-224">Payroll Earning Code</span></span> | <span data-ttu-id="7d8e2-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="7d8e2-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="7d8e2-226">Bankkontoauszahlungen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-226">Bank Account Disbursement</span></span> | <span data-ttu-id="7d8e2-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="7d8e2-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="7d8e2-228">Steuerregion</span><span class="sxs-lookup"><span data-stu-id="7d8e2-228">Tax Region</span></span> | <span data-ttu-id="7d8e2-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="7d8e2-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="7d8e2-230">Arbeitskräftetabellen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-230">Worker tables</span></span>

| <span data-ttu-id="7d8e2-231">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-231">Name</span></span> | <span data-ttu-id="7d8e2-232">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-233">Worker</span><span class="sxs-lookup"><span data-stu-id="7d8e2-233">Worker</span></span> | <span data-ttu-id="7d8e2-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="7d8e2-234">cdm_worker</span></span> |
| <span data-ttu-id="7d8e2-235">Arbeitskraftadresse</span><span class="sxs-lookup"><span data-stu-id="7d8e2-235">Worker Address</span></span> | <span data-ttu-id="7d8e2-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="7d8e2-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="7d8e2-237">Persönliches Detail der Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="7d8e2-237">Worker Personal Detail</span></span> | <span data-ttu-id="7d8e2-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="7d8e2-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="7d8e2-239">Personenidentifikationsnummer Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="7d8e2-239">Worker Person Identification Number</span></span> | <span data-ttu-id="7d8e2-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="7d8e2-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="7d8e2-241">Personenidentifikationstyp Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="7d8e2-241">Worker Person Identification Type</span></span> | <span data-ttu-id="7d8e2-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="7d8e2-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="7d8e2-243">Arbeitskalender</span><span class="sxs-lookup"><span data-stu-id="7d8e2-243">Work Calendar</span></span> | <span data-ttu-id="7d8e2-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="7d8e2-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="7d8e2-245">Arbeitskalendertag</span><span class="sxs-lookup"><span data-stu-id="7d8e2-245">Work Calendar Day</span></span> | <span data-ttu-id="7d8e2-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="7d8e2-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="7d8e2-247">Arbeitskalenderurlaub</span><span class="sxs-lookup"><span data-stu-id="7d8e2-247">Work Calendar Holiday</span></span> |<span data-ttu-id="7d8e2-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="7d8e2-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="7d8e2-249">Arbeitskalender-Datumsposition</span><span class="sxs-lookup"><span data-stu-id="7d8e2-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="7d8e2-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="7d8e2-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="7d8e2-251">Arbeitskalender-Zeitintervall</span><span class="sxs-lookup"><span data-stu-id="7d8e2-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="7d8e2-252">cdm_workcalendartimeinterval (Nicht aktiviert für benutzerdefinierte Feldunterstützung)</span><span class="sxs-lookup"><span data-stu-id="7d8e2-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="7d8e2-253">Arbeitskraftbankkonto</span><span class="sxs-lookup"><span data-stu-id="7d8e2-253">Worker Bank Account</span></span> | <span data-ttu-id="7d8e2-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="7d8e2-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="7d8e2-255">Arbeitskräfteeinrichtungstabellen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-255">Worker setup tables</span></span>

| <span data-ttu-id="7d8e2-256">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-256">Name</span></span> | <span data-ttu-id="7d8e2-257">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-258">Veteranenstatus</span><span class="sxs-lookup"><span data-stu-id="7d8e2-258">Veteran Status</span></span> | <span data-ttu-id="7d8e2-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="7d8e2-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="7d8e2-260">Nationalität</span><span class="sxs-lookup"><span data-stu-id="7d8e2-260">Ethnic Origin</span></span> | <span data-ttu-id="7d8e2-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="7d8e2-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="7d8e2-262">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="7d8e2-262">Reason Code</span></span> | <span data-ttu-id="7d8e2-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="7d8e2-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="7d8e2-264">Ausstellende Behörde für Personenkennungen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="7d8e2-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="7d8e2-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="7d8e2-266">Kompetenztabellen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-266">Competency tables</span></span>

| <span data-ttu-id="7d8e2-267">Name</span><span class="sxs-lookup"><span data-stu-id="7d8e2-267">Name</span></span> | <span data-ttu-id="7d8e2-268">Tabelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="7d8e2-269">Qualifikationstyp</span><span class="sxs-lookup"><span data-stu-id="7d8e2-269">Skill Type</span></span> | <span data-ttu-id="7d8e2-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="7d8e2-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="7d8e2-271">Tabellenbeziehungsmodelle</span><span class="sxs-lookup"><span data-stu-id="7d8e2-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="7d8e2-272">Worker</span><span class="sxs-lookup"><span data-stu-id="7d8e2-272">Worker</span></span>

![Worker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="7d8e2-274">Stelle und Stellenposition</span><span class="sxs-lookup"><span data-stu-id="7d8e2-274">Job and Job Position</span></span>

![Stelle und Stellenposition](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="7d8e2-276">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-276">Benefits</span></span>

![Vergütungen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="7d8e2-278">Kompensation</span><span class="sxs-lookup"><span data-stu-id="7d8e2-278">Compensation</span></span>

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="7d8e2-280">Verlasen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-280">Leave</span></span>

![Verlasen](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="7d8e2-282">Arbeitskalender</span><span class="sxs-lookup"><span data-stu-id="7d8e2-282">Work Calendar</span></span>

![Arbeitskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="7d8e2-284">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d8e2-284">See also</span></span>

[<span data-ttu-id="7d8e2-285">Eine Datenintegrationstechnologie auswählen</span><span class="sxs-lookup"><span data-stu-id="7d8e2-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="7d8e2-286">Dataverse-Integration konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7d8e2-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="7d8e2-287">Virtuelle Dataverse-Tabellen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7d8e2-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="7d8e2-288">FAQ zu virtuellen Tabellen für Human Resources</span><span class="sxs-lookup"><span data-stu-id="7d8e2-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="7d8e2-289">Was ist Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="7d8e2-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="7d8e2-290">Terminologie-Updates</span><span class="sxs-lookup"><span data-stu-id="7d8e2-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]