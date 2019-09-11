---
title: Fehlermanagement
description: In diesem Thema wird das Fehlermanagement in der Anlagenverwaltung erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 48c90a8b776cc16804de8e20ada7d8ca347fa5b9
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874738"
---
# <a name="fault-management"></a><span data-ttu-id="fa059-103">Fehlermanagement</span><span class="sxs-lookup"><span data-stu-id="fa059-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fa059-104">In der Anlagenverwaltung können Sie den Fehlerdesigner verwenden, um Fehlersymptome, Fehlerbereiche und Fehlerarten für Anlagentypen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="fa059-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="fa059-105">Auf diese Weise können Sie Fehler verwalten, die bei Anlagen erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="fa059-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="fa059-106">Darüber hinaus können Fehlerursachen und Vorschläge für das Korrigieren von Fehlern für einen Arbeitsauftrag erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="fa059-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="fa059-107">Der Prozess für die Fehlererfassung und -verwaltung besteht aus folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="fa059-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="fa059-108">Erstellen einer Liste der Fehlersymptome, Fehlerbereiche und Fehlerarten, die bei Ihren Anlagentypen auftreten könnten.</span><span class="sxs-lookup"><span data-stu-id="fa059-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="fa059-109">Im Fehlerdesigner das Einrichten von Symptomen, Fehlerbereichen und Fehlerarten.</span><span class="sxs-lookup"><span data-stu-id="fa059-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="fa059-110">Unten sind einige Beispiele angegeben, mit deren Hilfe Sie den Unterschied zwischen Fehlersymptomen, Fehlerbereichen und Fehlerarten erkennen können.</span><span class="sxs-lookup"><span data-stu-id="fa059-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="fa059-111">**Fehlersymptome:**</span><span class="sxs-lookup"><span data-stu-id="fa059-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="fa059-112">Unausgeglichene Spannungen</span><span class="sxs-lookup"><span data-stu-id="fa059-112">Unbalanced voltages</span></span>
- <span data-ttu-id="fa059-113">Kurzschluss</span><span class="sxs-lookup"><span data-stu-id="fa059-113">Short circuit</span></span>
- <span data-ttu-id="fa059-114">Lärm</span><span class="sxs-lookup"><span data-stu-id="fa059-114">Noise</span></span>
- <span data-ttu-id="fa059-115">Leck</span><span class="sxs-lookup"><span data-stu-id="fa059-115">Leak</span></span>
- <span data-ttu-id="fa059-116">Erschütterungen</span><span class="sxs-lookup"><span data-stu-id="fa059-116">Vibrations</span></span>

<span data-ttu-id="fa059-117">**Fehlerbereiche:**</span><span class="sxs-lookup"><span data-stu-id="fa059-117">**Fault areas:**</span></span>

- <span data-ttu-id="fa059-118">Elektrisch</span><span class="sxs-lookup"><span data-stu-id="fa059-118">Electrical</span></span>
- <span data-ttu-id="fa059-119">Mechanisch</span><span class="sxs-lookup"><span data-stu-id="fa059-119">Mechanical</span></span>
- <span data-ttu-id="fa059-120">Hydraulisch</span><span class="sxs-lookup"><span data-stu-id="fa059-120">Hydraulic</span></span>
- <span data-ttu-id="fa059-121">Pneumatisch</span><span class="sxs-lookup"><span data-stu-id="fa059-121">Pneumatic</span></span>

<span data-ttu-id="fa059-122">**Fehlertypen:**</span><span class="sxs-lookup"><span data-stu-id="fa059-122">**Fault types:**</span></span>

- <span data-ttu-id="fa059-123">Fehlerhafte Hauptstatorwicklung</span><span class="sxs-lookup"><span data-stu-id="fa059-123">Faulty main stator winding</span></span>
- <span data-ttu-id="fa059-124">Fehlerhafte Diode</span><span class="sxs-lookup"><span data-stu-id="fa059-124">Faulty diode</span></span>
- <span data-ttu-id="fa059-125">Geänderte Wicklungen</span><span class="sxs-lookup"><span data-stu-id="fa059-125">Dirty windings</span></span>
- <span data-ttu-id="fa059-126">Fehlerhafter Generator</span><span class="sxs-lookup"><span data-stu-id="fa059-126">Defective generator</span></span>
- <span data-ttu-id="fa059-127">Fehlerhafter Sensor</span><span class="sxs-lookup"><span data-stu-id="fa059-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="fa059-128">Erstellen von Fehlersymptomen</span><span class="sxs-lookup"><span data-stu-id="fa059-128">Create fault symptoms</span></span>

