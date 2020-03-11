---
title: Common Data Service-Entitäten
description: Microsoft Dynamics 365 Human Resources verwendet Common Data Service, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087345"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="bd097-103">Common Data Service-Entitäten</span><span class="sxs-lookup"><span data-stu-id="bd097-103">Common Data Service entities</span></span>

<span data-ttu-id="bd097-104">Microsoft Dynamics 365 Human Resources verwendet Common Data Service, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bd097-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="bd097-105">Weitere Informationen zu Common Data Service finden Sie unter [Was ist Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="bd097-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="bd097-106">Die folgenden Human Resources-Entitäten sind in Common Data Service verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bd097-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="bd097-107">Vorteilsentitäten</span><span class="sxs-lookup"><span data-stu-id="bd097-107">Benefit entities</span></span>

| <span data-ttu-id="bd097-108">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-108">Name</span></span> | <span data-ttu-id="bd097-109">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-110">Vorteilsberechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="bd097-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="bd097-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="bd097-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="bd097-112">Berechnungshäufigkeit Lohnperiode für Vergütungen</span><span class="sxs-lookup"><span data-stu-id="bd097-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="bd097-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="bd097-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="bd097-114">Vergütungsberechnungssatz</span><span class="sxs-lookup"><span data-stu-id="bd097-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="bd097-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="bd097-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="bd097-116">Vergütungsberechnungssatz-Detail</span><span class="sxs-lookup"><span data-stu-id="bd097-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="bd097-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="bd097-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="bd097-118">Vergütungsoption</span><span class="sxs-lookup"><span data-stu-id="bd097-118">Benefit Option</span></span> | <span data-ttu-id="bd097-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="bd097-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="bd097-120">Vergütungsplan</span><span class="sxs-lookup"><span data-stu-id="bd097-120">Benefit Plan</span></span> | <span data-ttu-id="bd097-121">cdm_benefitplan (Nicht aktiviert für benutzerdefinierte Feldunterstützung)</span><span class="sxs-lookup"><span data-stu-id="bd097-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="bd097-122">Vergütungstyp</span><span class="sxs-lookup"><span data-stu-id="bd097-122">Benefit Type</span></span> | <span data-ttu-id="bd097-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="bd097-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="bd097-124">Entitäten von Geschäftsprozessaufgaben</span><span class="sxs-lookup"><span data-stu-id="bd097-124">Business process tasks entities</span></span>

| <span data-ttu-id="bd097-125">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-125">Name</span></span> | <span data-ttu-id="bd097-126">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-127">Geschäftsprozesskalender</span><span class="sxs-lookup"><span data-stu-id="bd097-127">Business Process Calendar</span></span> | <span data-ttu-id="bd097-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="bd097-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="bd097-129">Zuweisung der Geschäftsprozessgruppe</span><span class="sxs-lookup"><span data-stu-id="bd097-129">Business Process Group Assignment</span></span> | <span data-ttu-id="bd097-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="bd097-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="bd097-131">Geschäftsprozessbibliothek-Aufgabengruppe</span><span class="sxs-lookup"><span data-stu-id="bd097-131">Business Process Library Task Group</span></span> | <span data-ttu-id="bd097-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="bd097-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="bd097-133">Geschäftsprozessphase</span><span class="sxs-lookup"><span data-stu-id="bd097-133">Business Process Stage</span></span> | <span data-ttu-id="bd097-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="bd097-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="bd097-135">Kopfzeile der Prüflistenvorlage</span><span class="sxs-lookup"><span data-stu-id="bd097-135">Checklist Template Header</span></span> | <span data-ttu-id="bd097-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="bd097-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="bd097-137">Prüflistenvorlagen-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="bd097-137">Checklist Template Task</span></span> | <span data-ttu-id="bd097-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="bd097-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="bd097-139">Entschädigungseinheiten</span><span class="sxs-lookup"><span data-stu-id="bd097-139">Compensation entities</span></span>

| <span data-ttu-id="bd097-140">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-140">Name</span></span> | <span data-ttu-id="bd097-141">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-142">Plan mit fester Vergütung</span><span class="sxs-lookup"><span data-stu-id="bd097-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="bd097-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="bd097-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="bd097-144">Vergütungsraster</span><span class="sxs-lookup"><span data-stu-id="bd097-144">Compensation Grid</span></span> | <span data-ttu-id="bd097-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="bd097-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="bd097-146">Vergütungsstufe</span><span class="sxs-lookup"><span data-stu-id="bd097-146">Compensation Level</span></span> | <span data-ttu-id="bd097-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="bd097-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="bd097-148">Häufigkeit der Vergütungszahlung</span><span class="sxs-lookup"><span data-stu-id="bd097-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="bd097-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="bd097-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="bd097-150">Vergütungsreferenzpunkten einrichten</span><span class="sxs-lookup"><span data-stu-id="bd097-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="bd097-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="bd097-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="bd097-152">Vergütungsreferenzpunktzeile einrichten</span><span class="sxs-lookup"><span data-stu-id="bd097-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="bd097-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="bd097-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="bd097-154">Vergütungsregion</span><span class="sxs-lookup"><span data-stu-id="bd097-154">Compensation Region</span></span> | <span data-ttu-id="bd097-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="bd097-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="bd097-156">Vergütungsstruktur</span><span class="sxs-lookup"><span data-stu-id="bd097-156">Compensation Structure</span></span> | <span data-ttu-id="bd097-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="bd097-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="bd097-158">Variabler Plan für Vergütung</span><span class="sxs-lookup"><span data-stu-id="bd097-158">Compensation Variable Plan</span></span> | <span data-ttu-id="bd097-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="bd097-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="bd097-160">Variable Planstufe für Vergütung</span><span class="sxs-lookup"><span data-stu-id="bd097-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="bd097-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="bd097-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="bd097-162">Plantyp für variable Vergütung</span><span class="sxs-lookup"><span data-stu-id="bd097-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="bd097-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="bd097-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="bd097-164">Ereignis für feste Vergütung</span><span class="sxs-lookup"><span data-stu-id="bd097-164">Fixed Compensation Event</span></span> | <span data-ttu-id="bd097-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="bd097-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="bd097-166">Übertragungsregel</span><span class="sxs-lookup"><span data-stu-id="bd097-166">Vesting Rule</span></span> | <span data-ttu-id="bd097-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="bd097-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="bd097-168">Feste Vergütung für Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="bd097-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="bd097-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="bd097-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="bd097-170">Organisationsentitäten</span><span class="sxs-lookup"><span data-stu-id="bd097-170">Organization entities</span></span>

| <span data-ttu-id="bd097-171">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-171">Name</span></span> | <span data-ttu-id="bd097-172">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-173">Abteilung</span><span class="sxs-lookup"><span data-stu-id="bd097-173">Department</span></span> | <span data-ttu-id="bd097-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="bd097-174">cdm_department</span></span> |
| <span data-ttu-id="bd097-175">Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="bd097-175">Employment</span></span> | <span data-ttu-id="bd097-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="bd097-176">cdm_employment</span></span> |
| <span data-ttu-id="bd097-177">Firma</span><span class="sxs-lookup"><span data-stu-id="bd097-177">Company</span></span> | <span data-ttu-id="bd097-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="bd097-178">cdm_company</span></span> |
| <span data-ttu-id="bd097-179">Auftrag</span><span class="sxs-lookup"><span data-stu-id="bd097-179">Job</span></span> | <span data-ttu-id="bd097-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="bd097-180">cdm_job</span></span> |
| <span data-ttu-id="bd097-181">Stellenfunktion</span><span class="sxs-lookup"><span data-stu-id="bd097-181">Job Function</span></span> | <span data-ttu-id="bd097-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="bd097-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="bd097-183">Position</span><span class="sxs-lookup"><span data-stu-id="bd097-183">Job Position</span></span> | <span data-ttu-id="bd097-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="bd097-184">cdm_jobposition</span></span> |
| <span data-ttu-id="bd097-185">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="bd097-185">Position Type</span></span> | <span data-ttu-id="bd097-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="bd097-186">cdm_positiontype</span></span> |
| <span data-ttu-id="bd097-187">Arbeitskraftzuweisung für die Position</span><span class="sxs-lookup"><span data-stu-id="bd097-187">Position Worker Assignment</span></span> | <span data-ttu-id="bd097-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="bd097-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="bd097-189">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="bd097-189">Job Type</span></span> | <span data-ttu-id="bd097-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="bd097-190">cdm_jobtype</span></span> |
| <span data-ttu-id="bd097-191">Sprache</span><span class="sxs-lookup"><span data-stu-id="bd097-191">Language</span></span> | <span data-ttu-id="bd097-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="bd097-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="bd097-193">Urlaubs- und Abwesenheitsentitäten</span><span class="sxs-lookup"><span data-stu-id="bd097-193">Leave and absence entities</span></span>

| <span data-ttu-id="bd097-194">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-194">Name</span></span> | <span data-ttu-id="bd097-195">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-196">Bankgeschäft verlassen</span><span class="sxs-lookup"><span data-stu-id="bd097-196">Leave Bank Transaction</span></span> | <span data-ttu-id="bd097-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="bd097-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="bd097-198">Urlaubsregistrierung</span><span class="sxs-lookup"><span data-stu-id="bd097-198">Leave Enrollment</span></span> | <span data-ttu-id="bd097-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="bd097-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="bd097-200">Urlaubsplan</span><span class="sxs-lookup"><span data-stu-id="bd097-200">Leave Plan</span></span> | <span data-ttu-id="bd097-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="bd097-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="bd097-202">Urlaubsantrag</span><span class="sxs-lookup"><span data-stu-id="bd097-202">Leave Request</span></span> | <span data-ttu-id="bd097-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="bd097-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="bd097-204">Urlaubsantragdetail</span><span class="sxs-lookup"><span data-stu-id="bd097-204">Leave Request Detail</span></span> | <span data-ttu-id="bd097-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="bd097-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="bd097-206">Urlaubstyp</span><span class="sxs-lookup"><span data-stu-id="bd097-206">Leave Type</span></span> | <span data-ttu-id="bd097-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="bd097-207">cdm_leavetype</span></span> |
| <span data-ttu-id="bd097-208">Ursachencode für Abwesenheitstyp</span><span class="sxs-lookup"><span data-stu-id="bd097-208">Leave Type Reason Code</span></span> | <span data-ttu-id="bd097-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="bd097-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="bd097-210">Lohnentitäten</span><span class="sxs-lookup"><span data-stu-id="bd097-210">Payroll entities</span></span>

| <span data-ttu-id="bd097-211">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-211">Name</span></span> | <span data-ttu-id="bd097-212">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-213">Zahlungszyklus</span><span class="sxs-lookup"><span data-stu-id="bd097-213">Pay Cycle</span></span> | <span data-ttu-id="bd097-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="bd097-214">cdm_paycycle</span></span> |
| <span data-ttu-id="bd097-215">Lohnperiode</span><span class="sxs-lookup"><span data-stu-id="bd097-215">Pay Period</span></span> | <span data-ttu-id="bd097-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="bd097-216">cdm_payperiod</span></span> |
| <span data-ttu-id="bd097-217">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="bd097-217">Payroll Earning Code</span></span> | <span data-ttu-id="bd097-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="bd097-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="bd097-219">Bankkontoauszahlungen</span><span class="sxs-lookup"><span data-stu-id="bd097-219">Bank Account Disbursement</span></span> | <span data-ttu-id="bd097-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="bd097-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="bd097-221">Steuerregion</span><span class="sxs-lookup"><span data-stu-id="bd097-221">Tax Region</span></span> | <span data-ttu-id="bd097-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="bd097-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="bd097-223">Arbeitskraftentitäten</span><span class="sxs-lookup"><span data-stu-id="bd097-223">Worker entities</span></span>

| <span data-ttu-id="bd097-224">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-224">Name</span></span> | <span data-ttu-id="bd097-225">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-226">Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="bd097-226">Worker</span></span> | <span data-ttu-id="bd097-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="bd097-227">cdm_worker</span></span> |
| <span data-ttu-id="bd097-228">Adresse Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="bd097-228">Worker Address</span></span> | <span data-ttu-id="bd097-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="bd097-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="bd097-230">Persönliches Detail der Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="bd097-230">Worker Personal Detail</span></span> | <span data-ttu-id="bd097-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="bd097-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="bd097-232">Personenidentifikationsnummer Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="bd097-232">Worker Person Identification Number</span></span> | <span data-ttu-id="bd097-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="bd097-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="bd097-234">Personenidentifikationstyp Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="bd097-234">Worker Person Identification Type</span></span> | <span data-ttu-id="bd097-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="bd097-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="bd097-236">Arbeitskalender</span><span class="sxs-lookup"><span data-stu-id="bd097-236">Work Calendar</span></span> | <span data-ttu-id="bd097-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="bd097-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="bd097-238">Arbeitskalendertag</span><span class="sxs-lookup"><span data-stu-id="bd097-238">Work Calendar Day</span></span> | <span data-ttu-id="bd097-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="bd097-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="bd097-240">Arbeitskalenderurlaub</span><span class="sxs-lookup"><span data-stu-id="bd097-240">Work Calendar Holiday</span></span> |<span data-ttu-id="bd097-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="bd097-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="bd097-242">Arbeitskalender-Datumsposition</span><span class="sxs-lookup"><span data-stu-id="bd097-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="bd097-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="bd097-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="bd097-244">Arbeitskalender-Zeitintervall</span><span class="sxs-lookup"><span data-stu-id="bd097-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="bd097-245">cdm_workcalendartimeinterval (Nicht aktiviert für benutzerdefinierte Feldunterstützung)</span><span class="sxs-lookup"><span data-stu-id="bd097-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="bd097-246">Arbeitskraftbankkonto</span><span class="sxs-lookup"><span data-stu-id="bd097-246">Worker Bank Account</span></span> | <span data-ttu-id="bd097-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="bd097-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="bd097-248">Arbeiter-Einrichtungseinheiten</span><span class="sxs-lookup"><span data-stu-id="bd097-248">Worker setup entities</span></span>

| <span data-ttu-id="bd097-249">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-249">Name</span></span> | <span data-ttu-id="bd097-250">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-251">Veteranenstatus</span><span class="sxs-lookup"><span data-stu-id="bd097-251">Veteran Status</span></span> | <span data-ttu-id="bd097-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="bd097-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="bd097-253">Nationalität</span><span class="sxs-lookup"><span data-stu-id="bd097-253">Ethnic Origin</span></span> | <span data-ttu-id="bd097-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="bd097-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="bd097-255">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="bd097-255">Reason Code</span></span> | <span data-ttu-id="bd097-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="bd097-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="bd097-257">Ausstellende Agentur für Personenidentifikation</span><span class="sxs-lookup"><span data-stu-id="bd097-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="bd097-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="bd097-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="bd097-259">Zuständigkeitseinheiten</span><span class="sxs-lookup"><span data-stu-id="bd097-259">Competency entities</span></span>

| <span data-ttu-id="bd097-260">Name</span><span class="sxs-lookup"><span data-stu-id="bd097-260">Name</span></span> | <span data-ttu-id="bd097-261">Entität</span><span class="sxs-lookup"><span data-stu-id="bd097-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="bd097-262">Qualifikationstyp</span><span class="sxs-lookup"><span data-stu-id="bd097-262">Skill Type</span></span> | <span data-ttu-id="bd097-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="bd097-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="bd097-264">Entitätsbeziehungsmodelle</span><span class="sxs-lookup"><span data-stu-id="bd097-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="bd097-265">Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="bd097-265">Worker</span></span>

![Arbeitskraft](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="bd097-267">Stelle und Stellenposition</span><span class="sxs-lookup"><span data-stu-id="bd097-267">Job and Job Position</span></span>

![Stelle und Stellenposition](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="bd097-269">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="bd097-269">Benefits</span></span>

![Vergütungen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="bd097-271">Kompensation</span><span class="sxs-lookup"><span data-stu-id="bd097-271">Compensation</span></span>

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="bd097-273">Verlasen</span><span class="sxs-lookup"><span data-stu-id="bd097-273">Leave</span></span>

![Verlasen](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="bd097-275">Arbeitskalender</span><span class="sxs-lookup"><span data-stu-id="bd097-275">Work Calendar</span></span>

![Arbeitskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="bd097-277">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd097-277">See also</span></span>

[<span data-ttu-id="bd097-278">Eine Datenintegrationstechnologie auswählen</span><span class="sxs-lookup"><span data-stu-id="bd097-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="bd097-279">Common Data Service-Integration konfigurieren</span><span class="sxs-lookup"><span data-stu-id="bd097-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)