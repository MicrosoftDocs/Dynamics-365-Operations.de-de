---
title: Registrierungsberechtigung verarbeiten
description: In diesem Artikel wird erläutert, wie der Prozess der Registrierungsberechtigung ausgeführt wird.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009093"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="2c6db-103">Registrierungsberechtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="2c6db-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2c6db-104">In diesem Artikel wird erläutert, wie der Prozess der Registrierungsberechtigung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c6db-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="2c6db-105">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Bearbeitung** die Option **Verarbeitung von Registrierungsberechtigung**.</span><span class="sxs-lookup"><span data-stu-id="2c6db-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="2c6db-106">Geben Sie im Dialogfeld **Verarbeitung von Vorteilsregistrierungsberechtigung ausführen** Werte für die folgenden Felder ein:</span><span class="sxs-lookup"><span data-stu-id="2c6db-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="2c6db-107">Feld</span><span class="sxs-lookup"><span data-stu-id="2c6db-107">Field</span></span> | <span data-ttu-id="2c6db-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c6db-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2c6db-109">Registrierungsperiode</span><span class="sxs-lookup"><span data-stu-id="2c6db-109">Enrollment period</span></span> | <span data-ttu-id="2c6db-110">Die Registrierungsperiode, für die die Registrierungsberechtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="2c6db-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="2c6db-111">Juristische Person</span><span class="sxs-lookup"><span data-stu-id="2c6db-111">Legal entity</span></span> | <span data-ttu-id="2c6db-112">Die juristische Person, für die die Registrierungsberechtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="2c6db-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="2c6db-113">Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="2c6db-113">Worker</span></span> | <span data-ttu-id="2c6db-114">Die Arbeitskraft, für die die Registrierungsberechtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="2c6db-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="2c6db-115">Wenn Sie dieses Feld leer lassen, wird die Registrierungsberechtigung für alle Arbeitskräfte verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2c6db-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="2c6db-116">Vergütungsplan</span><span class="sxs-lookup"><span data-stu-id="2c6db-116">Benefit plan</span></span> | <span data-ttu-id="2c6db-117">Der Vorteilsplan, für den die Registrierungsberechtigung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="2c6db-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="2c6db-118">Wenn Sie den Prozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="2c6db-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="2c6db-119">Geben Sie Informationen für den Prozess ein.</span><span class="sxs-lookup"><span data-stu-id="2c6db-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="2c6db-120">Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c6db-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="2c6db-121">Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c6db-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="2c6db-122">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c6db-122">Select **OK**.</span></span> <span data-ttu-id="2c6db-123">Der Prozess wird mit den von Ihnen festgelegten Parametern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c6db-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="2c6db-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c6db-124">Select **OK**.</span></span>
