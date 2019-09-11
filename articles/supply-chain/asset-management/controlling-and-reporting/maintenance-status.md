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
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918348"
---
# <a name="maintenance-status"></a><span data-ttu-id="cbbc7-103">Wartungsstatus</span><span class="sxs-lookup"><span data-stu-id="cbbc7-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="cbbc7-104">Im Asset Management können Sie eine Kalkulation durchführen, um sich einen Überblick über neue, aktive und abgeschlossene Instandhaltungsanforderungen, Arbeitsaufträge und Stillstandszeiten für einen bestimmten Zeitraum zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-104">In Asset Management, you can make a calculation to see an overview of new, active, and completed maintenance requests, work orders, and maintenance downtime activities for a specific period.</span></span> <span data-ttu-id="cbbc7-105">Sie können auch die Anzahl der abgeschlossenen Zustandsbewertungen für den gleichen Zeitraum sehen.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="cbbc7-106">Verwenden Sie diese Kalkulation, um sich einen Überblick über den Arbeitsaufwand bei eingehenden und abgeschlossenen Instandhaltungsanforderungen und Arbeitsaufträgen zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-106">Use this calculation to get an overview of workload regarding incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="cbbc7-107">Eine Berechnung des Wartungsstatus durchführen</span><span class="sxs-lookup"><span data-stu-id="cbbc7-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="cbbc7-108">Klicken Sie auf **Anlagemanagement** > **Anfragen** > **Wartungsstatus**.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="cbbc7-109">Wählen Sie im Dialog **Status berechnen** in den Feldern **Ab Datum** und **Bis Datum** den Zeitraum, für den Sie die Berechnung durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-109">In the **Calculate status** dialog, select the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="cbbc7-110">Über das Feld **Stufe** können Sie angeben, wie detailliert die Wartungszeilen zu Technischen Standorten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> <span data-ttu-id="cbbc7-111">Wenn Sie z.B. die Zahl in das Feld einfügen und eine mehrstufige Struktur des Technischen Standorts haben, werden alle Wartungszeilen zu einem Technischen Standort auf der obersten Ebene angezeigt, so dass der Status auf einer Zeile von untergeordneten Technischen Standorten aufsummiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="cbbc7-112">Wenn Sie in das Feld **Ebene** die Zahl „0“ eingeben, erhalten Sie ein detailliertes Ergebnis, das alle Wartungszeilen auf allen Ebenen des Technischen Standorts anzeigt, auf denen sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="cbbc7-113">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="cbbc7-114">In den Aktivitätsbereichsgruppen **Gruppieren nach…** klicken Sie auf die entsprechenden Schaltflächen, um die erforderliche Detailebene der Berechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-114">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="cbbc7-115">Die ausgewählten Aktionsbereichschaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-115">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="cbbc7-116">Klicken Sie auf eine Schaltfläche, um sie zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="cbbc7-117">Denken Sie daran, auf die Schaltfläche **Aktualisieren** zu klicken, um die Berechnung jedes Mal zu aktualisieren, wenn Sie Änderungen vornehmen, indem Sie **Gruppieren nach...** Tasten aktivieren oder deaktivieren oder eine Berechnung für einen neuen Zeitraum durchführen.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by...** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="cbbc7-118">Klicken Sie auf **Status**, wenn Sie eine neue Berechnung des Wartungsstatus erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="cbbc7-119">Die unter **Wartungsstatus** angezeigten Ergebnisse umfassen nur Wartungsanforderungen und Arbeitsaufträge, die ein tatsächliches Startdatum und eine tatsächliche Startzeit haben.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="cbbc7-120">Enddatum und -zeit können leer sein.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-120">End date and time may be blank.</span></span>

<span data-ttu-id="cbbc7-121">*Beispiel 1:* Übersicht</span><span class="sxs-lookup"><span data-stu-id="cbbc7-121">*Example 1:*</span></span>

<span data-ttu-id="cbbc7-122">In der folgenden Abbildung wurden die Schaltflächen **Jahr** und **Monat** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-122">In the figure below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="cbbc7-123">Hier erhalten Sie einen allgemeinen Überblick über den monatlichen Arbeitsaufwand und -durchsatz im Zusammenhang mit Instandhaltungsanforderungen und Arbeitsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-123">Here, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Abbildung 1](media/13-controlling-and-reporting.png)

<span data-ttu-id="cbbc7-125">*Beispiel 2:* Übersicht</span><span class="sxs-lookup"><span data-stu-id="cbbc7-125">*Example 2:*</span></span>

<span data-ttu-id="cbbc7-126">In der folgenden Abbildung wurden Informationen über Technische Standorte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-126">In the figure below, information about functional locations has been added.</span></span> <span data-ttu-id="cbbc7-127">Jetzt ist es möglich, Arbeitslast und Durchsatz über Technische PlätStandorte hinweg zu vergleichen, die geografische Standorte, Fabriken oder Arbeitsbereiche repräsentieren können.</span><span class="sxs-lookup"><span data-stu-id="cbbc7-127">Now, it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Abbildung 2](media/14-controlling-and-reporting.png)

