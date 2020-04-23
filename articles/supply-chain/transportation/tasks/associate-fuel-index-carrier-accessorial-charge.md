---
title: Brennstoffindex einem Spediteur als Zusatzgebühr zuordnen
description: Dieses Handbuch, zeigt wie Sie eine Zusatzleistungszuweisung, Spediteurzusatzgebühr sowie einen Zusatzleistungsmaster für Benzinzuschlag erstellen und einen Spediteurskraftstoffindex einem Spediteur zuordnen.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b3267122594329444fc4b0458db6b14aa5c672
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206195"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="e4641-103">Brennstoffindex einem Spediteur als Zusatzgebühr zuordnen</span><span class="sxs-lookup"><span data-stu-id="e4641-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4641-104">Dieses Handbuch, zeigt wie Sie eine Zusatzleistungszuweisung, Spediteurzusatzgebühr sowie einen Zusatzleistungsmaster für Benzinzuschlag erstellen und einen Spediteurskraftstoffindex einem Spediteur zuordnen.</span><span class="sxs-lookup"><span data-stu-id="e4641-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="e4641-105">Sie müssen einen Spediteurskraftstoffindex eingerichtet haben, bevor Sie dieses Handbuch ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4641-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="e4641-106">Sie können das Handbuch „Einrichten eines Spedituerkraftstoffindex“ für diese Aufgaben verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4641-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="e4641-107">Diese Einrichtungsaufgaben werden normalerweise von einem Logistikmanager durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4641-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="e4641-108">Die Demodaten, die verwendet werden, um diese Prozedur zu erstellen, sind USMF.</span><span class="sxs-lookup"><span data-stu-id="e4641-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="e4641-109">Erstellen eines Zusatzleistungsmaster</span><span class="sxs-lookup"><span data-stu-id="e4641-109">Create an accessorial master</span></span>
1. <span data-ttu-id="e4641-110">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Zusatzleistungsmaster".</span><span class="sxs-lookup"><span data-stu-id="e4641-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="e4641-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e4641-111">Click New.</span></span>
3. <span data-ttu-id="e4641-112">Geben Sie einen Wert in das Feld "Zusatzleistungsmaster" ein.</span><span class="sxs-lookup"><span data-stu-id="e4641-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="e4641-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e4641-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e4641-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e4641-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="e4641-115">Spediteurzusatzgebühr erstellen</span><span class="sxs-lookup"><span data-stu-id="e4641-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="e4641-116">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Bewertung" > "Spediteurzusatzgebühren".</span><span class="sxs-lookup"><span data-stu-id="e4641-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="e4641-117">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e4641-117">Click New.</span></span>
3. <span data-ttu-id="e4641-118">Geben Sie einen Wert in das Feld "Spediteurzusatzleistungs-Kennung" ein.</span><span class="sxs-lookup"><span data-stu-id="e4641-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="e4641-119">Klicken Sie im Feld "Spediteur " auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4641-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e4641-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e4641-121">In diesem Beispiel wählen Sie LKW-Spediteur aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="e4641-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e4641-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e4641-123">Klicken Sie im Feld "Spediteurdienstleistung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4641-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e4641-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e4641-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e4641-125">Klicken Sie im Feld "Zusatzleistungsmaster" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4641-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e4641-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e4641-127">In diesem Beispiel wählen Sie den neu erstellten Zusatzleistungsmaster aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="e4641-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e4641-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="e4641-129">Erstellen einer Zusatzleistungszuweisung</span><span class="sxs-lookup"><span data-stu-id="e4641-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="e4641-130">Klicken Sie auf "Zusatzleistungszuweisungen".</span><span class="sxs-lookup"><span data-stu-id="e4641-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="e4641-131">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e4641-131">Click New.</span></span>
3. <span data-ttu-id="e4641-132">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e4641-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e4641-133">Schalten Sie die Erweiterung des Abschnitts "Kriterien" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="e4641-134">In den Kriterien können Sie festlegen, dass der Benzinzuschlag immer angewendet wird, oder für dieses Beispiel wählen Sie aus, dass es nur innerhalb einer bestimmten Region gilt.</span><span class="sxs-lookup"><span data-stu-id="e4641-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="e4641-135">Geben Sie im Feld "Postleitzahl Absender" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e4641-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="e4641-136">Geben Sie im Feld "Postleitzahl Empfänger" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e4641-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="e4641-137">Schalten Sie die Erweiterung des Abschnitts "Berechnung" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="e4641-138">Im Berechnungsabschnitt können Sie angeben, wie der Benzinzuschlag berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e4641-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="e4641-139">Diese Berechnung hängt von der Zusatzleistungseinheit ab, die Sie als Grundlage für die Berechnung ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="e4641-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="e4641-140">Wählen Sie im Feld "Gebührentyp Zusatzleistung" "Benzinzuschlag"aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="e4641-141">Wählen Sie im Feld "Zusatzleistungseinheit" "Kilometerleistung" aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="e4641-142">Klicken Sie im Feld "Region" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4641-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e4641-143">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e4641-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e4641-144">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e4641-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="e4641-145">Spediteurbewertungsprofil aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e4641-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="e4641-146">Wechseln Sie zu "Transportverwaltung" > "Einrichten" > "Spediteure" > "Spediteure".</span><span class="sxs-lookup"><span data-stu-id="e4641-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="e4641-147">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e4641-148">Schalten Sie die Erweiterung des Abschnitts "Bewertungsprofile" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="e4641-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="e4641-149">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e4641-149">Click Edit.</span></span>
5. <span data-ttu-id="e4641-150">Klicken Sie im Feld "Spediteur-Kraftstoffindex" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4641-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e4641-151">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e4641-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e4641-152">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e4641-152">Click Save.</span></span>

