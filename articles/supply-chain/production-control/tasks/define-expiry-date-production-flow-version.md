---
title: Ablaufdatum für eine Produktionsflussversion definieren
description: Um die Gültigkeitsdauer und die Verarbeitung einer Produktionsflussversion an einem bestimmten Datum zu beenden, oder den Ersatz einer aktiven Version mit einer neuen Version zu planen, müssen Sie ein Ablaufdatum für die Version festgelegt.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 87063653eb78209caaefd3fafa7783f425e710b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257290"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="593d9-103">Ablaufdatum für eine Produktionsflussversion definieren</span><span class="sxs-lookup"><span data-stu-id="593d9-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="593d9-104">Um die Gültigkeitsdauer und die Verarbeitung einer Produktionsflussversion an einem bestimmten Datum zu beenden, oder den Ersatz einer aktiven Version mit einer neuen Version zu planen, müssen Sie ein Ablaufdatum für die Version festgelegt.</span><span class="sxs-lookup"><span data-stu-id="593d9-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="593d9-105">Es ist nicht erforderlich, die Version zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="593d9-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="593d9-106">Wählen Sie ein Ablaufdatum, um eine Produktionsflussversion zu beenden</span><span class="sxs-lookup"><span data-stu-id="593d9-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="593d9-107">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="593d9-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="593d9-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="593d9-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="593d9-109">Wählen einen Produktionsfluss aus, der eine Version aufweist, die bereits definiert ist.</span><span class="sxs-lookup"><span data-stu-id="593d9-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="593d9-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="593d9-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="593d9-111">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="593d9-111">Click Edit.</span></span>
5. <span data-ttu-id="593d9-112">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="593d9-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="593d9-113">Geben Sie im Feld "Ablaufdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="593d9-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="593d9-114">Zum Ablaufdatum wird keine neue Version gestartet oder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="593d9-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="593d9-115">Es ist nicht mehr möglich, Einzelvorgänge für den Produktionsfluss zu erstellen oder zu starten.</span><span class="sxs-lookup"><span data-stu-id="593d9-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="593d9-116">Können Sie gestartete Einzelvorgänge nach Ablaufdatum noch ausführen.</span><span class="sxs-lookup"><span data-stu-id="593d9-116">You can still complete started jobs after the expiration date.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]