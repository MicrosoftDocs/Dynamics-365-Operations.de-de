---
title: Einen Lagerort einrichten
description: In diesem Thema wird beschrieben, wie Sie einen Lagerort für die Verwendung mit einem neuen Kanal in Microsoft Dynamics 365 Commerce einrichten.
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
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113758"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="fc6b2-103">Lagerort einrichten</span><span class="sxs-lookup"><span data-stu-id="fc6b2-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fc6b2-104">In diesem Thema wird beschrieben, wie Sie einen Lagerort für die Verwendung mit einem neuen Kanal in Microsoft Dynamics 365 Commerce einrichten.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fc6b2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="fc6b2-105">Overview</span></span>

<span data-ttu-id="fc6b2-106">Jedem Commerce-Kanal muss ein konfigurierter Lagerort zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="fc6b2-107">Die folgenden Verfahren bieten die Mindestkonfiguration, die zum Einrichten eines Lagerorts für einen Commerce-Kanal erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="fc6b2-108">Weitere Informationen zur Einrichtung des Lagerorts finden Sie in der [Übersicht über die Lagerortverwaltung](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fc6b2-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="fc6b2-109">Standort eines Lagerorts konfigurieren</span><span class="sxs-lookup"><span data-stu-id="fc6b2-109">Configure a warehouse site</span></span>

<span data-ttu-id="fc6b2-110">Vor dem Einrichten eines Lagerorts müssen Sie den Standort eines Lagerorts konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="fc6b2-111">Gehen Sie folgendermaßen vor, um den Standort eines Lagerorts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="fc6b2-112">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Kanaleinrichtung \> Standorte**.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="fc6b2-113">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fc6b2-114">Geben Sie im Feld **Standort** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="fc6b2-115">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="fc6b2-116">Legen Sie im Abschnitt **Allgemeines** die entsprechende **Zeitzone** fest.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="fc6b2-117">Geben Sie im Abschnitt **Adressen** eine Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="fc6b2-118">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fc6b2-119">Das folgende Bild zeigt ein Beispiel für den Standort eines Lagerorts.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-119">The following image shows an example warehouse site.</span></span>

![Beispiel: Standort eines Lagerorts](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="fc6b2-121">Einen Lagerort einrichten</span><span class="sxs-lookup"><span data-stu-id="fc6b2-121">Set up a warehouse</span></span>

<span data-ttu-id="fc6b2-122">Um einen Lagerort einzurichten, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="fc6b2-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="fc6b2-123">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Kanaleinrichtung \> Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="fc6b2-124">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fc6b2-125">Geben Sie im Feld **Lagerort** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="fc6b2-126">Wenn es sich um eine 1:1-Zuordnung zu einem Geschäft handelt, sollten Sie den Namen des Geschäfts oder den Namen eines regionalen Vertriebszentrums verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="fc6b2-127">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="fc6b2-128">In der Dropdown-Liste **Standort** wählen Sie den zuvor erstellten Standort des Lagerorts aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="fc6b2-129">Wählen Sie im Feld **Typ** die Option **Standard**.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="fc6b2-130">Wenn Sie ein **Quarantänelager** einrichten möchten, führen Sie zunächst die folgenden Schritte aus, um einen zusätzlichen Lagerort zu erstellen, in dem der **Typ** auf **Quarantäne** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="fc6b2-131">Wenn Sie ein **Transitlager** einrichten möchten, führen Sie zunächst die folgenden Schritte aus, um einen zusätzlichen Lagerort zu erstellen, in dem der **Typ** auf **Transit** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="fc6b2-132">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="fc6b2-133">Lagergänge einrichten</span><span class="sxs-lookup"><span data-stu-id="fc6b2-133">Set up inventory aisles</span></span>

<span data-ttu-id="fc6b2-134">Gehen Sie zum Einrichten von Lagergängen folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="fc6b2-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="fc6b2-135">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Kanaleinrichtung \> Standorteinrichtung \> Lagergänge**.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="fc6b2-136">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fc6b2-137">In der Dropdown-Liste **Lagerort** wählen Sie den zuvor erstellten Lagerort aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="fc6b2-138">Geben Sie im Feld **Gang** einen Namen ein (beispielsweise „Def”).</span><span class="sxs-lookup"><span data-stu-id="fc6b2-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="fc6b2-139">Geben Sie im Feld **Name** einen Namen ein (beispielsweise „Standardgang”).</span><span class="sxs-lookup"><span data-stu-id="fc6b2-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="fc6b2-140">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="fc6b2-141">Standorte für Lagerort-Lagerplätze einrichten</span><span class="sxs-lookup"><span data-stu-id="fc6b2-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="fc6b2-142">Führen Sie die folgenden Schritte aus, um Lagerorte für Standard-, beschädigte und zurückgegebene Bestände einzurichten.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="fc6b2-143">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Kanaleinrichtung \> Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="fc6b2-144">Wählen Sie den Lagerort aus, den Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="fc6b2-145">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="fc6b2-146">Wählen Sie im Aktionsbereich **Lagerort** und dann **Standort des Lagerorts** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="fc6b2-147">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-147">On the action pane, select **New**.</span></span> <span data-ttu-id="fc6b2-148">Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="fc6b2-149">Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="fc6b2-150">Stellen Sie **Manuelles Update** auf **Ja**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="fc6b2-151">Geben Sie im Feld **Standort** den Namen des Lagerorts ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="fc6b2-152">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="fc6b2-153">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="fc6b2-154">Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="fc6b2-155">Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="fc6b2-156">Stellen Sie **Manuelles Update** auf **Ja**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="fc6b2-157">Geben Sie im Feld **Lagerort** „Beschädigt“ ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="fc6b2-158">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="fc6b2-159">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="fc6b2-160">Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="fc6b2-161">Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="fc6b2-162">Stellen Sie **Manuelles Update** auf **Ja**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="fc6b2-163">Geben Sie im Feld **Lagerort** „Retouren“ ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="fc6b2-164">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="fc6b2-165">Die folgende Abbildung zeigt eine Einrichtung eines Lagerort-Standorts in San Francisco.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Beispiel für die Einrichtung des Standorts eines Lagerorts](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="fc6b2-167">Vollständige Einrichtung eines Lagerorts</span><span class="sxs-lookup"><span data-stu-id="fc6b2-167">Complete warehouse setup</span></span>

<span data-ttu-id="fc6b2-168">Führen Sie zum Abschließen der Einrichtung eines Lagerorts die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="fc6b2-169">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Kanaleinrichtung \> Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="fc6b2-170">Wählen Sie den Lagerort aus, den Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="fc6b2-171">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="fc6b2-172">Unter **Bestands- und Lagerortverwaltung**:</span><span class="sxs-lookup"><span data-stu-id="fc6b2-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="fc6b2-173">Stellen Sie **Standard-Zugangslagerplatz** auf den oben erstellten Standardstandort.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="fc6b2-174">Wählen Sie **Standard-Abgangslagerplatz** als den oben erstellten Standardstandort.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="fc6b2-175">Geben Sie im Abschnitt **Adressen** eine Lageradresse ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="fc6b2-176">Im Abschnitt **Einzelhandel**:</span><span class="sxs-lookup"><span data-stu-id="fc6b2-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="fc6b2-177">Geben Sie im **Standard-Rückgabeort** den zuvor erstellten Rückgabeort ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="fc6b2-178">Stellen Sie **Geschäft** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="fc6b2-179">Legen Sie **Gewicht** auf **1.00** fest.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="fc6b2-180">Geben Sie im Feld **Lagerdimensionen** den zuvor erstellten Standardlagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="fc6b2-181">Setzen Sie im Abschnitt **Lagerort** die Option **Negativbestand** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="fc6b2-182">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fc6b2-183">Das folgende Bild zeigt Details für einen konfigurierten Lagerort.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-183">The following image shows details for a configured warehouse.</span></span>

![Beispiel für einen konfigurierten Lagerort](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="fc6b2-185">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fc6b2-185">Additional resources</span></span>

[<span data-ttu-id="fc6b2-186">Lagerortverwaltung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="fc6b2-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="fc6b2-187">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="fc6b2-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="fc6b2-188">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="fc6b2-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="fc6b2-189">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="fc6b2-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="fc6b2-190">Einen Onlinekanal einrichten</span><span class="sxs-lookup"><span data-stu-id="fc6b2-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="fc6b2-191">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="fc6b2-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





