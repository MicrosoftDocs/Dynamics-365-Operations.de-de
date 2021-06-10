---
title: Problembehandlung bei analytischen Berichten
description: In diesem Artikel wird erläutert, was zu tun ist, wenn die Datenänderungen eines Kunden in keinem der Arbeitsbereiche des Kunden angezeigt werden.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053538"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="be172-103">Problembehandlung bei analytischen Berichten</span><span class="sxs-lookup"><span data-stu-id="be172-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="be172-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="be172-104">**Issue**</span></span>

<span data-ttu-id="be172-105">Die Datenänderungen eines Kunden werden nicht in der Registerkarte **Analyse** von irgendeinem der Arbeitsbereiche des Kunden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="be172-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="be172-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="be172-106">**Cause**</span></span>

<span data-ttu-id="be172-107">Standardmäßig werden die Microsoft Power BI-Berichte alle vier Stunden aktualisiert, entsprechend dem Zeitplan des Batch-Jobs „Messung bereitstellen“.</span><span class="sxs-lookup"><span data-stu-id="be172-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="be172-108">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="be172-108">**Resolution**</span></span>

<span data-ttu-id="be172-109">Dieses Problem ist möglicherweise nur eine Frage der Zeitmessung.</span><span class="sxs-lookup"><span data-stu-id="be172-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="be172-110">Gehen Sie folgendermaßen vor, um den Batchauftrag zu starten und die Analysearbeitsbereiche zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="be172-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="be172-111">Öffnen Sie die Seite **Batchaufträge** unter **Systemverwaltung \> Links \> Batchaufträge \> Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="be172-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="be172-112">Alternativ verwenden Sie „Suche” und geben Sie **Batchaufträge** ein.</span><span class="sxs-lookup"><span data-stu-id="be172-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="be172-113">Suchen Sie den Einzelvorgang **Messung bereitstellen** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="be172-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="be172-114">Wählen Sie **Bearbeiten** am oberen Seitenrand aus, und legen Sie das geplante Startdatum/Uhrzeit auf einen Wert fest, durch den die Analyse näher an der aktuellen Uhrzeit aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="be172-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchaufträge](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]