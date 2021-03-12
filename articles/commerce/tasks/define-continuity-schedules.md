---
title: " Anschlusszeitpläne definieren"
description: In diesem Thema lernen Sie das Einrichten eines Anschlussprogramms kennen (auch als wiederkehrende Aufträge bezeichnet).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 37c4022cb2f2acf567437c821946ad452ba8f37c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972329"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="b3764-103"> Anschlusszeitpläne definieren</span><span class="sxs-lookup"><span data-stu-id="b3764-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3764-104">In diesem Thema lernen Sie das Einrichten eines Anschlussprogramms kennen (auch als wiederkehrende Aufträge bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="b3764-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="b3764-105">Für dieses Thema werden die USRT-Demodaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3764-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="b3764-106">Erstellen eines Anschlussprogramms</span><span class="sxs-lookup"><span data-stu-id="b3764-106">Create continuity program</span></span>
1. <span data-ttu-id="b3764-107">Navigieren Sie zu Retail and Commerce > Anschluss > Anschlussprogramme.</span><span class="sxs-lookup"><span data-stu-id="b3764-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="b3764-108">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="b3764-108">Click New.</span></span>
3. <span data-ttu-id="b3764-109">Geben Sie im Feld "Planungskennung" die Anschlusszeitplankennung ein</span><span class="sxs-lookup"><span data-stu-id="b3764-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="b3764-110">Wählen Sie im "Auftragsanfang"-Feld "Erstes Ereignis" aus.</span><span class="sxs-lookup"><span data-stu-id="b3764-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="b3764-111">Wenn ein Kunde einen neuen Auftrag für das Kontinuitätsprogramm platziert, gibt es zwei Optionen für das Produkt versendet wird: . 1.</span><span class="sxs-lookup"><span data-stu-id="b3764-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="b3764-112">Erstes Ereignis: das erste Produkt im Kontinuitätsprogramm wird versendet.</span><span class="sxs-lookup"><span data-stu-id="b3764-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="b3764-113">2.</span><span class="sxs-lookup"><span data-stu-id="b3764-113">2.</span></span> <span data-ttu-id="b3764-114">Aktuelles Ereignis: das aktuelle Produkt wird versendet.</span><span class="sxs-lookup"><span data-stu-id="b3764-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="b3764-115">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b3764-115">For example.</span></span> <span data-ttu-id="b3764-116">nach drei Monaten im Programm erhält der Debitor das dritte im Programm.</span><span class="sxs-lookup"><span data-stu-id="b3764-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="b3764-117">Wählen Sie "Ja" aus, um das Auftragsstartdatum einzugeben.</span><span class="sxs-lookup"><span data-stu-id="b3764-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="b3764-118">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b3764-118">Click Add line.</span></span>
7. <span data-ttu-id="b3764-119">Geben Sie im Feld Artikelnummer die Artikelnummer für das erste Produkt ein ('0013').</span><span class="sxs-lookup"><span data-stu-id="b3764-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="b3764-120">Geben Sie "AP" ein.</span><span class="sxs-lookup"><span data-stu-id="b3764-120">Type 'CP'.</span></span>
9. <span data-ttu-id="b3764-121">Geben Sie das Datum ein, an dem das erste Produkt bestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3764-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="b3764-122">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b3764-122">Click Add line.</span></span>
11. <span data-ttu-id="b3764-123">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0014" ein.</span><span class="sxs-lookup"><span data-stu-id="b3764-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="b3764-124">Löschen Sie im Feld Datumsintervallcode den Wert, sodass das Feld leer ist.</span><span class="sxs-lookup"><span data-stu-id="b3764-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="b3764-125">Bei diesem Verfahren löschen Sie das Datumsintervall.</span><span class="sxs-lookup"><span data-stu-id="b3764-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="b3764-126">Sie legen das Datum als inkrementell vom Startdatum des ersten Artikels fest.</span><span class="sxs-lookup"><span data-stu-id="b3764-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="b3764-127">Hier geben Sie den Intervall ein, in dem die Produkte geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="b3764-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="b3764-128">Geben Sie 30 ein.</span><span class="sxs-lookup"><span data-stu-id="b3764-128">Type '30'.</span></span>
    * <span data-ttu-id="b3764-129">Für ein Monatsprogramm geben Sie 30 Tage für das Intervall ein.</span><span class="sxs-lookup"><span data-stu-id="b3764-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="b3764-130">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b3764-130">Click Add line.</span></span>
15. <span data-ttu-id="b3764-131">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0015" ein.</span><span class="sxs-lookup"><span data-stu-id="b3764-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="b3764-132">Geben Sie "Ende" ein.</span><span class="sxs-lookup"><span data-stu-id="b3764-132">Type 'End'.</span></span>
17. <span data-ttu-id="b3764-133">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b3764-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="b3764-134">Zuweisen zu Anschlussartikel</span><span class="sxs-lookup"><span data-stu-id="b3764-134">Assign to continuity item</span></span>
1. <span data-ttu-id="b3764-135">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="b3764-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b3764-136">Wählen Sie Artikel 0016 aus.</span><span class="sxs-lookup"><span data-stu-id="b3764-136">Select item '0016'.</span></span>
    * <span data-ttu-id="b3764-137">Für diese Prozedur wählen Sie die Artikelnummer 0016 aus.</span><span class="sxs-lookup"><span data-stu-id="b3764-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="b3764-138">Normalerweise haben Sie ein freigegebenes Produkt erstellt, für das zusätzliche Anschlussgeschäftslogik angewendet wird, wenn es im Callcenter für einen Auftrag platziert wird.</span><span class="sxs-lookup"><span data-stu-id="b3764-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="b3764-139">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b3764-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b3764-140">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="b3764-140">Click Edit.</span></span>
5. <span data-ttu-id="b3764-141">Erweitern oder reduzieren Sie den Abschnitt ''Verkaufen".</span><span class="sxs-lookup"><span data-stu-id="b3764-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="b3764-142">Hier geben Sie das Anschlussprogramm ein, das dieser Artikel darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3764-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="b3764-143">Geben Sie die Planungskennung ein, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b3764-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="b3764-144">Wenn dieser Artikel in einem Callcenter verkauft wird, wird über das ausgewählte Anschlussprogramm eine zusätzliche Geschäftslogik angewendet.</span><span class="sxs-lookup"><span data-stu-id="b3764-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="b3764-145">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b3764-145">Click Save.</span></span>

