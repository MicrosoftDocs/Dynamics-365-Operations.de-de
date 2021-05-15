---
title: National Motor Freight Classification (NMFC)-Codes
description: Dieses Thema beschreibt, wie Sie mit National Motor Freight Classification (NMFC)-Codes in Microsoft Dynamics 365 Supply Chain Management arbeiten.
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941881"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="11454-103">National Motor Freight Classification (NMFC)-Codes</span><span class="sxs-lookup"><span data-stu-id="11454-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11454-104">National Motor Freight Classification (NMFC)-Codes helfen Ihnen, Elemente zu klassifizieren, die versendet werden können.</span><span class="sxs-lookup"><span data-stu-id="11454-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="11454-105">Der NMFC-Code ist eine Bezeichnung, die zur Gruppierung von Waren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11454-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="11454-106">Es ermöglicht Transportfirmen, Waren für den Versand zu bewerten, indem sie Elemente auf der Basis von Überlegungen wie LKW-Passform, Ladungsproblemen, Handhabungsproblemen und Verderblichkeit klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="11454-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="11454-107">Waren werden in eine von 18 Frachtklassen gruppiert, indem ein Zahlenbereich von 50 bis 500 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11454-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="11454-108">Die Klasse, in die eine Ware eingeteilt wird, basiert auf einer Bewertung von vier Transportmerkmalen: Dichte, Verstaubarkeit, Handhabung und Haftung.</span><span class="sxs-lookup"><span data-stu-id="11454-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="11454-109">Zusammen bestimmen diese Merkmale die Transportfähigkeit der Ware.</span><span class="sxs-lookup"><span data-stu-id="11454-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="11454-110">Ein NMFC-Code ist mit jedem Versandelement für weniger als Teilladungen (LTL) verbunden.</span><span class="sxs-lookup"><span data-stu-id="11454-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="11454-111">Zum Beispiel könnte einem Laptop ein NMFC zugewiesen werden, der mit 2,5 eingestuft ist, während elektrischen Kabeln ein NMFC zugewiesen werden könnte, der mit 65 eingestuft ist.</span><span class="sxs-lookup"><span data-stu-id="11454-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="11454-112">Diese Funktion kann Arbeitskräften helfen, NMFC-Codes zur Klassifizierung von LTL-Versandartikeln zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="11454-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="11454-113">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="11454-113">Here are some examples:</span></span>

- <span data-ttu-id="11454-114">Wenn Ihre Firma eine Frachtbeschreibung auf dem Frachtbrief (BOL) angibt, hat der Spediteur eine Vorstellung davon, worum es sich bei der Fracht handelt.</span><span class="sxs-lookup"><span data-stu-id="11454-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="11454-115">Fracht ist eine wichtige Klassifizierung, da viele Firmen ihr gesamtes Geschäftsmodell auf die Arten von Fracht stützen, die sie versenden.</span><span class="sxs-lookup"><span data-stu-id="11454-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="11454-116">Diese Klassifizierung kann für Ihre Firma wichtig sein, da sie zur Bestimmung der Kalkulation einer bestimmten Ladung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11454-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="11454-117">Ihre Firma kann die Rentabilität eines LTL-Logistik- und Transportunternehmens ermitteln.</span><span class="sxs-lookup"><span data-stu-id="11454-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="11454-118">Dieses Thema beschreibt, wie Sie in Microsoft Dynamics 365 Supply Chain Management mit NMFC-Codes arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="11454-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="11454-119">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="11454-119">Prerequisites</span></span>

<span data-ttu-id="11454-120">Bevor Sie NMFC-Codes erstellen können, müssen Sie alle LTL-Frachtklassen festlegen, die diesen zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="11454-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="11454-121">LTL-Frachtklassen stellen Kategorien von Artikeln dar, während NMFC-Codes sich auf bestimmte Waren in jeder der 18 Frachtklassen beziehen.</span><span class="sxs-lookup"><span data-stu-id="11454-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="11454-122">Weitere Informationen zum Arbeiten mit LTL-Klassen finden Sie unter [Klassen für weniger als Teilladungen (LTL)](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="11454-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="11454-123">Erstellen eines NMFC-Codes</span><span class="sxs-lookup"><span data-stu-id="11454-123">Create an NMFC code</span></span>

<span data-ttu-id="11454-124">Führen Sie diese Schritte aus, um einen NMFC-Code zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="11454-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="11454-125">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="11454-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="11454-126">Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> NMFC-Codes**.</span><span class="sxs-lookup"><span data-stu-id="11454-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="11454-127">Gehen Sie zu **Transportverwaltung \> Einrichten \> Transportstandards \> NMFC-Codes**.</span><span class="sxs-lookup"><span data-stu-id="11454-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="11454-128">Wählen Sie **Neu**, um einen NMFC-Code zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="11454-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="11454-129">Legen Sie anschließend die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="11454-129">Then set the following fields:</span></span>

    - <span data-ttu-id="11454-130">**NMFC-Code** – Geben Sie den NMFC-Code für die Warenart ein.</span><span class="sxs-lookup"><span data-stu-id="11454-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="11454-131">**Name** – Geben Sie einen Namen für den NMFC-Code ein.</span><span class="sxs-lookup"><span data-stu-id="11454-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="11454-132">**LTL-Klasse** – Wählen Sie die LTL-Klasse, die mit dem NMFC-Code verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="11454-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="11454-133">**BOL-Handling-Einheit** – Definieren Sie die Standard-Handling-Art für die Sendung.</span><span class="sxs-lookup"><span data-stu-id="11454-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="11454-134">Beispiel: NMFC-Codes festlegen</span><span class="sxs-lookup"><span data-stu-id="11454-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="11454-135">Das folgende Beispiel zeigt, wie Sie zwei verschiedene NMFC-Codes festlegen, die Sie mit verschiedenen Produkten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="11454-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="11454-136">Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> NMFC-Codes**.</span><span class="sxs-lookup"><span data-stu-id="11454-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="11454-137">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="11454-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="11454-138">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="11454-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="11454-139">**NMFC-Code:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="11454-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="11454-140">**Name:** *Computer*</span><span class="sxs-lookup"><span data-stu-id="11454-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="11454-141">**LTL-Klasse:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="11454-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="11454-142">**BOL-Handling-Einheit:** *Einheit*</span><span class="sxs-lookup"><span data-stu-id="11454-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="11454-143">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="11454-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="11454-144">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="11454-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="11454-145">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="11454-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="11454-146">**NMFC-Code:** *125*</span><span class="sxs-lookup"><span data-stu-id="11454-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="11454-147">**Name:** *Telefone*</span><span class="sxs-lookup"><span data-stu-id="11454-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="11454-148">**LTL-Klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="11454-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="11454-149">**BOL-Handling-Einheit:** *Einheit*</span><span class="sxs-lookup"><span data-stu-id="11454-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="11454-150">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="11454-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11454-151">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="11454-151">Additional resources</span></span>

- [<span data-ttu-id="11454-152">Klassen für weniger als Teilladung (LTL)</span><span class="sxs-lookup"><span data-stu-id="11454-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="11454-153">Erstellen Sie einen Frachtbrief</span><span class="sxs-lookup"><span data-stu-id="11454-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
