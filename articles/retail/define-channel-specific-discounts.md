---
title: Kanalspezifische Rabatte definieren
description: "Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest. Dieses Thema prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 34039b298e8994e50a7c06ef034698e8c1264389
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="define-channel-specific-discounts"></a><span data-ttu-id="caf4c-104">Kanalspezifische Rabatte definieren</span><span class="sxs-lookup"><span data-stu-id="caf4c-104">Define channel-specific discounts</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="caf4c-105">Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest.</span><span class="sxs-lookup"><span data-stu-id="caf4c-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="caf4c-106">Dieses Thema prüft die Konzepte, die Sie kennen müssen, um einen Rabatt für einen bestimmten Kanal zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="caf4c-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span> 

<a name="channel-specific-discounts"></a><span data-ttu-id="caf4c-107">Kanalspezifische Rabatte</span><span class="sxs-lookup"><span data-stu-id="caf4c-107">Channel-specific discounts</span></span>
--------------------------

<span data-ttu-id="caf4c-108">Einzelhändler legen häufig verschiedene Rabatte in verschiedenen Kanälen fest.</span><span class="sxs-lookup"><span data-stu-id="caf4c-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="caf4c-109">Dies kann erfolgen, um die lokalen Marktbedingungen anzusprechenoder mit einem konkurrierenden Einzelhändler in den Wettbewerb zu treten..</span><span class="sxs-lookup"><span data-stu-id="caf4c-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="caf4c-110">Microsoft Dynamics 365 für Retail verwendet Preisgruppen, um kanalspezifische Rabatte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="caf4c-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="caf4c-111">Preisgruppen können einer oder mehreren der folgenden Entitäten zugewiesen werden: Kanäle, Kataloge, Zugehörigkeiten und Treueprogramme.</span><span class="sxs-lookup"><span data-stu-id="caf4c-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="caf4c-112">Dieser Artikel behandelt Kanäle. Aber die gleichen Konzepte gelten für Katalograbatte, Zugehörigkeitsrabatte und Treuerabatte.</span><span class="sxs-lookup"><span data-stu-id="caf4c-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="caf4c-113">Preisgruppen</span><span class="sxs-lookup"><span data-stu-id="caf4c-113">Price groups</span></span>

<span data-ttu-id="caf4c-114">[![Preisgruppen](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="caf4c-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="caf4c-115">Im Diagramm wird die Beziehung zwischen Entitäten dargelegt die auf einer Buchung (Kanal, Katalog, Zugehörigkeit, Debitor, Treuekarte) erscheinen und die verschiedenen Rabatttypen, die konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="caf4c-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="caf4c-116">Alle Buchungen sind in einem Kanal vorhanden, daher ist sichergestellt, dass der Kanal in einer Buchung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="caf4c-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="caf4c-117">Die verbleibende Entitäten sind optional.</span><span class="sxs-lookup"><span data-stu-id="caf4c-117">The remaining entities are optional.</span></span> <span data-ttu-id="caf4c-118">Auf jeder Masterdaten Seite ist ein Link zu einer zugehörigen Preisgruppenseite, in der Sie Preisgruppen nach Bedarf anzeigen und hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="caf4c-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="caf4c-119">Eine Preisgruppe wird verwendet, um vier unterschiedliche Arten Entitäten zu unterscheiden die auf Rabatte, Preisregulierungen und Handelsvereinbarungen angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="caf4c-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="caf4c-120">Es wird empfohlen, eine Strategie für die Planung zu erstellen, wie die Preisgruppen benannt werden sollen, um sie organisiert zu behalten.</span><span class="sxs-lookup"><span data-stu-id="caf4c-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="caf4c-121">Eine Option wäre, einen Buchstaben oder eine Nummer als Präfix oder Suffix zu verwenden, um zwischen unterschiedlichen Arten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="caf4c-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="caf4c-122">Beispiel 1 xxxxx für Kanalpreisgruppen und 2 xxxxx für Katalogpreisgruppen.</span><span class="sxs-lookup"><span data-stu-id="caf4c-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="caf4c-123">Es gibt vier Abfrageseiten für die verschiedenen Einzelhandeltsentitäten für die Rabatten möglich sind.</span><span class="sxs-lookup"><span data-stu-id="caf4c-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

-   <span data-ttu-id="caf4c-124">**Preisgruppen Retail Channel**- Diese Seite enthält eine Liste der Kanäle und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="caf4c-124">**Retail channel price groups** - This page shows a list of channels and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="caf4c-125">**Katalogpreisgruppen**- Diese Seite enthält eine Liste der Kataloge und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="caf4c-125">**Catalog price groups** - This page shows a list of catalogs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="caf4c-126">**Treuepreisgruppen**- Diese Seite enthält eine Liste der Treueprogramme und Rabatte, die für die jeweilige Preisgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="caf4c-126">**Loyalty price groups** - This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="caf4c-127">**Zugehörigkeitspreisgruppen**- Diese Seite enthält eine Liste der Zugehörigkeiten und Rabatte, die für jede Preisgruppe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="caf4c-127">**Affiliation price groups** - This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="caf4c-128">Beispieleinrichtung für Kanalrabatte</span><span class="sxs-lookup"><span data-stu-id="caf4c-128">Example channel discount set up</span></span>
<span data-ttu-id="caf4c-129">Das folgende Beispiel veranschaulicht die Aufgaben zur Einrichtung von Kanalrabatten.</span><span class="sxs-lookup"><span data-stu-id="caf4c-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1.  <span data-ttu-id="caf4c-130">In vorliegenden Beispiel haben Sie einen Kanal namens **Houston** und erstellen einen neuen Rabatt namens **Zurück zur Schule.**</span><span class="sxs-lookup"><span data-stu-id="caf4c-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School.**</span></span>
2.  <span data-ttu-id="caf4c-131">Da die Preisgestaltungs- und Rabattstrategie die Möglichkeit von Kanalrabatten umfasst, erstellen Sie immer eine kanalspezifische Preisgruppe, wenn Sie einen Kanal erstellen.</span><span class="sxs-lookup"><span data-stu-id="caf4c-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3.  <span data-ttu-id="caf4c-132">Sie haben die Preisgruppe **Houston-PG** und diese ist dem Kanal **Houston** zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="caf4c-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4.  <span data-ttu-id="caf4c-133">Nachdem Sie den neuen Rabatt **Zurück zur Schule** erstellt haben, müssen Sie auf **Preisgruppen** oben auf der Seite **Rabatt** klicken.</span><span class="sxs-lookup"><span data-stu-id="caf4c-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="caf4c-134">Die **Rabattpreisgruppen**-Seite wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="caf4c-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="caf4c-135">Danach klicken Sie auf **Neu** und wählen die Preisgruppe **Houston-PG** aus.</span><span class="sxs-lookup"><span data-stu-id="caf4c-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5.  <span data-ttu-id="caf4c-136">Jetzt können Sie den Rabatt aktivieren und für den Kanal umsetzen.</span><span class="sxs-lookup"><span data-stu-id="caf4c-136">Now you can enable the discount and push it to the channel.</span></span>



<a name="see-also"></a><span data-ttu-id="caf4c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caf4c-137">See also</span></span>
--------

[<span data-ttu-id="caf4c-138">Preisregulierungen und Rabatte</span><span class="sxs-lookup"><span data-stu-id="caf4c-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)




