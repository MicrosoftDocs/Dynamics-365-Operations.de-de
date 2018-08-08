--- 
title: "Ablaufdatum für eine Produktionsflussversion definieren"
description: "Um die Gültigkeitsdauer und die Verarbeitung einer Produktionsflussversion an einem bestimmten Datum zu beenden, oder den Ersatz einer aktiven Version mit einer neuen Version zu planen, müssen Sie ein Ablaufdatum für die Version festgelegt."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e12452feb5ac91917848abbb710b80f86b4cb6e9
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="57500-103">Ablaufdatum für eine Produktionsflussversion definieren</span><span class="sxs-lookup"><span data-stu-id="57500-103">Define an expiry date for a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57500-104">Um die Gültigkeitsdauer und die Verarbeitung einer Produktionsflussversion an einem bestimmten Datum zu beenden, oder den Ersatz einer aktiven Version mit einer neuen Version zu planen, müssen Sie ein Ablaufdatum für die Version festgelegt.</span><span class="sxs-lookup"><span data-stu-id="57500-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="57500-105">Es ist nicht erforderlich, die Version zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="57500-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="57500-106">Wählen Sie ein Ablaufdatum, um eine Produktionsflussversion zu beenden</span><span class="sxs-lookup"><span data-stu-id="57500-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="57500-107">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="57500-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="57500-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="57500-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57500-109">Wählen einen Produktionsfluss aus, der eine Version aufweist, die bereits definiert ist.</span><span class="sxs-lookup"><span data-stu-id="57500-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="57500-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="57500-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="57500-111">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="57500-111">Click Edit.</span></span>
5. <span data-ttu-id="57500-112">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="57500-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="57500-113">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="57500-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="57500-114">Zum Ablaufdatum wird keine neue Version gestartet oder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="57500-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="57500-115">Es ist nicht mehr möglich, Einzelvorgänge für den Produktionsfluss zu erstellen oder zu starten.</span><span class="sxs-lookup"><span data-stu-id="57500-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="57500-116">Können Sie gestartete Einzelvorgänge nach Ablaufdatum noch ausführen.</span><span class="sxs-lookup"><span data-stu-id="57500-116">You can still complete started jobs after the expiration date.</span></span>  


