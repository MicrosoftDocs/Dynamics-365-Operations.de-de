---
title: Ein Onlinefunktionsprofil erstellen
description: In diesem Thema wird beschrieben, wie Sie ein Online-Funktionsprofil in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cb9d78a945132c913dcb8a5d5b41eaacd1a6db3b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477731"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="7d068-103">Ein Onlinefunktionsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="7d068-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d068-104">In diesem Thema erhalten Sie einen Überblick über das Einrichten eines Onlinefunktionsprofils für Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7d068-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7d068-105">Das Online-Funktionalitätsprofil bietet verschiedene Einstellungen für Onlinekanäle.</span><span class="sxs-lookup"><span data-stu-id="7d068-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="7d068-106">Jeder Online-Kanal muss ein Online-Funktionsprofil angeben.</span><span class="sxs-lookup"><span data-stu-id="7d068-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="7d068-107">Ein Onlinefunktionsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="7d068-107">Create an online functionality profile</span></span>

<span data-ttu-id="7d068-108">In der folgenden Prozedur wird erläutert, wie Sie ein Onlinefunktionalitätsprofil in der Commerce Headquarters-App erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d068-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="7d068-109">Gehen Sie im Navigationsbereich zu **Module \> Kanaleinrichtung \> Oline Shop einrichten \> Funktionsprofile**.</span><span class="sxs-lookup"><span data-stu-id="7d068-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="7d068-110">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7d068-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7d068-111">In dem Feld **Profil** geben Sie eine ID für das Profil ein.</span><span class="sxs-lookup"><span data-stu-id="7d068-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="7d068-112">Geben Sie im Feld **Beschreibung** einen Wert ein („Adventure Works Profile“ im folgenden Beispielbild).</span><span class="sxs-lookup"><span data-stu-id="7d068-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="7d068-113">In dem Abschnitt **Funktionen** ändern Sie die Einstellungen **EINKAUFSWAGEN**, **EINZELHANDELSKUNDEN** oder **AUSCHECKEN** nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7d068-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="7d068-114">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="7d068-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7d068-115">Das folgende Bild zeigt ein Beispiel für ein Online-Funktionsprofil.</span><span class="sxs-lookup"><span data-stu-id="7d068-115">The following image shows an example online functionality profile.</span></span>
  
![Online-Funktionsprofil Beispiel](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="7d068-117">Funktionen</span><span class="sxs-lookup"><span data-stu-id="7d068-117">Functions</span></span>

- <span data-ttu-id="7d068-118">**Aggregatprodukte**: Wenn diese Funktion aktiviert ist, kann der Warenkorb die Menge aktualisieren, wenn derselbe Artikel mehrmals hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7d068-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="7d068-119">**Kasse ohne Zahlungen zulassen** : Wenn diese Funktion aktiviert ist, wird das Szenario behandelt, wenn zum Warenkorb hinzugefügte Artikel einen Preis von $0.00 haben.</span><span class="sxs-lookup"><span data-stu-id="7d068-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="7d068-120">**Kunden im asynchronen Modus erstellen**: Dies ist eine Vorgängereinstellung für E-Commerce-Kanäle von Drittanbietern und gilt nicht für die Dynamics 365-E-Commerce-Site.</span><span class="sxs-lookup"><span data-stu-id="7d068-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d068-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7d068-121">Additional resources</span></span>

[<span data-ttu-id="7d068-122">Kanäle Übersicht</span><span class="sxs-lookup"><span data-stu-id="7d068-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7d068-123">Kanaleinstellungen – Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7d068-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7d068-124">Einen Onlinekanal einrichten</span><span class="sxs-lookup"><span data-stu-id="7d068-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7d068-125">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="7d068-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="7d068-126">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="7d068-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
