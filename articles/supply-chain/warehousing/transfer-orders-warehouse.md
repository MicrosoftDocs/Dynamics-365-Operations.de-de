---
title: Einrichten von Lagerorten für Umlagerungsaufträge
description: In diesem Thema wird beschrieben, wie Sie Lager für Transportaufträge einrichten können.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 8111601cb2948c66097b0f5b2f261b7462b279f9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "337462"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="1ad96-103">Einrichten von Lagerorten für Umlagerungsaufträge</span><span class="sxs-lookup"><span data-stu-id="1ad96-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ad96-104">Mithilfe von Lagerortebenen kann eine Hierarchie erstellt werden, die Umlagerungsaufträge zwischen Lagerorten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ad96-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="1ad96-105">Basierend auf dieser Einstellung berechnet die Produktprogrammplanung den Artikelbedarf auf den einzelnen Lagerortebenen und generiert geplante Umlagerungsaufträge von einem zugeordneten Quelllagerort, um diesen Artikelbedarf zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="1ad96-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="1ad96-106">Klicken Sie auf **Bestandsverwaltung > Einstellungen > Lageraufschlüsselung > Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="1ad96-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="1ad96-107">Wählen Sie den Lagerort aus, der aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ad96-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="1ad96-108">Aktivieren Sie auf der **Masterplanungs**-FastTab das Kontrollkästchen **Nachfüllen**.</span><span class="sxs-lookup"><span data-stu-id="1ad96-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="1ad96-109">Wählen Sie im Feld **Hauptlager** das Lager aus, das Sie als Nachfülllager zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="1ad96-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="1ad96-110">Die Produktprogrammplanung berechnet eine Umlagerungsanforderung für den ausgewählten Lagerort und generiert einen geplanten Umlagerungsauftrag vom zugewiesenen **Hauptlager**.</span><span class="sxs-lookup"><span data-stu-id="1ad96-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="1ad96-111">Wenn Sie das Feld <STRONG>Wird aufgefüllt</STRONG> deaktivieren lassen, wird dem ausgewählten Lagerort eine Lagerortebene in Bezug zum <STRONG>Auffülllagerort</STRONG> zugewiesen, der <STRONG>Auffülllagerort</STRONG> wird jedoch nicht als Lagerort für Auffüllungen eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="1ad96-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="1ad96-112">Schließt die Seite, um die neuen Einstellungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="1ad96-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="1ad96-113">Wenn Sie ein Lager zum Nachfüllen zuordnen möchten, müssen Sie das Lager zunächst als Lagerdimension auf der Seite <STRONG>Lagerdimensionsgruppen</STRONG> einrichten.</span><span class="sxs-lookup"><span data-stu-id="1ad96-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="1ad96-114">Wählen Sie auf dieser Seite das Feld <STRONG>Aktiv</STRONG> und das Feld <STRONG>Deckungsplan nach Dimension</STRONG> für das Lager aus.</span><span class="sxs-lookup"><span data-stu-id="1ad96-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="1ad96-115">Transportvorlaufzeit einrichten</span><span class="sxs-lookup"><span data-stu-id="1ad96-115">Set up transport lead time</span></span>

<span data-ttu-id="1ad96-116">Außerdem müssen Sie die Transportvorlaufzeit zwischen den Lagern auf der Seite **Transporttage** einstellen.</span><span class="sxs-lookup"><span data-stu-id="1ad96-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="1ad96-117">Gehen Sie zu **Bestandsverwaltung > Einrichtung > Verteilung > Transporttage**.</span><span class="sxs-lookup"><span data-stu-id="1ad96-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="1ad96-118">Wählen Sie im Feld **Empfangsstelle** die Option **Lager**.</span><span class="sxs-lookup"><span data-stu-id="1ad96-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="1ad96-119">Wählen Sie das **Versandlager**, das **Eingangslager** und die **Transporttage** aus.</span><span class="sxs-lookup"><span data-stu-id="1ad96-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="1ad96-120">(Optional) Sie können die Transportzeit je nach Lieferart auch unter der Registerkarte **Transporttage pro Lieferart** einstellen.</span><span class="sxs-lookup"><span data-stu-id="1ad96-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>