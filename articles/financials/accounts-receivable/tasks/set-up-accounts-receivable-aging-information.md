---
title: Debitoren-Fälligkeitsinformationen einrichten und generieren
description: Dieses Handbuch unterstützt Sie dabei, eine Zahlungsfristdefinition sowie Dauerdebitorensalden einzurichten und Salden in der Liste "Saldorückblick" und auf der Seite "Inkasso" anzuzeigen.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fd8738cfd3466464c9fec1760e9a369ff3a4a67
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568234"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="e10ee-103">Debitoren-Fälligkeitsinformationen einrichten und generieren</span><span class="sxs-lookup"><span data-stu-id="e10ee-103">Set up and generate accounts receivable aging information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e10ee-104">Dieses Handbuch unterstützt Sie dabei, eine Zahlungsfristdefinition sowie Dauerdebitorensalden einzurichten und Salden in der Liste "Saldorückblick" und auf der Seite "Inkasso" anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e10ee-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="e10ee-105">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="e10ee-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="e10ee-106">Eine Zahlungsfristdefinition erstellen</span><span class="sxs-lookup"><span data-stu-id="e10ee-106">Create an aging period definition</span></span>
1. <span data-ttu-id="e10ee-107">Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Zahlungsfristdefinitionen".</span><span class="sxs-lookup"><span data-stu-id="e10ee-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="e10ee-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e10ee-108">Click New.</span></span>
3. <span data-ttu-id="e10ee-109">Geben Sie im Feld "Zahlungsfristdefinition" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e10ee-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="e10ee-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e10ee-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e10ee-111">Klicken Sie auf "Unten hinzufügen", um eine neue Zahlungsfrist einzufügen.</span><span class="sxs-lookup"><span data-stu-id="e10ee-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="e10ee-112">Geben Sie im Feld "Periode" die Beschreibung ein, die bei Fälligkeitsberichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e10ee-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="e10ee-113">Geben Sie im Feld "Einheit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="e10ee-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="e10ee-114">Wählen Sie im Feld "Intervall" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="e10ee-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="e10ee-115">Die Sachkontoperiode passt die Periode an Ihren Sachkontokalender an.</span><span class="sxs-lookup"><span data-stu-id="e10ee-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="e10ee-116">Tag, Woche, Monat, Quartal und Jahre definieren die Größe des Intervalls nach Datumstyp.</span><span class="sxs-lookup"><span data-stu-id="e10ee-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="e10ee-117">Bei "Unbegrenzt" werden alle Buchungen vor oder nach der vorherigen Periode ausgewählt, je nachdem, ob sie die erste oder letzte Periode ist.</span><span class="sxs-lookup"><span data-stu-id="e10ee-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="e10ee-118">Wählen Sie im Feld "Fälligkeitsindikator" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="e10ee-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="e10ee-119">Wählen Sie die Periode oben im Raster aus.</span><span class="sxs-lookup"><span data-stu-id="e10ee-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="e10ee-120">Aktualisieren Sie die Beschreibung, um die älteste Periode in der Zahlungsfristdefinition zu beschreiben</span><span class="sxs-lookup"><span data-stu-id="e10ee-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="e10ee-121">Geben Sie im Feld "Periode" die neue Beschreibung der Zahlungsfrist ein.</span><span class="sxs-lookup"><span data-stu-id="e10ee-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="e10ee-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e10ee-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="e10ee-123">Die Salden nach Fälligkeit anzeigen</span><span class="sxs-lookup"><span data-stu-id="e10ee-123">Age the balances</span></span>
1. <span data-ttu-id="e10ee-124">Wechseln Sie zu "Kredit und Inkasso" > "Periodische Aufgaben" > "Fälligkeit von Debitorensalden bestimmen".</span><span class="sxs-lookup"><span data-stu-id="e10ee-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="e10ee-125">Wählen Sie im Feld "Zahlungsfristdefinition" die Zahlungsfristdefinition aus, die Sie selbst erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e10ee-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="e10ee-126">Sie können eine aktive Momentaufnahme für jede Zahlungsfristdefinition haben.</span><span class="sxs-lookup"><span data-stu-id="e10ee-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="e10ee-127">Alle Debitoren werden standardmäßig verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e10ee-127">All customers are processed by default.</span></span> <span data-ttu-id="e10ee-128">Sie können diese Auswahl verwenden, um einen einzelnen Inkassopool von Debitoren zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e10ee-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="e10ee-129">Wählen Sie das Datum aus der Transaktion aus, das Sie für die Fälligkeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="e10ee-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="e10ee-130">Wählen Sie ein "per"-Datum für die Fälligkeit aus.</span><span class="sxs-lookup"><span data-stu-id="e10ee-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="e10ee-131">Der Standardwert ist Heute, aber, wenn Sie dieses Feld zu "Ausgewähltes Datum" ändern, können Sie das Datum auswählen, das sie möchten.</span><span class="sxs-lookup"><span data-stu-id="e10ee-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="e10ee-132">Verwenden Sie für die Stapelverarbeitung das "Heutige Datum".</span><span class="sxs-lookup"><span data-stu-id="e10ee-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="e10ee-133">Erweitern Sie den "Unternehmensbereich".</span><span class="sxs-lookup"><span data-stu-id="e10ee-133">Expand the Company range.</span></span> <span data-ttu-id="e10ee-134">Sie können die Unternehmen auswählen, die in die Momentaufnahme eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e10ee-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="e10ee-135">Das aktuelle Unternehmen wird standardmäßig ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e10ee-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="e10ee-136">Klicken Sie auf OK, um die Momentaufnahme zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e10ee-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="e10ee-137">Es wird einige Zeit dauern. Warten Sie deshalb, bis der Schieberegler ausgeblendet wird und überprüfen Sie das Nachrichtencenter nach einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e10ee-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="e10ee-138">Die Salden auf der Liste "Saldenrückblick" und auf der Seite "Inkasso" anzeigen</span><span class="sxs-lookup"><span data-stu-id="e10ee-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="e10ee-139">Wechseln Sie zu "Kredit und Inkasso" > "Inkassi" > "Saldenrückblick".</span><span class="sxs-lookup"><span data-stu-id="e10ee-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="e10ee-140">Auf der Listenseite werden die Salden für den Debitor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e10ee-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="e10ee-141">Das Fälligkeitssymbol zeigt die Zahlungsfrist für die älteste Transaktion an.</span><span class="sxs-lookup"><span data-stu-id="e10ee-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="e10ee-142">Wählen Sie einen Debitor mit einem Saldo aus.</span><span class="sxs-lookup"><span data-stu-id="e10ee-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="e10ee-143">Erweitern Sie den Infoboxbereich "Fälligkeit", um den Saldenrückblick anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e10ee-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="e10ee-144">Die Zahlungsfristdefinition für die Infobox ist der standardmäßigen Zahlungsfristdefinition entnommen, die in den Parametern angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e10ee-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="e10ee-145">Sie können sie mithilfe des Menüs "Mahnen" ändern.</span><span class="sxs-lookup"><span data-stu-id="e10ee-145">You can change it using the Collect menu.</span></span>  

