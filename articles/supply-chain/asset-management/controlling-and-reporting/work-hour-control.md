---
title: Arbeitszeitsteuerung
description: In diesem Thema wird die Arbeitszeitsteuerung im Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc4382d72e032fdfad05f2077ffe8e41e64c6a55
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018470"
---
# <a name="work-hour-control"></a><span data-ttu-id="8c934-103">Arbeitszeitsteuerung</span><span class="sxs-lookup"><span data-stu-id="8c934-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8c934-104">Im Anlagenmanagement können Sie Stunden berechnen, um sich einen Überblick über die Iststunden im Vergleich zu den Budgetstunden auf Anlagen, Technischen Standorten oder Arbeitsaufträgen zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="8c934-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="8c934-105">Die Ist-Stunden basieren auf gebuchten Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="8c934-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="8c934-106">Arbeitszeitsteuerung für Anlagen, Technische Standorte und Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="8c934-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="8c934-107">Die Berechnungen für Anlagen, Technische Standorte und Arbeitsaufträge sind nahezu identisch.</span><span class="sxs-lookup"><span data-stu-id="8c934-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="8c934-108">Der einzige Unterschied besteht darin, dass Sie bei Anlagen und Technischen Standorten auch Teilanlagen und Teilstandorte in Ihre Kalkulation einbeziehen können.</span><span class="sxs-lookup"><span data-stu-id="8c934-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="8c934-109">Das Datum ist das Transaktionsdatum, an dem die Registrierung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="8c934-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="8c934-110">Klicken Sie auf **Anlagenmanagement** > **Anfragen** > **Anlagen** > **Anlagenstundensteuerung** oder **Funktionsstandortsteuerung**, oder **Anlagenmanagement** > **Anfragen** > **Aufträge** > **Auftragsstundensteuerung**.</span><span class="sxs-lookup"><span data-stu-id="8c934-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="8c934-111">Im Dialog **Anlagenstundensteuerung**, .</span><span class="sxs-lookup"><span data-stu-id="8c934-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="8c934-112">Wählen Sie im Dialog **Assetstundensteuerung** / **Funktionsstandortsteuerung** / **Arbeitsauftragsstundensteuerung** in den Feldern **Ab Datum** und **Bis Datum** einen zu berechnenden Zeitraum aus.</span><span class="sxs-lookup"><span data-stu-id="8c934-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="8c934-113">Wählen Sie bei Bedarf ein **Finanzdimensionssatz**, das in die Berechnung einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8c934-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="8c934-114">Wählen Sie „Ja“ auf der Schaltfläche **Null überspringen** Umschalten, wenn Sie keine Ergebnisse mit Nullstunden anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c934-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="8c934-115">Im Feld **Stufe** können Sie angeben, wie detailliert die Stundenkontrollzeilen zu Technischen Standorten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="8c934-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="8c934-116">Wenn Sie z.B. die Zahl in das Feld einfügen und eine mehrstufige Technische Platzhierarchie haben, werden alle Stundensteuerzeilen für einen Technischen Standort auf der obersten Ebene angezeigt, so dass die Stunden auf einer Zeile von Technischen Standorten auf einer niedrigeren Ebene summiert werden können.</span><span class="sxs-lookup"><span data-stu-id="8c934-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="8c934-117">Wenn Sie die Zahl „0“ in das Feld **Ebene** eingeben, erhalten Sie ein detailliertes Ergebnis, das alle Stundenkontrollzeilen auf allen Ebenen des Technischen Standorts anzeigt, auf denen sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="8c934-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="8c934-118">Wählen Sie „Ja“ auf der Schaltfläche **Teilanlagen einbeziehen** Umschalten, um die mit Teilanlagen verbundenen Kosten als separate Zeilen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c934-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="8c934-119">Wenn Sie die Suche einschränken möchten, können Sie bestimmte Anlagen / Technische Standorte / Arbeitsaufträge auf den **Sätzen auswählen, die mit** FastTab versehen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c934-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="8c934-120">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="8c934-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="8c934-121">Klicken Sie auf der Seite **Anlagenstundensteuerung** auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c934-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="8c934-122">Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="8c934-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="8c934-123">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8c934-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="8c934-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8c934-124">Example</span></span>

<span data-ttu-id="8c934-125">Die Abbildung zeigt ein Beispiel für eine Berechnung der **Anlagenstundensteuerung**.</span><span class="sxs-lookup"><span data-stu-id="8c934-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="8c934-126">Das Feld **Originalbudget** zeigt Budgetstunden aus der Arbeitsauftragsprognose.</span><span class="sxs-lookup"><span data-stu-id="8c934-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="8c934-127">Das Feld **Iststunden** zeigt gebuchte Stunden auf Arbeitsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="8c934-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="8c934-128">Das Feld **Verpflichtete Stunden** zeigt die Gesamtzahl der Stunden, die Ihr Unternehmen in Bezug auf Arbeitsaufträge verpflichtet ist.</span><span class="sxs-lookup"><span data-stu-id="8c934-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Beispiel der Berechnung der Anlagenstundensteuerung](media/04-controlling-and-reporting.png)

<span data-ttu-id="8c934-130">Eine weitere Möglichkeit, eine Stundenberechnung durchzuführen, besteht darin, Anlagen in **Alle Anlagen** oder **Aktive Anlagen** mehrfach auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8c934-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="8c934-131">Dann klicken Sie auf die Schaltfläche **Stundensteuerung** auf dem Inforegister **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="8c934-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="8c934-132">Die ausgewählten Anlagen werden automatisch in das Feld **Anlagen** auf der Seite **Einzubeziehende Anlagen** FastTab eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8c934-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="8c934-133">Klicken Sie im Dialog **Anlagenstundensteuerung** auf **OK**, und die Berechnung für die ausgewählten Anlagen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c934-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="8c934-134">Das gleiche Verfahren kann für Technische Standorte in **Alle Technischen Standorte** oder **Aktive Technische Standorte** und für Arbeitsaufträge in **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c934-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


