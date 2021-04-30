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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893399"
---
# <a name="dataverse-tables"></a><span data-ttu-id="cd260-103">Dataverse-Tabellen</span><span class="sxs-lookup"><span data-stu-id="cd260-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cd260-104">Microsoft Dynamics 365 Human Resources verwendet Dataverse, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cd260-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="cd260-105">Human Resources-Entitäten entsprechen Dataverse-Tabellen.</span><span class="sxs-lookup"><span data-stu-id="cd260-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="cd260-106">Weitere Informationen zu Dataverse (früher Common Data Service) und Terminologie-Updates finden Sie unter [Was ist Microsoft Dataverse ?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="cd260-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="cd260-107">Die folgenden Dataverse-Tabellen sind basierend auf Human Resources-Entitäten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd260-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="cd260-108">Vorteilstabellen</span><span class="sxs-lookup"><span data-stu-id="cd260-108">Benefit tables</span></span>

| <span data-ttu-id="cd260-109">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-109">Name</span></span> | <span data-ttu-id="cd260-110">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-111">Vorteilsberechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="cd260-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="cd260-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="cd260-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="cd260-113">Berechnungshäufigkeit Lohnperiode für Vergütungen</span><span class="sxs-lookup"><span data-stu-id="cd260-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="cd260-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="cd260-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="cd260-115">Vergütungsberechnungssatz</span><span class="sxs-lookup"><span data-stu-id="cd260-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="cd260-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="cd260-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="cd260-117">Vergütungsberechnungssatz-Detail</span><span class="sxs-lookup"><span data-stu-id="cd260-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="cd260-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="cd260-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="cd260-119">Vergütungsoption</span><span class="sxs-lookup"><span data-stu-id="cd260-119">Benefit Option</span></span> | <span data-ttu-id="cd260-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="cd260-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="cd260-121">Vergütungsplan</span><span class="sxs-lookup"><span data-stu-id="cd260-121">Benefit Plan</span></span> | <span data-ttu-id="cd260-122">cdm_benefitplan (Nicht aktiviert für benutzerdefinierte Feldunterstützung)</span><span class="sxs-lookup"><span data-stu-id="cd260-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="cd260-123">Vergütungstyp</span><span class="sxs-lookup"><span data-stu-id="cd260-123">Benefit Type</span></span> | <span data-ttu-id="cd260-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="cd260-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="cd260-125">Tabellen von Geschäftsprozessaufgaben</span><span class="sxs-lookup"><span data-stu-id="cd260-125">Business process tasks tables</span></span>

| <span data-ttu-id="cd260-126">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-126">Name</span></span> | <span data-ttu-id="cd260-127">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-128">Geschäftsprozesskalender</span><span class="sxs-lookup"><span data-stu-id="cd260-128">Business Process Calendar</span></span> | <span data-ttu-id="cd260-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="cd260-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="cd260-130">Zuweisung der Geschäftsprozessgruppe</span><span class="sxs-lookup"><span data-stu-id="cd260-130">Business Process Group Assignment</span></span> | <span data-ttu-id="cd260-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="cd260-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="cd260-132">Geschäftsprozessbibliothek-Aufgabengruppe</span><span class="sxs-lookup"><span data-stu-id="cd260-132">Business Process Library Task Group</span></span> | <span data-ttu-id="cd260-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="cd260-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="cd260-134">Geschäftsprozessphase</span><span class="sxs-lookup"><span data-stu-id="cd260-134">Business Process Stage</span></span> | <span data-ttu-id="cd260-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="cd260-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="cd260-136">Kopfzeile der Prüflistenvorlage</span><span class="sxs-lookup"><span data-stu-id="cd260-136">Checklist Template Header</span></span> | <span data-ttu-id="cd260-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="cd260-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="cd260-138">Prüflistenvorlagen-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="cd260-138">Checklist Template Task</span></span> | <span data-ttu-id="cd260-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="cd260-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="cd260-140">Vergütungstabellen</span><span class="sxs-lookup"><span data-stu-id="cd260-140">Compensation tables</span></span>

