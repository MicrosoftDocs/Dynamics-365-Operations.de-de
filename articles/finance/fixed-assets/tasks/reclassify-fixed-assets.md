---
title: Anlagen umgliedern
description: Wenn Sie eine Anlage umgliedern möchten, müssen Sie sie in eine neue Anlagengruppe übertragen oder ihr eine neue Anlagennummer in der gleichen Gruppe zuordnen.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cfc1425aca7a62205e0c7c50237f206a179a0e7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968853"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="61546-103">Anlagen umgliedern</span><span class="sxs-lookup"><span data-stu-id="61546-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61546-104">Wenn Sie eine Anlage umgliedern möchten, müssen Sie sie in eine neue Anlagengruppe übertragen oder ihr eine neue Anlagennummer in der gleichen Gruppe zuordnen.</span><span class="sxs-lookup"><span data-stu-id="61546-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="61546-105">Wenn eine Anlage neu klassifiziert wird:</span><span class="sxs-lookup"><span data-stu-id="61546-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="61546-106">Alle Bücher für die vorhandene Anlage werden für die neue Anlage erstellt.</span><span class="sxs-lookup"><span data-stu-id="61546-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="61546-107">Alle für die ursprüngliche Anlage eingerichteten Daten werden in die neue Anlage kopiert.</span><span class="sxs-lookup"><span data-stu-id="61546-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="61546-108">Der Status der Bücher für die ursprüngliche Anlage lautet „Geschlossen“.</span><span class="sxs-lookup"><span data-stu-id="61546-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="61546-109">Bei den neuen Büchern der neuen Anlage ist das Neuklassifizierungsdatum im Feld **Anschafungsdatum** enthalten.</span><span class="sxs-lookup"><span data-stu-id="61546-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="61546-110">Das Datum im Feld **Ausführungsdatum der Abschreibung** stammt aus den ursprünglichen Informationen der Anlage.</span><span class="sxs-lookup"><span data-stu-id="61546-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="61546-111">Hat die Abschreibung bereits begonnen, zeigt das Feld **Datum der letzten Abschreibung** das Datum der letzten Neuklassifizierung an.</span><span class="sxs-lookup"><span data-stu-id="61546-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="61546-112">Die vorhandenen Anlagenbuchungen für die ursprüngliche Anlage werden storniert und für die neue Anlage neu generiert.</span><span class="sxs-lookup"><span data-stu-id="61546-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="61546-113">Gehen Sie folgendermaßen vor, um eine Anlage neu zu klassifizieren:</span><span class="sxs-lookup"><span data-stu-id="61546-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="61546-114">Wechseln Sie zu **Anlagen > Periodische Aufgaben > Neuklassifizierung**.</span><span class="sxs-lookup"><span data-stu-id="61546-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="61546-115">Wählen Sie im Feld **Anlagengruppe** die Gruppe aus, die neu klassifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="61546-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="61546-116">Wählen Sie im Feld **Anlagennummer** die Anlage aus, die neu klassifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="61546-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="61546-117">Wählen Sie im Feld **Neue Anlagengruppe** eine Gruppe aus, an die die Anlage übertragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="61546-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="61546-118">Wenn die neue Anlagengruppe einem Nummernkreis zugeordnet ist, wird das Feld **Neue Anlagennummer** mit der Nummer aus dem Nummernkreis für die neue Anlagengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="61546-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="61546-119">Anderenfalls wird das Feld **Neue Anlagennummer** mit der Nummer aus dem Nummernkreis aktualisiert, der auf der Seite **Anlagenparameter** eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="61546-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="61546-120">Wenn ein Nummernkreis nicht auf der Seite **Anlagenparameter** eingerichtet ist, geben Sie eine Nummer im Feld **Neue Anlagennummer** ein.</span><span class="sxs-lookup"><span data-stu-id="61546-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="61546-121">Geben Sie im Feld **Neuklassifizierungsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="61546-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="61546-122">Geben Sie im Feld **Belegserie** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="61546-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="61546-123">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="61546-123">Click **OK**.</span></span>
