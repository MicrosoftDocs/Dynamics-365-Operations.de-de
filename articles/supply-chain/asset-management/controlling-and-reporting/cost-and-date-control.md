---
title: Kosten- und Datenkontrolle
description: In diesem Thema wird die Kosten- und Datenkontrolle in der Anlagenverwaltung erläutert.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dc3b4d22f5ce9a7e14b3834c299fa5a86d8d2868
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205505"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="94f15-103">Kosten- und Datenkontrolle</span><span class="sxs-lookup"><span data-stu-id="94f15-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="94f15-104">In der Anlagenverwaltung können Sie Kosten berechnen, um sich so einen Überblick über die Istkosten im Vergleich zu den Budgetkosten für Anlagen, funktionale Standorte und Arbeitsaufträge zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="94f15-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="94f15-105">Istkosten basieren auf gebuchten Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="94f15-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="94f15-106">Sie können auch eine Datumsberechnung vornehmen, wenn Sie geplante Start- und Enddaten mit tatsächlichen Start- und Enddaten für Arbeitsaufträge vergleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="94f15-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="94f15-107">Kostenkontrolle für Anlagen, funktionale Standorte und Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="94f15-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="94f15-108">Die Berechnungen für Anlagen, Technische Standorte und Arbeitsaufträge sind nahezu identisch.</span><span class="sxs-lookup"><span data-stu-id="94f15-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="94f15-109">Der einzige Unterschied besteht darin, dass Sie bei Anlagen und funktionalen Standorten auch Teilanlagen und Teilstandorte in Ihre Kalkulation einbeziehen können.</span><span class="sxs-lookup"><span data-stu-id="94f15-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="94f15-110">Das Datum ist das Transaktionsdatum, an dem die Registrierung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="94f15-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="94f15-111">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Kostensteuerung für Anlagen** oder **Kostensteuerung für funktionalen Standort**, oder auf **Anlagenverwaltung** > **Abfragen** > **Arbeitsaufträge** > **Kostensteuerung für Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="94f15-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="94f15-112">Wählen Sie im Dialogfeld **Kostensteuerung für Anlagen** / **Kostensteuerung für funktionalen Standort** / **Kostensteuerung für Arbeitsaufträge** einen zu berechnenden Zeitbereich aus.</span><span class="sxs-lookup"><span data-stu-id="94f15-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="94f15-113">Bei Bedarf wählen Sie eine Finanzdimensionsgruppe aus, die in die Berechnung einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="94f15-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="94f15-114">Wählen Sie „Ja“ auf der Umschaltfläche **Null überspringen** aus, wenn keine Ergebnisse mit Kosten von Null angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94f15-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="94f15-115">Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Kostensteuerungspositionen bezüglich funktionaler Standorte sein sollen.</span><span class="sxs-lookup"><span data-stu-id="94f15-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="94f15-116">Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standorthierarchie auf mehreren Ebenen haben, werden alle Kostenkontrollpositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="94f15-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="94f15-117">Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Kostenkontrollpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="94f15-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="94f15-118">Wählen Sie „Ja“ für die Umschaltschaltfläche **Offene zugesagte Kosten anzeigen** aus, wenn diese Spalte in die Berechnung einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="94f15-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="94f15-119">Wählen Sie „Ja“ auf der Schaltfläche **Teilanlagen einbeziehen** Umschalten, um die mit Teilanlagen verbundenen Kosten als separate Zeilen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="94f15-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="94f15-120">Wenn Sie die Suche einschränken möchten, können Sie bestimmte Anlagen / Technische Standorte / Arbeitsaufträge auf den **Sätzen auswählen, die mit** FastTab versehen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94f15-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="94f15-121">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="94f15-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="94f15-122">In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Kostensteuerung für Anlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94f15-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Dialogfeld „Kostensteuerung für Anlagen“](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="94f15-124">Klicken Sie auf der Seite **Kostensteuerung für Anlagen** auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="94f15-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="94f15-125">Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="94f15-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="94f15-126">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="94f15-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="94f15-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="94f15-127">Example</span></span>

<span data-ttu-id="94f15-128">Im folgenden Screenshot wird ein Beispiel der Berechnungsergebnisse in **Kostensteuerung für Anlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94f15-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="94f15-129">Das Feld **Ursprüngliches Budget** zeigt Budgetkosten aus der Arbeitsauftragsplanung.</span><span class="sxs-lookup"><span data-stu-id="94f15-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="94f15-130">Das Feld **Zugesagte Kosten** zeigt den Ausgabengesamtbetrag an, dessen Zahlung eine juristische Person zugesagt hat.</span><span class="sxs-lookup"><span data-stu-id="94f15-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="94f15-131">Das Feld **Offene zugesagte Kosten** zeigt die Zahlungszusagen für Artikel, Stunden und Dienstleistungen an, die Sie bestellt oder erhalten, aber noch nicht bezahlt haben.</span><span class="sxs-lookup"><span data-stu-id="94f15-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="94f15-132">Wenn alle Verbrauchserfassungen gebucht wurden, werden die zugehörigen Kosten im Feld **Istkosten** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94f15-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Beispiel Berechnungsergebnisse in Kostensteuerung für Anlagen](media/02-controlling-and-reporting.png)

<span data-ttu-id="94f15-134">Eine weitere Möglichkeit der Erstellung einer Kostenberechnung ist die Mehrfachauswahl von Anlagen in **Alle Anlagen** oder **Aktive Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="94f15-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="94f15-135">Klicken Sie anschließend auf die Schaltfläche **Kostensteuerung** auf der Registerkarte **Allgemein** . Im Dialogfeld **Kostensteuerung für Anlagen** werden die ausgewählten Anlagen automatisch in das Feld **Anlage** im Inforegister **Einzuschließende Datensätze** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="94f15-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="94f15-136">Klicken Sie auf **OK**, und eine Kostenberechnung für die ausgewählten Anlagen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94f15-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="94f15-137">Das gleiche Verfahren kann für Technische Standorte in **Alle Technischen Standorte** oder **Aktive Technische Standorte** und für Arbeitsaufträge in **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="94f15-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="94f15-138">Datumskontrolle für Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="94f15-138">Work order date control</span></span>

<span data-ttu-id="94f15-139">Verwenden Sie diese Seite, um einen Überblick über die erwarteten Start- und Enddaten im Vergleich zu den tatsächlichen Start- und Enddaten für Arbeitsaufträge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="94f15-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="94f15-140">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Arbeitsaufträge** > **Datumskontrolle für Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="94f15-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="94f15-141">Klicken Sie auf **Berechnen**.</span><span class="sxs-lookup"><span data-stu-id="94f15-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="94f15-142">Wählen Sie einen funktionalen Standort im Feld **Funktionaler Standort** aus.</span><span class="sxs-lookup"><span data-stu-id="94f15-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="94f15-143">Fügen Sie den Bereich für die Berechnung in den Feldern **Anfangsdatum** und **Enddatum** ein.</span><span class="sxs-lookup"><span data-stu-id="94f15-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="94f15-144">Alle Arbeitsaufträge mit dem erwarteten Startdatum innerhalb des Bereichs werden einbezogen.</span><span class="sxs-lookup"><span data-stu-id="94f15-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="94f15-145">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="94f15-145">Click **OK**.</span></span>

6. <span data-ttu-id="94f15-146">Klicken Sie auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="94f15-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="94f15-147">Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="94f15-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="94f15-148">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="94f15-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="94f15-149">Beispiel</span><span class="sxs-lookup"><span data-stu-id="94f15-149">Example</span></span>

<span data-ttu-id="94f15-150">Im folgenden Screenshot wird ein Beispiel der Berechnungsergebnisse in **Datumskontrolle für Arbeitsaufträge** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94f15-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="94f15-151">Das Feld **Durchschn. Startverzögerung** zeigt die Differenz in Tagen zwischen dem geplanten Startdatum für einen Arbeitsauftrag im Vergleich zum tatsächlichen Startdatum an.</span><span class="sxs-lookup"><span data-stu-id="94f15-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="94f15-152">Wenn beispielsweise das tatsächliche Startdatum zwei Tage vor dem geplanten Startdatum war, wird „-2“ in diesem Feld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94f15-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="94f15-153">Das Feld **Durchschn. Endverzögerung** zeigt die Differenz in Tagen zwischen dem geplanten Enddatum für einen Arbeitsauftrag im Vergleich zum tatsächlichen Enddatum an.</span><span class="sxs-lookup"><span data-stu-id="94f15-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="94f15-154">Wenn beispielsweise das tatsächliche Enddatum drei Tage nach dem geplanten Enddatum war, wird „3“ in diesem Feld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94f15-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="94f15-155">Die Felder **Vorkommen** zeigen die Zahl der Häufigkeitsabweichungen in Bezug auf das geplante und das tatsächliche Startdatum und das geplante und tatsächliche Enddatum des Arbeitsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="94f15-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Beispiel Berechnungsergebnisse in Datumskontrolle für Arbeitsaufträge](media/03-controlling-and-reporting.png)