| <span data-ttu-id="cd260-141">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-141">Name</span></span> | <span data-ttu-id="cd260-142">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-143">Plan mit fester Vergütung</span><span class="sxs-lookup"><span data-stu-id="cd260-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="cd260-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="cd260-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="cd260-145">Vergütungsraster</span><span class="sxs-lookup"><span data-stu-id="cd260-145">Compensation Grid</span></span> | <span data-ttu-id="cd260-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="cd260-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="cd260-147">Vergütungsstufe</span><span class="sxs-lookup"><span data-stu-id="cd260-147">Compensation Level</span></span> | <span data-ttu-id="cd260-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="cd260-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="cd260-149">Häufigkeit der Vergütungszahlung</span><span class="sxs-lookup"><span data-stu-id="cd260-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="cd260-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="cd260-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="cd260-151">Vergütungsreferenzpunkten einrichten</span><span class="sxs-lookup"><span data-stu-id="cd260-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="cd260-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="cd260-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="cd260-153">Vergütungsreferenzpunktzeile einrichten</span><span class="sxs-lookup"><span data-stu-id="cd260-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="cd260-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="cd260-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="cd260-155">Vergütungsregion</span><span class="sxs-lookup"><span data-stu-id="cd260-155">Compensation Region</span></span> | <span data-ttu-id="cd260-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="cd260-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="cd260-157">Vergütungsstruktur</span><span class="sxs-lookup"><span data-stu-id="cd260-157">Compensation Structure</span></span> | <span data-ttu-id="cd260-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="cd260-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="cd260-159">Variabler Plan für Vergütung</span><span class="sxs-lookup"><span data-stu-id="cd260-159">Compensation Variable Plan</span></span> | <span data-ttu-id="cd260-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="cd260-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="cd260-161">Variable Planstufe für Vergütung</span><span class="sxs-lookup"><span data-stu-id="cd260-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="cd260-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="cd260-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="cd260-163">Plantyp für variable Vergütung</span><span class="sxs-lookup"><span data-stu-id="cd260-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="cd260-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="cd260-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="cd260-165">Ereignis für feste Vergütung</span><span class="sxs-lookup"><span data-stu-id="cd260-165">Fixed Compensation Event</span></span> | <span data-ttu-id="cd260-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="cd260-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="cd260-167">Übertragungsregel</span><span class="sxs-lookup"><span data-stu-id="cd260-167">Vesting Rule</span></span> | <span data-ttu-id="cd260-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="cd260-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="cd260-169">Feste Arbeitskraftvergütung</span><span class="sxs-lookup"><span data-stu-id="cd260-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="cd260-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="cd260-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="cd260-171">Organisationstabellen</span><span class="sxs-lookup"><span data-stu-id="cd260-171">Organization tables</span></span>

| <span data-ttu-id="cd260-172">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-172">Name</span></span> | <span data-ttu-id="cd260-173">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-174">Abteilung</span><span class="sxs-lookup"><span data-stu-id="cd260-174">Department</span></span> | <span data-ttu-id="cd260-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="cd260-175">cdm_department</span></span> |
| <span data-ttu-id="cd260-176">Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="cd260-176">Employment</span></span> | <span data-ttu-id="cd260-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="cd260-177">cdm_employment</span></span> |
| <span data-ttu-id="cd260-178">Firma</span><span class="sxs-lookup"><span data-stu-id="cd260-178">Company</span></span> | <span data-ttu-id="cd260-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="cd260-179">cdm_company</span></span> |
| <span data-ttu-id="cd260-180">Auftrag</span><span class="sxs-lookup"><span data-stu-id="cd260-180">Job</span></span> | <span data-ttu-id="cd260-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="cd260-181">cdm_job</span></span> |
| <span data-ttu-id="cd260-182">Stellenfunktion</span><span class="sxs-lookup"><span data-stu-id="cd260-182">Job Function</span></span> | <span data-ttu-id="cd260-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="cd260-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="cd260-184">Position</span><span class="sxs-lookup"><span data-stu-id="cd260-184">Job Position</span></span> | <span data-ttu-id="cd260-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="cd260-185">cdm_jobposition</span></span> |
| <span data-ttu-id="cd260-186">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="cd260-186">Position Type</span></span> | <span data-ttu-id="cd260-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="cd260-187">cdm_positiontype</span></span> |
| <span data-ttu-id="cd260-188">Arbeitskraftzuweisung für die Position</span><span class="sxs-lookup"><span data-stu-id="cd260-188">Position Worker Assignment</span></span> | <span data-ttu-id="cd260-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="cd260-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="cd260-190">Positionsdimension</span><span class="sxs-lookup"><span data-stu-id="cd260-190">Job Position Dimension</span></span> | <span data-ttu-id="cd260-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="cd260-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="cd260-192">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="cd260-192">Job Type</span></span> | <span data-ttu-id="cd260-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="cd260-193">cdm_jobtype</span></span> |
| <span data-ttu-id="cd260-194">Sprache</span><span class="sxs-lookup"><span data-stu-id="cd260-194">Language</span></span> | <span data-ttu-id="cd260-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="cd260-195">cdm_language</span></span> |
| <span data-ttu-id="cd260-196">Titel</span><span class="sxs-lookup"><span data-stu-id="cd260-196">Title</span></span> | <span data-ttu-id="cd260-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="cd260-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="cd260-198">Finanzielle Dimensionen für **Positionstyp**, **Arbeitskraftzuweisung für die Position**, und **Beschäftigung** bieten eine einseitige Integration in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="cd260-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="cd260-199">Aktualisierungen der Finanzdimensionen werden derzeit nicht synchronisiert von Dataverse zu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cd260-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="cd260-200">Tabelle „Urlaub und Abwesenheit“</span><span class="sxs-lookup"><span data-stu-id="cd260-200">Leave and absence tables</span></span>

