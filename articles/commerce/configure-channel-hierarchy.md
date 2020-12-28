---
title: Einen Kanal zur Verwendung einer Kanalnavigationshierarchie konfigurieren
description: In diesem Thema wird beschrieben, wie Sie einen Kanal für die Verwendung einer Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce konfigurieren.
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
ms.openlocfilehash: 7b5041d35d310125c314ab2cb77d3cc40cdb7113
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412469"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="a3372-103">Einen Kanal zur Verwendung einer Kanalnavigationshierarchie konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a3372-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a3372-104">In diesem Thema wird beschrieben, wie Sie einen Kanal für die Verwendung einer Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a3372-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a3372-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a3372-105">Overview</span></span>

<span data-ttu-id="a3372-106">Kanalnavigationshierarchien organisieren Produkte in Kategorien, sodass die Produkte auf einer E-Commerce-Website oder an Verkaufsstellen (POS) durchsucht werden können.</span><span class="sxs-lookup"><span data-stu-id="a3372-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="a3372-107">Einzelhandels- und Onlinekanäle müssen mit Kanalnavigationshierarchien konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a3372-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="a3372-108">Den Kanal konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a3372-108">Configure the channel</span></span>

<span data-ttu-id="a3372-109">Gehen Sie folgendermaßen vor, um einen Kanal für die Verwendung einer Kanalnavigationshierarchie zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a3372-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="a3372-110">Wechseln Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Kanaleinstellungen \> Kanalkategorien und Produktattribute**.</span><span class="sxs-lookup"><span data-stu-id="a3372-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="a3372-111">Wählen Sie den zu konfigurierenden Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="a3372-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="a3372-112">Wählen Sie im Aktivitätsbereich **Attributmetadaten festlegen**.</span><span class="sxs-lookup"><span data-stu-id="a3372-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="a3372-113">Wählen Sie in der Dropdownliste **Kategoriehierarchie** die entsprechende Kanalnavigationshierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="a3372-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="a3372-114">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="a3372-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="a3372-115">Fügen Sie unter **Attributgruppe** alle Attributgruppen hinzu, die globale Attribute für alle Knoten sein werden.</span><span class="sxs-lookup"><span data-stu-id="a3372-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="a3372-116">Das folgende Bild zeigt, wie Sie einen Kanal für die Verwendung einer Kanalnavigationshierarchie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a3372-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Beispiel Kanalkonfiguration](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="a3372-118">Attributmetadaten festlegen</span><span class="sxs-lookup"><span data-stu-id="a3372-118">Set attribute metadata</span></span>

<span data-ttu-id="a3372-119">Durch Festlegen der Attributmetadaten können Attribute auf jedem Knoten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a3372-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="a3372-120">Führen Sie die folgenden Schritte aus, um Attributmetadaten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a3372-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="a3372-121">Wählen Sie im Aktivitätsbereich **Attributmetadaten festlegen**.</span><span class="sxs-lookup"><span data-stu-id="a3372-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="a3372-122">Wählen Sie für jeden Knoten **Kanalproduktattribute** aus.</span><span class="sxs-lookup"><span data-stu-id="a3372-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="a3372-123">Legen Sie **Attribut auf Kanal anzeigen** auf **Ja** und **Kann verfeinert werden** auf **Ja** fest, um die Filter für diesen Kanal zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a3372-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="a3372-124">Nachdem Sie jeden Knoten wie gewünscht konfiguriert haben, wählen Sie im **Aktionsbereich** die Schaltfläche **Speichern** zum Speichern aus.</span><span class="sxs-lookup"><span data-stu-id="a3372-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="a3372-125">Wählen Sie das **X** in der oberen rechten Ecke, um diesen Bildschirm zu verlassen und zur Seite **Kanalkategorien und Produktattribute** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a3372-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="a3372-126">Die folgende Abbildung zeigt ein Beispiel für eine Reihe von Kanalproduktattributen, die auf einem Kanalkategorieknoten konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="a3372-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanalattribute auf einem Kanalkategorieknoten](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="a3372-128">Änderungen veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="a3372-128">Publish changes</span></span>

<span data-ttu-id="a3372-129">Damit die Änderungen wirksam werden, müssen Sie die Änderungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a3372-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="a3372-130">Führen Sie folgende Schritte aus, um die Änderungen zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a3372-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="a3372-131">Wählen Sie im Aktionsbereich **Kanalaktualisierungen veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="a3372-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="a3372-132">Wählen Sie im Bereich **Kanalaktualisierungen veröffentlichen** **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a3372-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="a3372-133">Das folgende Bild zeigt, wie Kanalaktualisierungen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="a3372-133">The following image shows how to publish channel updates.</span></span>

![Kanalupdates veröffentlichen](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="a3372-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a3372-135">Additional resources</span></span>

[<span data-ttu-id="a3372-136">Eine Kanalnavigationshierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="a3372-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