<span data-ttu-id="fa059-129">Gehen Sie folgendermaßen vor, um eine Liste von Symptomen zu erstellen, die im Fehlerdesigner verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fa059-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="fa059-130">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlersymptome** aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="fa059-131">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa059-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="fa059-132">Geben Sie im Feld **Fehlersymptom** einen Namen für das Fehlersymptom ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="fa059-133">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="fa059-134">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fa059-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="fa059-135">Erstellen von Fehlerbereichen</span><span class="sxs-lookup"><span data-stu-id="fa059-135">Create fault areas</span></span>

<span data-ttu-id="fa059-136">Gehen Sie folgendermaßen vor, um eine Liste von Bereichen oder Standorten zu erstellen, die im Fehlerdesigner verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fa059-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="fa059-137">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlerbereiche** aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="fa059-138">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa059-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="fa059-139">Geben Sie im Feld **Fehlerbereich** einen Namen für den Fehlerbereich ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="fa059-140">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="fa059-141">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fa059-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="fa059-142">Fehlertypen erstellen</span><span class="sxs-lookup"><span data-stu-id="fa059-142">Create fault types</span></span>

<span data-ttu-id="fa059-143">Gehen Sie folgendermaßen vor, um eine Liste von Fehlertypen zu erstellen, die im Fehlerdesigner verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fa059-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="fa059-144">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlertypen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="fa059-145">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa059-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="fa059-146">Geben Sie im Feld **Fehlertyp** einen Namen für den Fehlertyp ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="fa059-147">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="fa059-148">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fa059-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="fa059-149">Einrichten des Fehlerdesigners</span><span class="sxs-lookup"><span data-stu-id="fa059-149">Set up the fault designer</span></span>

<span data-ttu-id="fa059-150">Im Fehlerdesigner richten Sie Fehlerdaten für Anlagentypen ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="fa059-151">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlerdesigner** aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="fa059-152">Wählen Sie im linken Bereich den Typ der Anlage aus, für die Sie einen Fehlerdatensatz einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="fa059-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="fa059-153">Wählen Sie im Inforegister **Fehlersymptom** **Position hinzufügen** und dann im Feld **Fehlersymptom** ein Fehlersymptom aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="fa059-154">Wählen Sie im Inforegister **Fehlerbereich** **Position hinzufügen** und dann im Feld **Fehlerbereich** einen Fehlerbereich aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="fa059-155">Wählen Sie im Inforegister **Fehlertyp** **Position hinzufügen** und dann im Feld **Fehlertyp** einen Fehlertyp aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="fa059-156">Um schnell Kombinationen aller vorhandenen Fehlersymptome, -bereiche und -typen für den ausgewählten Anlagetyp erstellen zu können, wählen Sie **Fehlerkombinationen erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="fa059-157">Diese Funktion ist hilfreich, wenn Sie viele Fehlersymptome, -bereiche und -typen hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="fa059-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="fa059-158">Es ist einfacher, die Positionen für beliebige Kombinationen zu löschen, die nicht für den Anlagentyp relevant sind, als neue Positionen manuell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa059-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa059-159">Um die Einstellungen von Fehlersymptomen, -bereichen und -typen von einem Anlagentyp in den ausgewählten Anlagentyp zu kopieren, wählen Sie **Aus Anlagentyp kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="fa059-160">Wählen Sie **Speichern** aus, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fa059-160">Select **Save** to save your changes.</span></span>

![Abbildung 1](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="fa059-162">Fehlerursachen erstellen</span><span class="sxs-lookup"><span data-stu-id="fa059-162">Create fault causes</span></span>

<span data-ttu-id="fa059-163">Gehen Sie folgendermaßen vor, um eine Liste bekannter Fehlerursachen zu erstellen, die einem Arbeitsauftrag oder einer Wartungsanforderung hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="fa059-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="fa059-164">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlerursachen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="fa059-165">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa059-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="fa059-166">Geben Sie im Feld **Fehlerursache** einen Namen für die Fehlerursache ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="fa059-167">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="fa059-168">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fa059-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="fa059-169">Erstellen von Fehlerlösungen</span><span class="sxs-lookup"><span data-stu-id="fa059-169">Create fault remedies</span></span>

<span data-ttu-id="fa059-170">Gehen Sie folgendermaßen vor, um eine Liste von Lösungs- und Reparaturvorschlägen zu erstellen, die einem Arbeitsauftrag oder einer Wartungsanforderung hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="fa059-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="fa059-171">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Fehler** \> **Fehlerlösungen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa059-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="fa059-172">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa059-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="fa059-173">Geben Sie im Feld **Fehlerlösung** einen Namen für die Fehlerlösung ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="fa059-174">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="fa059-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="fa059-175">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fa059-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="fa059-176">Sie können die Namen der Fehlersymptome, -bereiche, -typen, -ursachen und -lösungen nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="fa059-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="fa059-177">Die Namenänderungen werden automatisch in den betreffenden Fehlererfassungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa059-177">The name changes are automatically reflected in the related fault registrations.</span></span>