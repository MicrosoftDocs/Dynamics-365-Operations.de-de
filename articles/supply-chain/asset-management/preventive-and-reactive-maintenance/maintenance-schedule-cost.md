---
title: Kosten – Wartungszeitplan
description: In diesem Thema wird die Kosten für Wartungszeitplan in Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: b30fa3c142057b43202a8f5a323c0b425865e971
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571322"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="88ef2-103">Kosten – Wartungszeitplan</span><span class="sxs-lookup"><span data-stu-id="88ef2-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="88ef2-104">In Asset-Management können Sie Budgetkosten auf Wartungszeitplanpositionen berechnen.</span><span class="sxs-lookup"><span data-stu-id="88ef2-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="88ef2-105">Dies ist nützlich, wenn Sie sich einen Überblick über zu erwartenden Kosten verschaffen möchten, z.B. Kosten für geplante vorbeugende Wartungsaufträge für das nächste Jahr.</span><span class="sxs-lookup"><span data-stu-id="88ef2-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="88ef2-106">Die Berechnungen basieren auf vorhandenen Wartungszeitplanpositionen vom Typ „Wartungspläne“ und „Wartungsdurchgänge“ und „Wartungsanfragen“.</span><span class="sxs-lookup"><span data-stu-id="88ef2-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="88ef2-107">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Wartungszeitplankosten**.</span><span class="sxs-lookup"><span data-stu-id="88ef2-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="88ef2-108">Im Dialog **Wartungszeitplankosten** können Sie einen **Finanzdimensionssatz** auswählen, wenn Sie die Kosten nach Finanzdimensionen gruppieren möchten.</span><span class="sxs-lookup"><span data-stu-id="88ef2-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="88ef2-109">Finanzdimensionssätze werden in **Hauptbuch** > **Kontenplan** > **Dimensionen** > **Finanzdimensionssätze** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="88ef2-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="88ef2-110">Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert der Wartungszeitplan bezüglich funktionaler Standorte sein sollen.</span><span class="sxs-lookup"><span data-stu-id="88ef2-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="88ef2-111">Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Wartungszeitplanpositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="88ef2-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="88ef2-112">Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Wartungszeitplanpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="88ef2-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="88ef2-113">Wenn Sie eine Berechnung für bestimmte Anlagen durchführen möchten, klicken Sie auf **Filter** auf dem Inforegister **Einzuschließende Datensätze**, und wählen Sie die entsprechenden Anlagen aus.</span><span class="sxs-lookup"><span data-stu-id="88ef2-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="88ef2-114">Bei Bedarf können Sie auch einen **Voraussichtlichen Starttermin** für die Kostenkalkulation angeben oder einen anderen **Status** für die Kostenkalkulation auswählen.</span><span class="sxs-lookup"><span data-stu-id="88ef2-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="88ef2-115">Klicken Sie zum Starten der Kostneberechnung auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="88ef2-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="88ef2-116">Klicken Sie auf der Registerkarte **Wartungszeitplankosten** > in den Aktivitätsbereichsgruppen **Gruppieren nach...** auf die entsprechenden Schaltflächen, um die gewünschten Detailstufe der Kostenkalkulation anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="88ef2-116">On the **Maintenance schedule cost** tab > in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="88ef2-117">Die ausgewählten Aktionsbereichsgruppenschaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="88ef2-117">The selected action pane group buttons are highlighted.</span></span> <span data-ttu-id="88ef2-118">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="88ef2-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="88ef2-119">Klicken Sie auf die Schaltfläche **Kosten berechnen**, wenn Sie eine neue Kostenberechnung vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="88ef2-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="88ef2-120">In der folgende Abbildung wird die Ergebnisse einer Wartungsplankostenberechnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88ef2-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Abbildung 1](media/17-preventive-maintenance.png)