| <span data-ttu-id="cd260-201">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-201">Name</span></span> | <span data-ttu-id="cd260-202">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-203">Urlaubsbankbuchung</span><span class="sxs-lookup"><span data-stu-id="cd260-203">Leave Bank Transaction</span></span> | <span data-ttu-id="cd260-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="cd260-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="cd260-205">Urlaubsregistrierung</span><span class="sxs-lookup"><span data-stu-id="cd260-205">Leave Enrollment</span></span> | <span data-ttu-id="cd260-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="cd260-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="cd260-207">Urlaubsplan</span><span class="sxs-lookup"><span data-stu-id="cd260-207">Leave Plan</span></span> | <span data-ttu-id="cd260-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="cd260-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="cd260-209">Urlaubsantrag</span><span class="sxs-lookup"><span data-stu-id="cd260-209">Leave Request</span></span> | <span data-ttu-id="cd260-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="cd260-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="cd260-211">Urlaubsantragdetail</span><span class="sxs-lookup"><span data-stu-id="cd260-211">Leave Request Detail</span></span> | <span data-ttu-id="cd260-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="cd260-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="cd260-213">Urlaubstyp</span><span class="sxs-lookup"><span data-stu-id="cd260-213">Leave Type</span></span> | <span data-ttu-id="cd260-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="cd260-214">cdm_leavetype</span></span> |
| <span data-ttu-id="cd260-215">Ursachencode für Abwesenheitstyp</span><span class="sxs-lookup"><span data-stu-id="cd260-215">Leave Type Reason Code</span></span> | <span data-ttu-id="cd260-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="cd260-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="cd260-217">Lohntabellen</span><span class="sxs-lookup"><span data-stu-id="cd260-217">Payroll tables</span></span>

| <span data-ttu-id="cd260-218">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-218">Name</span></span> | <span data-ttu-id="cd260-219">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-220">Lohnzyklus</span><span class="sxs-lookup"><span data-stu-id="cd260-220">Pay Cycle</span></span> | <span data-ttu-id="cd260-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="cd260-221">cdm_paycycle</span></span> |
| <span data-ttu-id="cd260-222">Lohnperiode</span><span class="sxs-lookup"><span data-stu-id="cd260-222">Pay Period</span></span> | <span data-ttu-id="cd260-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="cd260-223">cdm_payperiod</span></span> |
| <span data-ttu-id="cd260-224">Lohneinkommenscode</span><span class="sxs-lookup"><span data-stu-id="cd260-224">Payroll Earning Code</span></span> | <span data-ttu-id="cd260-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="cd260-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="cd260-226">Bankkontoauszahlungen</span><span class="sxs-lookup"><span data-stu-id="cd260-226">Bank Account Disbursement</span></span> | <span data-ttu-id="cd260-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="cd260-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="cd260-228">Steuerregion</span><span class="sxs-lookup"><span data-stu-id="cd260-228">Tax Region</span></span> | <span data-ttu-id="cd260-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="cd260-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="cd260-230">Arbeitskräftetabellen</span><span class="sxs-lookup"><span data-stu-id="cd260-230">Worker tables</span></span>

