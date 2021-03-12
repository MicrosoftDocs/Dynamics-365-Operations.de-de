---
title: Callcentervertriebs-Funktionen
description: Dieses Thema bietet einen Überblick über die Callcenter-Vertriebsfunktionen in Dynamics 365 Commerce.
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
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d188138654ba20d8393ed4bca8124a65402daff2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991439"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="27a58-103">Callcenter-Vertriebsfunktionen</span><span class="sxs-lookup"><span data-stu-id="27a58-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="27a58-104">In Dynamics 365 Commerce ist ein Callcenter ein Kanaltyp, der in der Anwendung definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="27a58-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="27a58-105">Durch die Definition eines bestimmten Kanals für Ihre Call-Center-Einheiten kann das System bestimmte Datenvorgaben und Auftragsbearbeitungsvorgaben an Kundenaufträge binden, die von einem Benutzer des Call-Center-Kanals angelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="27a58-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="27a58-106">Call-Center-Funktionen umfassen erweiterte Preise und Promotionen, Kataloge, Geschenkkarten, Treueprogramme und Gutscheine.</span><span class="sxs-lookup"><span data-stu-id="27a58-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="27a58-107">Call-Center-Aufträge werden auch von der POS-Anwendung (Point of Sale) genutzt, um kanalübergreifende Auftragserfüllungsszenarien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="27a58-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="27a58-108">Es ist wichtig zu beachten, dass das Callcenter-Modul zwar auch von anderen Branchen außerhalb von Commerce genutzt werden kann, die aktuelle Version der -Callcenter-Anwendung jedoch nicht für den Einsatz in Business-to-Business (B2B)-Auftragsabwicklungsszenarien oder Szenarien mit einer großen Zahl von Verkaufspositionen optimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="27a58-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large number of sales lines.</span></span> <span data-ttu-id="27a58-109">Es wird empfohlen, dass Benutzer, die die Call-Center-Funktionen für die Auftragsbearbeitung außerhalb der typischen Direct-to-Consumer-Transaktionsverarbeitung nutzen möchten, sich ausreichend Zeit nehmen, um zu testen und zu bestätigen, dass die Call-Center-Funktionalität den funktionalen und Leistungsanforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="27a58-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="27a58-110">Zusätzlich zur Unterstützung der Auftragserstellung bietet das Call-Center-Modul auch eine benutzerfreundliche Anwendung für den Kundenservice, die es den Benutzern erleichtert, Debitorenkonten zu finden und alle zugehörigen Auftragsdaten und -attribute zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="27a58-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="27a58-111">Der Kundendienstbildschirm ist so gestaltet, dass der Benutzer schnell auf die auftragsbezogenen Daten zugreifen kann, um so die häufigsten Fragen zu beantworten, die er von Kunden erhält.</span><span class="sxs-lookup"><span data-stu-id="27a58-111">The customer service screen is designed to enable a user to quickly access order-related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="27a58-112">Auf dieser Seite finden Sie Links zu relevanter Dokumentation zur Einrichtung, Konfiguration und funktionalen Nutzung der Callcenter-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="27a58-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="27a58-113">Callcenter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="27a58-113">Configure the call center</span></span>

[<span data-ttu-id="27a58-114">Einrichten von Callcenterkanälen</span><span class="sxs-lookup"><span data-stu-id="27a58-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="27a58-115">Auftragsbearbeitung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="27a58-115">Configure order processing</span></span>

[<span data-ttu-id="27a58-116">Einstellungen und Arbeiten mit Callcenterbetrugswarnungen</span><span class="sxs-lookup"><span data-stu-id="27a58-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="27a58-117">Konfigurieren und Arbeiten mit Callcenter-Auftragssperren</span><span class="sxs-lookup"><span data-stu-id="27a58-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="27a58-118">Zahlungsabwicklung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="27a58-118">Configure payment processing</span></span>

[<span data-ttu-id="27a58-119">Zahlungsmethoden in Callcentern</span><span class="sxs-lookup"><span data-stu-id="27a58-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="27a58-120">Konfigurieren von Lieferarten</span><span class="sxs-lookup"><span data-stu-id="27a58-120">Configure delivery modes</span></span>

[<span data-ttu-id="27a58-121">Konfigurieren von Callcenter-Lieferarten und -Belastungen</span><span class="sxs-lookup"><span data-stu-id="27a58-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="27a58-122">Direktmarketing konfigurieren</span><span class="sxs-lookup"><span data-stu-id="27a58-122">Configure direct marketing</span></span>

[<span data-ttu-id="27a58-123">Callcenterkataloge</span><span class="sxs-lookup"><span data-stu-id="27a58-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="27a58-124">Einrichten von Analysen zu Aktualität, Häufigkeit und Geldbeträgen (RFM)</span><span class="sxs-lookup"><span data-stu-id="27a58-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="27a58-125">Kontinuitätsprogramme konfigurieren</span><span class="sxs-lookup"><span data-stu-id="27a58-125">Configure continuity programs</span></span>

[<span data-ttu-id="27a58-126">Einrichten von Anschlussprogrammen für Callcenter</span><span class="sxs-lookup"><span data-stu-id="27a58-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
