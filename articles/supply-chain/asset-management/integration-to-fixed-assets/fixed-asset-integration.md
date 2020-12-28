---
title: Anlagenverwaltung in Anlagen integrieren
description: In diesem Thema wird erläutert, wie Sie die Module Anlagenverwaltung und Anlagevermögen integrieren, damit Sie Sachanlagen mit Wartungsanlagen verknüpfen können.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428594"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="94e55-103">Anlagenverwaltung in Anlagen integrieren</span><span class="sxs-lookup"><span data-stu-id="94e55-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="94e55-104">Indem Sie die Module **Anlagenverwaltung** und **Anlagevermögen** integrieren, können Sie Sachanlagen mit Wartungsanlagen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="94e55-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="94e55-105">Benutzer von Anlagevermögen können dann ein Wartungsobjekt aus einem neuen oder vorhandenen Anlagevermögen erstellen, und Benutzer der Vermögensverwaltung können ein Wartungsobjekt einem vorhandenen Anlagevermögen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="94e55-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="94e55-106">Diese Funktion erleichtert es Benutzern von Anlagevermögen auch, die Kosten anzuzeigen, die aus Arbeitsaufträgen für zugehörige Wartungsanlagen gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="94e55-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="94e55-107">In diesem Thema bezeichnen *Wartungsanlagen* Vermögenswerte aus dem Modul **Anlagenverwaltung** und *Anlagevermögen* bezieht sich auf Vermögenswerte aus dem Modul **Anlagevermögen**.</span><span class="sxs-lookup"><span data-stu-id="94e55-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="94e55-108">Legen Sie einen Standardspeicherort für neue Wartungsressourcen fest, die aus dem Anlagevermögen erstellt werden (optional).</span><span class="sxs-lookup"><span data-stu-id="94e55-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="94e55-109">Durch diese optionale Konfiguration können Sie einen funktionalen Standardspeicherort für neue Wartungsanlagen festlegen, die aus dem Anlagevermögen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="94e55-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="94e55-110">Normalerweise schließen Sie diese Konfiguration nur einmal ab, wenn Sie sie überhaupt abschließen.</span><span class="sxs-lookup"><span data-stu-id="94e55-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="94e55-111">Führen Sie zum Abschließen dieser Konfiguration die folgenden Schritte durch.</span><span class="sxs-lookup"><span data-stu-id="94e55-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="94e55-112">Wechseln Sie zu **Anlagenverwaltung \> Einstellungen \> Anlagenverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="94e55-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="94e55-113">Wählen Sie auf der Registerkarte **Anlagen** im Feld **Funktionaler Standort** den Standardlagerplatz aus, der für Fertigerzeugnisse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="94e55-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="94e55-114">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="94e55-115">Arbeiten mit integrierten Wartungsanlagen und Sachanlagen</span><span class="sxs-lookup"><span data-stu-id="94e55-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="94e55-116">Dieser Abschnitt enthält eine Sammlung von Verfahren, die verschiedene Möglichkeiten zeigen, wie Sie mit den integrierten Funktionen Anlageverwaltung und Anlagevermögen arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="94e55-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="94e55-117">Verknüpfen Sie ein vorhandenes Wartungsobjekt mit einem Anlagevermögen</span><span class="sxs-lookup"><span data-stu-id="94e55-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="94e55-118">Um ein vorhandenes Wartungsobjekt mit einem Anlagevermögen zu verknüpfen, folgen Sie den Schritten.</span><span class="sxs-lookup"><span data-stu-id="94e55-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="94e55-119">Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).</span><span class="sxs-lookup"><span data-stu-id="94e55-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="94e55-120">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-120">Select an asset.</span></span>
1. <span data-ttu-id="94e55-121">Auf dem Inforegister **Anlage** im Feld **Anlagennummer** wählen Sie eine vorhandene Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="94e55-122">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="94e55-123">Zeigen Sie die Anlage an, die einer ausgewählten Wartungsanlage zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="94e55-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="94e55-124">Um die Anlage anzuzeigen, die einer ausgewählten Wartungsanlage zugeordnet ist, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="94e55-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="94e55-125">Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).</span><span class="sxs-lookup"><span data-stu-id="94e55-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="94e55-126">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-126">Select an asset.</span></span>
1. <span data-ttu-id="94e55-127">Auf dem Inforegister **Anlage** im Feld **Anlagennummer** wählen Sie den Link aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="94e55-128">Die Seite **Anlage** für die ausgewählte Anlage wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="94e55-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="94e55-129">(Normalerweise befindet sich diese Seite unter **Anlagen \> Anlagen \> Anlagen**.)</span><span class="sxs-lookup"><span data-stu-id="94e55-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="94e55-130">Zeigen Sie die Wartungsanlage an, die einer ausgewählten Anlage zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="94e55-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="94e55-131">Um die Wartungsanlage anzuzeigen, die einer ausgewählten Anlage zugeordnet ist, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="94e55-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="94e55-132">Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="94e55-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="94e55-133">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-133">Select an asset.</span></span>
1. <span data-ttu-id="94e55-134">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Ansicht** die Option **Wartungsanlage**.</span><span class="sxs-lookup"><span data-stu-id="94e55-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="94e55-135">Die Seite **Wartungsanlage** für die Anlage, die einer ausgewählten Anlage zugeordnet ist, wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="94e55-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="94e55-136">(Normalerweise befindet sich diese Seite unter **Anlagenverwaltung \> Anlagen \> Alle Anlagen** .)</span><span class="sxs-lookup"><span data-stu-id="94e55-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="94e55-137">Zeigen Sie Wartungskosten an, die mit einer Anlage verbunden sind</span><span class="sxs-lookup"><span data-stu-id="94e55-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="94e55-138">Anlagenverwaltungs-Arbeitsaufträge können für Wartungsanlagen gebucht werden, und jeder dieser Arbeitsaufträge hat normalerweise Kosten.</span><span class="sxs-lookup"><span data-stu-id="94e55-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="94e55-139">Wenn eine Anlage einer Wartungsanlage zugeordnet ist, können Sie direkt von der Anlage aus die entsprechenden Kosten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="94e55-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="94e55-140">Um die Wartungskosten anzuzeigen, die einer ausgewählten Anlage zugeordnet sind, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="94e55-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="94e55-141">Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="94e55-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="94e55-142">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-142">Select an asset.</span></span>
1. <span data-ttu-id="94e55-143">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Ansicht** die Option **Wartungskosten**.</span><span class="sxs-lookup"><span data-stu-id="94e55-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="94e55-144">Die Seite **Wartungskosten** wird geöffnet und zeigt die damit verbundenen Kosten.</span><span class="sxs-lookup"><span data-stu-id="94e55-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="94e55-145">Erstellen einer neuen Wartungsanlage für eine bestehende Anlage</span><span class="sxs-lookup"><span data-stu-id="94e55-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="94e55-146">Um eine neue Wartungsanlage für eine Anlage zu erstellen, folgen Sie den Schritten.</span><span class="sxs-lookup"><span data-stu-id="94e55-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="94e55-147">Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="94e55-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="94e55-148">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-148">Select an asset.</span></span>
1. <span data-ttu-id="94e55-149">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Neu** die Option **Wartungsanlage erstellen**.</span><span class="sxs-lookup"><span data-stu-id="94e55-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="94e55-150">(Wenn diese Option nicht verfügbar ist, ist der ausgewählten Anlage möglicherweise bereits ein Wartungsobjekt zugeordnet.)</span><span class="sxs-lookup"><span data-stu-id="94e55-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="94e55-151">Beenden Sie die Erstellung der Anlage wie in [Eine Anlage erstellen](../objects/create-an-object.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="94e55-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="94e55-152">Erstellen Sie eine neue Anlage und eine neue Wartungsanlage dafür</span><span class="sxs-lookup"><span data-stu-id="94e55-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="94e55-153">Um eine neue Anlage zu erstellen und eine neue Wartungsanlage dafür hinzuzufügen, folgen Sie den Schritten.</span><span class="sxs-lookup"><span data-stu-id="94e55-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="94e55-154">Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="94e55-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="94e55-155">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="94e55-156">Beenden Sie die Erstellung der Anlage wie in [Anlage erstellen](../../../finance/fixed-assets/tasks/create-fixed-asset.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="94e55-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="94e55-157">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Neu** die Option **Wartungsanlage erstellen**.</span><span class="sxs-lookup"><span data-stu-id="94e55-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="94e55-158">Beenden Sie die Erstellung der Anlage wie in [Eine Anlage erstellen](../objects/create-an-object.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="94e55-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="94e55-159">Entfernen Sie die Zuordnung zwischen zwei Anlagen</span><span class="sxs-lookup"><span data-stu-id="94e55-159">Remove the association between two assets</span></span>

<span data-ttu-id="94e55-160">In einigen Fällen müssen Sie möglicherweise eine Wartungsanlage von der Anlage trennen.</span><span class="sxs-lookup"><span data-stu-id="94e55-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="94e55-161">Zum Beispiel, wenn Sie [ein neues Wartungsobjekt](#new-maintenance-from-fixed) aus einer Anlage erstellen möchten, müssen Sie zuerst eine vorhandene Zuordnung entfernen.</span><span class="sxs-lookup"><span data-stu-id="94e55-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="94e55-162">Um eine vorhandene Zuordnung zwischen einer Wartungsanlage und einer Anlage zu entfernen, folgen Sie den Schritten.</span><span class="sxs-lookup"><span data-stu-id="94e55-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="94e55-163">Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).</span><span class="sxs-lookup"><span data-stu-id="94e55-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="94e55-164">Suchen und öffnen Sie die Anlage.</span><span class="sxs-lookup"><span data-stu-id="94e55-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="94e55-165">Auf dem Inforegister **Anlage** löschen Sie den Wert aus dem Feld **Funktionaler Standort**.</span><span class="sxs-lookup"><span data-stu-id="94e55-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="94e55-166">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="94e55-166">On the Action Pane, select **Save**.</span></span>
