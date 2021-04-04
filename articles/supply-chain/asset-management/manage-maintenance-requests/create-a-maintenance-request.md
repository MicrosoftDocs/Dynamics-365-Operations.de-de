---
title: Wartungsanfragen erstellen
description: In diesem Thema wird erläutert, wie Wartungsanfragen in der Anlagenverwaltung erstellt werden.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a85125853b3b69d33f07249e0d2aa7592de1cc8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253421"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="8596e-103">Wartungsanfragen erstellen</span><span class="sxs-lookup"><span data-stu-id="8596e-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8596e-104">Wartungsanfragen können verwendet werden, wenn Wartungsarbeiter oder Produktionsarbeitskräfte bemerken, dass Maschinen eine Reparatur erfordern, die Reparaturarbeiten aber nicht sofort ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="8596e-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="8596e-105">**Beispiel:** Während eine Wartungsarbeiterin eine Reparatur durchführt, stellt sie fest, dass eine andere Anlage am gleichen Standort gewartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="8596e-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="8596e-106">Die Wartungsarbeiterin hat jedoch nicht die Zeit oder erforderlichen Ersatzteile, um die Reparatur durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8596e-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="8596e-107">Aus diesem Grund erstellt sie eine Wartungsanfrage für die Anlage und gibt eine kurze Beschreibung des Problems ein.</span><span class="sxs-lookup"><span data-stu-id="8596e-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="8596e-108">Der Abschnitt **Aktive Wartungsanfragen** des Bereichs **Zugehörige Informationen** rechts auf der Seite **Alle Anlagen** oder **Aktive Anlagen** (**Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen** oder **Aktive Anlagen**) enthält die aktiven Wartungsanfragen, die der ausgewählten Anlage zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8596e-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="8596e-109">Wählen Sie **Anlagenverwaltung** \> **Allgemein** \> **Wartungsanfragen** \> **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** aus.</span><span class="sxs-lookup"><span data-stu-id="8596e-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="8596e-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8596e-110">Select **New**.</span></span>
3. <span data-ttu-id="8596e-111">Wählen Sie im Dialogfeld **Anforderung erstellen** im Feld **Wartungsanfragetyp** den Typ der Wartungsanfrage aus.</span><span class="sxs-lookup"><span data-stu-id="8596e-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="8596e-112">Ein Standardtyp wird vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="8596e-112">A default type is suggested.</span></span>
4. <span data-ttu-id="8596e-113">Geben Sie im Feld **Beschreibung** einen Namen oder einen Titel ein, der die Wartungsanfrage kurz beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8596e-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="8596e-114">Wählen Sie in den Feldern **Funktionaler Standort** und **Anlage** einen funktionalen Standort oder eine Anlage oder eine Kombination eines funktionalen Standorts und einer Anlage aus (je nach Anforderung).</span><span class="sxs-lookup"><span data-stu-id="8596e-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="8596e-115">Sie können eine Wartungsanfrage erstellen, ohne eine Anlage auszuwählen, und die Anlage kann der Wartungsanfrage erst später hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8596e-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="8596e-116">Wenn der Wartungsarbeiter, der angemeldet ist, einer Ressource zugeordnet ist, die zu einer Anlage gehört, wird das Feld **Anlage** automatisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8596e-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="8596e-117">Wenn der ausgewählten Anlage bereits eine Wartungsanfrage zugeordnet ist, wird oben im Dialogfeld **Anforderung erstellen** eine Meldungsleiste angezeigt, Sie Ihnen die Kennung der Wartungsanfrage mitteilt.</span><span class="sxs-lookup"><span data-stu-id="8596e-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="8596e-118">Eine Meldungsleiste informiert Sie auch darüber, wenn die Anlage von einer Garantievereinbarung abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="8596e-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="8596e-119">Wählen Sie im Feld **Leistungsebene** eine Leistungsebene aus, die die Dringlichkeit der Anforderung angibt.</span><span class="sxs-lookup"><span data-stu-id="8596e-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="8596e-120">Wenn Sie in Schritt 5 eine Anlage ausgewählt haben, können Sie die Felder **Fehlersymptom**, **Fehlerbereich** und **Fehlertyp** verwenden, um eine Fehlererfassung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8596e-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="8596e-121">Wenn die Wartungsanfrage eine Wartungsausfallzeit verursacht hat, geben Sie Startdatum und -zeit der Ausfallzeit ein.</span><span class="sxs-lookup"><span data-stu-id="8596e-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="8596e-122">Im Feld **Gestartet von** wird automatisch Ihr Name eingetragen.</span><span class="sxs-lookup"><span data-stu-id="8596e-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="8596e-123">Das Feld **Tatsächlicher Start** wird automatisch auf das aktuelle Datum und die aktuelle Uhrzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8596e-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="8596e-124">Allerdings können Sie den Wert in diesem Feld ändern.</span><span class="sxs-lookup"><span data-stu-id="8596e-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="8596e-125">Geben Sie im Feld **Hinweise** zusätzliche Hinweise ein, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8596e-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="8596e-126">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8596e-126">Select **OK**.</span></span>

