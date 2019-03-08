---
title: Clusterkommissionierung einrichten
description: In diesem Thema wird beschrieben, wie die Clusterentnahme eingerichtet und wie Artikelbestätigung mit Clusterentnahme angewendet wird.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7adec850cfb473b0bfc9536dcb1ef1cfd74129a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "364096"
---
[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="bec78-103">Clusterkommissionierung einrichten</span><span class="sxs-lookup"><span data-stu-id="bec78-103">Set up cluster picking</span></span>

<span data-ttu-id="bec78-104">In diesem Thema wird beschrieben, wie Arbeitskräften ermöglicht wird, ihre mobilen Geräte zu verwenden, um Entnahmearbeit in Cluster zu gruppieren, sodass sie Artikel von einem einzelnen Lagerplatz für mehrere Arbeitsaufträge gleichzeitig entnehmen können.</span><span class="sxs-lookup"><span data-stu-id="bec78-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="bec78-105">Dies wird als *Clusterkommissionierung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bec78-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="bec78-106">Zur Clusterkommissionierung</span><span class="sxs-lookup"><span data-stu-id="bec78-106">About cluster picking</span></span>

<span data-ttu-id="bec78-107">Nachdem Arbeitsaufträge für den Lagerort freigegeben sind, kann die Arbeitskraft ein mobiles Gerät verwenden, um die Aufträge einem Cluster zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="bec78-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="bec78-108">Das Cluster organisiert die Entnahmerbeit für die Arbeitskraft.</span><span class="sxs-lookup"><span data-stu-id="bec78-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="bec78-109">Wenn einem Cluster ein Arbeitsauftrag zugewiesen wird, muss die Arbeitskraft Clusterkommissionierung verwenden, um die Entnahmearbeit für den Auftrag auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bec78-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="bec78-110">Die Arbeitskraft kann anderen Entnahmemethoden nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="bec78-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="bec78-111">Wenn einem Cluster ein Arbeitsauftrag versehentlich zugewiesen wird, muss die Arbeitskraft den Cluster unterbrechen und ihn anschließend neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bec78-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="bec78-112">Bei Bedarf kann eine Arbeitskraft einen Cluster an eine andere Arbeitskraft weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="bec78-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="bec78-113">Dieses ändert den Clusterstatus zu Erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bec78-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="bec78-114">Wenn die Arbeitskraft ein mobiles Gerät verwendet, um anzugeben, dass die Entnahme und die Entnahmearbeit abgeschlossen ist, müssen die Lieferung oder die Ladung im Dynamics 365 for Finance and Operations Client bestätigt werden.</span><span class="sxs-lookup"><span data-stu-id="bec78-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="bec78-115">Clusterkommissionierung einrichten</span><span class="sxs-lookup"><span data-stu-id="bec78-115">Set up cluster picking</span></span>

<span data-ttu-id="bec78-116">Um Clusterentnahme zu aktivieren, müssen Sie Folgendes einrichten:</span><span class="sxs-lookup"><span data-stu-id="bec78-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="bec78-117">**Clusterprofile** - Geben Sie an, ob automatisch Cluster Kennungen generiert werden, die Anzahl der zu verwendenden Positionen, wann Cluster abgebrochen werden und wie die Entnahmearbeit sequenziert und geprüft wird.</span><span class="sxs-lookup"><span data-stu-id="bec78-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="bec78-118">**Arbeitsvorlagen** - definieren Sie, wie die Entnahmearbeit für Clusterkommissionierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bec78-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="bec78-119">**Standortweisungen** - Angeben, von wo Artikel entnommen werden und wo sie eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="bec78-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="bec78-120">**Mobile Geräte-Menüartikel** - Konfigurieren einer Menüoption des Mobilgeräts, um vorhandene Arbeit zu verwenden, die durch Clusterkommissionierung geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="bec78-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="bec78-121">Sie müssen die Menüoption einem Menü des mobilen Geräts hinzufügen, damit es auf mobilen Geräten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bec78-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="bec78-122">**Lagerortverwaltungsparameter** - Geben Sie den Nummernkreis an, der verwendet wird, wenn Sie Kennungen für Cluster generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="bec78-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="bec78-123">Einrichten eines Clusterprofils</span><span class="sxs-lookup"><span data-stu-id="bec78-123">Set up a cluster profile</span></span>

<span data-ttu-id="bec78-124">Gehen Sie zum Einrichten eines Clusterprofils folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="bec78-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="bec78-125">Klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Mobiles Gerät** \> **Clusterprofile**.</span><span class="sxs-lookup"><span data-stu-id="bec78-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="bec78-126">Klicken Sie auf **Neu**, um ein neues Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bec78-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="bec78-127">Klicken Sie **Erstellen Sie Cluster**, und unter **Clustersortieren**, klicken Sie **Neu**, um der Sortierkriterien für den Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="bec78-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="bec78-128">Die Sortierkriterien steuern die Reihenfolge, in dem die Arbeitskraft die Entnahmearbeit ausführt.</span><span class="sxs-lookup"><span data-stu-id="bec78-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="bec78-129">Sie können beliebig viele Kriterien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bec78-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="bec78-130">Geben Sie im Feld **Sequenzzahl** die Anzahl ein, um die Reihenfolge zu definieren, in der die Sortierkriterien verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bec78-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="bec78-131">Wählen Sie im Feld **Feldname** das Feld aus, das die Sortierung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bec78-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="bec78-132">Wenn Sie beispielsweise das Feld **WMSLocationId** aktiviert haben, wird die Arbeit nach Lagerplatz sortiert.</span><span class="sxs-lookup"><span data-stu-id="bec78-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="bec78-133">Wählen Sie im Feld **Sortieren** eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="bec78-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="bec78-134">**Option**</span><span class="sxs-lookup"><span data-stu-id="bec78-134">**Option**</span></span>     | <span data-ttu-id="bec78-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bec78-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec78-136">**Aufsteigend**</span><span class="sxs-lookup"><span data-stu-id="bec78-136">**Ascending**</span></span>  | <span data-ttu-id="bec78-137">Die Entnahmearbeit wird in einer aufsteigenden Reihenfolge auf Basis der Sortierkriterien geordnet.</span><span class="sxs-lookup"><span data-stu-id="bec78-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="bec78-138">Wenn Sie beispielsweise das Feld **WMSLocationId** als Sortierkriterium verwenden, und Ihre Lagerplatz Kennungen sind 1, 2, 3, 4, entnehmen Sie von Lagerplatz 4 zuerst.</span><span class="sxs-lookup"><span data-stu-id="bec78-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="bec78-139">**Absteigend**</span><span class="sxs-lookup"><span data-stu-id="bec78-139">**Descending**</span></span> | <span data-ttu-id="bec78-140">Die Entnahmearbeit wird in einer absteigenden Reihenfolge auf Basis der Sortierkriterien geordnet.</span><span class="sxs-lookup"><span data-stu-id="bec78-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="bec78-141">Wenn Sie beispielsweise das Feld **WMSLocationId** als Sortierkriterium verwenden, und Ihre Lagerplatz Kennungen sind 1, 2, 3, 4, entnehmen Sie von Lagerplatz 1 zuerst.</span><span class="sxs-lookup"><span data-stu-id="bec78-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="bec78-142">Artikelbestätigung</span><span class="sxs-lookup"><span data-stu-id="bec78-142">Item confirmation</span></span>

<span data-ttu-id="bec78-143">Wann die Clusterentnahme angewendet wird, ist die Artikelbestätigung wichtig, um die Artikel zu prüfen, die den Clustern hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bec78-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="bec78-144">Sie können Artikel in der Clusterentnahme während des Clusterentnahmevorgangs überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bec78-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="bec78-145">Die Einrichtung basiert auf dem Produktstrichcode-Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="bec78-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="bec78-146">Einrichten der Artikelprüfung mit Clusterentnahme</span><span class="sxs-lookup"><span data-stu-id="bec78-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="bec78-147">Öffnen Sie über ein Menüelement des mobilen Geräts das Einstellungsformular für Arbeitsbestätigung:  **Lagerortverwaltung** \> **Lagerortverwaltung** \> **Einrichtung** \> **Mobiles Gerät** \> **Mobiles Gerätemenü**.</span><span class="sxs-lookup"><span data-stu-id="bec78-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="bec78-148">Öffnen Sie über das Menüelement des mobilen Geräts die Option **Einrichtung Arbeitsbestätigung**.</span><span class="sxs-lookup"><span data-stu-id="bec78-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="bec78-149">Die **Produktbestätigung** ermöglicht Ihnen, beim Scannen jeden Inventurartikel über das mobile Gerät zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="bec78-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
