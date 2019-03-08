---
title: Maßeinheit verwalten
description: Im folgenden Verfahren wird dargestellt, wie eine Maßeinheit definiert wird, Übersetzungen und eine Beschreibung für die Einheit bereitgestellt werden und Umrechnungsregeln für zugehörige Einheiten definiert werden.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e208b7f1faab77f2b97ff7b440a228656684fca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "358921"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="b73f6-103">Maßeinheit verwalten</span><span class="sxs-lookup"><span data-stu-id="b73f6-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b73f6-104">Im folgenden Verfahren wird dargestellt, wie eine Maßeinheit definiert wird, Übersetzungen und eine Beschreibung für die Einheit bereitgestellt werden und Umrechnungsregeln für zugehörige Einheiten definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b73f6-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="b73f6-105">Sie können diese Prozedur Schritt für Schritt mit den Demodaten durchführen oder Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="b73f6-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="b73f6-106">Wechseln Sie zu "Freigegebene Produktverwaltung".</span><span class="sxs-lookup"><span data-stu-id="b73f6-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="b73f6-107">Klicken Sie auf "Einheiten".</span><span class="sxs-lookup"><span data-stu-id="b73f6-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="b73f6-108">Erstellen Sie eine Maßeinheit.</span><span class="sxs-lookup"><span data-stu-id="b73f6-108">Create a unit of measure</span></span>
1. <span data-ttu-id="b73f6-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b73f6-109">Click New.</span></span>
2. <span data-ttu-id="b73f6-110">Geben Sie im Feld "Einheiten" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b73f6-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="b73f6-111">Geben Sie die Kennung oder das Symbol ein, das für Verweise auf die Maßeinheit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b73f6-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="b73f6-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b73f6-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b73f6-113">Geben Sie einen beschreibenden Namen für die Maßeinheit in der Systemsprache ein.</span><span class="sxs-lookup"><span data-stu-id="b73f6-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="b73f6-114">Wählen Sie im Feld "Einheitenklasse" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="b73f6-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="b73f6-115">Die Einheitenklasse legt die logische Gruppierung der Maßeinheiten fest, wie Bereich, Masse oder Menge.</span><span class="sxs-lookup"><span data-stu-id="b73f6-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="b73f6-116">Geben Sie im Feld "Dezimalstellen" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b73f6-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="b73f6-117">Legen Sie die Anzahl von Dezimalstellen fest, auf die die umgerechnete Maßeinheit gerundet wird, wenn eine Berechnung für die Maßeinheit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b73f6-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="b73f6-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b73f6-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="b73f6-119">Einheitenübersetzungen definieren</span><span class="sxs-lookup"><span data-stu-id="b73f6-119">Define unit translations</span></span>
1. <span data-ttu-id="b73f6-120">Klicken Sie auf "Einheitentexte".</span><span class="sxs-lookup"><span data-stu-id="b73f6-120">Click Unit texts.</span></span>
2. <span data-ttu-id="b73f6-121">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b73f6-121">Click New.</span></span>
    * <span data-ttu-id="b73f6-122">Verwenden Sie Einheitentext, um eine Übersetzung der Kennung oder eines Symbols zu erstellen, das die Maßeinheit zur Verwendung in externen Dokumenten in debitor- oder kreditorspezifischer Sprache wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="b73f6-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="b73f6-123">Geben Sie im Feld "Sprache" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b73f6-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="b73f6-124">Geben Sie im Feld "Text" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b73f6-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="b73f6-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b73f6-125">Click Save.</span></span>
6. <span data-ttu-id="b73f6-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b73f6-126">Close the page.</span></span>
7. <span data-ttu-id="b73f6-127">Klicken Sie auf "Übersetzte Einheitenbeschreibungen".</span><span class="sxs-lookup"><span data-stu-id="b73f6-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="b73f6-128">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b73f6-128">Click New.</span></span>
    * <span data-ttu-id="b73f6-129">Definiert sprachspezifische Beschreibungen für die Maßeinheit.</span><span class="sxs-lookup"><span data-stu-id="b73f6-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="b73f6-130">Geben Sie im Feld "Sprache" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b73f6-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="b73f6-131">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b73f6-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="b73f6-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b73f6-132">Click Save.</span></span>
12. <span data-ttu-id="b73f6-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b73f6-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="b73f6-134">Definieren Sie Einheitenumrechnungsregeln</span><span class="sxs-lookup"><span data-stu-id="b73f6-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="b73f6-135">Klicken Sie auf "Einheitenumrechnungen".</span><span class="sxs-lookup"><span data-stu-id="b73f6-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="b73f6-136">Definieren von Regeln zum Konvertieren der Maßeinheit nach und aus anderen Maßeinheiten in der ausgewählten Einheitenklasse.</span><span class="sxs-lookup"><span data-stu-id="b73f6-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="b73f6-137">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b73f6-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="b73f6-138">Geben Sie im Feld "Faktor" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b73f6-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="b73f6-139">Der Umrechnungsfaktor zwischen "Von Einheit" und "In Einheit".</span><span class="sxs-lookup"><span data-stu-id="b73f6-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="b73f6-140">Der Faktor für die Umrechnung von Zentimeter in Meter beträgt beispielsweise 100, da 100 Zentimeter einem Meter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b73f6-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="b73f6-141">Geben Sie im Feld "In Einheit" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b73f6-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="b73f6-142">Wählen Sie im Feld "Rundung" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="b73f6-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="b73f6-143">Definiert, wie der konvertierte Wert gerundet werden soll</span><span class="sxs-lookup"><span data-stu-id="b73f6-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="b73f6-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b73f6-144">Click OK.</span></span>
7. <span data-ttu-id="b73f6-145">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b73f6-145">Close the page.</span></span>