![Wartungsanfrage erstellen](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="8596e-128">Nachfolgende Verarbeitung von Wartungsanfragen</span><span class="sxs-lookup"><span data-stu-id="8596e-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="8596e-129">Nachdem eine Wartungsanfrage erstellt wurde – jedoch bevor sie in einen Arbeitsauftrag umgewandelt wird –, sollten in der Anforderung verschiedene Informationen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8596e-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="8596e-130">Normalerweise wird diese Aufgabe von einem Planer oder einem anderen Sachbearbeiter erledigt.</span><span class="sxs-lookup"><span data-stu-id="8596e-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="8596e-131">Wählen Sie auf der Seite **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** die Anforderung aus, mit der gearbeitet werden soll. Wählen Sie dann **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8596e-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="8596e-132">In der Detailansicht können Sie verschiedene Informationen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8596e-132">In the details view, you can update various information.</span></span> <span data-ttu-id="8596e-133">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="8596e-133">Here are some examples:</span></span>

- <span data-ttu-id="8596e-134">Wählen Sie die Anlage aus, und überprüfen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="8596e-134">Select and verify the asset.</span></span> <span data-ttu-id="8596e-135">Wenn Sie später eine andere Anlage auswählen müssen, können Sie die Option **Anlage geprüft** auf **Nein** festlegen.</span><span class="sxs-lookup"><span data-stu-id="8596e-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="8596e-136">Wählen Sie eine zuständige Wartungsarbeitergruppe und/oder einen zuständigen Wartungsarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="8596e-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="8596e-137">Weitere Informationen zu den erforderlichen Einstellungen finden Sie unter [Zuständige Wartungsarbeitskräfte](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="8596e-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="8596e-138">Wählen Sie einen Wartungsauftragstyp aus. Wenn diese Information relevant ist, wählen Sie auch eine zugehörige Wartungsauftragsvariante und eine Facharbeit aus.</span><span class="sxs-lookup"><span data-stu-id="8596e-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="8596e-139">Geben Sie in den Feldern **Breitengrad** und **Längengrad** die geografischen Koordinaten ein.</span><span class="sxs-lookup"><span data-stu-id="8596e-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="8596e-140">Sämtliche Koordinaten, die einer Wartungsanfrage hinzugefügt werden, werden automatisch an einen zugehörigen Arbeitsauftrag übertragen.</span><span class="sxs-lookup"><span data-stu-id="8596e-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Wartungsanfrage aktualisieren](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="8596e-142">Wenn Sie bei der Erstellung einer Wartungsanfrage eine Anlage auswählen, können Sie der Anlage einen Fehler hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8596e-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="8596e-143">Nachdem die Wartungsanfrage erstellt wurde, können Sie ggf. weitere Fehler hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8596e-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="8596e-144">Um Fehler hinzuzufügen, wählen Sie auf der Seite **Alle Wartungsanfragen** die Option **Anlagenfehler** aus.</span><span class="sxs-lookup"><span data-stu-id="8596e-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]