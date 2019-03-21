---
title: Workflow-FAQs
description: Diese Thema enthält Antworten auf häufig gestellte Fragen zum Workflowsystem in Microsoft Dynamics 365 for Finance and Operations
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
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
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2019
ms.locfileid: "773211"
---
# <a name="workflow-system"></a><span data-ttu-id="16ac9-103">Workflowsystem</span><span class="sxs-lookup"><span data-stu-id="16ac9-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16ac9-104">Diese Thema enthält Antworten auf häufig gestellte Fragen zum Workflowsystem in Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="16ac9-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="16ac9-105">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="16ac9-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="16ac9-106">Warum erhalte ich mehrere Benachrichtigungen, wenn eine Arbeitsaufgabe abgelehnt wird?</span><span class="sxs-lookup"><span data-stu-id="16ac9-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="16ac9-107">Wenn eine Arbeitsaufgabe abgelehnt wird, erscheint die Arbeitsaufgabe als wegen Ablehnung beendet.</span><span class="sxs-lookup"><span data-stu-id="16ac9-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="16ac9-108">Dem Ersteller wird eine andere Arbeitsaufgabe erstellt und zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="16ac9-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="16ac9-109">Das bedeutet, dass eine Benachrichtigung zur abgelehnten Arbeitsaufgabe an den Ersteller und eine separate Benachrichtigung an den Benutzer gesendet wird, dem die neue „Änderung angefordert“-Arbeitsaufgabe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="16ac9-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="16ac9-110">Jede Benachrichtigung gilt für eine andere Arbeitsaufgabe, die Ähnlichkeit kann jedoch zu Unklarheiten führen.</span><span class="sxs-lookup"><span data-stu-id="16ac9-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="16ac9-111">Wir suchen nach Wegen, dies in einer späteren Versionen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="16ac9-111">We are looking at ways to improve this in a future release.</span></span>
