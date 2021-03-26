---
title: Übersicht zur Umsatzerkennung
description: Dieses Thema enthält Informationen zur Umsatzerkennungsfunktion. Diese Funktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln zur Erfassung des Umsatzerlöspreises und des Umsatzerlöszeitplans bei Aufträgen mit mehreren Elementen festlegen können.
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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: b21cf04674d01df31dc3304886e7cda035bdcce2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238255"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="4fd3b-104">Übersicht zur Umsatzerkennung</span><span class="sxs-lookup"><span data-stu-id="4fd3b-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fd3b-105">Unternehmen in Branchen, bei denen Verkäufe auf mehreren Ebenen getätigt werden, wie beispielsweise Produkte, Services, Abonnements usw., müssen Aufträge mit mehreren Elementen erstellen können, damit Umsatzerlöse basierend auf unternehmens- sowie branchenspezifischen Richtlinien erfasst werden können.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="4fd3b-106">Die Funktion zur Umsatzerkennung kann nicht mithilfe der Funktionsverwaltung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="4fd3b-107">Derzeit erfolgt die Aktivierung mit Konfigurationsschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="4fd3b-108">Die Umsatzerkennung, einschließlich Bündelfunktion, wird in Commerce-Kanälen (E-Commerce, POS, Callcenter) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="4fd3b-109">Mit Umsatzerkennung konfigurierte Artikel dürfen nicht in Bestellungen oder Transaktionen ergänzt werden, die in Commerce-Kanälen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="4fd3b-110">Im Allgemeinen dient die Umsatzerkennung zur Erledigung folgender Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="4fd3b-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="4fd3b-111">Umsatzerlöse zuweisen – um sicherzustellen, dass der entsprechende Umsatzerlöspreis bei Aufträgen mit mehreren Elementen auf den Werten der Bestandteile beruht.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="4fd3b-112">Umsatzerlöse verzögern – basierend auf einem Umsatzerlöszeitplan, der den Vertragszeitrahmen und die prozentualen Anteile für Umsatzerlöse im Zeitverlauf erkennt, werden die Umsatzerlöse verzögert dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="4fd3b-113">Das Video [Verwendung der Umsatzerkennung in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (oben) ist in der [Finance and Operations-Playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) auf YouTube enthalten.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="4fd3b-114">Die Umsatzerkennungsfunktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln zur Erfassung des Umsatzerlöspreises und des Umsatzerlöszeitplans definieren können.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="4fd3b-115">Für die Umsatzerkennung werden Verkaufsauftragsdokumente für veröffentlichte Produkte verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="4fd3b-116">Die veröffentlichten Produkte enthalten die nötigen Informationen, um den Umsatzerlöspreis und den Umsatzerlöszeitplan festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="4fd3b-117">Der Verkaufsauftrag kann aus einem Aufwandsprojekt stammen.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="4fd3b-118">Unternehmen können die Umsatzerlöszeitplan-Funktionen ohne die Umsatzerlöspreis-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="4fd3b-119">Daher wird der Preis in den Verkaufsauftragspositionen entweder als Umsatzerlös oder als verzögerter Umsatzerlös verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="4fd3b-120">Wenn ein Umsatzerlöszeitplan für die Verkaufsauftragsposition vorhanden ist, wird der Preis für die Verkaufsauftragsposition verzögert.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="4fd3b-121">Wenn kein Umsatzerlöszeitplan für die Verkaufsauftragsposition vorhanden ist, wird der Preis für die Verkaufsauftragsposition auf einem Umsatzerlöskonto gebucht, wenn er in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="4fd3b-122">Der Umsatzerlöspreis wird entweder berechnet, wenn der Verkaufsauftrag bestätigt wurde oder wenn die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="4fd3b-123">Um eine Vorschau des Umsatzerlöspreises anzuzeigen, bevor die Rechnung gebucht wird, müssen Sie den Verkaufsauftrag bestätigen.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="4fd3b-124">Nach der Bestätigung des Verkaufsauftrags wird auch ein Zeitplan für den voraussichtlichen Umsatzerlös erstellt, falls eine Verkaufsauftragsposition einen Umsatzerlöszeitplan enthält.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="4fd3b-125">Wenn der Verkaufsauftrag in Rechnung gestellt wird, wird der Zeitplan für den voraussichtlichen Umsatzerlös gelöscht, und der Zeitplan für den voraussichtlichen Umsatzerlös wird durch den tatsächlichen Umsatzerlöszeitplan ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="4fd3b-126">Die Details des Umsatzerkennungszeitplans werden für jede Auftragsposition verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="4fd3b-127">Daher kann der Umsatzerkennungsmanager die Details anzeigen und Positionen für den Umsatzerlös freigeben, wenn die vertragliche Verpflichtung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="4fd3b-128">Am Ende jeder Periode kann der Umsatzerkennungsmanager eine Umsatzerlöserfassung erstellen, um alle Zeitplanpositionen freizugeben, die an oder vor einem definierten Datum fällig werden.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="4fd3b-129">Diese Umsatzerlöserfassung wird nicht sofort gebucht.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="4fd3b-130">Daher kann der Umsatzerkennungsmanager überprüfen, ob die richtigen Beträge aus dem verzögerten Umsatzerlös aus dem tatsächlichen Umsatz freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="4fd3b-131">Wenn eine Vertragsänderung dafür sorgt, dass eine neue Verkaufsauftragsposition entweder dem vorhandenen Verkaufsauftrag oder einem neuen Verkaufsauftrag hinzugefügt wird, kann ein Umlegungsverfahren ausgeführt werden, um den Umsatzerlöspreis für alle Positionen in allen Verkaufsaufträgen zu berichtigen.</span><span class="sxs-lookup"><span data-stu-id="4fd3b-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]