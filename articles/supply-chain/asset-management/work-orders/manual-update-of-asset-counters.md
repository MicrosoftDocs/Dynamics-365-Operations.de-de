---
title: Manuelle Aktualisierung der Anlagenzähler
description: Dieses Thema beschreibt die manuelle Aktualisierung von Anlagenzählern im Anlagenmanagement.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23a94415a662059ddbd41cc6a0ba9dab24aae44e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889432"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="c9f91-103">Die manuelle Aktualisierung von Anlagenzählern</span><span class="sxs-lookup"><span data-stu-id="c9f91-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c9f91-104">Zähler werden verwendet, um Erfassungen für eine Anlage zu erstellen, z. B. Erfassungen zur Anzahl der Stunden, die die Anlage in Betrieb war, oder zur Menge, die produziert wurde.</span><span class="sxs-lookup"><span data-stu-id="c9f91-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="c9f91-105">Der Zählertyp, der für einen Zähler aktiviert wird, kann festgelegt werden, um Zählerwerte zu vererben.</span><span class="sxs-lookup"><span data-stu-id="c9f91-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="c9f91-106">Das bedeutet, die Option **Anlagenzählerwerte vererben** ist auf **Ja** gesetzt auf dem Inforegister **Allgemein** der Seite **Zähler** (**Anlangenverwaltung** > **Einstellungen** > **Anlagentypen** > **Zähler**).</span><span class="sxs-lookup"><span data-stu-id="c9f91-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="c9f91-107">In diesem Fall, wenn Sie eine neue Zählerposition dieses Typs erstellen, wird jede untergeordnete Anlage, die den gleichen Zählertyp verwendet, automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c9f91-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="c9f91-108">Auf der Seite **Alle Anlagen** erstellen Sie Stunden- oder Mengenzählerregistrierungen für eine Anlage, basierend auf Ihren Messwerten für die Anlage.</span><span class="sxs-lookup"><span data-stu-id="c9f91-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="c9f91-109">Wählen Sie **Anlagenverwaltung** > **Allgemeines** > **Anlagen** > **Alle Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="c9f91-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="c9f91-110">Wählen Sie die Anlage aus und dann im Aktivitätsbereich auf der Registerkarte **Anlage** in der Gruppe **Vorbeugend** die Option **Zähler**.</span><span class="sxs-lookup"><span data-stu-id="c9f91-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="c9f91-111">Auf der Seite **Anlagenzähler** sehen Sie eine Liste aller früheren Zählerregistrierungen für die ausgewählte Anlage.</span><span class="sxs-lookup"><span data-stu-id="c9f91-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="c9f91-112">Wählen Sie **Neu** aus, um eine Registrierung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9f91-112">Select **New** to create a registration.</span></span> <span data-ttu-id="c9f91-113">Die Anlagen-ID wird automatisch in das Feld **Anlage** eingetragen.</span><span class="sxs-lookup"><span data-stu-id="c9f91-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="c9f91-114">Wählen Sie im Feld **Zähler** den entsprechenden Zähler aus.</span><span class="sxs-lookup"><span data-stu-id="c9f91-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="c9f91-115">Es sind nur Zähler zur Auswahl verfügbar, die sich auf die auf der Anlage ausgewählte Anlagenart beziehen.</span><span class="sxs-lookup"><span data-stu-id="c9f91-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="c9f91-116">Die zugehörige Einheit wird automatisch in das Feld **Einheit** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="c9f91-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="c9f91-117">Im Feld **Erfasst** wählen Sie das Datum und die Uhrzeit für die Zählererfassung aus.</span><span class="sxs-lookup"><span data-stu-id="c9f91-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="c9f91-118">Geben Sie im Feld **Wert** die Zahl seit der letzten Zählererfassung ein.</span><span class="sxs-lookup"><span data-stu-id="c9f91-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="c9f91-119">Sie können stattdessen im Feld **Aggregierter Wert** die gesamte Zählerzahl eingeben.</span><span class="sxs-lookup"><span data-stu-id="c9f91-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="c9f91-120">Beachten Sie die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="c9f91-120">Note the following points:</span></span>

- <span data-ttu-id="c9f91-121">Wenn Sie einen neuen Zähler physisch auf einer Anlage installieren, müssen Sie die Änderung auf der Anlage auf der Seite **Anlagenzähler** registrieren.</span><span class="sxs-lookup"><span data-stu-id="c9f91-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="c9f91-122">Danach müssen Sie zwei Erfassungspositionen erstellen, die identische Zeitstempel haben.</span><span class="sxs-lookup"><span data-stu-id="c9f91-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="c9f91-123">Die erste Position muss für den Zähler sein, den Sie ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c9f91-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="c9f91-124">Auf der Position, die dem neuen Zähler zugeordnet ist, aktivieren Sie das Kontrollkästchen **Zähler zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="c9f91-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="c9f91-125">Im Feld **Summen** ist die Gesamtzahl die Summe der Zählersummen aller registrierten Werte auf diesem Zählertyp.</span><span class="sxs-lookup"><span data-stu-id="c9f91-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="c9f91-126">Wenn das Kontrollkästchen **Zähler zurücksetzen** bei einer Anlage mit einem Wartungsplan mit Intervalltyp „Einmal von...“ oder „Einmal erreicht...“ aktiviert ist, ist der Zähler auf der neuen Zählerposition weiterhin aktiv, da Sie eine separate Zählerposition erstellen und mit einem neuen Zähler neu beginnen.</span><span class="sxs-lookup"><span data-stu-id="c9f91-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="c9f91-127">In der folgenden Abbildung wird ein Beispiel der Seite **Anlagenzähler** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9f91-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Abbildung 1](media/11-work-orders.png)

<span data-ttu-id="c9f91-129">Auf der Seite **Anlagenzähler** (**Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Anlagenzähler**) können Sie Zählererfassungen für mehrere Anlagen gleichzeitig nach Bedarf vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c9f91-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="c9f91-130">Sie können einen Bereich einrichten, um Abweichungen in den manuellen Zählererfassungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c9f91-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="c9f91-131">Sie können auch die Art der Meldung angeben, die angezeigt wird, wenn Erfassungen außerhalb des definierten Bereich sind.</span><span class="sxs-lookup"><span data-stu-id="c9f91-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="c9f91-132">Weitere Informationen zum Einrichten von Zählern finden Sie unter [Zähler](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="c9f91-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

