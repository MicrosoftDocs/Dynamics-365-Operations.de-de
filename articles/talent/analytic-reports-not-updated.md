---
title: Analyseberichte werden nicht aktualisiert
description: In diesem Thema wird erläutert, was zu tun ist, wenn die Datenänderungen eines Kunden in keinem der Arbeitsbereiche des Kunden angezeigt werden.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518129"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="6adeb-103">Analyseberichte werden nicht aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6adeb-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6adeb-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="6adeb-104">**Issue**</span></span>

<span data-ttu-id="6adeb-105">Die Datenänderungen eines Kunden werden nicht in der Registerkarte **Analyse** von irgendeinem der Arbeitsbereiche des Kunden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6adeb-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="6adeb-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="6adeb-106">**Cause**</span></span>

<span data-ttu-id="6adeb-107">Standardmäßig werden Microsoft Power BI-Berichte alle vier Stunden aktualisiert, entsprechend des Zeitplans des Batchauftrags „Messung bereitstellen”.</span><span class="sxs-lookup"><span data-stu-id="6adeb-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="6adeb-108">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="6adeb-108">**Resolution**</span></span>

<span data-ttu-id="6adeb-109">Dieses Problem ist möglicherweise nur eine Frage der Zeitmessung.</span><span class="sxs-lookup"><span data-stu-id="6adeb-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="6adeb-110">Gehen Sie folgendermaßen vor, um den Batchauftrag zu starten und die Analysearbeitsbereiche zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6adeb-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="6adeb-111">Öffnen Sie die Seite **Batchaufträge** unter **Systemverwaltung \> Links \> Batchaufträge \> Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="6adeb-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="6adeb-112">Alternativ verwenden Sie „Suche” und geben Sie **Batchaufträge** ein.</span><span class="sxs-lookup"><span data-stu-id="6adeb-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="6adeb-113">Suchen Sie den Einzelvorgang **Messung bereitstellen** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="6adeb-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="6adeb-114">Wählen Sie **Bearbeiten** am oberen Seitenrand aus, und legen Sie das geplante Startdatum/Uhrzeit auf einen Wert fest, durch den die Analyse näher an der aktuellen Uhrzeit aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6adeb-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchaufträge](media/batch-jobs.png)
