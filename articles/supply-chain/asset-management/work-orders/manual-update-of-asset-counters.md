---
title: Manuelle Aktualisierung der Anlagenzähler
description: Dieses Thema beschreibt die manuelle Aktualisierung von Anlagenzählern im Anlagenmanagement.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875674"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="e54ca-103">Manuelle Aktualisierung der Anlagenzähler</span><span class="sxs-lookup"><span data-stu-id="e54ca-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="e54ca-104">Zähler werden verwendet, um Registrierungen auf einer Anlage zu erstellen, z.B. hinsichtlich der Anzahl der Betriebsstunden oder der Anzahl der produzierten Mengen.</span><span class="sxs-lookup"><span data-stu-id="e54ca-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="e54ca-105">Wenn der für einen Zähler ausgewählte Zählertyp auf Vererbung von Zählerwerten eingestellt ist (**Anlagenmanagement** > **Einrichtung** > **Anlagentypen** > **Zähler** > **Allgemein** FastTab > **Anlagenzählerwerte vererben** Umschalttaste auf „Ja“ gesetzt), Wenn Sie dann eine neue Gegenzeile dieses Typs erstellen, wird jede untergeordnete Kühlstelle, die den gleichen Zählertyp verwendet, automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e54ca-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="e54ca-106">Unter **Alle Anlagen** erstellen Sie Stunden- oder Mengenzählerregistrierungen für eine Anlage, basierend auf Ihren Messwerten für die Anlage.</span><span class="sxs-lookup"><span data-stu-id="e54ca-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="e54ca-107">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Anlagen** > **Alle Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="e54ca-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="e54ca-108">Wählen Sie das Objekt in der Liste aus und klicken Sie auf **Zähler**.</span><span class="sxs-lookup"><span data-stu-id="e54ca-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="e54ca-109">Im Formular **Anlagenzähler** sehen Sie eine Liste aller früheren Zählerregistrierungen für die ausgewählte Anlage.</span><span class="sxs-lookup"><span data-stu-id="e54ca-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="e54ca-110">Klicken Sie auf **Neu**, um eine neue Registrierung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e54ca-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="e54ca-111">Die Asset-ID wird automatisch eingefügt.</span><span class="sxs-lookup"><span data-stu-id="e54ca-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="e54ca-112">Wählen Sie im Feld **Zähler** den entsprechenden Zähler aus.</span><span class="sxs-lookup"><span data-stu-id="e54ca-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="e54ca-113">Es sind nur Zähler verfügbar, die sich auf die auf der Anlage ausgewählte Anlagenart beziehen.</span><span class="sxs-lookup"><span data-stu-id="e54ca-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="e54ca-114">Die zugehörige Einheit wird automatisch in das Feld **Einheit** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="e54ca-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="e54ca-115">Wählen Sie Datum und Uhrzeit für die Zählerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="e54ca-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="e54ca-116">Geben Sie in das Feld **Wert** die Nummer seit der letzten Zählerregistrierung ein oder geben Sie im Feld **Aggregierter Wert** die Gesamtzählnummer ein.</span><span class="sxs-lookup"><span data-stu-id="e54ca-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="e54ca-117">Wenn Sie einen neuen Zähler physisch auf einer Anlage installieren, müssen Sie die Änderung auf der Anlage in **Anlagenzähler** registrieren.</span><span class="sxs-lookup"><span data-stu-id="e54ca-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="e54ca-118">Als nächstes müssen Sie zwei Registrierungszeilen mit identischen Zeitstempeln erstellen, und auf der Zeile mit dem neuen Zähler aktivieren Sie das Kontrollkästchen **Zähler zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="e54ca-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="e54ca-119">Wenn Sie die beiden Registrierungszeilen anlegen, muss die erste Zeile für den Zähler sein, den Sie ersetzen.</span><span class="sxs-lookup"><span data-stu-id="e54ca-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="e54ca-120">Im Feld **Summen** ist die Gesamtzahl die Summe der Zählersumme aller registrierten Werte auf diesem Zählertyp.</span><span class="sxs-lookup"><span data-stu-id="e54ca-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="e54ca-121">Wenn das Kontrollkästchen **Zählerrückstellung** bei einer Anlage mit einem Wartungsplan mit Intervalltyp „Einmal von...“ oder „Einmal erreicht...“ aktiviert ist, ist der Zähler auf der neuen Zählerzeile weiterhin aktiv, da Sie eine separate Zählerzeile erstellen und mit einem neuen Zähler neu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e54ca-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Abbildung 1](media/11-work-orders.png)


<span data-ttu-id="e54ca-123">Wenn Sie für mehrere Anlagen Gegenregistrierungen vornehmen müssen, kann dies in **Anlagenmanagement** > **Anfragen** > **Anlagen** > **Anlagenzähler** erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e54ca-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="e54ca-124">Sie können einen Bereich einrichten, um Abweichungen bei manuellen Zählerregistrierungen zu definieren, und die Art der Meldung, die angezeigt werden soll, wenn Registrierungen außerhalb des definierten Bereichs liegen.</span><span class="sxs-lookup"><span data-stu-id="e54ca-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="e54ca-125">Lesen Sie das Thema [Zähler](../setup-for-objects/counters.md) zur Einrichtung von Zählern.</span><span class="sxs-lookup"><span data-stu-id="e54ca-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
