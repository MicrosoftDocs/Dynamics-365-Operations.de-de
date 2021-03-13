---
title: Gestalten der Ausführungsschnittstelle auf Produktionsebene
description: Dieses Thema beschreibt, wie Sie den Inhalt der Benutzeroberfläche für jede Konfiguration entwerfen.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 786ea9a3da98e9f1812b007d4301cb47680e6894
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077577"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="ba517-103">Gestalten der Ausführungsschnittstelle auf Produktionsebene</span><span class="sxs-lookup"><span data-stu-id="ba517-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ba517-104">Sie können den Inhalt der Benutzeroberfläche für jede Konfiguration entwerfen, die von der Produktionsausführungsoberfläche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba517-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="ba517-105">So kann es z. B. sein, dass die Arbeitskräfte in einer Arbeitszelle in der Lage sein müssen, Arbeitsanweisungen im Produktionsbereich zu öffnen, während in einer anderen Arbeitszelle keine Anweisungen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="ba517-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="ba517-106">In diesem Fall sollten zwei Konfigurationen erstellt werden, eine mit einer Schaltfläche zum Öffnen von Dokumentenanhängen und eine ohne diese Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="ba517-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="ba517-107">Gestalten Sie eine Registerkarte</span><span class="sxs-lookup"><span data-stu-id="ba517-107">Design a tab</span></span>

<span data-ttu-id="ba517-108">Auf der Seite **Produktionsablauf konfigurieren** können Sie Registerkarten erstellen und konfigurieren, indem Sie **Registerkarten entwerfen** im Aktivitätsbereich wählen.</span><span class="sxs-lookup"><span data-stu-id="ba517-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="ba517-109">Jede Registerkarte ist in vier Abschnitte unterteilt, wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba517-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="ba517-110">![Registerkarten-Layout](media/pfe-tab-layout.png "Anordnung der Registerkarten")</span><span class="sxs-lookup"><span data-stu-id="ba517-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="ba517-111">Die folgenden Elemente sind in der Abbildung zu sehen:</span><span class="sxs-lookup"><span data-stu-id="ba517-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="ba517-112">Primäre Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="ba517-112">Primary toolbar</span></span>
1. <span data-ttu-id="ba517-113">Sekundäre Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="ba517-113">Secondary toolbar</span></span>
1. <span data-ttu-id="ba517-114">Hauptansicht</span><span class="sxs-lookup"><span data-stu-id="ba517-114">Main view</span></span>
1. <span data-ttu-id="ba517-115">Detaillierte Ansicht</span><span class="sxs-lookup"><span data-stu-id="ba517-115">Detailed view</span></span>

<span data-ttu-id="ba517-116">Um eine neue Registerkarte zu erstellen und zu konfigurieren, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="ba517-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="ba517-117">Gehen Sie zu **Produktionssteuerung &gt; Einrichten &gt; Fertigungsausführung**.</span><span class="sxs-lookup"><span data-stu-id="ba517-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="ba517-118">Wählen Sie **Design-Registerkarten** im Aktivitätsbereich, um die Seite **Design-Registerkarten** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ba517-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="ba517-119">![Die Seite Entwurfsregisterkarten](media/pfe-design-tabs.png "Die Seite Registerkarten Design")</span><span class="sxs-lookup"><span data-stu-id="ba517-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="ba517-120">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ba517-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="ba517-121">Legen Sie die folgenden Einstellungen in der Kopfzeile der Seite fest:</span><span class="sxs-lookup"><span data-stu-id="ba517-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="ba517-122">**Registerkartenname** - Geben Sie einen Namen für die Registerkarte an.</span><span class="sxs-lookup"><span data-stu-id="ba517-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="ba517-123">**Hauptansicht** – Wählen Sie zwischen den drei vordefinierten Auftragslisten (*Aktive Aufträge*, *Alle Aufträge* oder *Meine Maschine*).</span><span class="sxs-lookup"><span data-stu-id="ba517-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="ba517-124">**Detailansicht** - Wählen Sie zwischen einem leeren Wert oder **Job-Details**.</span><span class="sxs-lookup"><span data-stu-id="ba517-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="ba517-125">Wenn Sie den leeren Wert wählen, gibt es in der Registerkarte keine Detailansicht. Wenn Sie **Job-Details** wählen, enthält die Detailansicht eine detaillierte Beschreibung des Jobs, der in der Jobliste in der Hauptansicht ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="ba517-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="ba517-126">Im Bereich **Primäre Symbolleiste** wählen Sie, welche Schaltflächen in der primären Symbolleiste verfügbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="ba517-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="ba517-127">Die Spalte **Verfügbare Aktionen** zeigt eine Liste mit allen Schaltflächen, die hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="ba517-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="ba517-128">Die Spalten **Ausgewählte Aktionen** zeigt eine Liste aller Schaltflächen, die in der aktuellen Konfiguration enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ba517-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="ba517-129">Verwenden Sie die Schaltflächen zwischen den Spalten, um ausgewählte Elemente nach Bedarf zwischen den Spalten zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ba517-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="ba517-130">Verwenden Sie die Aufwärts- und Abwärts-Schaltflächen neben der Spalte **Ausgewählte Aktionen**, um die Reihenfolge zu steuern, in der die Schaltflächen in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ba517-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="ba517-131">Wählen Sie im Bereich **Sekundär** **Symbolleiste**, welche Schaltflächen in der sekundären Symbolleiste verfügbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="ba517-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="ba517-132">Die Spalte **Verfügbare Aktionen** zeigt eine Liste mit allen Schaltflächen, die hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="ba517-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="ba517-133">Die Spalten **Ausgewählte Aktionen** zeigt eine Liste aller Schaltflächen, die in der aktuellen Konfiguration enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ba517-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="ba517-134">Verwenden Sie die Schaltflächen zwischen den Spalten, um ausgewählte Elemente nach Bedarf zwischen den Spalten zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ba517-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="ba517-135">Verwenden Sie die Aufwärts- und Abwärts-Schaltflächen neben der Spalte **Ausgewählte Aktionen**, um die Reihenfolge zu steuern, in der die Schaltflächen in der Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ba517-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="ba517-136">Verknüpfen einer Registerkarte mit einer Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ba517-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="ba517-137">Nachdem Sie alle benötigten Registerkarten entworfen haben, können Sie diese mit einer Konfiguration verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="ba517-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="ba517-138">Gehen Sie zu **Produktionssteuerung &gt; Einrichten &gt; Ausführung der Produktionsfläche konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="ba517-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="ba517-139">![Produktionsausführung konfigurieren](media/pfe-config-prod-floor-execution.png "Produktionsausführung konfigurieren")</span><span class="sxs-lookup"><span data-stu-id="ba517-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="ba517-140">Wählen Sie auf dem Inforegister **Registerauswahl** **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ba517-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="ba517-141">Eine neue Zeile wird dem Raster hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ba517-141">A new row is added to the grid.</span></span> <span data-ttu-id="ba517-142">Wählen Sie für diese neue Zeile den Namen einer Registerkarte, die Sie der Konfiguration hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ba517-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="ba517-143">Fahren Sie fort, weitere Registerkarten nach Bedarf hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ba517-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="ba517-144">Verwenden Sie die Schaltflächen **Aufwärts bewegen** und **Abwärts bewegen** in der Symbolleiste, um die Registerkarten nach Bedarf anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ba517-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="ba517-145">Die Registerkarten werden von links nach rechts in der im obigen Screenshot gezeigten Reihenfolge angezeigt (die oberste Registerkarte wird links angezeigt).</span><span class="sxs-lookup"><span data-stu-id="ba517-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>
