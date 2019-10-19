---
title: Kapazitätsauslastung berechnen
description: In diesem Thema wird erläutert, wie die Kapazitätsauslastung in der Anlagenverwaltung berechnet wird.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 82f65293679591f278e0e3b79c112ba36debc3bb
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2277942"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="c2cc1-103">Kapazitätsauslastung berechnen</span><span class="sxs-lookup"><span data-stu-id="c2cc1-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="c2cc1-104">In der Anlagenverwaltung können Sie die Kapazitätsauslastung berechnen für</span><span class="sxs-lookup"><span data-stu-id="c2cc1-104">In Asset Management, you can calculate capacity load on</span></span>

- <span data-ttu-id="c2cc1-105">Wartungszeitplanpositionen</span><span class="sxs-lookup"><span data-stu-id="c2cc1-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="c2cc1-106">Arbeitsaufträge, die noch nicht geplant wurden</span><span class="sxs-lookup"><span data-stu-id="c2cc1-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="c2cc1-107">Geplante Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="c2cc1-107">scheduled work orders</span></span>

<span data-ttu-id="c2cc1-108">Dies ist hilfreich, wenn Sie einen Überblick über die erwarteten Kapazitätsauslastung während einer bestimmten Periode erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="c2cc1-109">Die Berechnung der Kapazitätsauslastung kann für alle oder ausgewählte Anlagen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="c2cc1-110">Sie können auch eine Berechnung für Wartungsausfallzeitaktivitäten oder Arbeitsauftragspools erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="c2cc1-111">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Kapazitätsauslastung** oder **Anlagenverwaltung** > **Allgemein** > **Arbeitsauftragspools** > **Alle Arbeitsauftragspools** / **Aktive Arbeitsauftragspools** > Arbeitsauftragspool in der Liste auswählen > Schaltfläche **Kapazitätsauslastung** oder **Anlagenverwaltung** > **Allgemein** > **Wartungsausfallzeitaktivitäten** > **Alle Wartungsausfallzeitaktivitäten** / **Aktive Wartungsausfallzeitaktivitäten** > Wartungsausfallzeitaktivität in der Liste auswählen > Schaltfläche **Kapazitätsauslastung**.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="c2cc1-112">Wählen Sie im Dialogfeld **Kapazitätsauslastung berechnen** eine Periode für die Berechnung in den Feldern **Startdatum/-uhrzeit** und **Enddatum/-uhrzeit** aus.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="c2cc1-113">Wählen Sie „Ja“ auf der Umschaltschaltfläche **Wartungszeitplan einbeziehen** aus, wenn Sie Wartungszeitplanpositionen in die Berechnung einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="c2cc1-114">Wählen Sie „Ja“ auf der Umschaltschaltfläche **Arbeitsauftrag einbeziehen** aus, wenn Sie Arbeitsauftragspositionen in die Berechnung einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="c2cc1-115">Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Kapazitätsauslastungspositionen bezüglich funktionaler Standorte sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> <span data-ttu-id="c2cc1-116">Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Wartungszeitplanpositionen und Arbeitsaufträge für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="c2cc1-117">Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Wartungszeitplanpositionen und allen Arbeitsaufträgen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="c2cc1-118">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="c2cc1-119">In den Aktivitätsbereichsgruppen **Gruppieren nach…** klicken Sie auf die entsprechenden Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-119">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c2cc1-120">Die ausgewählten Schaltflächen der Aktivitätsbereichsgruppen werden blau hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-120">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="c2cc1-121">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-121">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="c2cc1-122">Die folgende Abbildung zeigt ein Beispiel der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="c2cc1-122">The figure below shows an example of the interface.</span></span>

![Abbildung 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="c2cc1-124">Wenn Sie sich nur auf die Kapazitätsplanung bezüglich geplanter Arbeitsaufträge konzentrieren möchten, finden Sie Informationen unter [Berechnen der Kapazitätsauslastung für geplante Arbeitsaufträge](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="c2cc1-124">If you want to focus only on capacity planning regarding scheduled work orders, refer to [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