| <span data-ttu-id="cd260-231">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-231">Name</span></span> | <span data-ttu-id="cd260-232">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-233">Worker</span><span class="sxs-lookup"><span data-stu-id="cd260-233">Worker</span></span> | <span data-ttu-id="cd260-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="cd260-234">cdm_worker</span></span> |
| <span data-ttu-id="cd260-235">Arbeitskraftadresse</span><span class="sxs-lookup"><span data-stu-id="cd260-235">Worker Address</span></span> | <span data-ttu-id="cd260-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="cd260-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="cd260-237">Persönliches Detail der Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="cd260-237">Worker Personal Detail</span></span> | <span data-ttu-id="cd260-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="cd260-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="cd260-239">Personenidentifikationsnummer Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="cd260-239">Worker Person Identification Number</span></span> | <span data-ttu-id="cd260-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="cd260-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="cd260-241">Personenidentifikationstyp Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="cd260-241">Worker Person Identification Type</span></span> | <span data-ttu-id="cd260-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="cd260-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="cd260-243">Arbeitskalender</span><span class="sxs-lookup"><span data-stu-id="cd260-243">Work Calendar</span></span> | <span data-ttu-id="cd260-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="cd260-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="cd260-245">Arbeitskalendertag</span><span class="sxs-lookup"><span data-stu-id="cd260-245">Work Calendar Day</span></span> | <span data-ttu-id="cd260-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="cd260-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="cd260-247">Arbeitskalenderurlaub</span><span class="sxs-lookup"><span data-stu-id="cd260-247">Work Calendar Holiday</span></span> |<span data-ttu-id="cd260-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="cd260-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="cd260-249">Arbeitskalender-Datumsposition</span><span class="sxs-lookup"><span data-stu-id="cd260-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="cd260-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="cd260-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="cd260-251">Arbeitskalender-Zeitintervall</span><span class="sxs-lookup"><span data-stu-id="cd260-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="cd260-252">cdm_workcalendartimeinterval (Nicht aktiviert für benutzerdefinierte Feldunterstützung)</span><span class="sxs-lookup"><span data-stu-id="cd260-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="cd260-253">Arbeitskraftbankkonto</span><span class="sxs-lookup"><span data-stu-id="cd260-253">Worker Bank Account</span></span> | <span data-ttu-id="cd260-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="cd260-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="cd260-255">Arbeitskräfteeinrichtungstabellen</span><span class="sxs-lookup"><span data-stu-id="cd260-255">Worker setup tables</span></span>

| <span data-ttu-id="cd260-256">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-256">Name</span></span> | <span data-ttu-id="cd260-257">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-258">Veteranenstatus</span><span class="sxs-lookup"><span data-stu-id="cd260-258">Veteran Status</span></span> | <span data-ttu-id="cd260-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="cd260-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="cd260-260">Nationalität</span><span class="sxs-lookup"><span data-stu-id="cd260-260">Ethnic Origin</span></span> | <span data-ttu-id="cd260-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="cd260-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="cd260-262">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="cd260-262">Reason Code</span></span> | <span data-ttu-id="cd260-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="cd260-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="cd260-264">Ausstellende Behörde für Personenkennungen</span><span class="sxs-lookup"><span data-stu-id="cd260-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="cd260-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="cd260-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="cd260-266">Kompetenztabellen</span><span class="sxs-lookup"><span data-stu-id="cd260-266">Competency tables</span></span>

| <span data-ttu-id="cd260-267">Name</span><span class="sxs-lookup"><span data-stu-id="cd260-267">Name</span></span> | <span data-ttu-id="cd260-268">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd260-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="cd260-269">Qualifikationstyp</span><span class="sxs-lookup"><span data-stu-id="cd260-269">Skill Type</span></span> | <span data-ttu-id="cd260-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="cd260-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="cd260-271">Tabellenbeziehungsmodelle</span><span class="sxs-lookup"><span data-stu-id="cd260-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="cd260-272">Worker</span><span class="sxs-lookup"><span data-stu-id="cd260-272">Worker</span></span>

![Worker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="cd260-274">Stelle und Stellenposition</span><span class="sxs-lookup"><span data-stu-id="cd260-274">Job and Job Position</span></span>

![Stelle und Stellenposition](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="cd260-276">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="cd260-276">Benefits</span></span>

![Vergütungen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="cd260-278">Kompensation</span><span class="sxs-lookup"><span data-stu-id="cd260-278">Compensation</span></span>

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="cd260-280">Verlasen</span><span class="sxs-lookup"><span data-stu-id="cd260-280">Leave</span></span>

![Verlasen](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="cd260-282">Arbeitskalender</span><span class="sxs-lookup"><span data-stu-id="cd260-282">Work Calendar</span></span>

![Arbeitskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="cd260-284">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd260-284">See also</span></span>

[<span data-ttu-id="cd260-285">Eine Datenintegrationstechnologie auswählen</span><span class="sxs-lookup"><span data-stu-id="cd260-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="cd260-286">Dataverse-Integration konfigurieren</span><span class="sxs-lookup"><span data-stu-id="cd260-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="cd260-287">Virtuelle Dataverse-Tabellen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="cd260-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="cd260-288">FAQ zu virtuellen Tabellen für Human Resources</span><span class="sxs-lookup"><span data-stu-id="cd260-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="cd260-289">Was ist Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="cd260-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="cd260-290">Terminologie-Updates</span><span class="sxs-lookup"><span data-stu-id="cd260-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]