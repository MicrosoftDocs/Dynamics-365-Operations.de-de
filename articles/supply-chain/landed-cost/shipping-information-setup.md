---
title: Einstellungen für Versandinformationen
description: Dieses Thema beschreibt, wie Sie Versandinformationen für das Modul Gesamttransportkosten festlegen.
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 90794a154eb2a63f33277383cda80323dafd77b0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500933"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="31d39-103">Einstellungen für Versandinformationen</span><span class="sxs-lookup"><span data-stu-id="31d39-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="31d39-104">In diesem Thema wird beschrieben, wie Sie Versandinformationen für das Modul **Gesamttransportkosten** festlegen.</span><span class="sxs-lookup"><span data-stu-id="31d39-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="31d39-105">Warenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-105">Description of goods</span></span>

<span data-ttu-id="31d39-106">Warenbeschreibungen helfen, eine Fahrt, einen Transportcontainer oder eine Palette von Waren und die darin enthaltenen Waren zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="31d39-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="31d39-107">Sie können eine Warenbeschreibung in der Kopfzeile des Transportcontainers oder in der Kopfzeile des Paletten auswählen.</span><span class="sxs-lookup"><span data-stu-id="31d39-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="31d39-108">Um mit Warenbeschreibungen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Versandinformationen einrichten \> Beschreibung der Waren**.</span><span class="sxs-lookup"><span data-stu-id="31d39-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="31d39-109">Dort können Sie Datensätze für Beschreibungen von Waren anzeigen, öffnen, erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="31d39-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="31d39-110">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="31d39-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="31d39-111">Feld</span><span class="sxs-lookup"><span data-stu-id="31d39-111">Field</span></span> | <span data-ttu-id="31d39-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-112">Description</span></span> |
|---|---|
| <span data-ttu-id="31d39-113">Warenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-113">Description of goods</span></span> | <span data-ttu-id="31d39-114">Geben Sie einen eindeutigen Identifikationsnamen/eine eindeutige Identifikationsnummer für die Art der Waren ein, für die diese Beschreibung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="31d39-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="31d39-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-115">Description</span></span> | <span data-ttu-id="31d39-116">Geben Sie eine Beschreibung der Art der Waren in dieser Kategorie ein.</span><span class="sxs-lookup"><span data-stu-id="31d39-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="31d39-117">Schiffe</span><span class="sxs-lookup"><span data-stu-id="31d39-117">Vessels</span></span>

<span data-ttu-id="31d39-118">Ein Schiff ist der eindeutige Name eines Schiffs oder Schiffs, den eine Firma oder Agentur verwendet.</span><span class="sxs-lookup"><span data-stu-id="31d39-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="31d39-119">Wenn Sie eine Fahrt erstellen, müssen Sie immer ein Schiff dafür entweder auswählen oder eingeben.</span><span class="sxs-lookup"><span data-stu-id="31d39-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="31d39-120">Wenn Sie häufig dieselben Schiffe verwenden, können Sie das Erstellen einer neuen Fahrt beschleunigen und vereinfachen, indem Sie für jedes dieser Schiffe einen Schiffsdatensatz erstellen, so dass die Benutzer das Schiff aus einer Liste auswählen können und nicht jedes Mal den Namen oder die Nummer manuell eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="31d39-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="31d39-121">Um mit Schiffen zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Versandinformationen einrichten \> Schiffe**.</span><span class="sxs-lookup"><span data-stu-id="31d39-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="31d39-122">Dort können Sie Datensätze für Schiffe anzeigen, öffnen, erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="31d39-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="31d39-123">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="31d39-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="31d39-124">Feld</span><span class="sxs-lookup"><span data-stu-id="31d39-124">Field</span></span> | <span data-ttu-id="31d39-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-125">Description</span></span> |
|---|---|
| <span data-ttu-id="31d39-126">Schiff</span><span class="sxs-lookup"><span data-stu-id="31d39-126">Vessel</span></span> | <span data-ttu-id="31d39-127">Geben Sie einen eindeutigen Identifikationsnamen/eine eindeutige Identifikationsnummer für das Schiff ein, das zum Transport von Waren auf einer Fahrt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31d39-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="31d39-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-128">Description</span></span> | <span data-ttu-id="31d39-129">Geben Sie eine Beschreibung für das Schiff ein.</span><span class="sxs-lookup"><span data-stu-id="31d39-129">Enter a description of the vessel.</span></span> <span data-ttu-id="31d39-130">Typischerweise identifiziert diese Beschreibung den Namen des Schiffes und der Reederei/des Agenten.</span><span class="sxs-lookup"><span data-stu-id="31d39-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="31d39-131">Lieferart</span><span class="sxs-lookup"><span data-stu-id="31d39-131">Mode of delivery</span></span> | <span data-ttu-id="31d39-132">Wählen Sie die Lieferart, die das Schiff verwendet (z. B. _Luft_, _Meer_ oder _Schiene_).</span><span class="sxs-lookup"><span data-stu-id="31d39-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="31d39-133">Exporteure</span><span class="sxs-lookup"><span data-stu-id="31d39-133">Exporters</span></span>

