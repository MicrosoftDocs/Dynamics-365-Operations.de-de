---
title: Lebensereignisse verarbeiten
description: Während des Mitarbeiterlebenszyklus in Microsoft Dynamics 365 Human Resources kann es bei jedem Mitarbeiter zu verschiedenen Änderungen von Lebensereignissen kommen.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42b7e2606bca4bb5eda1c9bfc7940f9067c4b943
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112633"
---
# <a name="process-life-events"></a><span data-ttu-id="5627e-103">Lebensereignisse verarbeiten</span><span class="sxs-lookup"><span data-stu-id="5627e-103">Process life events</span></span>

<span data-ttu-id="5627e-104">Während des Mitarbeiterlebenszyklus in Microsoft Dynamics 365 Human Resources kann es bei jedem Mitarbeiter zu verschiedenen Änderungen von Lebensereignissen kommen.</span><span class="sxs-lookup"><span data-stu-id="5627e-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="5627e-105">Beispiel: Ehe, Wechsel der Beschäftigung oder Wechsel von Unterhaltsberechtigten/Begünstigten.</span><span class="sxs-lookup"><span data-stu-id="5627e-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="5627e-106">Um Lebensereignisse zu verwenden, müssen Sie Lebensereignisse im Formular „Vorteilparameter“ aktivieren, Lebensereignistypen einrichten und Lebensereignisoptionen für Plantypen einrichten.</span><span class="sxs-lookup"><span data-stu-id="5627e-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="5627e-107">Bevor Sie Lebensereignisse verarbeiten können, müssen Sie mindestens einmal während einer Einstellungsperiode eine offene Registrierung durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="5627e-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="5627e-108">In den USA erfolgt die offene Registrierung in der Regel einmal pro Jahr.</span><span class="sxs-lookup"><span data-stu-id="5627e-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="5627e-109">Außerhalb der USA kann eine offene Registrierung zum Zeitpunkt der Einstellung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5627e-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="5627e-110">Eine Arbeitskraft muss keinen Vorteilsplan auswählen, damit Lebensereignisse verarbeitet werden können, sie muss jedoch in die offene Registrierungsverarbeitung einbezogen worden sein.</span><span class="sxs-lookup"><span data-stu-id="5627e-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="5627e-111">Verwenden Sie die Lebensereignisverarbeitung, wenn Sie Arbeitskräfte haben, deren Lebensereignisse zu einem späteren Zeitpunkt stattfinden.</span><span class="sxs-lookup"><span data-stu-id="5627e-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="5627e-112">Dieses Ereignis verarbeitet alle nicht verarbeiteten Lebensereignisse (wie zukünftige Lebensereignisse oder hinzugefügte Lebensereignisse, die sich nicht auf eine bestimmte Arbeitskraft beziehen – ein Beispiel wäre ein neuer Vorteil).</span><span class="sxs-lookup"><span data-stu-id="5627e-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="5627e-113">Echtzeitereignisse sind ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="5627e-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="5627e-114">Wenn beispielsweise heute der 1. Februar ist und die Arbeitskraft Joe Smith am 14. Februar juristische Personen wechseln soll, verarbeitet das System alle Ereignisse bis zum 15. Februar, wenn Sie die Verarbeitung von Lebensereignissen für den 15. Februar ausführen.</span><span class="sxs-lookup"><span data-stu-id="5627e-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="5627e-115">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Bearbeitung** die Option **Verarbeitung von Lebensereignissen**.</span><span class="sxs-lookup"><span data-stu-id="5627e-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="5627e-116">Geben Sie im Dialogfeld **Verarbeitung von Lebensereignissen ausführen** Werte für die folgenden Felder ein:</span><span class="sxs-lookup"><span data-stu-id="5627e-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="5627e-117">Feld</span><span class="sxs-lookup"><span data-stu-id="5627e-117">Field</span></span> | <span data-ttu-id="5627e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5627e-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5627e-119">**Registrierungsperiode**</span><span class="sxs-lookup"><span data-stu-id="5627e-119">**Enrollment period**</span></span> | <span data-ttu-id="5627e-120">Die Registrierungsperiode, für die die Lebensereignisse verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5627e-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="5627e-121">**Juristische Person**</span><span class="sxs-lookup"><span data-stu-id="5627e-121">**Legal entity**</span></span> | <span data-ttu-id="5627e-122">Die juristische Person, für die die Lebensereignisse verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5627e-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="5627e-123">**Datum des Lebensereignisses**</span><span class="sxs-lookup"><span data-stu-id="5627e-123">**Life event date**</span></span> | <span data-ttu-id="5627e-124">Das System verarbeitet alle Ereignisse während der Registrierungsperiode, die bis zu diesem Datum auftreten.</span><span class="sxs-lookup"><span data-stu-id="5627e-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="5627e-125">**Arbeitskraft**</span><span class="sxs-lookup"><span data-stu-id="5627e-125">**Worker**</span></span> | <span data-ttu-id="5627e-126">Die Arbeitskraft, für die die Lebensereignisse verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5627e-126">The worker to process life events for.</span></span> <span data-ttu-id="5627e-127">Wenn Sie dieses Feld leer lassen, werden Lebensereignisse für alle Arbeitskräfte verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5627e-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="5627e-128">Wenn Sie den Prozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="5627e-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="5627e-129">Geben Sie Informationen für den Prozess ein.</span><span class="sxs-lookup"><span data-stu-id="5627e-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="5627e-130">Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5627e-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="5627e-131">Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="5627e-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="5627e-132">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5627e-132">Select **OK**.</span></span> <span data-ttu-id="5627e-133">Der Prozess wird mit den von Ihnen festgelegten Parametern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5627e-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="5627e-134">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5627e-134">Select **OK**.</span></span>
