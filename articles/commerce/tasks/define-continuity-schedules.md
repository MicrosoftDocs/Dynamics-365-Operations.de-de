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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06fd1e23ad84fdc5e94e309717d5a96fbff45035
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140898"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="eb613-103"> Anschlusszeitpläne definieren</span><span class="sxs-lookup"><span data-stu-id="eb613-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb613-104">In diesem Thema lernen Sie das Einrichten eines Anschlussprogramms kennen (auch als wiederkehrende Aufträge bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="eb613-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="eb613-105">Für dieses Thema werden die USRT-Demodaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb613-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="eb613-106">Erstellen eines Anschlussprogramms</span><span class="sxs-lookup"><span data-stu-id="eb613-106">Create continuity program</span></span>
1. <span data-ttu-id="eb613-107">Navigieren Sie zu Retail and Commerce > Anschluss > Anschlussprogramme.</span><span class="sxs-lookup"><span data-stu-id="eb613-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="eb613-108">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="eb613-108">Click New.</span></span>
3. <span data-ttu-id="eb613-109">Geben Sie im Feld "Planungskennung" die Anschlusszeitplankennung ein</span><span class="sxs-lookup"><span data-stu-id="eb613-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="eb613-110">Wählen Sie im "Auftragsanfang"-Feld "Erstes Ereignis" aus.</span><span class="sxs-lookup"><span data-stu-id="eb613-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="eb613-111">Wenn ein Kunde einen neuen Auftrag für das Kontinuitätsprogramm platziert, gibt es zwei Optionen für das Produkt versendet wird: . 1.</span><span class="sxs-lookup"><span data-stu-id="eb613-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="eb613-112">Erstes Ereignis: das erste Produkt im Kontinuitätsprogramm wird versendet.</span><span class="sxs-lookup"><span data-stu-id="eb613-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="eb613-113">2.</span><span class="sxs-lookup"><span data-stu-id="eb613-113">2.</span></span> <span data-ttu-id="eb613-114">Aktuelles Ereignis: das aktuelle Produkt wird versendet.</span><span class="sxs-lookup"><span data-stu-id="eb613-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="eb613-115">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eb613-115">For example.</span></span> <span data-ttu-id="eb613-116">nach drei Monaten im Programm erhält der Debitor das dritte im Programm.</span><span class="sxs-lookup"><span data-stu-id="eb613-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="eb613-117">Wählen Sie "Ja" aus, um das Auftragsstartdatum einzugeben.</span><span class="sxs-lookup"><span data-stu-id="eb613-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="eb613-118">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="eb613-118">Click Add line.</span></span>
7. <span data-ttu-id="eb613-119">Geben Sie im Feld Artikelnummer die Artikelnummer für das erste Produkt ein ('0013').</span><span class="sxs-lookup"><span data-stu-id="eb613-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="eb613-120">Geben Sie "AP" ein.</span><span class="sxs-lookup"><span data-stu-id="eb613-120">Type 'CP'.</span></span>
9. <span data-ttu-id="eb613-121">Geben Sie das Datum ein, an dem das erste Produkt bestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb613-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="eb613-122">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="eb613-122">Click Add line.</span></span>
11. <span data-ttu-id="eb613-123">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0014" ein.</span><span class="sxs-lookup"><span data-stu-id="eb613-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="eb613-124">Löschen Sie im Feld Datumsintervallcode den Wert, sodass das Feld leer ist.</span><span class="sxs-lookup"><span data-stu-id="eb613-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="eb613-125">Bei diesem Verfahren löschen Sie das Datumsintervall.</span><span class="sxs-lookup"><span data-stu-id="eb613-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="eb613-126">Sie legen das Datum als inkrementell vom Startdatum des ersten Artikels fest.</span><span class="sxs-lookup"><span data-stu-id="eb613-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="eb613-127">Hier geben Sie den Intervall ein, in dem die Produkte geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="eb613-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="eb613-128">Geben Sie 30 ein.</span><span class="sxs-lookup"><span data-stu-id="eb613-128">Type '30'.</span></span>
    * <span data-ttu-id="eb613-129">Für ein Monatsprogramm geben Sie 30 Tage für das Intervall ein.</span><span class="sxs-lookup"><span data-stu-id="eb613-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="eb613-130">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="eb613-130">Click Add line.</span></span>
15. <span data-ttu-id="eb613-131">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0015" ein.</span><span class="sxs-lookup"><span data-stu-id="eb613-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="eb613-132">Geben Sie "Ende" ein.</span><span class="sxs-lookup"><span data-stu-id="eb613-132">Type 'End'.</span></span>
17. <span data-ttu-id="eb613-133">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="eb613-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="eb613-134">Zuweisen zu Anschlussartikel</span><span class="sxs-lookup"><span data-stu-id="eb613-134">Assign to continuity item</span></span>
1. <span data-ttu-id="eb613-135">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="eb613-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="eb613-136">Wählen Sie Artikel 0016 aus.</span><span class="sxs-lookup"><span data-stu-id="eb613-136">Select item '0016'.</span></span>
    * <span data-ttu-id="eb613-137">Für diese Prozedur wählen Sie die Artikelnummer 0016 aus.</span><span class="sxs-lookup"><span data-stu-id="eb613-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="eb613-138">Normalerweise haben Sie ein freigegebenes Produkt erstellt, für das zusätzliche Anschlussgeschäftslogik angewendet wird, wenn es im Callcenter für einen Auftrag platziert wird.</span><span class="sxs-lookup"><span data-stu-id="eb613-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="eb613-139">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="eb613-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="eb613-140">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="eb613-140">Click Edit.</span></span>
5. <span data-ttu-id="eb613-141">Erweitern oder reduzieren Sie den Abschnitt ''Verkaufen".</span><span class="sxs-lookup"><span data-stu-id="eb613-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="eb613-142">Hier geben Sie das Anschlussprogramm ein, das dieser Artikel darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb613-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="eb613-143">Geben Sie die Planungskennung ein, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="eb613-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="eb613-144">Wenn dieser Artikel in einem Callcenter verkauft wird, wird über das ausgewählte Anschlussprogramm eine zusätzliche Geschäftslogik angewendet.</span><span class="sxs-lookup"><span data-stu-id="eb613-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="eb613-145">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="eb613-145">Click Save.</span></span>

