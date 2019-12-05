---
title: Unterlieferung einrichten
description: In diesem Thema wird erläutert, wie eingehende Lieferungsbestandsvorgänge konfiguriert werden.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 04b3fb3038a1373e203ec240a0163cf67de655cc
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813843"
---
# <a name="set-up-consignment"></a><span data-ttu-id="7b8da-103">Unterlieferung einrichten</span><span class="sxs-lookup"><span data-stu-id="7b8da-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b8da-104">In diesem Thema wird erläutert, wie eingehende Lieferungsbestandsvorgänge konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="7b8da-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="7b8da-105">Beim Lieferungsbestand handelt es sich um Bestand, der im Besitz eines Kreditors ist, der aber an Ihrem Standort gelagert ist.</span><span class="sxs-lookup"><span data-stu-id="7b8da-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="7b8da-106">Wenn Sie bereit sind, den Bestand zu verbrauchen oder verwenden, übernehmen Sie den Besitz des Bestands.</span><span class="sxs-lookup"><span data-stu-id="7b8da-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="7b8da-107">In diesem Thema werden die Einstellungen beschrieben, die benötigt werden, um Lieferungsprozesse zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7b8da-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="7b8da-108">Weitere Informationen zu Konsignationsprozessen finden Sie unter [Konsignation einrichten](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="7b8da-108">For more information about consignment processes, see [Set up consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="7b8da-109">Bestandsbesitzer</span><span class="sxs-lookup"><span data-stu-id="7b8da-109">Inventory owners</span></span>
<span data-ttu-id="7b8da-110">Um physischen, eingehenden Lieferungsbestand zu erfassen, müssen Sie einen Kreditoreneigentümer definieren.</span><span class="sxs-lookup"><span data-stu-id="7b8da-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="7b8da-111">Dies erfolgt auf der Seite **Bestandseigentümer**.</span><span class="sxs-lookup"><span data-stu-id="7b8da-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="7b8da-112">Wenn Sie ein **Kreditorenkonto** auswählen, generiert dies Standardwerte für die Felder **Name** und **Besitzer**.</span><span class="sxs-lookup"><span data-stu-id="7b8da-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="7b8da-113">Der Wert im Feld **Besitzer** wird für den Kreditor angezeigt, somit möchten Sie ihn möglicherweise ändern, wenn die Namen Ihres Kreditorenkontos von externen Personen nicht einfach erkannt werden können.</span><span class="sxs-lookup"><span data-stu-id="7b8da-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="7b8da-114">Es ist möglich, das Feld **Besitzer** zu bearbeiten. Dies gilt jedoch nur bis zu dem Zeiptunkt, an dem Sie den Datensatz **Bestandsbesitzer** speichern.</span><span class="sxs-lookup"><span data-stu-id="7b8da-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="7b8da-115">Das Feld **Name** wird mit dem Namen der Partei aufgefüllt, dem das Kreditorenkonto zugeordnet ist, und dieser kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7b8da-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="7b8da-116">[![Bestandsbesitzer](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="7b8da-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="7b8da-117">Rückverfolgungsgruppe</span><span class="sxs-lookup"><span data-stu-id="7b8da-117">Tracking dimension group</span></span>
<span data-ttu-id="7b8da-118">Artikel, die bei Lieferungsprozessen verwendet werden, müssen einer **Rückverfolgungsangabengruppe** zugeordnet werden, wobei die Dimension **Besitzer** auf **Aktiv** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7b8da-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="7b8da-119">Bei der „Besitzerdimension” sind die Optionen **Physischer Bestand** und **Wertmäßiger Bestand** immer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b8da-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="7b8da-120">Die Option **Disposition nach Dimensionen** ist nie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b8da-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="7b8da-121">[![Rückverfolgungsangabengruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="7b8da-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="7b8da-122">Erfassung für die Änderung von Bestandseigentümern</span><span class="sxs-lookup"><span data-stu-id="7b8da-122">Inventory ownership change journal</span></span>
<span data-ttu-id="7b8da-123">Die Erfassung **Bestandsbesitzänderung**wird verwendet, um die Übertragung des Besitzes des Lieferungsbestands vom Kreditor zur juristischen Person, die ihn verbraucht, aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="7b8da-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="7b8da-124">Wie jede Bestandserfassung muss sie mit einem Bestandserfassungsname identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7b8da-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="7b8da-125">Diese Namen werden auf der Seite **Bestandserfassungsnamen** erstellt, und der **Erfassungstyp** muss auf **Besitzänderung** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7b8da-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="7b8da-126">[![Bestandeigentümer-Änderungserfassung](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="7b8da-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="7b8da-127">Kreditorenzusammenarbeit in den Lieferungsprozessen</span><span class="sxs-lookup"><span data-stu-id="7b8da-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="7b8da-128">Wenn Ihre Kreditoren die Kreditorenzusammenarbeitschnittstelle verwenden, können sie diese verwenden, um den Verbrauch des Bestands an Ihrem Standort zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="7b8da-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="7b8da-129">Weitere Informationen zur Einrichtung von Kreditoren zur Verwendung der Kreditorenzusammenarbeit finden Sie unter [Benutzersicherheit für Kreditorenportal](../procurement/configure-security-vendor-portal-users.md)</span><span class="sxs-lookup"><span data-stu-id="7b8da-129">For more information about setting up vendors to use vendor collaboration, see [Vendor portal user security](../procurement/configure-security-vendor-portal-users.md).</span></span>
