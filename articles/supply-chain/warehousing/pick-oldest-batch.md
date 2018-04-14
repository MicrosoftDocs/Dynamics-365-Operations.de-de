---
title: "Älteste Charge auf einem mobilen Gerät entnehmen"
description: "In diesem Thema wird beschrieben, wie Sie die Optionen für die älteste Charge auf einem mobilen Gerät einrichten und anwenden."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8e5ddb8991d98aafc0a18788107ee65f0a950059
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="4c433-103">Älteste Charge auf einem mobilen Gerät entnehmen</span><span class="sxs-lookup"><span data-stu-id="4c433-103">Pick oldest batch on a mobile device</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="4c433-104">Sie können auf die Konfiguration **Älteste Charge entnehmen** über ein Menü auf dem mobilen Gerät zugreifen. Zudem können Sie Arbeitskräfte zwingen oder warnen, die älteste Charge an deren aktuellen Lagerplatz zu entnehmen.</span><span class="sxs-lookup"><span data-stu-id="4c433-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="4c433-105">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="4c433-105">Where it applies</span></span>
<span data-ttu-id="4c433-106">Die Entnahme der ältesten Charge wird über Menüoptionen auf dem mobilen Gerät konfiguriert und wirkt sich auf die Entnahme von Artikeln der ältesten Charge aus.</span><span class="sxs-lookup"><span data-stu-id="4c433-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="4c433-107">So richten Sie die Konfiguration für die Entnahme der ältesten Charge ein</span><span class="sxs-lookup"><span data-stu-id="4c433-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="4c433-108">Für Artikel, die für vorhandene Arbeit genutzt werden sollen, können Sie über das Menü des mobilen Geräts die Option für **Älteste Charge entnehmen** auf Werte wie **Keine**, **Warnen** oder **Erzwingen** setzen.</span><span class="sxs-lookup"><span data-stu-id="4c433-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="4c433-109">**Keine**: Arbeitskräfte enthalten keine Nachrichten. Sie sind befugt, jede Charge von ihrem Lagerplatz zu entnehmen.</span><span class="sxs-lookup"><span data-stu-id="4c433-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="4c433-110">**Warnen** und **Erzwingen**: Eine Liste der Chargen mit dem ältesten Ablaufdatum wird über der Chargenkontrolle anzeigt, wenn die Arbeitskraft eine Charge auswählt.</span><span class="sxs-lookup"><span data-stu-id="4c433-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="4c433-111">Wenn der Speicherort durch Ladungsträger kontrolliert wird, wird eine Liste mit Ladungsträgern, bei denen die älteste Charge über der Ladungsträgerkontrolle erscheint, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c433-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="4c433-112">**Warnen**: Wenn die Arbeitskraft einen Ladungsträger oder eine Charge auswählt, die nicht auf der Liste angezeigt wird, ist das Steuerelement leer und es wird eine Warnung angezeigt, dass eine ältere Charge ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c433-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="4c433-113">Damit die Arbeitskraft mit der Arbeit fortfahren kann, kann Sie denselben Ladungsträger oder dieselbe Charge erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="4c433-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="4c433-114">**Erzwingen**: Arbeitskräfte erhalten weiterhin Meldung dahingehend, dass eine ältere Charge zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="4c433-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

