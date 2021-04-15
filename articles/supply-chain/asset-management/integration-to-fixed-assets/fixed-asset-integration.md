---
title: Anlagenverwaltung in Anlagen integrieren
description: In diesem Thema wird erläutert, wie Sie die Module Anlagenverwaltung und Anlagevermögen integrieren, damit Sie Sachanlagen mit Wartungsanlagen verknüpfen können.
author: kamaybac
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a45bf1f62cdcc8abed2ec157a223e7f3fddec7ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809853"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="ea08d-103">Anlagenverwaltung in Anlagen integrieren</span><span class="sxs-lookup"><span data-stu-id="ea08d-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea08d-104">Indem Sie die Module **Anlagenverwaltung** und **Anlagevermögen** integrieren, können Sie Sachanlagen mit Wartungsanlagen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="ea08d-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="ea08d-105">Benutzer von Anlagevermögen können dann ein Wartungsobjekt aus einem neuen oder vorhandenen Anlagevermögen erstellen, und Benutzer der Vermögensverwaltung können ein Wartungsobjekt einem vorhandenen Anlagevermögen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="ea08d-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="ea08d-106">Diese Funktion erleichtert es Benutzern von Anlagevermögen auch, die Kosten anzuzeigen, die aus Arbeitsaufträgen für zugehörige Wartungsanlagen gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="ea08d-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="ea08d-107">In diesem Thema bezeichnen *Wartungsanlagen* Vermögenswerte aus dem Modul **Anlagenverwaltung** und *Anlagevermögen* bezieht sich auf Vermögenswerte aus dem Modul **Anlagevermögen**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="ea08d-108">Legen Sie einen Standardspeicherort für neue Wartungsressourcen fest, die aus dem Anlagevermögen erstellt werden (optional).</span><span class="sxs-lookup"><span data-stu-id="ea08d-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="ea08d-109">Durch diese optionale Konfiguration können Sie einen funktionalen Standardspeicherort für neue Wartungsanlagen festlegen, die aus dem Anlagevermögen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ea08d-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="ea08d-110">Normalerweise schließen Sie diese Konfiguration nur einmal ab, wenn Sie sie überhaupt abschließen.</span><span class="sxs-lookup"><span data-stu-id="ea08d-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="ea08d-111">Führen Sie zum Abschließen dieser Konfiguration die folgenden Schritte durch.</span><span class="sxs-lookup"><span data-stu-id="ea08d-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="ea08d-112">Wechseln Sie zu **Anlagenverwaltung \> Einstellungen \> Anlagenverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="ea08d-113">Wählen Sie auf der Registerkarte **Anlagen** im Feld **Funktionaler Standort** den Standardlagerplatz aus, der für Fertigerzeugnisse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea08d-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="ea08d-114">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="ea08d-115">Arbeiten mit integrierten Wartungsanlagen und Sachanlagen</span><span class="sxs-lookup"><span data-stu-id="ea08d-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="ea08d-116">Dieser Abschnitt enthält eine Sammlung von Verfahren, die verschiedene Möglichkeiten zeigen, wie Sie mit den integrierten Funktionen Anlageverwaltung und Anlagevermögen arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="ea08d-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="ea08d-117">Verknüpfen Sie ein vorhandenes Wartungsobjekt mit einem Anlagevermögen</span><span class="sxs-lookup"><span data-stu-id="ea08d-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="ea08d-118">Um ein vorhandenes Wartungsobjekt mit einem Anlagevermögen zu verknüpfen, folgen Sie den Schritten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="ea08d-119">Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).</span><span class="sxs-lookup"><span data-stu-id="ea08d-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="ea08d-120">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-120">Select an asset.</span></span>
1. <span data-ttu-id="ea08d-121">Auf dem Inforegister **Anlage** im Feld **Anlagennummer** wählen Sie eine vorhandene Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="ea08d-122">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="ea08d-123">Zeigen Sie die Anlage an, die einer ausgewählten Wartungsanlage zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="ea08d-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="ea08d-124">Um die Anlage anzuzeigen, die einer ausgewählten Wartungsanlage zugeordnet ist, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="ea08d-125">Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).</span><span class="sxs-lookup"><span data-stu-id="ea08d-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="ea08d-126">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-126">Select an asset.</span></span>
1. <span data-ttu-id="ea08d-127">Auf dem Inforegister **Anlage** im Feld **Anlagennummer** wählen Sie den Link aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="ea08d-128">Die Seite **Anlage** für die ausgewählte Anlage wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ea08d-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="ea08d-129">(Normalerweise befindet sich diese Seite unter **Anlagen \> Anlagen \> Anlagen**.)</span><span class="sxs-lookup"><span data-stu-id="ea08d-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="ea08d-130">Zeigen Sie die Wartungsanlage an, die einer ausgewählten Anlage zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="ea08d-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="ea08d-131">Um die Wartungsanlage anzuzeigen, die einer ausgewählten Anlage zugeordnet ist, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="ea08d-132">Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="ea08d-133">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-133">Select an asset.</span></span>
1. <span data-ttu-id="ea08d-134">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Ansicht** die Option **Wartungsanlage**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="ea08d-135">Die Seite **Wartungsanlage** für die Anlage, die einer ausgewählten Anlage zugeordnet ist, wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ea08d-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="ea08d-136">(Normalerweise befindet sich diese Seite unter **Anlagenverwaltung \> Anlagen \> Alle Anlagen** .)</span><span class="sxs-lookup"><span data-stu-id="ea08d-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="ea08d-137">Zeigen Sie Wartungskosten an, die mit einer Anlage verbunden sind</span><span class="sxs-lookup"><span data-stu-id="ea08d-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="ea08d-138">Anlagenverwaltungs-Arbeitsaufträge können für Wartungsanlagen gebucht werden, und jeder dieser Arbeitsaufträge hat normalerweise Kosten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="ea08d-139">Wenn eine Anlage einer Wartungsanlage zugeordnet ist, können Sie direkt von der Anlage aus die entsprechenden Kosten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ea08d-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="ea08d-140">Um die Wartungskosten anzuzeigen, die einer ausgewählten Anlage zugeordnet sind, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="ea08d-141">Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="ea08d-142">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-142">Select an asset.</span></span>
1. <span data-ttu-id="ea08d-143">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Ansicht** die Option **Wartungskosten**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="ea08d-144">Die Seite **Wartungskosten** wird geöffnet und zeigt die damit verbundenen Kosten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="ea08d-145">Erstellen einer neuen Wartungsanlage für eine bestehende Anlage</span><span class="sxs-lookup"><span data-stu-id="ea08d-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="ea08d-146">Um eine neue Wartungsanlage für eine Anlage zu erstellen, folgen Sie den Schritten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="ea08d-147">Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="ea08d-148">Wählen Sie eine Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-148">Select an asset.</span></span>
1. <span data-ttu-id="ea08d-149">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Neu** die Option **Wartungsanlage erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="ea08d-150">(Wenn diese Option nicht verfügbar ist, ist der ausgewählten Anlage möglicherweise bereits ein Wartungsobjekt zugeordnet.)</span><span class="sxs-lookup"><span data-stu-id="ea08d-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="ea08d-151">Beenden Sie die Erstellung der Anlage wie in [Eine Anlage erstellen](../objects/create-an-object.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea08d-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="ea08d-152">Erstellen Sie eine neue Anlage und eine neue Wartungsanlage dafür</span><span class="sxs-lookup"><span data-stu-id="ea08d-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="ea08d-153">Um eine neue Anlage zu erstellen und eine neue Wartungsanlage dafür hinzuzufügen, folgen Sie den Schritten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="ea08d-154">Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="ea08d-155">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ea08d-156">Beenden Sie die Erstellung der Anlage wie in [Anlage erstellen](../../../finance/fixed-assets/tasks/create-fixed-asset.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea08d-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="ea08d-157">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Neu** die Option **Wartungsanlage erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="ea08d-158">Beenden Sie die Erstellung der Anlage wie in [Eine Anlage erstellen](../objects/create-an-object.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea08d-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="ea08d-159">Entfernen Sie die Zuordnung zwischen zwei Anlagen</span><span class="sxs-lookup"><span data-stu-id="ea08d-159">Remove the association between two assets</span></span>

<span data-ttu-id="ea08d-160">In einigen Fällen müssen Sie möglicherweise eine Wartungsanlage von der Anlage trennen.</span><span class="sxs-lookup"><span data-stu-id="ea08d-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="ea08d-161">Zum Beispiel, wenn Sie [ein neues Wartungsobjekt](#new-maintenance-from-fixed) aus einer Anlage erstellen möchten, müssen Sie zuerst eine vorhandene Zuordnung entfernen.</span><span class="sxs-lookup"><span data-stu-id="ea08d-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="ea08d-162">Um eine vorhandene Zuordnung zwischen einer Wartungsanlage und einer Anlage zu entfernen, folgen Sie den Schritten.</span><span class="sxs-lookup"><span data-stu-id="ea08d-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="ea08d-163">Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).</span><span class="sxs-lookup"><span data-stu-id="ea08d-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="ea08d-164">Suchen und öffnen Sie die Anlage.</span><span class="sxs-lookup"><span data-stu-id="ea08d-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="ea08d-165">Auf dem Inforegister **Anlage** löschen Sie den Wert aus dem Feld **Funktionaler Standort**.</span><span class="sxs-lookup"><span data-stu-id="ea08d-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="ea08d-166">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ea08d-166">On the Action Pane, select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]