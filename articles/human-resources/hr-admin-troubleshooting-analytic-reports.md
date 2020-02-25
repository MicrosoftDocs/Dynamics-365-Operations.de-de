---
title: Problembehandlung bei analytischen Berichten
description: In diesem Artikel wird erläutert, was zu tun ist, wenn die Datenänderungen eines Kunden in keinem der Arbeitsbereiche des Kunden angezeigt werden.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009095"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="85e53-103">Problembehandlung bei analytischen Berichten</span><span class="sxs-lookup"><span data-stu-id="85e53-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="85e53-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="85e53-104">**Issue**</span></span>

<span data-ttu-id="85e53-105">Die Datenänderungen eines Kunden werden nicht in der Registerkarte **Analyse** von irgendeinem der Arbeitsbereiche des Kunden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="85e53-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="85e53-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="85e53-106">**Cause**</span></span>

<span data-ttu-id="85e53-107">Standardmäßig werden Microsoft Power BI-Berichte alle vier Stunden aktualisiert, entsprechend des Zeitplans des Batchauftrags „Messung bereitstellen”.</span><span class="sxs-lookup"><span data-stu-id="85e53-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="85e53-108">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="85e53-108">**Resolution**</span></span>

<span data-ttu-id="85e53-109">Dieses Problem ist möglicherweise nur eine Frage der Zeitmessung.</span><span class="sxs-lookup"><span data-stu-id="85e53-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="85e53-110">Gehen Sie folgendermaßen vor, um den Batchauftrag zu starten und die Analysearbeitsbereiche zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="85e53-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="85e53-111">Öffnen Sie die Seite **Batchaufträge** unter **Systemverwaltung \> Links \> Batchaufträge \> Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="85e53-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="85e53-112">Alternativ verwenden Sie „Suche” und geben Sie **Batchaufträge** ein.</span><span class="sxs-lookup"><span data-stu-id="85e53-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="85e53-113">Suchen Sie den Einzelvorgang **Messung bereitstellen** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="85e53-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="85e53-114">Wählen Sie **Bearbeiten** am oberen Seitenrand aus, und legen Sie das geplante Startdatum/Uhrzeit auf einen Wert fest, durch den die Analyse näher an der aktuellen Uhrzeit aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="85e53-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchaufträge](media/batch-jobs.png)
