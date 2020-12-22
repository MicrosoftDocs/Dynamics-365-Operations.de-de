---
title: Umsatzerkennungsübersicht
description: Dieses Thema enthält Informationen zur Umsatzerkennungsfunktion. Diese Funktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln zur Erfassung des Umsatzerlöspreises und des Umsatzerlöszeitplans für Aufträge mit mehreren Elementen definieren können.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4459115"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="9a2d4-104">Umsatzerkennungsübersicht</span><span class="sxs-lookup"><span data-stu-id="9a2d4-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9a2d4-105">Die Umsatzerkennungsfunktion kann nicht über die Funktionsverwaltung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="9a2d4-106">Sie müssen derzeit Konfigurationsschlüssel verwenden, um sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="9a2d4-107">Unternehmen in Branchen, bei denen Verkäufe auf mehreren Ebenen getätigt werden, wie beispielsweise Produkte, Services, Abonnements usw., müssen Aufträge mit mehreren Elementen erstellen können, sodass die Umsatzerlöse basierend auf unternehmensspezifischen wie branchenspezifischen Richtlinien erfasst werden können.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="9a2d4-108">Im Allgemeinen lässt sich der Umsatzerkennungsprozess verwenden, um folgende Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="9a2d4-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="9a2d4-109">Umsatzerlöse zuweisen – um sicherzustellen, dass der entsprechende Umsatzerlöspreis auf Grundlage der Komponentenwerte bei Aufträgen mit mehreren Elementen realisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="9a2d4-110">Umsatzerlöse verzögern – basierend auf einem Umsatzerlöszeitplan, der den Vertragszeitrahmen und die prozentualen Anteile für Umsatzerlöse im Zeitverlauf erkennt, werden die Umsatzerlöse verzögert dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="9a2d4-111">Das Video [Verwendung der Umsatzerkennung in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (oben) ist in der [Finance and Operations-Playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) auf YouTube enthalten.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="9a2d4-112">Die Umsatzerkennungsfunktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln zur Erfassung des Umsatzerlöspreises und des Umsatzerlöszeitplans definieren können.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="9a2d4-113">Für die Umsatzerkennung werden Verkaufsauftragsdokumente für veröffentlichte Produkte verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="9a2d4-114">Die veröffentlichten Produkte enthalten die nötigen Informationen, um den Umsatzerlöspreis und den Umsatzerlöszeitplan festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="9a2d4-115">Der Verkaufsauftrag kann aus einem Aufwandsprojekt stammen.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="9a2d4-116">Unternehmen können die Umsatzerlöszeitplan-Funktionen ohne die Umsatzerlöspreis-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="9a2d4-117">Daher wird der Preis in den Verkaufsauftragspositionen entweder als Umsatzerlös oder als verzögerter Umsatzerlös verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="9a2d4-118">Wenn ein Umsatzerlöszeitplan für die Verkaufsauftragsposition vorhanden ist, wird der Preis für die Verkaufsauftragsposition verzögert.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="9a2d4-119">Wenn kein Umsatzerlöszeitplan für die Verkaufsauftragsposition vorhanden ist, wird der Preis für die Verkaufsauftragsposition auf einem Umsatzerlöskonto gebucht, wenn er in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="9a2d4-120">Der Umsatzerlöspreis wird entweder berechnet, wenn der Verkaufsauftrag bestätigt wurde oder wenn die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="9a2d4-121">Um eine Vorschau des Umsatzerlöspreises anzuzeigen, bevor die Rechnung gebucht wird, müssen Sie den Verkaufsauftrag bestätigen.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="9a2d4-122">Nach der Bestätigung des Verkaufsauftrags wird auch ein Zeitplan für den voraussichtlichen Umsatzerlös erstellt, falls eine Verkaufsauftragsposition einen Umsatzerlöszeitplan enthält.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="9a2d4-123">Wenn der Verkaufsauftrag in Rechnung gestellt wird, wird der Zeitplan für den voraussichtlichen Umsatzerlös gelöscht, und der Zeitplan für den voraussichtlichen Umsatzerlös wird durch den tatsächlichen Umsatzerlöszeitplan ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="9a2d4-124">Die Details des Umsatzerkennungszeitplans werden für jede Auftragsposition verwaltet.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="9a2d4-125">Daher kann der Umsatzerkennungsmanager die Details anzeigen und Positionen für den Umsatzerlös freigeben, wenn die vertragliche Verpflichtung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="9a2d4-126">Am Ende jeder Periode kann der Umsatzerkennungsmanager eine Umsatzerlöserfassung erstellen, um alle Zeitplanpositionen freizugeben, die an oder vor einem definierten Datum fällig werden.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="9a2d4-127">Diese Umsatzerlöserfassung wird nicht sofort gebucht.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="9a2d4-128">Daher kann der Umsatzerkennungsmanager überprüfen, ob die richtigen Beträge aus dem verzögerten Umsatzerlös aus dem tatsächlichen Umsatz freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="9a2d4-129">Wenn eine Vertragsänderung dafür sorgt, dass eine neue Verkaufsauftragsposition entweder dem vorhandenen Verkaufsauftrag oder einem neuen Verkaufsauftrag hinzugefügt wird, kann ein Umlegungsverfahren ausgeführt werden, um den Umsatzerlöspreis für alle Positionen in allen Verkaufsaufträgen zu berichtigen.</span><span class="sxs-lookup"><span data-stu-id="9a2d4-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
