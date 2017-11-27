---
title: "Verzögerungen"
description: "Dieser Artikel enthält Informationen zu verzögerten Daten in der Masterplanung. Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum, das eine Transaktion erhält, wenn das früheste Erfüllungsdatum, das die Masterplanung berechnet, später ist als das angeforderte Datum."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed0df1abbf4f70ea70046eff7b91a25fdd59016c
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="delays"></a><span data-ttu-id="67ea2-104">Verzögerungen</span><span class="sxs-lookup"><span data-stu-id="67ea2-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="67ea2-105">Dieser Artikel enthält Informationen zu verzögerten Daten in der Masterplanung.</span><span class="sxs-lookup"><span data-stu-id="67ea2-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="67ea2-106">Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum, das eine Transaktion erhält, wenn das früheste Erfüllungsdatum, das die Masterplanung berechnet, später ist als das angeforderte Datum.</span><span class="sxs-lookup"><span data-stu-id="67ea2-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="67ea2-107">Der Produktprogrammplan kann das früheste Erfüllungsdatum für eine Buchung, für den Lieferzeiten, Materialverfügbarkeit, Kapazitätsverfügbarkeit und verschiedene Planungsparameter berechnen.</span><span class="sxs-lookup"><span data-stu-id="67ea2-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="67ea2-108">Wenn Produktprogrammplan ein Auftragsdatum berechnet, das vor dem aktuellen Datum liegt, kann der Auftrag nicht rechtzeitig erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="67ea2-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="67ea2-109">Daher wird der Auftrag verzögert.</span><span class="sxs-lookup"><span data-stu-id="67ea2-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="67ea2-110">In diesem Fall plant der Produktprogrammplan den Auftrag im Voraus, ausgehend vom aktuellen Datum und einschließlich Lieferzeiten.</span><span class="sxs-lookup"><span data-stu-id="67ea2-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="67ea2-111">Diese Lieferzeiten beginnen mit Komponentenartikeln auf niedrigerer Ebene.</span><span class="sxs-lookup"><span data-stu-id="67ea2-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="67ea2-112">Der Auftrag empfängt dann ein verzögertes Datum.</span><span class="sxs-lookup"><span data-stu-id="67ea2-112">The order then receives a delayed date.</span></span> <span data-ttu-id="67ea2-113">Ein verzögertes Datum ist ein realistisches Fälligkeitsdatum basierend auf den aktuellen Daten.</span><span class="sxs-lookup"><span data-stu-id="67ea2-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="67ea2-114">Produktprogrammplan berechnet auch die Anzahl der Verzögerungstagen.</span><span class="sxs-lookup"><span data-stu-id="67ea2-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="67ea2-115">In bestimmten Situationen möchten Sie möglicherweise Verzögerungen nicht berechnen, z. B. wenn Benutzer wissen, dass sie Durchlaufzeiten beschleunigen können, indem sie Alternativmodi der Lieferung auswählen.</span><span class="sxs-lookup"><span data-stu-id="67ea2-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="67ea2-116">Sie können konfigurieren, wie Verzögerungen für eine Dispositionssteuerungsgruppe berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="67ea2-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="67ea2-117">Sie können die Dispositionssteuerungsgruppe dann später einem Artikel zuordnen.</span><span class="sxs-lookup"><span data-stu-id="67ea2-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="67ea2-118">Auf der Seite **Parameter für Produktprogrammplanung** können Sie die Startzeit für die Berechnung von Verzögerungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="67ea2-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="67ea2-119">Wenn ein Auftrag nach dieser Zeit erfüllt wird, addiert das System einen Tag Verzögerung zum Verzögerungsdatum des Auftrags hinzu.</span><span class="sxs-lookup"><span data-stu-id="67ea2-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="67ea2-120">**Hinweis:** In früheren Versionen waren berechnete Verzögerungen als *Verfügbarkeitsmeldungen* bekannt, das verzögerte Datum als *Verfügbarkeitsdatum*, und eine verzögerte Buchung war als *eine Buchung mit Erfüllung in der Zukunft* bekannt.</span><span class="sxs-lookup"><span data-stu-id="67ea2-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="67ea2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67ea2-121">See also</span></span>
--------

[<span data-ttu-id="67ea2-122">Dispositionseinstellungen</span><span class="sxs-lookup"><span data-stu-id="67ea2-122">Coverage settings</span></span>](coverage-settings.md)




