---
title: Klassen für Teilladungen (LTL)
description: Dieses Thema erklärt, was Less than Teilladung (LTL) Klassen sind und beschreibt, wie Sie diese in Microsoft Dynamics 365 Supply Chain Management festlegen.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941809"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="40f08-103">Klassen für Teilladungen (LTL)</span><span class="sxs-lookup"><span data-stu-id="40f08-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40f08-104">Eine Klasse für Teilladungen (LTL) ist eine Frachtversandklasse, die zur Klassifizierung von Elementen verwendet wird, die versendet werden können.</span><span class="sxs-lookup"><span data-stu-id="40f08-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="40f08-105">Allgemein hat jede Art von Produkt oder Ware einen National Motor Freight Classification (NMFC) Code, der einer bestimmten Frachtklassennummer für LTL-Sendungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="40f08-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="40f08-106">LTL-Frachtklassen stellen Kategorien von Artikeln dar, während NMFC-Codes sich auf bestimmte Waren in jeder der 18 Frachtklassen beziehen.</span><span class="sxs-lookup"><span data-stu-id="40f08-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="40f08-107">Mit dieser Funktion können Sie mit Ihrem System die folgenden Aufgaben durchführen:</span><span class="sxs-lookup"><span data-stu-id="40f08-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="40f08-108">Definieren Sie die LTL-Frachtklassen, die in Ihrer Firma verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40f08-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="40f08-109">Weisen Sie jede LTL-Klasse einem NMFC-Code auf der Seite **NMFC-Codes** zu.</span><span class="sxs-lookup"><span data-stu-id="40f08-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="40f08-110">Weitere Informationen finden Sie unter [National Motor Freight Classification (NMFC)-Codes](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="40f08-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="40f08-111">Weisen Sie jedem Produkt auf der Seite **Produkte** einen NMFC-Code (und damit den zugehörigen LTL-Code) zu.</span><span class="sxs-lookup"><span data-stu-id="40f08-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="40f08-112">Schätzen Sie die LTL-Klasse jedes Produkts, dem ein NMFC-Code zugewiesen ist, genau ein.</span><span class="sxs-lookup"><span data-stu-id="40f08-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="40f08-113">Ermittelt die Verpackungsanforderungen für jede LTL-Klasse durch Überprüfung der internationalen LTL-Standards.</span><span class="sxs-lookup"><span data-stu-id="40f08-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="40f08-114">Auf diese Weise stellen Sie sicher, dass Ihre Produkte gut geschützt und sicher versandt werden.</span><span class="sxs-lookup"><span data-stu-id="40f08-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="40f08-115">Erhalten Sie genaue Versandschätzungen, basierend auf der LTL-Frachtklasse für jedes Produkt.</span><span class="sxs-lookup"><span data-stu-id="40f08-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="40f08-116">Dieses Thema beschreibt, wie Sie LTL-Klassen in Microsoft Dynamics 365 Supply Chain Management erstellen.</span><span class="sxs-lookup"><span data-stu-id="40f08-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="40f08-117">Erstellen einer LTL-Klasse</span><span class="sxs-lookup"><span data-stu-id="40f08-117">Create an LTL class</span></span>

<span data-ttu-id="40f08-118">Um eine LTL-Klasse zu erstellen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="40f08-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="40f08-119">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="40f08-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="40f08-120">Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> LTL-Klassen**.</span><span class="sxs-lookup"><span data-stu-id="40f08-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="40f08-121">Gehen Sie zu **Transportverwaltung \> Einrichten \> Transportstandards \> LTL-Klassen**.</span><span class="sxs-lookup"><span data-stu-id="40f08-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="40f08-122">Wählen Sie im Aktivitätsbereich **Neu**, um eine LTL-Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="40f08-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="40f08-123">Legen Sie anschließend die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="40f08-123">Then set the following fields:</span></span>

    - <span data-ttu-id="40f08-124">**LTL-Klasse** – Geben Sie die interne LTL-Klassen-Kennung (ID) Ihrer Firma für die Warenart ein.</span><span class="sxs-lookup"><span data-stu-id="40f08-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="40f08-125">Die meisten Firmen verwenden den internationalen Standard.</span><span class="sxs-lookup"><span data-stu-id="40f08-125">Most companies use the international standard.</span></span> <span data-ttu-id="40f08-126">In diesem Fall stimmt der Wert dieses Feldes mit dem Wert des Feldes **Klasse** überein.</span><span class="sxs-lookup"><span data-stu-id="40f08-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="40f08-127">Wenn Ihre Firma jedoch einen eigenen Standard verwendet, geben Sie einen Code ein, der mit diesem Standard übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="40f08-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="40f08-128">**Name** – Geben Sie einen beschreibenden Namen ein, der Ihnen und anderen Benutzern hilft, die richtige LTL-Klasse für jeden NMFC-Code auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="40f08-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="40f08-129">**Klasse:** – Geben Sie die internationale Standard-LTL-Klassen-ID für die Warenart ein.</span><span class="sxs-lookup"><span data-stu-id="40f08-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="40f08-130">Der Code, den Sie hier eingeben, muss mit dem offiziellen Standard übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="40f08-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="40f08-131">Beispiel: LTL-Klassen festlegen</span><span class="sxs-lookup"><span data-stu-id="40f08-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="40f08-132">Das folgende Beispiel zeigt, wie Sie zwei verschiedene LTL-Klassen festlegen, die Sie mit unterschiedlichen Produkttypen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="40f08-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="40f08-133">Gehen Sie zu **Lagerortverwaltung \> Einrichten \> Bestand \> LTL-Klassen**.</span><span class="sxs-lookup"><span data-stu-id="40f08-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="40f08-134">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="40f08-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="40f08-135">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="40f08-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="40f08-136">**LTL-Klasse:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="40f08-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="40f08-137">**Name:** *Computer, Monitore, Kühlgeräte*</span><span class="sxs-lookup"><span data-stu-id="40f08-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="40f08-138">**Klasse:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="40f08-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="40f08-139">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="40f08-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="40f08-140">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="40f08-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="40f08-141">Legen Sie die folgenden Werte für die neue Position fest:</span><span class="sxs-lookup"><span data-stu-id="40f08-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="40f08-142">**LTL-Klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="40f08-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="40f08-143">**Name:** *Kleine Haushaltsgeräte*</span><span class="sxs-lookup"><span data-stu-id="40f08-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="40f08-144">**Klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="40f08-144">**Class:** *125*</span></span>

1. <span data-ttu-id="40f08-145">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="40f08-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40f08-146">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="40f08-146">Additional resources</span></span>

- [<span data-ttu-id="40f08-147">National Motor Freight Classification (NMFC)-Codes</span><span class="sxs-lookup"><span data-stu-id="40f08-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="40f08-148">Frachtbrief erstellen</span><span class="sxs-lookup"><span data-stu-id="40f08-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