<span data-ttu-id="31d39-134">Jeder Ausführer-Datensatz identifiziert einen Lieferanten oder Ausführer, der als Lieferant für eine Fahrt definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="31d39-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="31d39-135">Der Exporteur kann mit einer Fahrt verknüpft und für Berichte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31d39-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="31d39-136">Um mit Exporteuren zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Versandinformationen einrichten \> Exporteure**.</span><span class="sxs-lookup"><span data-stu-id="31d39-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="31d39-137">Dort können Sie Datensätze für Exporteure anzeigen, öffnen, erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="31d39-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="31d39-138">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="31d39-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="31d39-139">Feld</span><span class="sxs-lookup"><span data-stu-id="31d39-139">Field</span></span> | <span data-ttu-id="31d39-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-140">Description</span></span> |
|---|---|
| <span data-ttu-id="31d39-141">Exporteur</span><span class="sxs-lookup"><span data-stu-id="31d39-141">Exporter</span></span> | <span data-ttu-id="31d39-142">Geben Sie einen eindeutigen Identifikationsnamen/Nummer für den Ausführer von Waren ein, die auf einer Fahrt transportiert werden.</span><span class="sxs-lookup"><span data-stu-id="31d39-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="31d39-143">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-143">Description</span></span> | <span data-ttu-id="31d39-144">Geben Sie eine Beschreibung des Ausführers ein.</span><span class="sxs-lookup"><span data-stu-id="31d39-144">Enter a description of the exporter.</span></span> <span data-ttu-id="31d39-145">Normalerweise identifiziert diese Beschreibung den vollständigen Namen der Firma/des Agenten der Reederei.</span><span class="sxs-lookup"><span data-stu-id="31d39-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="31d39-146">Warencodes</span><span class="sxs-lookup"><span data-stu-id="31d39-146">Commodity codes</span></span>

<span data-ttu-id="31d39-147">Sie verwenden Warencodes, um die Identifizierung der Zölle und die Berechnung der Sätze für Waren auf einer Fahrt zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="31d39-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="31d39-148">Sie können Warencodes auf der Seite **Freigegebene Produkte** auswählen.</span><span class="sxs-lookup"><span data-stu-id="31d39-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="31d39-149">Um mit Warencodes zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Versandinformationen einrichten \> Warencodes**.</span><span class="sxs-lookup"><span data-stu-id="31d39-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="31d39-150">Dort können Sie Datensätze für Warencodes anzeigen, öffnen, erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="31d39-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="31d39-151">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="31d39-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="31d39-152">Feld</span><span class="sxs-lookup"><span data-stu-id="31d39-152">Field</span></span> | <span data-ttu-id="31d39-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-153">Description</span></span> |
|---|---|
| <span data-ttu-id="31d39-154">Warencode</span><span class="sxs-lookup"><span data-stu-id="31d39-154">Commodity code</span></span> | <span data-ttu-id="31d39-155">Geben Sie einen eindeutigen Code für diese Art von Ware ein.</span><span class="sxs-lookup"><span data-stu-id="31d39-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="31d39-156">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-156">Description</span></span> | <span data-ttu-id="31d39-157">Geben Sie eine Beschreibung für die Warenart ein.</span><span class="sxs-lookup"><span data-stu-id="31d39-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="31d39-158">Zollbeschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-158">Customs description</span></span>

<span data-ttu-id="31d39-159">Zollbeschreibungen helfen, Waren für Zollzwecke zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="31d39-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="31d39-160">Sie können eine Zoll-Beschreibung auf der Seite **Freigegebene Produkte** oder auf Zeilen der Einkaufsbestellung auswählen.</span><span class="sxs-lookup"><span data-stu-id="31d39-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="31d39-161">Um mit Zollbeschreibungen zu arbeiten, gehen Sie auf die Seite **Gesamttransportkosten \> Versandinformationen einrichten \> Zollbeschreibung**.</span><span class="sxs-lookup"><span data-stu-id="31d39-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="31d39-162">Dort können Sie Datensätze für benutzerdefinierte Beschreibungen anzeigen, öffnen, erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="31d39-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="31d39-163">Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="31d39-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="31d39-164">Feld</span><span class="sxs-lookup"><span data-stu-id="31d39-164">Field</span></span> | <span data-ttu-id="31d39-165">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-165">Description</span></span> |
|---|---|
| <span data-ttu-id="31d39-166">Zollbeschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-166">Customs description</span></span> | <span data-ttu-id="31d39-167">Geben Sie einen eindeutigen Code für diese Art der Zollklassifizierung ein.</span><span class="sxs-lookup"><span data-stu-id="31d39-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="31d39-168">Oft wird dieser Code die offizielle Beschreibung sein, die von einer Zollbehörde für die Beschreibung und den qualitativen Wert der Waren bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="31d39-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="31d39-169">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d39-169">Description</span></span> | <span data-ttu-id="31d39-170">Geben Sie eine Beschreibung der Zollklassifizierung ein.</span><span class="sxs-lookup"><span data-stu-id="31d39-170">Enter a description of the customs classification.</span></span> |
