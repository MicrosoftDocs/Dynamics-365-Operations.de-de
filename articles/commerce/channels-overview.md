---
title: Kanalübersicht
description: Dieses Thema bietet einen Überblick über Kanäle in Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002357"
---
# <a name="channels-overview"></a><span data-ttu-id="48018-103">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="48018-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="48018-104">Dieses Thema bietet einen Überblick über Kanäle in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48018-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="48018-105">Er umfasst Informationen über die Aufgaben, die Sie durchführen müssen, bevor und nachdem Sie die einzelnen Kanäle einrichten.</span><span class="sxs-lookup"><span data-stu-id="48018-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="48018-106">Kanaltypen</span><span class="sxs-lookup"><span data-stu-id="48018-106">Types of Channels</span></span>

<span data-ttu-id="48018-107">Dynamics 365 Commerceunterstützt drei verschiedene Kanaltypen: Einzelhandel, Callcenter und Onlinekanäle.</span><span class="sxs-lookup"><span data-stu-id="48018-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="48018-108">Einzelhandelskanäle</span><span class="sxs-lookup"><span data-stu-id="48018-108">Retail channels</span></span>

<span data-ttu-id="48018-109">Retail Channel repräsentieren herkömmliche physische Shops.</span><span class="sxs-lookup"><span data-stu-id="48018-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="48018-110">Jeder Shop kann seine eigenen POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten.</span><span class="sxs-lookup"><span data-stu-id="48018-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="48018-111">Callcenterkanäle</span><span class="sxs-lookup"><span data-stu-id="48018-111">Call center channels</span></span>

<span data-ttu-id="48018-112">Callcenterkanäle stehen für die Callcenter-Bestellung und Kundenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="48018-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="48018-113">Onlinekanäle</span><span class="sxs-lookup"><span data-stu-id="48018-113">Online channels</span></span>

<span data-ttu-id="48018-114">Onlinekanäle repräsentieren Online-E-Commerce-Schaufenster.</span><span class="sxs-lookup"><span data-stu-id="48018-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="48018-115">Sobald ein Onlinekanal erstellt wurde, muss eine Site mit dem Microsoft Dynamics 365 Commerce Site Builder-Tool oder einer anderen E-Commerce-Lösung eines Drittanbieters erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="48018-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="48018-116">Grundlagen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="48018-116">Channel setup basics</span></span>

<span data-ttu-id="48018-117">Die Kanaleinrichtung wird im Commerce-Tool durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="48018-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="48018-118">Jeder Kanal kann über eigene Zahlungsmethoden, Preisgruppen, Produkthierarchien, Sortimente und Produktgruppen verfügen.</span><span class="sxs-lookup"><span data-stu-id="48018-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="48018-119">Nachdem Sie einen Kanal erstellt haben, weisen Sie die Produkte zu, die Sie führen und verkaufen möchten.</span><span class="sxs-lookup"><span data-stu-id="48018-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="48018-120">Jeder Kanaltyp verfügt über eine Reihe von Funktionen, die möglicherweise konfiguriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="48018-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="48018-121">Ein Retail Channel benötigt beispielsweise zugewiesene Mitarbeiter, Register und Kunden.</span><span class="sxs-lookup"><span data-stu-id="48018-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="48018-122">Sobald ein neuer Kanal erstellt wurde, muss er einer Organisationshierarchie zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="48018-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="48018-123">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="48018-123">Channel setup prerequisites</span></span>

<span data-ttu-id="48018-124">Bevor Sie einen Kanal einrichten können, müssen Sie einige erforderliche Aufgaben basierend auf dem Kanaltyp ausführen.</span><span class="sxs-lookup"><span data-stu-id="48018-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="48018-125">Weitere Informationen finden Sie unter [Voraussetzungen für die Kanaleinrichtung ](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="48018-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="48018-126">Einen Kanal einrichten</span><span class="sxs-lookup"><span data-stu-id="48018-126">Set up a channel</span></span>

<span data-ttu-id="48018-127">Verwenden Sie nach Abschluss der erforderlichen Aufgaben die folgenden Links, um weitere Anweisungen zur Einrichtung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="48018-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="48018-128">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="48018-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="48018-129">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="48018-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="48018-130">Einen Onlinekanal einrichten</span><span class="sxs-lookup"><span data-stu-id="48018-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="48018-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="48018-131">Additional resources</span></span>

[<span data-ttu-id="48018-132">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="48018-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="48018-133">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="48018-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="48018-134">Einen Onlinekanal einrichten</span><span class="sxs-lookup"><span data-stu-id="48018-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="48018-135">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="48018-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="48018-136">Organisationshierarchien einrichten</span><span class="sxs-lookup"><span data-stu-id="48018-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)
