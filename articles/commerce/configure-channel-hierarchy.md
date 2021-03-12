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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3dcba743e6557b1bd366ac79ecb49ead831dceb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001024"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="44df2-103">Einen Kanal zur Verwendung einer Kanalnavigationshierarchie konfigurieren</span><span class="sxs-lookup"><span data-stu-id="44df2-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="44df2-104">In diesem Thema wird beschrieben, wie Sie einen Kanal für die Verwendung einer Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="44df2-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="44df2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="44df2-105">Overview</span></span>

<span data-ttu-id="44df2-106">Kanalnavigationshierarchien organisieren Produkte in Kategorien, sodass die Produkte auf einer E-Commerce-Website oder an Verkaufsstellen (POS) durchsucht werden können.</span><span class="sxs-lookup"><span data-stu-id="44df2-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="44df2-107">Einzelhandels- und Onlinekanäle müssen mit Kanalnavigationshierarchien konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="44df2-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="44df2-108">Den Kanal konfigurieren</span><span class="sxs-lookup"><span data-stu-id="44df2-108">Configure the channel</span></span>

<span data-ttu-id="44df2-109">Gehen Sie folgendermaßen vor, um einen Kanal für die Verwendung einer Kanalnavigationshierarchie zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="44df2-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="44df2-110">Wechseln Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinstellungen \> Kanalkategorien und Produktattribute**.</span><span class="sxs-lookup"><span data-stu-id="44df2-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="44df2-111">Wählen Sie den zu konfigurierenden Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="44df2-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="44df2-112">Wählen Sie im Aktivitätsbereich **Attributmetadaten festlegen**.</span><span class="sxs-lookup"><span data-stu-id="44df2-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="44df2-113">Wählen Sie in der Dropdownliste **Kategoriehierarchie** die entsprechende Kanalnavigationshierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="44df2-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="44df2-114">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="44df2-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="44df2-115">Fügen Sie unter **Attributgruppe** alle Attributgruppen hinzu, die globale Attribute für alle Knoten sein werden.</span><span class="sxs-lookup"><span data-stu-id="44df2-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="44df2-116">Das folgende Bild zeigt, wie Sie einen Kanal für die Verwendung einer Kanalnavigationshierarchie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="44df2-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Beispiel Kanalkonfiguration](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="44df2-118">Attributmetadaten festlegen</span><span class="sxs-lookup"><span data-stu-id="44df2-118">Set attribute metadata</span></span>

<span data-ttu-id="44df2-119">Durch Festlegen der Attributmetadaten können Attribute auf jedem Knoten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="44df2-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="44df2-120">Führen Sie die folgenden Schritte aus, um Attributmetadaten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="44df2-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="44df2-121">Wählen Sie im Aktivitätsbereich **Attributmetadaten festlegen**.</span><span class="sxs-lookup"><span data-stu-id="44df2-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="44df2-122">Wählen Sie für jeden Knoten **Kanalproduktattribute** aus.</span><span class="sxs-lookup"><span data-stu-id="44df2-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="44df2-123">Legen Sie **Attribut auf Kanal anzeigen** auf **Ja** und **Kann verfeinert werden** auf **Ja** fest, um die Filter für diesen Kanal zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="44df2-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="44df2-124">Nachdem Sie jeden Knoten wie gewünscht konfiguriert haben, wählen Sie im **Aktionsbereich** die Schaltfläche **Speichern** zum Speichern aus.</span><span class="sxs-lookup"><span data-stu-id="44df2-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="44df2-125">Wählen Sie das **X** in der oberen rechten Ecke, um diesen Bildschirm zu verlassen und zur Seite **Kanalkategorien und Produktattribute** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="44df2-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="44df2-126">Die folgende Abbildung zeigt ein Beispiel für eine Reihe von Kanalproduktattributen, die auf einem Kanalkategorieknoten konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="44df2-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanalattribute auf einem Kanalkategorieknoten](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="44df2-128">Änderungen veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="44df2-128">Publish changes</span></span>

<span data-ttu-id="44df2-129">Damit die Änderungen wirksam werden, müssen Sie die Änderungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="44df2-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="44df2-130">Führen Sie folgende Schritte aus, um die Änderungen zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="44df2-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="44df2-131">Wählen Sie im Aktionsbereich **Kanalaktualisierungen veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="44df2-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="44df2-132">Wählen Sie im Bereich **Kanalaktualisierungen veröffentlichen** **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="44df2-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="44df2-133">Das folgende Bild zeigt, wie Kanalaktualisierungen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="44df2-133">The following image shows how to publish channel updates.</span></span>

![Kanalupdates veröffentlichen](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="44df2-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="44df2-135">Additional resources</span></span>

[<span data-ttu-id="44df2-136">Eine Kanalnavigationshierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="44df2-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


