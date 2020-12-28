---
title: Registrierungsberechtigung verarbeiten
description: In diesem Artikel wird erläutert, wie der Prozess der Registrierungsberechtigung ausgeführt wird.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfb7f13dce48f33c111af491918702763f7e3b8a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418629"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="39098-103">Registrierungsberechtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="39098-103">Process enrollment eligibility</span></span>

<span data-ttu-id="39098-104">In diesem Artikel wird erläutert, wie der Prozess der Registrierungsberechtigung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39098-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="39098-105">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Bearbeitung** die Option **Verarbeitung von Registrierungsberechtigung**.</span><span class="sxs-lookup"><span data-stu-id="39098-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="39098-106">Geben Sie im Dialogfeld **Verarbeitung von Vorteilsregistrierungsberechtigung ausführen** Werte für die folgenden Felder ein:</span><span class="sxs-lookup"><span data-stu-id="39098-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="39098-107">Feld</span><span class="sxs-lookup"><span data-stu-id="39098-107">Field</span></span> | <span data-ttu-id="39098-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39098-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="39098-109">**Registrierungsperiode**</span><span class="sxs-lookup"><span data-stu-id="39098-109">**Enrollment period**</span></span> | <span data-ttu-id="39098-110">Die Registrierungsperiode, für die die Registrierungsberechtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="39098-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="39098-111">**Juristische Person**</span><span class="sxs-lookup"><span data-stu-id="39098-111">**Legal entity**</span></span> | <span data-ttu-id="39098-112">Die juristische Person, für die die Registrierungsberechtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="39098-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="39098-113">**Arbeitskraft**</span><span class="sxs-lookup"><span data-stu-id="39098-113">**Worker**</span></span> | <span data-ttu-id="39098-114">Die Arbeitskraft, für die die Registrierungsberechtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="39098-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="39098-115">Wenn Sie dieses Feld leer lassen, wird die Registrierungsberechtigung für alle Arbeitskräfte verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="39098-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="39098-116">**Vergütungsplan**</span><span class="sxs-lookup"><span data-stu-id="39098-116">**Benefit plan**</span></span> | <span data-ttu-id="39098-117">Der Vorteilsplan, für den die Registrierungsberechtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="39098-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="39098-118">Wenn Sie den Prozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="39098-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="39098-119">Geben Sie Informationen für den Prozess ein.</span><span class="sxs-lookup"><span data-stu-id="39098-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="39098-120">Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="39098-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="39098-121">Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="39098-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="39098-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="39098-122">Select **OK**.</span></span> <span data-ttu-id="39098-123">Der Prozess wird mit den von Ihnen festgelegten Parametern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39098-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="39098-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="39098-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="39098-125">Anzeigen von Prozessergebnissen</span><span class="sxs-lookup"><span data-stu-id="39098-125">View Process Results</span></span>

<span data-ttu-id="39098-126">In diesem Artikel wird erläutert, wie die Berechtigung der Prozessergebnisse angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="39098-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="39098-127">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Prozess** die Option **Prozessergebnisse**.</span><span class="sxs-lookup"><span data-stu-id="39098-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="39098-128">In dem Formular **Prozessergebnisse** sind die folgenden Felder angegeben:</span><span class="sxs-lookup"><span data-stu-id="39098-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="39098-129">Feld</span><span class="sxs-lookup"><span data-stu-id="39098-129">Field</span></span> | <span data-ttu-id="39098-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39098-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="39098-131">**Prozesskennung**</span><span class="sxs-lookup"><span data-stu-id="39098-131">**Process ID**</span></span> | <span data-ttu-id="39098-132">Die eindeutige ID für die Kombination aus Arbeitskraft, juristischer Person und Prozesslauf.</span><span class="sxs-lookup"><span data-stu-id="39098-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="39098-133">**Prozesstyp**</span><span class="sxs-lookup"><span data-stu-id="39098-133">**Process type**</span></span> | <span data-ttu-id="39098-134">Dies identifiziert den Prozess, der ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="39098-134">This identifies the process that was run.</span></span> <span data-ttu-id="39098-135">Zum Beispiel: Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="39098-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="39098-136">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="39098-136">**Time stamp**</span></span> | <span data-ttu-id="39098-137">Die Zeit, zu der der Berechtigungsprozess ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="39098-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="39098-138">**Juristische Person**</span><span class="sxs-lookup"><span data-stu-id="39098-138">**Legal entity**</span></span> | <span data-ttu-id="39098-139">Die während des Registrierungsprozesses angegebene juristische Person.</span><span class="sxs-lookup"><span data-stu-id="39098-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="39098-140">**Worker**</span><span class="sxs-lookup"><span data-stu-id="39098-140">**Worker**</span></span> | <span data-ttu-id="39098-141">Die Arbeitskraft, die verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="39098-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="39098-142">\*\*Plan</span><span class="sxs-lookup"><span data-stu-id="39098-142">\*\*Plan</span></span> | <span data-ttu-id="39098-143">Der Leistungsplan, für den eine Registrierung versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="39098-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="39098-144">**Berechtigungsregel**</span><span class="sxs-lookup"><span data-stu-id="39098-144">**Eligibility rule**</span></span> | <span data-ttu-id="39098-145">Die Berechtigungsregel, die verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="39098-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="39098-146">Wenn vor dem Ausführen der Berechtigung ein Fehler aufgetreten ist, ist dieser leer.</span><span class="sxs-lookup"><span data-stu-id="39098-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="39098-147">Beispiel: Wenn für einen Mitarbeiter keine Vergütung definiert wurde, wird der Berechtigungsprozess nicht ausgeführt, und dieses Feld bleibt leer.</span><span class="sxs-lookup"><span data-stu-id="39098-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="39098-148">**Ergebnisstatus**</span><span class="sxs-lookup"><span data-stu-id="39098-148">**Result status**</span></span> | <span data-ttu-id="39098-149">Dies ist berechtigt oder nicht berechtigt.</span><span class="sxs-lookup"><span data-stu-id="39098-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="39098-150">Der Ergebnisstatus ist nicht berechtigt, wenn der Arbeitnehmer die Kriterien für die Berechtigungsregel nicht erfüllt, wenn dem Arbeitnehmer die erforderlichen Informationen wie eine Gehaltshäufigkeit oder eine feste Vergütung fehlen oder wenn im Leistungsplan Informationen fehlen, die die Einschreibung von Arbeitnehmern verhindern.</span><span class="sxs-lookup"><span data-stu-id="39098-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="39098-151">**Ergebnismeldung**</span><span class="sxs-lookup"><span data-stu-id="39098-151">**Result message**</span></span> | <span data-ttu-id="39098-152">Gibt an, warum ein Arbeitnehmer keinen Anspruch auf einen Leistungsplan hat oder ob die Anspruchsregel erfüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="39098-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

