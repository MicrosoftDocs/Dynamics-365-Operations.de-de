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
ms.openlocfilehash: 1b0afeabfecb60672156692f3cd809445624020c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969975"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="8f8be-103">Ein Onlinefunktionsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="8f8be-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8f8be-104">In diesem Thema erhalten Sie einen Überblick über das Einrichten eines Onlinefunktionsprofils für Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f8be-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8f8be-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8f8be-105">Overview</span></span>

<span data-ttu-id="8f8be-106">Das Online-Funktionalitätsprofil bietet verschiedene Einstellungen für Onlinekanäle.</span><span class="sxs-lookup"><span data-stu-id="8f8be-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="8f8be-107">Jeder Online-Kanal muss ein Online-Funktionsprofil angeben.</span><span class="sxs-lookup"><span data-stu-id="8f8be-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="8f8be-108">Ein Onlinefunktionsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="8f8be-108">Create an online functionality profile</span></span>

<span data-ttu-id="8f8be-109">In der folgenden Prozedur wird erläutert, wie Sie ein Onlinefunktionalitätsprofil in der Commerce Headquarters-App erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f8be-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="8f8be-110">Gehen Sie im Navigationsbereich zu **Module \> Kanaleinrichtung \> Oline Shop einrichten \> Funktionsprofile**.</span><span class="sxs-lookup"><span data-stu-id="8f8be-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="8f8be-111">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8f8be-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8f8be-112">In dem Feld **Profil** geben Sie eine ID für das Profil ein.</span><span class="sxs-lookup"><span data-stu-id="8f8be-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="8f8be-113">Geben Sie im Feld **Beschreibung** einen Wert ein („Adventure Works Profile“ im folgenden Beispielbild).</span><span class="sxs-lookup"><span data-stu-id="8f8be-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="8f8be-114">In dem Abschnitt **Funktionen** ändern Sie die Einstellungen **EINKAUFSWAGEN**, **EINZELHANDELSKUNDEN** oder **AUSCHECKEN** nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="8f8be-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="8f8be-115">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="8f8be-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8f8be-116">Das folgende Bild zeigt ein Beispiel für ein Online-Funktionsprofil.</span><span class="sxs-lookup"><span data-stu-id="8f8be-116">The following image shows an example online functionality profile.</span></span>
  
![Online-Funktionsprofil Beispiel](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="8f8be-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="8f8be-118">Functions</span></span>

- <span data-ttu-id="8f8be-119">**Aggregatprodukte**: Wenn diese Funktion aktiviert ist, kann der Warenkorb die Menge aktualisieren, wenn derselbe Artikel mehrmals hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8f8be-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="8f8be-120">**Kasse ohne Zahlungen zulassen** : Wenn diese Funktion aktiviert ist, wird das Szenario behandelt, wenn zum Warenkorb hinzugefügte Artikel einen Preis von $0.00 haben.</span><span class="sxs-lookup"><span data-stu-id="8f8be-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="8f8be-121">**Kunden im asynchronen Modus erstellen**: Dies ist eine Vorgängereinstellung für E-Commerce-Kanäle von Drittanbietern und gilt nicht für die Dynamics 365-E-Commerce-Site.</span><span class="sxs-lookup"><span data-stu-id="8f8be-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f8be-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8f8be-122">Additional resources</span></span>

[<span data-ttu-id="8f8be-123">Kanäle Übersicht</span><span class="sxs-lookup"><span data-stu-id="8f8be-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="8f8be-124">Kanaleinstellungen – Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8f8be-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="8f8be-125">Einen Onlinekanal einrichten</span><span class="sxs-lookup"><span data-stu-id="8f8be-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="8f8be-126">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="8f8be-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="8f8be-127">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="8f8be-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
