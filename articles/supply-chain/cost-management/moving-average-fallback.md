---
title: Flexible durchschnittliche Fallback-Kostensequenz
description: Dieses Thema enthält Informationen zu Fallback-Kostensequenzen für Berechnungen des flexiblen Durchschnitts in Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: AnnBe
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b2172dfbec0a7f0fa25a081e4d92635a09f00e46
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261333"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="6e8db-103">Flexible durchschnittliche Fallback-Kostensequenz</span><span class="sxs-lookup"><span data-stu-id="6e8db-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="6e8db-104">Eine Möglichkeit, die Kosten Ihres Inventars zu berechnen, ist die Verwendung von einem _flexiblens Durschnitt_.</span><span class="sxs-lookup"><span data-stu-id="6e8db-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="6e8db-105">Jedem Inventargegenstand können bis zu drei Kostenwerte zugeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="6e8db-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="6e8db-106">**Letztes Problem** – Die letzten Ausgabekosten, die zugewiesen wurden, bevor der Lagerbestand negativ wurde</span><span class="sxs-lookup"><span data-stu-id="6e8db-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="6e8db-107">**Aktive Kosten** – Die letzten Kosten, die in einer Kalkulationsversion aktiviert wurden</span><span class="sxs-lookup"><span data-stu-id="6e8db-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="6e8db-108">**Stückpreis** – Die Kosten, die für das freigegebene Produkt angegeben sind</span><span class="sxs-lookup"><span data-stu-id="6e8db-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="6e8db-109">Um zu bestimmen, welcher dieser Kostenwerte für Berechnungen des flexiblen Durchschnitts verwendet werden soll, verwendet das System eine _Fallback-Kostenfolge_, um die Präferenzreihenfolge für die Werte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6e8db-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="6e8db-110">Wenn der bevorzugte Kostenwert nicht verfügbar ist, verwendet das System den nächstvorzugten Wert usw.</span><span class="sxs-lookup"><span data-stu-id="6e8db-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="6e8db-111">In früheren Versionen von Microsoft Dynamics 365 Supply Chain Management verwendete das System eine feste Fallback-Kostensequenz (_Letzte Ausgabe – Aktive Kosten – Artikelpreis_).</span><span class="sxs-lookup"><span data-stu-id="6e8db-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="6e8db-112">In Version 10.0.11 ist diese Sequenz immer noch die Standardsequenz.</span><span class="sxs-lookup"><span data-stu-id="6e8db-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="6e8db-113">Sie können jedoch auch eine Funktion aktivieren, mit der Sie zwischen drei verfügbare Fallback-Kostensequenzen auswählen können.</span><span class="sxs-lookup"><span data-stu-id="6e8db-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="6e8db-114">Diese Funktion kann besonders nützlich sein für Organisationen, die regelmäßig negative Inventarwerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e8db-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="6e8db-115">Um den Selektor für die Fallback-Kostensequenz verfügbar zu machen, müssen Sie (oder ein Administrator) [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um die benannte Funktion _Gleitende durchschnittliche Fallback-Kostenfolge_ zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6e8db-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="6e8db-116">Führen Sie die folgenden Schritte aus, um die Fallback-Kostenfolge für Berechnungen des flexiblen Durchschnitts auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="6e8db-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="6e8db-117">Öffnen der Seite **Parameter**:</span><span class="sxs-lookup"><span data-stu-id="6e8db-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="6e8db-118">Auf der Registerkarte **Bestandsbuchhaltung** im Abschnitt **Gleitender Durchschnitt** stellen Sie legen Sie das Feld **Fallback-Kostenfolge** auf einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="6e8db-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="6e8db-119">**Letzte Ausgabe – Aktive Kosten – Artikelpreis** – Diese Sequenz ist die Standardsequenz.</span><span class="sxs-lookup"><span data-stu-id="6e8db-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="6e8db-120">Es ist die gleiche Sequenz, die verwendet wird, wenn die _Gleitende durchschnittliche Fallback-Kostenfolge_ Funktion nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6e8db-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="6e8db-121">**Aktive Kosten – Letztes Problem**</span><span class="sxs-lookup"><span data-stu-id="6e8db-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="6e8db-122">**Aktive Kosten – Artikelpreis** – Organisationen können Leistungsprobleme haben, wenn sie Geschäftsprozesse verwenden, bei denen der Lagerbestand regelmäßig negativ wird und gleichzeitig das Transaktionsvolumen hoch ist.</span><span class="sxs-lookup"><span data-stu-id="6e8db-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="6e8db-123">Diese Einstellung kann dazu beitragen, diese Leistungsprobleme zu verringern.</span><span class="sxs-lookup"><span data-stu-id="6e8db-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="6e8db-124">![Bestandsbuchhaltungsparameter](media/inventory-accounting-parameters.png "Bestandsbuchhaltungsparameter")</span><span class="sxs-lookup"><span data-stu-id="6e8db-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
