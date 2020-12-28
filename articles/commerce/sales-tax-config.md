---
title: Mehrwertsteuer für Online-Aufträge konfigurieren
description: Dieses Thema bietet eine Übersicht über die Auswahl von Mehrwertsteuergruppen für verschiedene Online-Auftragstypen in Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530196"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="2b1fd-103">Mehrwertsteuer für Online-Aufträge konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2b1fd-103">Configure sales tax for online orders</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2b1fd-104">Dieses Thema bietet eine Übersicht über die Auswahl von Mehrwertsteuergruppen für verschiedene Online-Auftragstypen.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="2b1fd-105">Ihr E-Commerce-Kanal möchte möglicherweise Optionen wie Lieferung oder Abholung für Online-Aufträge unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="2b1fd-106">Die Anwendbarkeit der Mehrwertsteuer basiert auf der von Ihren Online-Benutzern ausgewählten Option.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="2b1fd-107">Wenn ein Websitekunde sich entscheidet, einen Artikel online zu kaufen, und ihn an eine Adresse geliefert bekommt, wird die Mehrwertsteuer basierend auf der Steuergruppeneinstellung der Lieferadresse des Kunden bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="2b1fd-108">Wenn sich ein Kunde dafür entscheidet, einen gekauften Artikel in einem Geschäft abzuholen, wird die Mehrwertsteuer basierend auf der Steuergruppeneinstellung des Abholgeschäfts ermittelt.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="2b1fd-109">An eine Kundenadresse gelieferte Aufträge</span><span class="sxs-lookup"><span data-stu-id="2b1fd-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="2b1fd-110">Im Allgemeinen werden Steuern für Online-Aufträge, die an Kundenadressen geliefert werden, vom Zielort bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="2b1fd-111">Jede Mehrwertsteuergruppe hat eine Einzelhandelsziel-basierte Steuerkonfiguration, in der Ihr Unternehmen die Zieldetails definieren kann, wie Land/Region, Bundesland, Landkreis und Ort in einer hierarchischen Form.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="2b1fd-112">Wenn ein Online-Auftrag erteilt wird, verwendet das Commerce-Steuermodul die Lieferadresse jeder Position im Auftrag und sucht Mehrwertsteuergruppen mit übereinstimmenden zielbasierten Steuerkriterien.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="2b1fd-113">Bei einem Online-Auftrag mit San Francisco, Kalifornien, USA, als Positionslieferadresse findet das Steuermodul die Mehrwertsteuergruppe und den Mehrwertsteuercode für Kalifornien und berechnet dann entsprechend die Steuer für jede einzelne Position.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="2b1fd-114">Kundenbasierte Steuergruppen</span><span class="sxs-lookup"><span data-stu-id="2b1fd-114">Customer-based tax groups</span></span>

<span data-ttu-id="2b1fd-115">In der Commerce-Zentralverwaltung gibt es zwei Stellen, an denen Kundensteuergruppen konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="2b1fd-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="2b1fd-116">**Kundenprofil**</span><span class="sxs-lookup"><span data-stu-id="2b1fd-116">**Customer's profile**</span></span>
- <span data-ttu-id="2b1fd-117">**Lieferadresse des Kunden**</span><span class="sxs-lookup"><span data-stu-id="2b1fd-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="2b1fd-118">Wenn für das Profil eines Kunden eine Steuergruppe konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="2b1fd-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="2b1fd-119">Für den Profildatensatz eines Kunden in der Zentralverwaltung wurde möglicherweise eine Mehrwertsteuergruppe konfiguriert. Für Online-Aufträge wird die in einem Kundenprofil konfigurierte Mehrwertsteuergruppe jedoch nicht vom Steuermodul verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="2b1fd-120">Wenn für die Lieferadresse eines Kunden eine Steuergruppe konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="2b1fd-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="2b1fd-121">Wenn für den Lieferadressdatensatz eines Kunden eine Steuergruppe konfiguriert ist und ein Online-Auftrag (oder Positionsartikel) an die Lieferadresse des Kunden geliefert wird, wird die im Adressdatensatz des Kunden konfigurierte Steuergruppe vom Steuermodul für Steuerberechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="2b1fd-122">Eine Steuergruppe für den Lieferadressdatensatz eines Kunden konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2b1fd-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="2b1fd-123">Führen Sie die folgenden Schritte aus, um eine Steuergruppe für den Lieferadressdatensatz eines Kunden in der Commerce-Zentralverwaltung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2b1fd-124">Wechseln Sie zu **Alle Kunden** und wählen Sie dann den gewünschten Kunden aus.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="2b1fd-125">Im Inforegister **Adressen** wählen Sie die gewünschte Adresse und dann **Weitere Optionen \> Erweitert** aus.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="2b1fd-126">Unter der Registerkarte **Allgemein** auf der Seite **Adressen verwalten** legen Sie den Mehrwertsteuerwert nach Bedarf fest.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="2b1fd-127">Die Steuergruppe wird anhand der Lieferadresse der Auftragsposition definiert und die zielbasierten Steuern werden in der Steuergruppe selbst konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="2b1fd-128">Weitere Informationen finden Sie unter [Steuern für Online-Shops auf der Grundlage des Ziels einrichten](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="2b1fd-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="2b1fd-129">Auftragsabholung im Laden</span><span class="sxs-lookup"><span data-stu-id="2b1fd-129">Order pickup in store</span></span>

<span data-ttu-id="2b1fd-130">Für Auftragspositionen, bei denen Abholung im Laden oder Abholung am Straßenrand angegeben ist, wird die Steuergruppe aus dem ausgewählten Abholladen angewendet.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="2b1fd-131">Details zum Konfigurieren der Steuergruppe für einen bestimmten Laden finden Sie unter [Andere Steueroptionen für Läden festlegen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="2b1fd-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="2b1fd-132">Wenn eine Bestellposition in einem Geschäft abgeholt wird, werden die Adresssteuereinstellungen des Kunden (sofern eingerichtet) vom Steuermodul ignoriert und die Steuerkonfiguration des Abholladens werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="2b1fd-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="2b1fd-133">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2b1fd-133">Additional resources</span></span>

[<span data-ttu-id="2b1fd-134">Mehrwertsteuerübersicht</span><span class="sxs-lookup"><span data-stu-id="2b1fd-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="2b1fd-135">Mehrwertsteuer-Berechnungsmethoden im Feld „Ursprung“</span><span class="sxs-lookup"><span data-stu-id="2b1fd-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="2b1fd-136">Mehrwertsteuer-Zuweisung und -Außerkraftsetzungen</span><span class="sxs-lookup"><span data-stu-id="2b1fd-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="2b1fd-137">Optionen zur Berechnung von Gesamtbetrag und Intervall für Mehrwertsteuercodes</span><span class="sxs-lookup"><span data-stu-id="2b1fd-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="2b1fd-138">Berechnung der Steuerbefreiung</span><span class="sxs-lookup"><span data-stu-id="2b1fd-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 
