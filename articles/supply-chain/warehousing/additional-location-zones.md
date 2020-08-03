---
title: Zusätzliche Lagerplatzzonen
description: Dieses Thema enthält eine Übersicht über die neuen Lagerplatzzonen, die Microsoft Dynamics 365 Supply Chain Management hinzugefügt wurden.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 32114db4cf202870bae5ce307517170d3e618762
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597141"
---
# <a name="additional-location-zones"></a><span data-ttu-id="73eb7-103">Zusätzliche Lagerplatzzonen</span><span class="sxs-lookup"><span data-stu-id="73eb7-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73eb7-104">In Microsoft Dynamics 365 Supply Chain Management sind drei neue Zonenfelder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="73eb7-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="73eb7-105">Die Lagerortverwaltung kann damit zusätzliche Lagerortorganisationen oder -layouts definieren.</span><span class="sxs-lookup"><span data-stu-id="73eb7-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="73eb7-106">Die neuen Zonenfelder können entweder manuell oder mithilfe des **Lagerplatz-Setup-Assistenten** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="73eb7-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="73eb7-107">Sie können in jeder Abfrage oder Filterung verwendet werden, die die Tabelle „Lagerplätze“ verwendet.</span><span class="sxs-lookup"><span data-stu-id="73eb7-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="73eb7-108">Für die Verwendung der Zonenfelder sind keine zusätzlichen Einstellungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="73eb7-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="73eb7-109">Aktivieren der Funktion „Zusätzliche Lagerplatzzone“</span><span class="sxs-lookup"><span data-stu-id="73eb7-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="73eb7-110">Bevor Sie die Funktion *Zusätzliche Lagerplatzzone* verwenden können, muss sie in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="73eb7-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="73eb7-111">Administratoren können mit den Einstellungen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie gegebenenfalls aktivieren.</span><span class="sxs-lookup"><span data-stu-id="73eb7-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="73eb7-112">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="73eb7-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="73eb7-113">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="73eb7-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="73eb7-114">**Funktionsname:** *Zusätzliche Lagerplatzzone*</span><span class="sxs-lookup"><span data-stu-id="73eb7-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="73eb7-115">Verwenden von Lagerplatzzonen</span><span class="sxs-lookup"><span data-stu-id="73eb7-115">Use location zones</span></span>

1. <span data-ttu-id="73eb7-116">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplatz-Setup-Assistent**.</span><span class="sxs-lookup"><span data-stu-id="73eb7-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="73eb7-117">Legen Sie die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="73eb7-117">Set the following values:</span></span>

    - <span data-ttu-id="73eb7-118">Im Feld **Lagerort** wählen Sie _62_ aus.</span><span class="sxs-lookup"><span data-stu-id="73eb7-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="73eb7-119">Im Feld **Zonen-ID** wählen Sie _FLOOR_ aus.</span><span class="sxs-lookup"><span data-stu-id="73eb7-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="73eb7-120">Im Feld **Zusätzliche Zone 1** wählen Sie _PICKZONE1_ aus.</span><span class="sxs-lookup"><span data-stu-id="73eb7-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="73eb7-121">Im Feld **Zusätzliche Zone 2** wählen Sie _WEBSHOP1_ aus.</span><span class="sxs-lookup"><span data-stu-id="73eb7-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="73eb7-122">Im Feld **Lagerplatzprofilkennung** wählen Sie _FLOOR_ aus.</span><span class="sxs-lookup"><span data-stu-id="73eb7-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="73eb7-123">Wählen Sie die Zeile **Stockwert** aus.</span><span class="sxs-lookup"><span data-stu-id="73eb7-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="73eb7-124">Geben Sie im Feld **Von-Nummer** den Wert _1_ ein.</span><span class="sxs-lookup"><span data-stu-id="73eb7-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="73eb7-125">Geben Sie im Feld **An-Nummer** den Wert _3_ ein.</span><span class="sxs-lookup"><span data-stu-id="73eb7-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="73eb7-126">Wählen Sie die Zeile **Gang** aus.</span><span class="sxs-lookup"><span data-stu-id="73eb7-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="73eb7-127">Geben Sie im Feld **Von-Nummer** den Wert _1_ ein.</span><span class="sxs-lookup"><span data-stu-id="73eb7-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="73eb7-128">Geben Sie im Feld **An-Nummer** den Wert _5_ ein.</span><span class="sxs-lookup"><span data-stu-id="73eb7-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="73eb7-129">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="73eb7-129">Select **Create**.</span></span>
8. <span data-ttu-id="73eb7-130">Sie erhalten Nachrichten, dass neue Lagerplätze hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="73eb7-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="73eb7-131">Wählen Sie die Schaltfläche **Nachrichten anzeigen** aus, um die Nachrichten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="73eb7-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="73eb7-132">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerplätze**.</span><span class="sxs-lookup"><span data-stu-id="73eb7-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="73eb7-133">Die neuen Lagerplätze werden in der Liste angezeigt und alle Zonenfelder sind verfügbar (d. h. das vorhandene Zonenfeld und die neuen zusätzlichen Zonenfelder).</span><span class="sxs-lookup"><span data-stu-id="73eb7-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
