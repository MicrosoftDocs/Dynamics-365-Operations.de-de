---
title: Berechnen der Kapazitätsauslastung für geplante Arbeitsaufträge
description: In diesem Thema wird erläutert, wie die Kapazitätsauslastung für geplante Arbeitsaufträge in der Anlagenverwaltung berechnet wird.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5a6063db7a63975f439da9f20adec07de9103014
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264897"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="830d2-103">Berechnen der Kapazitätsauslastung für geplante Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="830d2-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="830d2-104">Sie können die Kapazitätsauslastung für geplante Arbeitsaufträge berechnen, um eine Übersicht der Arbeitsauslastung von Ressourcen für einen bestimmten Zeitraum zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="830d2-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="830d2-105">Berechnungen können für die folgenden Ressourcen vorgenommen werden: Wartungsarbeiter, Arbeitskraftgruppen, Werkzeuge und Anlagen.</span><span class="sxs-lookup"><span data-stu-id="830d2-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="830d2-106">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Planung** > **Kapazitätsauslastung**.</span><span class="sxs-lookup"><span data-stu-id="830d2-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="830d2-107">Wählen Sie im Dialogfeld **Kapazitätsauslastung berechnen** > **Anzeigen** aus, welchen Auslastungstyp Sie berechnen möchten: **Kapazität**, **Reserviert** oder **Rest**.</span><span class="sxs-lookup"><span data-stu-id="830d2-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="830d2-108">Wählen Sie **Ja** auf der Umschaltfläche **Null überspringen** aus, wenn keine Ergebnisse mit Null angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="830d2-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="830d2-109">Wählen Sie die Ressourcentypen aus, für die Sie die Kapazitätsauslastung berechnen möchten, indem Sie **Ja** auf den relevanten Umschaltschaltflächen auswählen: **Arbeitskraft**, **Wartungsarbeitergruppe**, **Werkzeug** und **Anlage**.</span><span class="sxs-lookup"><span data-stu-id="830d2-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="830d2-110">Wählen Sie das Startdatum für die Berechnung im Feld **Von Datum** aus.</span><span class="sxs-lookup"><span data-stu-id="830d2-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="830d2-111">Im Feld **Intervalltyp** wählen Sie das Intervall für die Kalkulation aus: **Tag**, **Woche**, **Monat** oder **Quartal**.</span><span class="sxs-lookup"><span data-stu-id="830d2-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="830d2-112">Fügen Sie im Feld **Periodenhäufigkeit** die Anzahl der Intervalle ein, für die Sie eine Kalkulation ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="830d2-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="830d2-113">Wenn Sie beispielsweise **Tag** als Intervalltyp ausgewählt haben und Sie die Zahl „5“ in diesem Feld eingeben, wird eine Berechnung von fünf Tagen ab dem Startdatum vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="830d2-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="830d2-114">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="830d2-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="830d2-115">Die Abbildung unten zeigt das Ergebnis einer Berechnung, die drei Wochen abdeckt, für den Auslastungstyp **Reserviert**.</span><span class="sxs-lookup"><span data-stu-id="830d2-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Abbildung 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="830d2-117">Wenn Sie Auslastungstypen **Kapazität** oder **Rest** für die Berechnung auswählen, wird dasselbe Ergebnis angezeigt, wenn keine Reservierungen für die Ressourcen in der ausgewählten Periode vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="830d2-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="830d2-118">Weitere Informationen darüber, wie die Kapazitätsauslastung für Wartungsplanpositionen und nicht geplante Arbeitsaufträge berechnet wird, finden Sie unter [Berechnen der Kapazitätsauslastung](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="830d2-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]