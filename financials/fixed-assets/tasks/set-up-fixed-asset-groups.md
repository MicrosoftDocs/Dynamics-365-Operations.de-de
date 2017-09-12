--- 
title: Anlagengruppen einrichten
description: Diese Prozedur zeigt, wie eine neue Anlagengruppe erstellt wird.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c44ce1219c0fc860d621aa32c8eec7c5d640fa03
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="a0f65-103">Anlagengruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="a0f65-103">Set up fixed asset groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0f65-104">Diese Prozedur zeigt, wie eine neue Anlagengruppe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a0f65-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="a0f65-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0f65-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="a0f65-106">Wechseln Sie zu Anlagen > Einstellungen > Anlagengruppen.</span><span class="sxs-lookup"><span data-stu-id="a0f65-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="a0f65-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a0f65-107">Click New.</span></span>
3. <span data-ttu-id="a0f65-108">Geben Sie im Feld "Anlagengruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a0f65-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="a0f65-109">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a0f65-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a0f65-110">"Anlagen automatisch nummerieren" und "Nummernkreiscode" zur "Anlagengruppe" überschreiben die Einstellungen zu den "Anlagenparametern".</span><span class="sxs-lookup"><span data-stu-id="a0f65-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="a0f65-111">Sie können sie hier ändern, wenn die Anlagen in dieser Anlagengruppe eine andere Nummerierung als andere Gruppen haben.</span><span class="sxs-lookup"><span data-stu-id="a0f65-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="a0f65-112">Klicken Sie auf Bücher.</span><span class="sxs-lookup"><span data-stu-id="a0f65-112">Click Books.</span></span>
6. <span data-ttu-id="a0f65-113">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a0f65-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="a0f65-114">Das Feld „Abschreibung berechnen” ist auf „Ja” festgelegt, daher wird das Anlagenbuch in die Abschreibungsvorschläge einbezogen.</span><span class="sxs-lookup"><span data-stu-id="a0f65-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="a0f65-115">Wenn "Abschreibung berechnen" auf "Nein" festgelegt ist, wird die Anlage automatisch abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="a0f65-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="a0f65-116">Legen Sie die Nutzungsdauer der Anlage in Jahren fest.</span><span class="sxs-lookup"><span data-stu-id="a0f65-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="a0f65-117">Beachten Sie, dass der Feldwert "Abschreibungszeiträume" nach der Festlegung der "Nutzungsdauer" berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="a0f65-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="a0f65-118">Wählen Sie im Feld "Abschreibungskonvention" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="a0f65-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="a0f65-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a0f65-119">Close the page.</span></span>


