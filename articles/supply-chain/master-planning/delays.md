---
title: Verzögerungen
description: Dieses Thema enthält Informationen zu verzögerten Daten in der Masterplanung. Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum, das eine Transaktion erhält, wenn das früheste Erfüllungsdatum, das die Masterplanung berechnet, später ist als das angeforderte Datum.
author: roxanadiaconu
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4216ed1d9b981eee94cfd4c621abd1da99111512
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813674"
---
# <a name="delays"></a><span data-ttu-id="4ba31-104">Verzögerungen</span><span class="sxs-lookup"><span data-stu-id="4ba31-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ba31-105">Dieses Thema enthält Informationen zu verzögerten Daten in der Masterplanung.</span><span class="sxs-lookup"><span data-stu-id="4ba31-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="4ba31-106">Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum, das eine Transaktion erhält, wenn das früheste Erfüllungsdatum, das die Masterplanung berechnet, später ist als das angeforderte Datum.</span><span class="sxs-lookup"><span data-stu-id="4ba31-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="4ba31-107">Der Produktprogrammplan kann das früheste Erfüllungsdatum für eine Buchung, für den Lieferzeiten, Materialverfügbarkeit, Kapazitätsverfügbarkeit und verschiedene Planungsparameter berechnen.</span><span class="sxs-lookup"><span data-stu-id="4ba31-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="4ba31-108">Wenn Produktprogrammplan ein Auftragsdatum berechnet, das vor dem aktuellen Datum liegt, kann der Auftrag nicht rechtzeitig erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="4ba31-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="4ba31-109">Daher wird der Auftrag verzögert.</span><span class="sxs-lookup"><span data-stu-id="4ba31-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="4ba31-110">In diesem Fall plant der Produktprogrammplan den Auftrag im Voraus, ausgehend vom aktuellen Datum und einschließlich Lieferzeiten.</span><span class="sxs-lookup"><span data-stu-id="4ba31-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="4ba31-111">Diese Lieferzeiten beginnen mit Komponentenartikeln auf niedrigerer Ebene.</span><span class="sxs-lookup"><span data-stu-id="4ba31-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="4ba31-112">Der Auftrag empfängt dann ein verzögertes Datum.</span><span class="sxs-lookup"><span data-stu-id="4ba31-112">The order then receives a delayed date.</span></span> <span data-ttu-id="4ba31-113">Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum basierend auf den aktuellen Daten.</span><span class="sxs-lookup"><span data-stu-id="4ba31-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="4ba31-114">Produktprogrammplan berechnet auch die Anzahl der Verzögerungstagen.</span><span class="sxs-lookup"><span data-stu-id="4ba31-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="4ba31-115">In bestimmten Situationen möchten Sie möglicherweise Verzögerungen nicht berechnen, z. B. wenn Benutzer wissen, dass sie Durchlaufzeiten beschleunigen können, indem sie Alternativmodi der Lieferung auswählen.</span><span class="sxs-lookup"><span data-stu-id="4ba31-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="4ba31-116">Sie können konfigurieren, wie Verzögerungen für eine Dispositionssteuerungsgruppe berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="4ba31-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="4ba31-117">Sie können die Dispositionssteuerungsgruppe dann später einem Artikel zuordnen.</span><span class="sxs-lookup"><span data-stu-id="4ba31-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="4ba31-118">Auf der Seite **Parameter für Produktprogrammplanung** können Sie die Startzeit für die Berechnung von Verzögerungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="4ba31-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="4ba31-119">Wenn ein Auftrag nach dieser Zeit erfüllt wird, addiert das System einen Tag Verzögerung zum Verzögerungsdatum des Auftrags hinzu.</span><span class="sxs-lookup"><span data-stu-id="4ba31-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="4ba31-120">In früheren Versionen waren berechnete Verzögerungen als *Verfügbarkeitsmeldungen* bekannt, das verzögerte Datum als *Verfügbarkeitsdatum*, und eine verzögerte Buchung war als eine *Transaktio mit Erfüllung in der Zukunft* bekannt.</span><span class="sxs-lookup"><span data-stu-id="4ba31-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="4ba31-121">Begrenzte Verzögerungen bei der Einrichtung der Produktion mit mehreren Stücklistenebenen</span><span class="sxs-lookup"><span data-stu-id="4ba31-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="4ba31-122">Wenn Sie mit Verzögerungen in einem Produktionssetup mit mehreren Stücklistenstufen arbeiten, ist es wichtig zu beachten, dass nur die Artikel direkt über dem Artikel (in der Stücklistenstruktur), die die Verzögerung verursachen, im Rahmen der Masterplanung mit einer Verzögerung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ba31-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="4ba31-123">Bei anderen Elementen in der Stücklistenstruktur wird die Verzögerung erst beim ersten Masterplanungslauf angewendet, wenn der geplante Auftrag für die oberste Ebene genehmigt oder bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="4ba31-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="4ba31-124">Um diese bekannte Einschränkung zu umgehen, können die Fertigungsaufträge oben in der Stücklistenstruktur mit Verzögerungen vor dem nächsten Masterplanungslauf genehmigt (oder bestätigt) werden.</span><span class="sxs-lookup"><span data-stu-id="4ba31-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="4ba31-125">Auf diese Weise bleibt die Verzögerung des verspäteten genehmigten geplanten Fertigungsauftrags erhalten und alle zugrunde liegenden Komponenten werden entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4ba31-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="4ba31-126">Aktionsnachrichten können auch verwendet werden, um Planaufträge zu identifizieren, die aufgrund anderer Verzögerungen in der Stücklistenstruktur zu einem späteren Zeitpunkt verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="4ba31-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="4ba31-127">Gewünschtes Datum</span><span class="sxs-lookup"><span data-stu-id="4ba31-127">Desired date</span></span>

<span data-ttu-id="4ba31-128">Auf der Seite **Bestellvorschlag** unter der Registerkarte **Verzögerungen** ist das **Gewünschtes Datum** für den Bestellvorschlag.</span><span class="sxs-lookup"><span data-stu-id="4ba31-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="4ba31-129">Das gewünschte Datum eines Bestellvorschlags ist das Basisdatum für Verzögerungen, was ein berechnetes Datum ist, dass dem **Angefordertes Datum** entspricht, das anhand des **Bedarfsverlauf** berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4ba31-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="4ba31-130">Wenn der Bestellvorschlag eine Stücklistenposition, eine Produktionsauftragsposition oder eine Kanbanposition ist, basiert das gewünschte Datum auf dem **Bedarfsdatum** und das gewünschte Datum wird auf nicht auf der Seite **Bestellvorschlag** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ba31-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="4ba31-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4ba31-131">Additional resources</span></span>
--------

[<span data-ttu-id="4ba31-132">Deckungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="4ba31-132">Coverage settings</span></span>](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]