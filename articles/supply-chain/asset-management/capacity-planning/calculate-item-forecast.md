---
title: Artikelprognose berechnen
description: In diesem Thema wird erläutert, wie die Artikelplanung in der Anlagenverwaltung berechnet wird.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f8f38ac7bfb270f648cd561da50ee5477721ab47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428820"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="c5cad-103">Artikelprognose berechnen</span><span class="sxs-lookup"><span data-stu-id="c5cad-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c5cad-104">Ebenso wie Sie Kapazitätsauslastungsberechnungen durchführen können, die im vorherigen Abschnitt beschrieben sind, können Sie Artikelplanungsberechnungen durchführen für</span><span class="sxs-lookup"><span data-stu-id="c5cad-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="c5cad-105">Wartungszeitplanpositionen</span><span class="sxs-lookup"><span data-stu-id="c5cad-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="c5cad-106">Arbeitsaufträge, die noch nicht geplant wurden</span><span class="sxs-lookup"><span data-stu-id="c5cad-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="c5cad-107">Geplante Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="c5cad-107">scheduled work orders</span></span>

<span data-ttu-id="c5cad-108">Dies ist hilfreich, wenn Sie einen Überblick über den erwarteten Artikelverbrauch (Ersatzteile sowie andere Artikel, die für die Ausführung von Arbeitsaufträgen erforderlich sind) während einer bestimmten Periode erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="c5cad-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="c5cad-109">Die Berechnung der Artikelplanung kann für alle oder ausgewählte Anlagen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c5cad-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="c5cad-110">Sie können eine Berechnung auch für eine Wartungsausfallzeitaktivität (**Alle Wartungsausfallzeitaktivitäten** oder **Aktive Wartungsausfallzeitaktivitäten**) oder für einen Arbeitsauftragspool (**Alle Arbeitsauftragspools** oder **Aktive Arbeitsauftragspools**) vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c5cad-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="c5cad-111">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Artikelplanung** oder **Anlagenverwaltung** > **Allgemein** > **Arbeitsauftragspools** > **Alle Arbeitsauftragspools** / **Aktive Arbeitsauftragspools** > Arbeitsauftragspool in der Liste auswählen > Schaltfläche **Artikelplanung** oder **Anlagenverwaltung** > **Allgemein** > **Wartungsausfallzeitaktivitäten** > **Alle Wartungsausfallzeitaktivitäten** / **Aktive Wartungsausfallzeitaktivitäten** > Wartungsausfallzeitaktivität in der Liste auswählen > Schaltfläche **Artikelplanung**.</span><span class="sxs-lookup"><span data-stu-id="c5cad-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="c5cad-112">Wählen Sie im Dialogfeld **Artikelprognose berechnen** eine Periode für die Berechnung in den Feldern **Startdatum/-uhrzeit** und **Enddatum/-uhrzeit** aus.</span><span class="sxs-lookup"><span data-stu-id="c5cad-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="c5cad-113">Wählen Sie „Ja“ auf der Umschaltschaltfläche **Wartungszeitplan einbeziehen** aus, wenn Sie Wartungszeitplanpositionen in die Planungsberechnung einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="c5cad-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="c5cad-114">Wählen Sie „Ja“ auf der Umschaltschaltfläche **Arbeitsauftrag einbeziehen** aus, wenn Sie Arbeitsauftragspositionen in die Planungsberechnung einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="c5cad-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="c5cad-115">Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Artikelplanungspositionen bezüglich funktionaler Standorte sein sollen.</span><span class="sxs-lookup"><span data-stu-id="c5cad-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="c5cad-116">Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Wartungszeitplanpositionen und Arbeitsaufträge für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c5cad-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="c5cad-117">Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Wartungszeitplanpositionen und allen Arbeitsaufträgen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c5cad-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="c5cad-118">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="c5cad-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="c5cad-119">In den Gruppen **Gruppieren nach…** klicken Sie auf die entsprechenden Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c5cad-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c5cad-120">Im Screenshot unten werden die ausgewählten **Gruppieren nach**-Schaltflächen in blauer Farbe hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="c5cad-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="c5cad-121">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5cad-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="c5cad-122">Klicken Sie auf die Schaltfläche **Dimensionen anzeigen**, wenn Sie das Produktdimensionen, die Lagerdimensionen oder die Rückverfolgungsangaben anzeigen möchten, die Artikeln zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c5cad-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="c5cad-123">Aktivieren Sie die relevanten Kontrollkästchen, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5cad-123">Select the relevant check boxes, and click **OK**.</span></span>

![Abbildung 1](media/02-capacity-planning.png)
