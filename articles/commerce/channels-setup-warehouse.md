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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 772c7584549b30a34e371a7911131edc01214ed8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477633"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="53e27-103">Lagerort einrichten</span><span class="sxs-lookup"><span data-stu-id="53e27-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53e27-104">In diesem Thema wird beschrieben, wie Sie einen Lagerort für die Verwendung mit einem neuen Kanal in Microsoft Dynamics 365 Commerce einrichten.</span><span class="sxs-lookup"><span data-stu-id="53e27-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="53e27-105">Jedem Commerce-Kanal muss ein konfigurierter Lagerort zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="53e27-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="53e27-106">Die folgenden Verfahren bieten die Mindestkonfiguration, die zum Einrichten eines Lagerorts für einen Commerce-Kanal erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="53e27-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="53e27-107">Weitere Informationen zur Einrichtung des Lagerorts finden Sie in der [Übersicht über die Lagerortverwaltung](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="53e27-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="53e27-108">Standort eines Lagerorts konfigurieren</span><span class="sxs-lookup"><span data-stu-id="53e27-108">Configure a warehouse site</span></span>

<span data-ttu-id="53e27-109">Vor dem Einrichten eines Lagerorts müssen Sie den Standort eines Lagerorts konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="53e27-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="53e27-110">Gehen Sie folgendermaßen vor, um den Standort eines Lagerorts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="53e27-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="53e27-111">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Standorte**.</span><span class="sxs-lookup"><span data-stu-id="53e27-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="53e27-112">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="53e27-113">Geben Sie im Feld **Standort** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="53e27-114">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="53e27-115">Legen Sie im Abschnitt **Allgemeines** die entsprechende **Zeitzone** fest.</span><span class="sxs-lookup"><span data-stu-id="53e27-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="53e27-116">Geben Sie im Abschnitt **Adressen** eine Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="53e27-117">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="53e27-118">Das folgende Bild zeigt ein Beispiel für den Standort eines Lagerorts.</span><span class="sxs-lookup"><span data-stu-id="53e27-118">The following image shows an example warehouse site.</span></span>

![Beispiel: Standort eines Lagerorts](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="53e27-120">Einen Lagerort einrichten</span><span class="sxs-lookup"><span data-stu-id="53e27-120">Set up a warehouse</span></span>

<span data-ttu-id="53e27-121">Um einen Lagerort einzurichten, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="53e27-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="53e27-122">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="53e27-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="53e27-123">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="53e27-124">Geben Sie im Feld **Lagerort** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="53e27-125">Wenn es sich um eine 1:1-Zuordnung zu einem Geschäft handelt, sollten Sie den Namen des Geschäfts oder den Namen eines regionalen Vertriebszentrums verwenden.</span><span class="sxs-lookup"><span data-stu-id="53e27-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="53e27-126">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="53e27-127">In der Dropdown-Liste **Standort** wählen Sie den zuvor erstellten Standort des Lagerorts aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="53e27-128">Wählen Sie im Feld **Typ** die Option **Standard**.</span><span class="sxs-lookup"><span data-stu-id="53e27-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="53e27-129">Wenn Sie ein **Quarantänelager** einrichten möchten, führen Sie zunächst die folgenden Schritte aus, um einen zusätzlichen Lagerort zu erstellen, in dem der **Typ** auf **Quarantäne** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="53e27-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="53e27-130">Wenn Sie ein **Transitlager** einrichten möchten, führen Sie zunächst die folgenden Schritte aus, um einen zusätzlichen Lagerort zu erstellen, in dem der **Typ** auf **Transit** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="53e27-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="53e27-131">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="53e27-132">Lagergänge einrichten</span><span class="sxs-lookup"><span data-stu-id="53e27-132">Set up inventory aisles</span></span>

<span data-ttu-id="53e27-133">Gehen Sie zum Einrichten von Lagergängen folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="53e27-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="53e27-134">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Standorteinrichtung \> Lagergänge**.</span><span class="sxs-lookup"><span data-stu-id="53e27-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="53e27-135">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="53e27-136">In der Dropdown-Liste **Lagerort** wählen Sie den zuvor erstellten Lagerort aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="53e27-137">Geben Sie im Feld **Gang** einen Namen ein (beispielsweise „Def”).</span><span class="sxs-lookup"><span data-stu-id="53e27-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="53e27-138">Geben Sie im Feld **Name** einen Namen ein (beispielsweise „Standardgang”).</span><span class="sxs-lookup"><span data-stu-id="53e27-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="53e27-139">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="53e27-140">Standorte für Lagerort-Lagerplätze einrichten</span><span class="sxs-lookup"><span data-stu-id="53e27-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="53e27-141">Führen Sie die folgenden Schritte aus, um Lagerorte für Standard-, beschädigte und zurückgegebene Bestände einzurichten.</span><span class="sxs-lookup"><span data-stu-id="53e27-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="53e27-142">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="53e27-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="53e27-143">Wählen Sie den Lagerort aus, den Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="53e27-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="53e27-144">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="53e27-145">Wählen Sie im Aktionsbereich **Lagerort** und dann **Standort des Lagerorts** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="53e27-146">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-146">On the action pane, select **New**.</span></span> <span data-ttu-id="53e27-147">Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="53e27-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="53e27-148">Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="53e27-149">Stellen Sie **Manuelles Update** auf **Ja**</span><span class="sxs-lookup"><span data-stu-id="53e27-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="53e27-150">Geben Sie im Feld **Standort** den Namen des Lagerorts ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="53e27-151">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="53e27-152">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="53e27-153">Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="53e27-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="53e27-154">Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="53e27-155">Stellen Sie **Manuelles Update** auf **Ja**</span><span class="sxs-lookup"><span data-stu-id="53e27-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="53e27-156">Geben Sie im Feld **Lagerort** „Beschädigt“ ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="53e27-157">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="53e27-158">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="53e27-159">Die Dropdown-Liste **Lagerort** sollte standardmäßig in Ihrem neuen Lagerort angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="53e27-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="53e27-160">Im Feld **Gang** geben Sie den Namen des zuvor angegebenen Gangs ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="53e27-161">Stellen Sie **Manuelles Update** auf **Ja**</span><span class="sxs-lookup"><span data-stu-id="53e27-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="53e27-162">Geben Sie im Feld **Lagerort** „Retouren“ ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="53e27-163">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="53e27-164">Die folgende Abbildung zeigt eine Einrichtung eines Lagerort-Standorts in San Francisco.</span><span class="sxs-lookup"><span data-stu-id="53e27-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Beispiel für die Einrichtung des Standorts eines Lagerorts](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="53e27-166">Vollständige Einrichtung eines Lagerorts</span><span class="sxs-lookup"><span data-stu-id="53e27-166">Complete warehouse setup</span></span>

<span data-ttu-id="53e27-167">Führen Sie zum Abschließen der Einrichtung eines Lagerorts die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="53e27-168">Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="53e27-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="53e27-169">Wählen Sie den Lagerort aus, den Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="53e27-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="53e27-170">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="53e27-171">Unter **Bestands- und Lagerortverwaltung**:</span><span class="sxs-lookup"><span data-stu-id="53e27-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="53e27-172">Stellen Sie **Standard-Zugangslagerplatz** auf den oben erstellten Standardstandort.</span><span class="sxs-lookup"><span data-stu-id="53e27-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="53e27-173">Wählen Sie **Standard-Abgangslagerplatz** als den oben erstellten Standardstandort.</span><span class="sxs-lookup"><span data-stu-id="53e27-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="53e27-174">Geben Sie im Abschnitt **Adressen** eine Lageradresse ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="53e27-175">Im Abschnitt **Einzelhandel**:</span><span class="sxs-lookup"><span data-stu-id="53e27-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="53e27-176">Geben Sie im **Standard-Rückgabeort** den zuvor erstellten Rückgabeort ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="53e27-177">Stellen Sie **Geschäft** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="53e27-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="53e27-178">Legen Sie **Gewicht** auf **1.00** fest.</span><span class="sxs-lookup"><span data-stu-id="53e27-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="53e27-179">Geben Sie im Feld **Lagerdimensionen** den zuvor erstellten Standardlagerplatz ein.</span><span class="sxs-lookup"><span data-stu-id="53e27-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="53e27-180">Setzen Sie im Abschnitt **Lagerort** die Option **Negativbestand** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="53e27-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="53e27-181">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="53e27-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="53e27-182">Das folgende Bild zeigt Details für einen konfigurierten Lagerort.</span><span class="sxs-lookup"><span data-stu-id="53e27-182">The following image shows details for a configured warehouse.</span></span>

![Beispiel für einen konfigurierten Lagerort](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="53e27-184">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="53e27-184">Additional resources</span></span>

[<span data-ttu-id="53e27-185">Lagerortverwaltung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="53e27-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="53e27-186">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="53e27-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="53e27-187">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="53e27-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="53e27-188">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="53e27-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="53e27-189">Einen Onlinekanal einrichten</span><span class="sxs-lookup"><span data-stu-id="53e27-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="53e27-190">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="53e27-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
