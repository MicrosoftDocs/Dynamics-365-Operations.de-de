--- 
title: "Eingeben einer Anlagenerweiterung für eine Anlage"
description: "Diese Prozedur zeigt an, wie einer vorhandenen Anlage einer Erweiterung hinzugefügt wird."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 4c22fb105d0deedda1b7dbfdd919d1745ad0ca2f
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="8224e-103">Eingeben einer Anlagenerweiterung für eine Anlage</span><span class="sxs-lookup"><span data-stu-id="8224e-103">Enter an addition to a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8224e-104">Diese Prozedur zeigt an, wie einer vorhandenen Anlage einer Erweiterung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8224e-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="8224e-105">Der Zweck der Anlagenerweiterungen besteht darin, Artikelerweiterungen, Verwaltung oder Verbesserungen für eine Anlage nachzuverfolgen und dient nur zur Information.</span><span class="sxs-lookup"><span data-stu-id="8224e-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="8224e-106">Sämtliche Änderungen am Anlagenwert oder der Nutzungsdauer müssen separat vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="8224e-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="8224e-107">Die Prozedur verwendet die "Buchhalterrolle" und die Demodaten für die juristische Person USMF.</span><span class="sxs-lookup"><span data-stu-id="8224e-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="8224e-108">Wechseln Sie zu Anlagen > Anlagen > Anlagen.</span><span class="sxs-lookup"><span data-stu-id="8224e-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="8224e-109">Suchen Sie in der Liste die Anlage für die Erweiterung und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="8224e-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="8224e-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8224e-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8224e-111">Klicken Sie im Aktivitätsbereich auf "Anlage".</span><span class="sxs-lookup"><span data-stu-id="8224e-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="8224e-112">Klicken Sie auf "Anlagenerweiterungen".</span><span class="sxs-lookup"><span data-stu-id="8224e-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="8224e-113">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="8224e-113">Click New.</span></span>
7. <span data-ttu-id="8224e-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8224e-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="8224e-115">Legen Sie das Datum des Erweiterungseinkaufs oder des Erweiterungsdienstes fest.</span><span class="sxs-lookup"><span data-stu-id="8224e-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="8224e-116">Geben Sie die Kosten für den Artikel, die Wartung oder für andere Verbesserungen für die Anlage ein.</span><span class="sxs-lookup"><span data-stu-id="8224e-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="8224e-117">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8224e-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8224e-118">Die Gesamtkosten haben keine Auswirkungen auf den Wert der Anlage und dienen nur Nachverfolgungs- und Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="8224e-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="8224e-119">Wenn die Kosten aktiviert werden, muss eine Höherbewertungstransaktion separat gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="8224e-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="8224e-120">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="8224e-120">Click the General tab.</span></span>
    * <span data-ttu-id="8224e-121">Legen Sie "Verlängert die Nutzungsdauer" fest, falls die Erweiterung die Nutzungsdauer der Anlage erhöht.</span><span class="sxs-lookup"><span data-stu-id="8224e-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="8224e-122">Dieses Feld dient nur zur Information.</span><span class="sxs-lookup"><span data-stu-id="8224e-122">This field is informational only.</span></span> <span data-ttu-id="8224e-123">Um die Nutzungsdauer zu erhöhen, ändern Sie die "Nutzungsdauer" in den "Wertmodellen" und/oder den "Abschreibungsbüchern" für die Anlage.</span><span class="sxs-lookup"><span data-stu-id="8224e-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  


