---
title: Arbeitszeitsteuerung
description: In diesem Thema wird die Arbeitszeitsteuerung im Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918371"
---
# <a name="work-hour-control"></a><span data-ttu-id="a9b88-103">Arbeitszeitsteuerung</span><span class="sxs-lookup"><span data-stu-id="a9b88-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a9b88-104">Im Anlagenmanagement können Sie Stunden berechnen, um sich einen Überblick über die Iststunden im Vergleich zu den Budgetstunden auf Anlagen, Technischen Standorten oder Arbeitsaufträgen zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="a9b88-105">Die Ist-Stunden basieren auf gebuchten Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="a9b88-106">Arbeitszeitsteuerung für Anlagen, Technische Standorte und Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="a9b88-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="a9b88-107">Die Berechnungen für Anlagen, Technische Standorte und Arbeitsaufträge sind nahezu identisch.</span><span class="sxs-lookup"><span data-stu-id="a9b88-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="a9b88-108">Der einzige Unterschied besteht darin, dass Sie bei Anlagen und Technischen Standorten auch Teilanlagen und Teilstandorte in Ihre Kalkulation einbeziehen können.</span><span class="sxs-lookup"><span data-stu-id="a9b88-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="a9b88-109">Das Datum ist das Transaktionsdatum, an dem die Registrierung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="a9b88-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="a9b88-110">Klicken Sie auf **Anlagenmanagement** > **Anfragen** > **Anlagen** > **Anlagenstundensteuerung** oder **Funktionsstandortsteuerung**, oder **Anlagenmanagement** > **Anfragen** > **Aufträge** > **Auftragsstundensteuerung**.</span><span class="sxs-lookup"><span data-stu-id="a9b88-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="a9b88-111">Im Dialog **Anlagenstundensteuerung**, .</span><span class="sxs-lookup"><span data-stu-id="a9b88-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="a9b88-112">Wählen Sie im Dialog **Assetstundensteuerung** / **Funktionsstandortsteuerung** / **Arbeitsauftragsstundensteuerung** in den Feldern **Ab Datum** und **Bis Datum** einen zu berechnenden Zeitraum aus.</span><span class="sxs-lookup"><span data-stu-id="a9b88-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="a9b88-113">Wählen Sie bei Bedarf ein **Finanzdimensionssatz**, das in die Berechnung einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9b88-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="a9b88-114">Wählen Sie „Ja“ auf der Schaltfläche **Null überspringen**Umschalten, wenn Sie keine Ergebnisse mit Nullstunden anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="a9b88-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="a9b88-115">Im Feld **Stufe** können Sie angeben, wie detailliert die Stundenkontrollzeilen zu Technischen Standorten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> <span data-ttu-id="a9b88-116">Wenn Sie z.B. die Zahl in das Feld einfügen und eine mehrstufige Technische Platzhierarchie haben, werden alle Stundensteuerzeilen für einen Technischen Standort auf der obersten Ebene angezeigt, so dass die Stunden auf einer Zeile von Technischen Standorten auf einer niedrigeren Ebene summiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a9b88-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="a9b88-117">Wenn Sie die Zahl „0“ in das Feld **Ebene** eingeben, erhalten Sie ein detailliertes Ergebnis, das alle Stundenkontrollzeilen auf allen Ebenen des Technischen Standorts anzeigt, auf denen sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="a9b88-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="a9b88-118">Wählen Sie „Ja“ auf der Schaltfläche **Teilanlagen einbeziehen** Umschalten, um die mit Teilanlagen verbundenen Kosten als separate Zeilen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="a9b88-119">Wenn Sie die Suche einschränken möchten, können Sie bestimmte Anlagen / Technische Standorte / Arbeitsaufträge auf den **Sätzen auswählen, die mit** FastTab versehen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="a9b88-120">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="a9b88-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="a9b88-121">Klicken Sie auf der Seite **Anlagenstundensteuerung** in den Gruppen des Aktionsbereichs **Gruppieren nach...** auf die entsprechenden Schaltflächen, um den gewünschten Detaillierungsgrad der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-121">On the **Asset hour control** page, in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="a9b88-122">Die ausgewählten Aktionsbereichschaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="a9b88-122">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="a9b88-123">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a9b88-123">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="a9b88-124">Die folgende Abbildung zeigt ein Beispiel für eine Berechnung der **Anlagenstundensteuerung**.</span><span class="sxs-lookup"><span data-stu-id="a9b88-124">The figure below shows an example of an **Asset hour control** calculation.</span></span>

![Abbildung 1](media/04-controlling-and-reporting.png)

<span data-ttu-id="a9b88-126">Eine weitere Möglichkeit, eine Stundenberechnung durchzuführen, besteht darin, Anlagen in **Alle Anlagen** oder **Aktive Anlagen** mehrfach auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-126">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="a9b88-127">Dann klicken Sie auf die Schaltfläche **Stundensteuerung** auf der Seite **Allgemein** FastTab.</span><span class="sxs-lookup"><span data-stu-id="a9b88-127">Then, you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="a9b88-128">Die ausgewählten Anlagen werden automatisch in das Feld **Anlagen** auf der Seite **Einzubeziehende Anlagen** FastTab eingefügt.</span><span class="sxs-lookup"><span data-stu-id="a9b88-128">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="a9b88-129">Klicken Sie im Dialog **Anlagenstundensteuerung** auf **OK**, und die Berechnung für die ausgewählten Anlagen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9b88-129">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="a9b88-130">Das gleiche Verfahren kann für Technische Standorte in **Alle Technischen Standorte** oder **Aktive Technische Standorte** und für Arbeitsaufträge in **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a9b88-130">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="a9b88-131">Das Feld **Originalbudget** zeigt Budgetstunden aus der Arbeitsauftragsprognose.</span><span class="sxs-lookup"><span data-stu-id="a9b88-131">The **Original budget** field shows budget hours from the work order forecast.</span></span> <span data-ttu-id="a9b88-132">Das Feld **Iststunden** zeigt gebuchte Stunden auf Arbeitsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="a9b88-132">The **Actual hours** field shows posted hours on work orders.</span></span> <span data-ttu-id="a9b88-133">Das Feld **Verpflichtete Stunden** zeigt die Gesamtzahl der Stunden, die Ihr Unternehmen in Bezug auf Arbeitsaufträge verpflichtet ist.</span><span class="sxs-lookup"><span data-stu-id="a9b88-133">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

