---
title: Vergütungssatzänderungen verarbeiten
description: Vergütungssatzänderungen verarbeiten in Microsoft Dynamics 365 Human Resources, wenn ein neuer oder bestehender Vorteilsplan eine Änderung an den Einstellungen der Berechtigungsregel aufweist.
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
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009105"
---
# <a name="process-rate-changes"></a><span data-ttu-id="f2187-103">Vergütungssatzänderungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f2187-103">Process rate changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f2187-104">Vergütungssatzänderungen verarbeiten in Microsoft Dynamics 365 Human Resources, wenn ein neuer oder bestehender Vorteilsplan eine Änderung an den Einstellungen der Berechtigungsregel aufweist.</span><span class="sxs-lookup"><span data-stu-id="f2187-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="f2187-105">Wenn eine neue Berechtigungsregel erstellt und dem Plan zugewiesen wird, fordert dies das System auf, die Berechtigung der Mitarbeiter erneut auszuführen, um zu prüfen, ob die Mitarbeiter nun aufgrund neuer Berechtigungsoptionen für den Plan berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="f2187-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to re-run worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="f2187-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Bearbeitung** die Option **Verarbeitung von aktualisierten Satzänderungen**.</span><span class="sxs-lookup"><span data-stu-id="f2187-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="f2187-107">Geben Sie im Dialogfeld **Verarbeitung von Vorteilssatzaktualisierungen ausführen** Werte für die folgenden Felder ein:</span><span class="sxs-lookup"><span data-stu-id="f2187-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="f2187-108">Feld</span><span class="sxs-lookup"><span data-stu-id="f2187-108">Field</span></span> | <span data-ttu-id="f2187-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2187-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f2187-110">Registrierungsperiode</span><span class="sxs-lookup"><span data-stu-id="f2187-110">Enrollment period</span></span> | <span data-ttu-id="f2187-111">Die Registrierungsperiode, für die die Vergütungssatzänderung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f2187-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="f2187-112">Wenn Sie den Prozess im Hintergrund ausführen möchten, wählen Sie **Im Hintergrund ausführen** und führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="f2187-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="f2187-113">Geben Sie Informationen für den Prozess ein.</span><span class="sxs-lookup"><span data-stu-id="f2187-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="f2187-114">Um eine wiederkehrende Stelle einzurichten, wählen Sie **Wiederholung**, geben Sie die Wiederholungsinformationen ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2187-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="f2187-115">Um eine Stellenbenachrichtigung einzurichten, wählen Sie **Benachrichtigungen**, wählen Sie die zu empfangenden Benachrichtigungen und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2187-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="f2187-116">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2187-116">Select **OK**.</span></span> <span data-ttu-id="f2187-117">Der Prozess wird mit den von Ihnen festgelegten Parametern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2187-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="f2187-118">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2187-118">Select **OK**.</span></span>
