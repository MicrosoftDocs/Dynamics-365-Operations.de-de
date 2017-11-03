---
title: Callcenterfunktionen
description: "Dieser Artikel gibt eine Übersicht über die Call Center Verkaufsfunktionalität in Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2c58f71230a0781ee957632b453ced86ca03b15a
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="0cdaa-103">Callcenterfunktionen</span><span class="sxs-lookup"><span data-stu-id="0cdaa-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="0cdaa-104">Dieser Artikel gibt eine Übersicht über die Call Center Verkaufsfunktionalität in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="0cdaa-105">Dynamics 365 for Retail unterstützt außerdem Callcenter als einen Einzelhandelskanalstyp.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="0cdaa-106">In einem Callcenter nehmen Arbeitskräfte Aufträge von Debitoren per Telefon entgegen und erstellen Aufträge.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="0cdaa-107">Callcenterfunktionen umfassen Funktionen, die vorgesehen sind, um es zu vereinfachen, Telephonaufträge anzunehmen und Kundenservice während des Auftragserfüllungsprozesses zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="0cdaa-108">So können Callcenterarbeitskräfte Zahlungsinformationen direkt in den Auftrag eingeben und können eine detaillierte Übersicht von Belastungen und der Zahlungen anzeigen, bevor sie den Auftrag versenden.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="0cdaa-109">Arbeitskräfte haben auch Optionen zum Steuern der Preisgestaltung und können auf verschiedene Daten zu Debitoren, Produkten und Preisen von der **Auftrag**-Seite zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="0cdaa-110">Callcenter verfügen zudem über Funktionen für die Verfolgung der Debitorenhistorie sowie und des Auftragsstatus.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="0cdaa-111">Jedes Callcenter kann eigene Benutzer, Zahlungsmethoden, Preisgruppen, Finanzdimensionen und Lieferarten haben.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="0cdaa-112">Sie können diese Optionen konfigurieren, wenn Sie das Callcenter erstellen.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="0cdaa-113">Darüber hinaus können Sie die Seite **Callcenter** verwenden, um die folgenden Gruppen von Funktionen zu aktivieren oder zu deaktivieren, die für Callcenter eindeutig sind:</span><span class="sxs-lookup"><span data-stu-id="0cdaa-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="0cdaa-114">**Auftragsabschluss** – Diese Gruppe umfasst Funktionen, die mit Zahlungen und Auftragsabschluss auf der Seite **Auftrag** verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="0cdaa-115">**Direktverkauf** – Diese Gruppe umfasst Funktionen, die Quellcodes, Skripts und Kataloganforderungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="0cdaa-116">Wenn Sie diese Funktionen in den Callcentereinstellungen aktiviert haben, sind sie auf der Seite **Auftrag** für Benutzer verfügbar, die dem Callcenter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="0cdaa-117">Die meisten dieser Funktionen erfordern zusätzliche Einstellungen, bevor sie verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="0cdaa-118">Bevor Benutzer Callcenteraufträge erstellen können, müssen Sie diese Benutzer dem Callcenter als Callcenterbenutzer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="0cdaa-119">Dieser Schritt ermöglicht callcenterkanalspezifische Konfigurationen und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="0cdaa-120">Nachfolgend finden Sie einige Beispiele der Funktionen, die zur Verfügung stehen:</span><span class="sxs-lookup"><span data-stu-id="0cdaa-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="0cdaa-121">Geführte Verkäufe stellen Konfigurationsoptionen für Telesales-Skripts und Produktbilder bereit, um Verkaufssachbearbeitern zu helfen und zu führen, während diese Aufträge entgegennehmen.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-121">Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="0cdaa-122">Aufträge können erst abgeschlossen werden, wenn Verkaufssachbearbeiter mindestens eine Zahlungsmethode aufgezeichnet haben.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="0cdaa-123">Regeln für weiteren Verkauf/ergänzenden Verkauf können konfiguriert werden, um Verkaufssachbearbeiter aufzufordern, bestimmte Produkte für Kunden zu bewerben.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="0cdaa-124">Verkaufssachbearbeiter können den Quellcode für den Katalog aufzeichnen, von dem ein Debitor bestellt.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="0cdaa-125">Verkaufssachbearbeiter können die Coupons eines Einzelhändlers dem Auftrag hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="0cdaa-126">Verkaufssachbearbeiter können Anschlussprogramme verkaufen.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="0cdaa-127">Aufträge können manuell oder automatisch gesperrt werden, um anzugeben, dass weitere Untersuchungen erforderlich sind, bevor der Auftrag bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0cdaa-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





