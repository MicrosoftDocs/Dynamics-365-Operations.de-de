---
title: Workflow-FAQs
description: Diese Thema enthält Antworten auf häufig gestellte Fragen zum Workflowsystem in Microsoft Dynamics 365 for Finance and Operations
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509290"
---
# <a name="workflow-system"></a><span data-ttu-id="d9cb1-103">Workflowsystem</span><span class="sxs-lookup"><span data-stu-id="d9cb1-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9cb1-104">Diese Thema enthält Antworten auf häufig gestellte Fragen zum Workflowsystem in Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d9cb1-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="d9cb1-105">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="d9cb1-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="d9cb1-106">Warum erhalte ich mehrere Benachrichtigungen, wenn eine Arbeitsaufgabe abgelehnt wird?</span><span class="sxs-lookup"><span data-stu-id="d9cb1-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="d9cb1-107">Wenn eine Arbeitsaufgabe abgelehnt wird, erscheint die Arbeitsaufgabe als wegen Ablehnung beendet.</span><span class="sxs-lookup"><span data-stu-id="d9cb1-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="d9cb1-108">Dem Ersteller wird eine andere Arbeitsaufgabe erstellt und zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d9cb1-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="d9cb1-109">Das bedeutet, dass eine Benachrichtigung zur abgelehnten Arbeitsaufgabe an den Ersteller und eine separate Benachrichtigung an den Benutzer gesendet wird, dem die neue „Änderung angefordert“-Arbeitsaufgabe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d9cb1-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="d9cb1-110">Jede Benachrichtigung gilt für eine andere Arbeitsaufgabe, die Ähnlichkeit kann jedoch zu Unklarheiten führen.</span><span class="sxs-lookup"><span data-stu-id="d9cb1-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="d9cb1-111">Wir suchen nach Wegen, dies in einer späteren Versionen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d9cb1-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="d9cb1-112">Warum schlagen meine Workflowexporte fehl?</span><span class="sxs-lookup"><span data-stu-id="d9cb1-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="d9cb1-113">Derzeit gibt es eine Einschränkung der Workflowexportfunktion, durch die Workflownamen 48 Zeichen nicht überschreiten können.</span><span class="sxs-lookup"><span data-stu-id="d9cb1-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="d9cb1-114">Das Verwenden eines Namens, der länger als 48 Zeichen ist, kann zu einem „Fehler beim Authentifizieren der Anforderung durch Server“ führen und/oder verhindern, dass eine Datei ohne Dateityp exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9cb1-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="d9cb1-115">Der folgende Blogbeitrag enthält weitere Details: [Workflow zur Exprotfehlerbehebung](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="d9cb1-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
