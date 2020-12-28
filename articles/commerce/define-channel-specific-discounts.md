---
title: Kanalspezifische Rabatte definieren
description: Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dieses Thema prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 539a6f2df46450c5e0fd18ba69501432d6f3fbdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412575"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="bd7d8-104">Kanalspezifische Rabatte definieren</span><span class="sxs-lookup"><span data-stu-id="bd7d8-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd7d8-105">Dieses Thema prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="bd7d8-106">Kanalspezifische Rabatte</span><span class="sxs-lookup"><span data-stu-id="bd7d8-106">Channel-specific discounts</span></span>

<span data-ttu-id="bd7d8-107">Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="bd7d8-108">Dies kann erfolgen, um die lokalen Marktbedingungen anzusprechen oder mit konkurrierenden Einzelhändlern in den Wettbewerb zu treten.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="bd7d8-109">Commerce verwendet Preisgruppen, um kanalspezifische Rabatte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="bd7d8-110">Preisgruppen können einer oder mehreren der folgenden Entitäten zugewiesen werden: Kanäle, Kataloge, Zugehörigkeiten und Treueprogramme.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="bd7d8-111">Dieser Artikel behandelt Kanäle. Aber die gleichen Konzepte gelten für Katalograbatte, Zugehörigkeitsrabatte und Treuerabatte.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="bd7d8-112">Preisgruppen</span><span class="sxs-lookup"><span data-stu-id="bd7d8-112">Price groups</span></span>

<span data-ttu-id="bd7d8-113">[![Preisgruppen](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="bd7d8-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="bd7d8-114">Im Diagramm wird die Beziehung zwischen Entitäten dargelegt die auf einer Buchung (Kanal, Katalog, Zugehörigkeit, Debitor, Treuekarte) erscheinen und die verschiedenen Rabatttypen, die konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="bd7d8-115">Alle Buchungen sind in einem Kanal vorhanden, daher ist sichergestellt, dass der Kanal in einer Buchung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="bd7d8-116">Die verbleibende Entitäten sind optional.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-116">The remaining entities are optional.</span></span> <span data-ttu-id="bd7d8-117">Auf jeder Masterdaten Seite ist ein Link zu einer zugehörigen Preisgruppenseite, in der Sie Preisgruppen nach Bedarf anzeigen und hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="bd7d8-118">Eine Preisgruppe wird verwendet, um vier unterschiedliche Arten Entitäten zu unterscheiden die auf Rabatte, Preisregulierungen und Handelsvereinbarungen angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="bd7d8-119">Es wird empfohlen, eine Strategie für die Planung zu erstellen, wie die Preisgruppen benannt werden sollen, um sie organisiert zu behalten.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="bd7d8-120">Eine Option wäre, einen Buchstaben oder eine Nummer als Präfix oder Suffix zu verwenden, um zwischen unterschiedlichen Arten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="bd7d8-121">Beispiel 1 xxxxx für Kanalpreisgruppen und 2 xxxxx für Katalogpreisgruppen.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="bd7d8-122">Es gibt vier Abfrageseiten für die verschiedenen Commerce-Entitäten für die Rabatten möglich sind.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="bd7d8-123">**Kanal Channel-Preisgruppen**– Diese Seite enthält eine Liste der Kanäle und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="bd7d8-124">**Katalogpreisgruppen**- Diese Seite enthält eine Liste der Kataloge und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="bd7d8-125">**Treuepreisgruppen**- Diese Seite  enthält eine Liste der Treueprogramme und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="bd7d8-126">**Zugehörigkeitspreisgruppen**- Diese Seite enthält eine Liste der Zugehörigkeiten und Rabatte, die für jede Preisgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="bd7d8-127">Beispieleinrichtung für Kanalrabatte</span><span class="sxs-lookup"><span data-stu-id="bd7d8-127">Example channel discount set up</span></span>

<span data-ttu-id="bd7d8-128">Das folgende Beispiel veranschaulicht die Aufgaben zur Einrichtung von Kanalrabatten.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="bd7d8-129">In vorliegenden Beispiel haben Sie einen  Kanal namens **Houston** und erstellen einen neuen Rabatt namens **Zurück zur Schule**.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="bd7d8-130">Da die Preisgestaltungs- und Rabattstrategie die Möglichkeit von Kanalrabatten umfasst, erstellen Sie immer eine kanalspezifische Preisgruppe, wenn Sie einen Kanal erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="bd7d8-131">Sie haben die Preisgruppe **Houston-PG** und diese ist dem Kanal **Houston** zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="bd7d8-132">Nachdem Sie den neuen Rabatt **Zurück zur Schule** erstellt haben, müssen Sie auf **Preisgruppen** oben auf der Seite **Rabatt** klicken.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="bd7d8-133">Die **Rabattpreisgruppen**-Seite wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="bd7d8-134">Danach klicken Sie auf **Neu** und wählen die Preisgruppe **Houston-PG** aus.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="bd7d8-135">Jetzt können Sie den Rabatt aktivieren und für den Kanal umsetzen.</span><span class="sxs-lookup"><span data-stu-id="bd7d8-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd7d8-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bd7d8-136">Additional resources</span></span>

[<span data-ttu-id="bd7d8-137">Preisregulierungen und Rabatte</span><span class="sxs-lookup"><span data-stu-id="bd7d8-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)
