---
title: Wartungsstatus
description: In diesem Thema wird erläutert, wie Sie den Instandhaltungsstatus in der Anlagenverwaltung berechnen.
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
ms.openlocfilehash: 8f336086838632dd3f464de2870e9a9197746daa
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652125"
---
# <a name="maintenance-status"></a><span data-ttu-id="4ee6c-103">Wartungsstatus</span><span class="sxs-lookup"><span data-stu-id="4ee6c-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4ee6c-104">Im Anlagenmanagement können Sie eine Übersichtskalkulation für eine bestimmte Periode für neue, aktive und abgeschlossene Wartungsanfragen, Arbeitsaufträge und Wartungsausfallzeiten durchführen.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="4ee6c-105">Sie können auch die Anzahl der abgeschlossenen Zustandsbewertungen für den gleichen Zeitraum sehen.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="4ee6c-106">Verwenden Sie diese Kalkulation, um sich einen Überblick über den Arbeitsaufwand bei eingehenden und abgeschlossenen Wartungsanfragen und Arbeitsaufträgen zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="4ee6c-107">Eine Berechnung des Wartungsstatus durchführen</span><span class="sxs-lookup"><span data-stu-id="4ee6c-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="4ee6c-108">Klicken Sie auf **Anlagemanagement** > **Anfragen** > **Wartungsstatus**.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="4ee6c-109">Wählen Sie im Dialog **Status berechnen** in den Feldern **Ab Datum** und **Bis Datum** den Zeitbereich aus, für den Sie die Berechnung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="4ee6c-110">Über das Feld **Stufe** können Sie angeben, wie detailliert die Wartungszeilen zu Technischen Standorten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="4ee6c-111">Wenn Sie z.B. die Zahl in das Feld einfügen und eine mehrstufige Struktur des Technischen Standorts haben, werden alle Wartungszeilen zu einem Technischen Standort auf der obersten Ebene angezeigt, so dass der Status auf einer Zeile von untergeordneten Technischen Standorten aufsummiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="4ee6c-112">Wenn Sie in das Feld **Ebene** die Zahl „0“ eingeben, erhalten Sie ein detailliertes Ergebnis, das alle Wartungszeilen auf allen Ebenen des Technischen Standorts anzeigt, auf denen sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="4ee6c-113">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="4ee6c-114">Klicken Sie auf die **Gruppieren nach…**-Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="4ee6c-115">Die ausgewählten **Gruppieren nach…**-Schaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="4ee6c-116">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="4ee6c-117">Denken Sie daran, auf die Schaltfläche **Aktualisieren** zu klicken, um die Berechnung jedes Mal zu aktualisieren, wenn Sie Änderungen vornehmen, indem Sie die **Gruppieren nach...**-Schaltflächen aktivieren oder deaktivieren oder eine Berechnung für einen neuen Zeitraum durchführen.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="4ee6c-118">Klicken Sie auf **Status**, wenn Sie eine neue Berechnung des Wartungsstatus erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="4ee6c-119">Die unter **Wartungsstatus** angezeigten Ergebnisse umfassen nur Wartungsanforderungen und Arbeitsaufträge, die ein tatsächliches Startdatum und eine tatsächliche Startzeit haben.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="4ee6c-120">Enddatum und -zeit können leer sein.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="4ee6c-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ee6c-121">Example 1</span></span>

<span data-ttu-id="4ee6c-122">Im Screenshot unten wurden die Schaltflächen **Jahr** und **Monat** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="4ee6c-123">Werden diese **Gruppieren nach...**-Optionen ausgewählt, erhalten Sie einen allgemeinen Überblick über den monatlichen Arbeitsaufwand und -durchsatz im Zusammenhang mit Wartungsanfragen und Arbeitsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Beispiel des monatlichen Arbeitsaufwands](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="4ee6c-125">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ee6c-125">Example 2</span></span>

<span data-ttu-id="4ee6c-126">Im Screenshot unten wurden Informationen über funktionale Standorte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="4ee6c-127">Jetzt ist es möglich, Arbeitslast und Durchsatz über funktionale Standorte hinweg zu vergleichen, die geografische Standorte, Fabriken oder Arbeitsbereiche repräsentieren können.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Beispiel des monatlichen Arbeitsaufwands mit funktionalen Standorten](media/14-controlling-and-reporting.png)

