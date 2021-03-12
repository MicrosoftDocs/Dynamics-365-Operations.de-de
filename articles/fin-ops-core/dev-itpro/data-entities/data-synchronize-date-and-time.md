---
title: Synchronisieren von Datum und Uhrzeit in Importaufträgen
description: Verwenden Sie UTC-Zeitzonen in Importaufträgen, um Probleme mit Zeitzonenkonvertierungen zu vermeiden.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798718"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="c5572-103">Synchronisieren von Datum und Uhrzeit in Importaufträgen</span><span class="sxs-lookup"><span data-stu-id="c5572-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5572-104">Es ist wichtig, die Zeitzone für Ihren Importauftrag auf die koordinierte Weltzeit (UTC) einzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5572-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c5572-105">Wenn Sie eine andere Einstellung verwenden, werden möglicherweise unerwartete Daten und Zeiten in Ihren importierten Daten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5572-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="c5572-106">Ohne die richtige Einstellung konvertiert der Importvorgang das UTC-Datum in das lokale Format, und die Systemeinstellungen konvertieren es erneut.</span><span class="sxs-lookup"><span data-stu-id="c5572-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="c5572-107">Diese doppelte Konvertierung führt dazu, dass sich die Datumsangaben zwischen den Anwendungen ändern.</span><span class="sxs-lookup"><span data-stu-id="c5572-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="c5572-108">Beispielsweise kann die doppelte Konvertierung dazu führen, dass das Startdatum eines Mitarbeiters sich in Dynamics 365 Human Resources und Dynamics 365 Finance aufgrund von Unterschieden in den lokalen Zeitzonen unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="c5572-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="c5572-109">Durch Setzen des Importauftrags auf UTC wird dieses Problem behoben.</span><span class="sxs-lookup"><span data-stu-id="c5572-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="c5572-110">In Dynamics 365 Finance and Operations wählen Sie **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="c5572-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="c5572-111">Wählen Sie **Importprojekte**, und wählen Sie dann das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="c5572-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="c5572-112">Unter **Quelldatumsformat** wählen Sie **CSV-Unicode** aus.</span><span class="sxs-lookup"><span data-stu-id="c5572-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="c5572-113">[![Ändern des Quelldatumsformats in UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="c5572-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="c5572-114">Ändern Sie die **Zeitzone** in **Koordinierte Weltzeit**, und ändern Sie **Sprache** in **En-US**.</span><span class="sxs-lookup"><span data-stu-id="c5572-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>


