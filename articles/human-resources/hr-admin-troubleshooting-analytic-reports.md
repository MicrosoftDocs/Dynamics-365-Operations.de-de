---
title: Problembehandlung bei analytischen Berichten
description: In diesem Artikel wird erläutert, was zu tun ist, wenn die Datenänderungen eines Kunden in keinem der Arbeitsbereiche des Kunden angezeigt werden.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112672"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="ba765-103">Problembehandlung bei analytischen Berichten</span><span class="sxs-lookup"><span data-stu-id="ba765-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="ba765-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="ba765-104">**Issue**</span></span>

<span data-ttu-id="ba765-105">Die Datenänderungen eines Kunden werden nicht in der Registerkarte **Analyse** von irgendeinem der Arbeitsbereiche des Kunden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba765-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="ba765-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="ba765-106">**Cause**</span></span>

<span data-ttu-id="ba765-107">Standardmäßig werden Microsoft Power BI-Berichte alle vier Stunden aktualisiert, entsprechend des Zeitplans des Batchauftrags „Messung bereitstellen”.</span><span class="sxs-lookup"><span data-stu-id="ba765-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="ba765-108">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="ba765-108">**Resolution**</span></span>

<span data-ttu-id="ba765-109">Dieses Problem ist möglicherweise nur eine Frage der Zeitmessung.</span><span class="sxs-lookup"><span data-stu-id="ba765-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="ba765-110">Gehen Sie folgendermaßen vor, um den Batchauftrag zu starten und die Analysearbeitsbereiche zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ba765-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="ba765-111">Öffnen Sie die Seite **Batchaufträge** unter **Systemverwaltung \> Links \> Batchaufträge \> Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="ba765-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="ba765-112">Alternativ verwenden Sie „Suche” und geben Sie **Batchaufträge** ein.</span><span class="sxs-lookup"><span data-stu-id="ba765-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="ba765-113">Suchen Sie den Einzelvorgang **Messung bereitstellen** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="ba765-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="ba765-114">Wählen Sie **Bearbeiten** am oberen Seitenrand aus, und legen Sie das geplante Startdatum/Uhrzeit auf einen Wert fest, durch den die Analyse näher an der aktuellen Uhrzeit aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba765-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchaufträge](media/batch-jobs.png)
