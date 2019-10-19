---
title: Callcentervertriebs-Funktionen
description: Dieses Thema bietet einen Überblick über die Callcenter-Vertriebsfunktionen in Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
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
ms.openlocfilehash: 902db94164b35077a876c8041c038af36561a634
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025770"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="0d66b-103">Callcenter-Vertriebsfunktionen</span><span class="sxs-lookup"><span data-stu-id="0d66b-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0d66b-104">In Dynamics 365 Retail ist ein Callcenter ein Retail Channel-Typ, der in der Anwendung definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d66b-104">In Dynamics 365 Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="0d66b-105">Durch die Definition eines bestimmten Kanals für Ihre Call-Center-Einheiten kann das System bestimmte Datenvorgaben und Auftragsbearbeitungsvorgaben an Kundenaufträge binden, die von einem Benutzer des Call-Center-Kanals angelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="0d66b-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="0d66b-106">Call-Center-Funktionen umfassen erweiterte Einzelhandelspreise und Promotions, Kataloge, Geschenkkarten, Treueprogramme und Gutscheine.</span><span class="sxs-lookup"><span data-stu-id="0d66b-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="0d66b-107">Call-Center-Aufträge werden auch von der POS-Anwendung (Point of Sale) genutzt, um kanalübergreifende Auftragserfüllungsszenarien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0d66b-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="0d66b-108">Es ist wichtig zu beachten, dass das Callcenter-Modul zwar auch von anderen Branchen außerhalb des Einzelhandels genutzt werden kann, die aktuelle Version der Retail-Callcenter-Anwendung jedoch nicht für den Einsatz in Business-to-Business(B2B)-Auftragsabwicklungsszenarien oder Szenarien mit einer großen Anzahl von Verkaufspositionen optimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0d66b-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="0d66b-109">Es wird empfohlen, dass Benutzer, die die Call-Center-Funktionen für die Auftragsbearbeitung außerhalb der typischen Direct-to-Consumer-Transaktionsverarbeitung nutzen möchten, sich ausreichend Zeit nehmen, um zu testen und zu bestätigen, dass die Call-Center-Funktionalität den funktionalen und Leistungsanforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="0d66b-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="0d66b-110">Zusätzlich zur Unterstützung der Auftragserstellung bietet das Call-Center-Modul auch eine benutzerfreundliche Anwendung für den Kundenservice, die es den Benutzern erleichtert, Debitorenkonten zu finden und alle zugehörigen Auftragsdaten und -attribute zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0d66b-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="0d66b-111">Der Kundendienstbildschirm ist so gestaltet, dass der Benutzer schnell auf die auftragsbezogenen Daten zugreifen kann, um die häufigsten Fragen zu beantworten, die er von Kunden erhält.</span><span class="sxs-lookup"><span data-stu-id="0d66b-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="0d66b-112">Auf dieser Seite finden Sie Links zu relevanter Dokumentation zur Einrichtung, Konfiguration und funktionalen Nutzung der Callcenter-Funktionen in Retail.</span><span class="sxs-lookup"><span data-stu-id="0d66b-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Retail.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="0d66b-113">Callcenter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0d66b-113">Configure the call center</span></span>

[<span data-ttu-id="0d66b-114">Auftragsabwicklungsoptionen einrichten</span><span class="sxs-lookup"><span data-stu-id="0d66b-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="0d66b-115">Auftragsbearbeitung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0d66b-115">Configure order processing</span></span>

[<span data-ttu-id="0d66b-116">Betrugswarnungen einrichten</span><span class="sxs-lookup"><span data-stu-id="0d66b-116">Set up fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="0d66b-117">Manuelle Auftragssperren</span><span class="sxs-lookup"><span data-stu-id="0d66b-117">Manual Order Holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="0d66b-118">Zahlungsabwicklung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0d66b-118">Configure payment processing</span></span>

[<span data-ttu-id="0d66b-119">Zahlungsmethoden in einem Callcenter</span><span class="sxs-lookup"><span data-stu-id="0d66b-119">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="0d66b-120">Konfigurieren von Lieferarten</span><span class="sxs-lookup"><span data-stu-id="0d66b-120">Configure delivery modes</span></span>

[<span data-ttu-id="0d66b-121">Konfigurieren von Callcenter-Lieferarten und -Belastungen</span><span class="sxs-lookup"><span data-stu-id="0d66b-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="0d66b-122">Direktmarketing konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0d66b-122">Configure direct marketing</span></span>

[<span data-ttu-id="0d66b-123">Callcenterkataloge</span><span class="sxs-lookup"><span data-stu-id="0d66b-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="0d66b-124">Analyse nach Aktualität, Häufigkeit und finanziellen Gesichtspunkten (RFM) einrichten</span><span class="sxs-lookup"><span data-stu-id="0d66b-124">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="0d66b-125">Kontinuitätsprogramme konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0d66b-125">Configure continuity programs</span></span>

[<span data-ttu-id="0d66b-126">Einrichten eines Anschlussprogramms für einen Callcenter</span><span class="sxs-lookup"><span data-stu-id="0d66b-126">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)
