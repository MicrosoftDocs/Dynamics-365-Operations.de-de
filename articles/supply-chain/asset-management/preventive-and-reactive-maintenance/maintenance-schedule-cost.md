---
title: Kosten – Wartungszeitplan
description: In diesem Thema wird die Kosten für Wartungszeitplan in Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.openlocfilehash: 91c5b2e70ee083bf2741e245f1ca840ab939ad3f
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3382974"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="d26b2-103">Kosten – Wartungszeitplan</span><span class="sxs-lookup"><span data-stu-id="d26b2-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d26b2-104">In Asset-Management können Sie Budgetkosten auf Wartungszeitplanpositionen berechnen.</span><span class="sxs-lookup"><span data-stu-id="d26b2-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="d26b2-105">Dies ist nützlich, wenn Sie sich einen Überblick über zu erwartenden Kosten verschaffen möchten, z.B. Kosten für geplante vorbeugende Wartungsaufträge für das nächste Jahr.</span><span class="sxs-lookup"><span data-stu-id="d26b2-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="d26b2-106">Die Berechnungen basieren auf vorhandenen Wartungszeitplanpositionen vom Typ „Wartungspläne“ und „Wartungsdurchgänge“ und „Wartungsanfragen“.</span><span class="sxs-lookup"><span data-stu-id="d26b2-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="d26b2-107">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Wartungszeitplankosten**.</span><span class="sxs-lookup"><span data-stu-id="d26b2-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="d26b2-108">Im Dialog **Wartungszeitplankosten** können Sie einen **Finanzdimensionssatz** auswählen, wenn Sie die Kosten nach Finanzdimensionen gruppieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d26b2-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="d26b2-109">Finanzdimensionssätze werden in **Hauptbuch** > **Kontenplan** > **Dimensionen** > **Finanzdimensionssätze** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="d26b2-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="d26b2-110">Sie können das Feld **Ebene** verwenden, um anzugeben, wie detailliert der Wartungszeitplan bezüglich funktionaler Standorte sein sollen.</span><span class="sxs-lookup"><span data-stu-id="d26b2-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="d26b2-111">Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Wartungszeitplanpositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d26b2-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="d26b2-112">Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Wartungszeitplanpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d26b2-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="d26b2-113">Wenn Sie eine Berechnung für bestimmte Anlagen durchführen möchten, klicken Sie auf **Filter** auf dem Inforegister **Einzuschließende Datensätze**, und wählen Sie die entsprechenden Anlagen aus.</span><span class="sxs-lookup"><span data-stu-id="d26b2-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="d26b2-114">Bei Bedarf können Sie auch einen **Voraussichtlichen Starttermin** für die Kostenkalkulation angeben oder einen anderen **Status** für die Kostenkalkulation auswählen.</span><span class="sxs-lookup"><span data-stu-id="d26b2-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="d26b2-115">Klicken Sie zum Starten der Kostneberechnung auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d26b2-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="d26b2-116">Klicken Sie auf der Registerkarte **Wartungszeitplankosten** > in den Aktivitätsbereichsgruppen **Gruppieren nach...** auf die entsprechenden Schaltflächen, um die gewünschten Detailstufe der Kostenkalkulation anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d26b2-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="d26b2-117">Die ausgewählten Aktionsbereichsgruppenschaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="d26b2-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="d26b2-118">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d26b2-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="d26b2-119">Klicken Sie auf die Schaltfläche **Kosten berechnen**, wenn Sie eine neue Kostenberechnung vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="d26b2-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="d26b2-120">In der folgende Abbildung wird die Ergebnisse einer Wartungsplankostenberechnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d26b2-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Abbildung 1](media/17-preventive-maintenance.png)

