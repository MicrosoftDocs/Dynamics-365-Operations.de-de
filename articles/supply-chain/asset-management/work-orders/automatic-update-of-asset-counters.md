---
title: Die automatische Aktualisierung von Anlagenzählern
description: In diesem Thema wird die automatische Aktualisierung von Anlagenzählern in Asset Management beschrieben.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcc46fad8d57b7d4d57edfa4f2ae06de923d1c14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428525"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="5b7e0-103">Die automatische Aktualisierung von Anlagenzählern</span><span class="sxs-lookup"><span data-stu-id="5b7e0-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b7e0-104">Informationen zur manuellen Erfassung von Anlagenzählern finden Sie unter [Manuelle Aktualisierung der Anlagenzähler](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="5b7e0-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="5b7e0-105">Informationen zum Einrichten von Anlagenzählern finden Sie unter [Zähler](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="5b7e0-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="5b7e0-106">Zählerwerte können auch aus Produktionserfassungen automatisch aktualisiert werden, die auf Produktionsstunden oder Produktionsmenge basieren (d. h. der produzierten Menge).</span><span class="sxs-lookup"><span data-stu-id="5b7e0-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="5b7e0-107">Die Aktualisierung wird auf der Seite **Anlagenzähler aktualisieren** ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="5b7e0-108">Sie können eine oder mehrere Anlagen aktualisieren, indem Sie den Parameter **Von Datum** festlegen.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="5b7e0-109">Dieser Parameter gibt das Startdatum für Produktionserfassungen an (Produktionsstunden oder Produktionsmengen).</span><span class="sxs-lookup"><span data-stu-id="5b7e0-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="5b7e0-110">Das bedeutet, er gibt das Datum an, ab dem die Zählerwerte aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="5b7e0-111">Alle Anlagen, die einer Ressource zugeordnet sind *und* Anlagenzähler enthalten, die so eingerichtet wurden, das sie basierend auf den Produktionsstunden oder der Produktionsmenge aktualisiert werden, werden in einer automatischen Aktualisierung berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="5b7e0-112">Neue Zählerwerte werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-112">New counter values will be created.</span></span>

<span data-ttu-id="5b7e0-113">Für Zähler, die auf der Produktionsmenge basieren, umfasst die Anzahl sowohl die Gutmenge als auch die Ausschussmenge, die erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="5b7e0-114">Wenn die Einheit, die für die Erfassung der Produktionsmenge verwendet wird, sich von der Einheit unterscheidet, die für den Zähler verwendet wird, wird die Menge konvertiert, um der Zählereinheit zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="5b7e0-115">Wie bereits angegeben können automatische Zähler aus Produktionserfassungen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="5b7e0-116">Daher muss die Anlage, für die Sie automatisch Zähler aktualisieren möchten, einer Ressource (Maschine) zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="5b7e0-117">Bei produzierte Mengen oder Produktionsstunden für die Ressource erfasst wurden, können Sie die zugehörigen Anlagenzähler aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="5b7e0-118">Wählen Sie **Anlagenverwaltung** > **Periodisch** > **Anlagen** > **Anlagenzähler aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="5b7e0-119">Wählen Sie im Feld **Von Datum** das Startdatum der automatischen Aktualisierung aus.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="5b7e0-120">Das Datum in diesem Feld ist das Datum „In Bearbeitung“ aus **Arbeitsplanbuchungen** (Feld **Produktionssteuerung** > **Abfragen und Berichte** > **Produktion** > **Arbeitsplanbuchungen** > **Physisches Datum**).</span><span class="sxs-lookup"><span data-stu-id="5b7e0-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="5b7e0-121">Auf dem Inforegister **Einzuschließende Datensätze** können Sie bestimmte Anlagen, Anlagentypen oder Ressourcen für die automatische Aktualisierung auswählen.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="5b7e0-122">Wählen Sie **Filtern** aus und treffen Sie die zutreffende Auswahl.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="5b7e0-123">Im Inforegister **Im Hintergrund ausführen** können Sie die automatische Aktualisierung bei Bedarf als Batchauftrag einrichten.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="5b7e0-124">In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Anlagenzähler aktualisieren** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![Abbildung 1](media/12-work-orders.png)

5. <span data-ttu-id="5b7e0-126">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-126">Select **OK**.</span></span> 

<span data-ttu-id="5b7e0-127">Wenn die automatische Aktualisierung von Anlagenzählern erfolgt ist, können Sie die Zählererfassungen anzeigen, die auf die Anlage auf der Seite **Anlagenzähler** bezogen sind.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="5b7e0-128">Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Anlagen** > **Alle Anlagen** aus, wählen Sie die Anlage aus, und wählen Sie dann im Aktivitätsbereich auf der **Anlage**-Registerkarte in der Gruppe **Vorbeugend** **Zähler** aus.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="5b7e0-129">Auf der Seite **Aggregierter Wert für Anlage** können Sie einen Überblick der letzten Erfassung abrufen, die für alle Zählertypen für alle Anlagen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="5b7e0-130">Wählen Sie **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Aggregierter Wert für Anlage** aus.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="5b7e0-131">Diese Seite ähnelt der Seite **Anlagenzähler**, Sie können jedoch keine Erfassungen hinzufügen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="5b7e0-132">Es ist nur für den Überblick.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-132">It's for overview only.</span></span>

<span data-ttu-id="5b7e0-133">In der folgenden Abbildung wird ein Beispiel der Seite **Aggregierter Wert für Anlage** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Abbildung 2](media/13-work-orders.png)

<span data-ttu-id="5b7e0-135">Beachten Sie die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="5b7e0-135">Note the following points:</span></span>

- <span data-ttu-id="5b7e0-136">Es ist trotzdem möglich, manuelle Zählerwerterfassungen für Zählertypen zu erstellen, die automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="5b7e0-137">Weitere Informationen finden Sie unter [Manuelle Aktualisierung von Anlagenzählern](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="5b7e0-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="5b7e0-138">Sie können Zähler einrichten, die einem anderen Zähler zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="5b7e0-139">In diesem Fall, wenn ein Zähler aktualisiert wird, werden zugehörige Zähler automatisch gleichzeitig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5b7e0-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="5b7e0-140">Weitere Informationen zum Einrichten von zugehörigen Zählern finden Sie unter [Zähler](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="5b7e0-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

