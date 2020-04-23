---
title: Dauerauftragsworkflow (Übersicht)
description: Dieses Thema enthält eine Übersicht über den Dauerauftragsworkflow.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cb8b86ef0e2a1bd90590c8cc2a20e18e82ef9c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206587"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="bc9e0-103">Dauerauftragsworkflow (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="bc9e0-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bc9e0-104">Sie sind Administrator für Daueraufträge in einem Unternehmen, das Daueraufträge für die Wartung von Beleuchtungseinrichtungen anbietet.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="bc9e0-105">Ein Debitor tritt an das Unternehmen heran, um einen Dauerauftrag für eine jährliche Wartung seiner Beleuchtungseinrichtungen abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="bc9e0-106">Einrichten von Daueraufträgen</span><span class="sxs-lookup"><span data-stu-id="bc9e0-106">Setting up subscriptions</span></span>

<span data-ttu-id="bc9e0-107">Der erste Schritt beim Einrichten eines Dauerauftrags besteht im Erstellen einer Dauerauftragsgruppe für die neue Servicevereinbarung bzw. darin, sich zu vergewissern, dass die Dauerauftragsgruppe vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="bc9e0-108">Ist bereits eine Dauerauftragsgruppe vorhanden, muss diese für eine jährliche Fakturierung für den Debitor sowie für die Antizipierung von Umsatzerlösen auf Monatsbasis eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="bc9e0-109">Weitere Informationen zum Einrichten von Daueraufträgen finden Sie unter [Dauerauftragsgruppen einrichten](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e0-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="bc9e0-110">Nach Erstellung der Dauerauftragsgruppe kann der Dauerauftrag erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="bc9e0-111">Weitere Informationen dazu, wie von Daueraufträgen, finden Sie unter[Erstellen von Daueraufträgen auf der Grundlage einer Dauerauftragsgruppe](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e0-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="bc9e0-112">Erstellen und Ändern von Dauerauftragsbuchungen</span><span class="sxs-lookup"><span data-stu-id="bc9e0-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="bc9e0-113">Nach dem Einrichten des Dauerauftrags erstellen Sie die Buchung der Dauerauftragsgebühr für den ersten Rechnungsstellungszeitraum (in diesem Fall: ein Jahr).</span><span class="sxs-lookup"><span data-stu-id="bc9e0-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="bc9e0-114">Bei den Buchungen handelt es sich um Buchungen vom Typ **Regelmäßig**.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="bc9e0-115">Das bedeutet, dass lediglich Dauerauftragsbuchungen erstellt werden können, bei denen Anfangs- und Startdatum den im Formular **Periodentypen** erstellten Perioden entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="bc9e0-116">Weitere Informationen zu kostenlosen Transaktionen finden Sie unter [Dauerauftragsgebühren-Buchungen erstellen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e0-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="bc9e0-117">Nach dem Einrichten des Dauerauftrags für den Debitor erfahren Sie, dass dem Debitor ein Preisnachlass von 10 Prozent auf alle Listenpreise des Serviceangebots gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="bc9e0-118">Der Preis der erstellten Buchungsgebühr muss deshalb entsprechend verringert werden.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="bc9e0-119">Ein paar Stunden später erhalten Sie einen Anruf von Ihrer Kontaktperson beim Debitor, und sie erfahren, dass die Servicevereinbarung für die Beleuchtungseinrichtung zwar immer noch gewünscht wird, gegen Ende des Jahres allerdings eine Erneuerung dieser Einrichtung geplant ist.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="bc9e0-120">Aus diesem Grund werden die Wartungsleistungen lediglich bis Oktober 2013 benötigt.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="bc9e0-121">Also erstellen Sie eine neue Buchung für Dauerauftragsgebühren vom Typ **Minderungstage**, um die Monatsanzahl des Dauerauftrags für den Debitor zu verringern.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="bc9e0-122">Weitere Informationen dazu, wie Sie Tage reduzieren, finden Sie unter [Verringern der Tage für Dauerauftragsgebühren](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e0-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="bc9e0-123">Fakturieren und Antizipieren von Dauerauftragsbuchungen</span><span class="sxs-lookup"><span data-stu-id="bc9e0-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="bc9e0-124">Die Einrichtung des Dauerauftrags ist nun abgeschlossen, und der Dauerauftrag kann dem Debitor in Rechnung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="bc9e0-125">Weitere Informationen zum Fakturieren von Daueraufträgen finden Sie unter [Dauerauftragstransaktionen faktuieren](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e0-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="bc9e0-126">Zwei Tage später erhalten Sie einen Anruf des Debitors, der darum bittet, die Rechnung nicht in Euro, sondern in US-Dollar auszustellen.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="bc9e0-127">Also erstellen Sie eine Gutschrift sowie eine neue Dauerauftragsbuchung in der korrekten Währung.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="bc9e0-128">Weitere Informationen zum Erstellen einer Gutschrift für Dauerauftragsbuchungen finden Sie unter [Gutschreiben von Dauerauftragsbuchungen](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e0-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="bc9e0-129">Am Monatsende kann der Monatsumsatz des Dauerauftrags des Debitors für das GuV-Konto sowie für die RIF-Konten antizipiert werden.</span><span class="sxs-lookup"><span data-stu-id="bc9e0-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="bc9e0-130">Weitere Informationen zum Antizipieren von Umsatzerlös für Daueraufträge finden Sie unter [Dauerauftragsumsatz antizipieren](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="bc9e0-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


