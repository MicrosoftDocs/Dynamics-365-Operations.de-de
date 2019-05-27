---
title: Konfigurieren Sie App-Feldnamen in der Warehousing-App
description: In diesem Thema wird beschrieben, wie Lagerort-App-Feldnamen und -Prioritäten in Finance and Operations definiert und konfiguriert werden.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0162014189ed6bffb17e6718a67eecfd55c334a5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548928"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="1028d-103">Konfigurieren Sie App-Feldnamen in der Warehousing-App</span><span class="sxs-lookup"><span data-stu-id="1028d-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1028d-104">In diesem Thema wird beschrieben, wie Lagerort-App-Feldnamen und -Prioritäten in Finance and Operations definiert und konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="1028d-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="1028d-105">**Hinweis:** Dieser Artikel gilt für Funktionen im Modul "Lagerortverwaltung".</span><span class="sxs-lookup"><span data-stu-id="1028d-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="1028d-106">Er gilt nicht für Funktionen im Modul "Bestandverwaltung".</span><span class="sxs-lookup"><span data-stu-id="1028d-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="1028d-107">Finance and Operations - Warehousing ist eine Anwendung, die Sie verwenden können, um Lagerortaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1028d-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="1028d-108">Sie können die Feldnamen definieren und konfigurieren, die in der App verwendet werden und die Priorität konfigurieren, der die Feldnamen zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1028d-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="1028d-109">In diesem Thema wird beschrieben, wie Lagerort-App-Feldnamen und -Prioritäten in Finance and Operations definiert und konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="1028d-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="1028d-110">Ausführliche Informationen dazu, wie die Verbindung zu Finance and Operations - Warehousing konfiguriert wird, finden Sie im Lernprogramm [Installieren und Konfigurieren von Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="1028d-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="1028d-111">Konfigurieren von Lagerort-Feldnamen in der App</span><span class="sxs-lookup"><span data-stu-id="1028d-111">Configure warehouse app field names</span></span>

<span data-ttu-id="1028d-112">Wenn Sie Arbeitsgänge für Finance and Operations - Warehousing auf Ihrem mobilen Gerät nutzen, können Sie auf der Seite **Lagerort-App-Feldnamen** konfigurieren, wie Metadaten für das Gerät angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1028d-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="1028d-113">In einem neuen Unternehmen in Finance and Operations wählen Sie **Standardeinstellungen erstellen** aus, um alle Feldnamen zu generieren, die im Workflow des mobilen Geräts für Lagerort verwendet werden, und weisen Sie diesen dann einen bevorzugten Eingabemodus zu, und geben Sie einen Typ ein.</span><span class="sxs-lookup"><span data-stu-id="1028d-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="1028d-114">Nachdem Sie alle Feldnamen generiert haben, können folgende Eingabeoptionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="1028d-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1028d-115">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="1028d-115">Option</span></span></th>
<th><span data-ttu-id="1028d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1028d-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1028d-117">Bevorzugter Eingabemodus</span><span class="sxs-lookup"><span data-stu-id="1028d-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="1028d-118">Mit dieser Option wird definiert, ob eine Bildfläche oder ein Eingabefeld oder eine manuelle Eingabe für den Feldnamen ausgewählt und angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1028d-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="1028d-119">Dies ist nützlich, um Felder entsprechend den Strichcodes zu unterscheiden, wenn solche für das Feld verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1028d-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="1028d-120"><strong>Hinweis:</strong> Für Feldnamen mit bevorzugtem Eingabemodus wählen Sie <strong>Durchsuchen</strong>. Sie können Informationen manuell eingeben, wenn der Strichcode nicht lesbar oder beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="1028d-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1028d-121">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="1028d-121">Input type</span></span></td>
<td><span data-ttu-id="1028d-122">Diese Option definiert, welcher eingegebene Typ des ausgewählten Feldnamen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1028d-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="1028d-123">Es sind vier Optionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="1028d-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="1028d-124"><strong>Auswahl</strong> - Enthält eine Liste der Optionen zum Auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1028d-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="1028d-125">Feldnamen mit dieser Option können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1028d-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="1028d-126"><strong>Datum </strong> -Feldnamen, definiert als Datum zeigen das Datumsformat der Beschriftung an.</span><span class="sxs-lookup"><span data-stu-id="1028d-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="1028d-127">Damit können Lagerarbeiter sehen, welches Datumsformat sie eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="1028d-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="1028d-128">Feldnamen mit dieser Option können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1028d-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="1028d-129"><strong>Alphanumerisch</strong> - Wenn ausgewähltes, wird die Gerätentastatur verwendet, um die Informationen manuell in de App einzugeben.</span><span class="sxs-lookup"><span data-stu-id="1028d-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="1028d-130">Die Tastaturerfahrung kann geändert werden, je nach Gerät, das verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1028d-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="1028d-131"><strong>Numerisch</strong> - Für Feldnamen, die nur numerische Eingaben verwenden; Sie könne diese Option auswählen, um eine benutzerdefinierte Zehnertastatur dem Eingabefeld anstelle der Gerätentastatur anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1028d-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="1028d-132">Feldpriorität in Lagerortanwendung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="1028d-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="1028d-133">Auf der Seite L **agerort-App-Feldpriorität** können Sie Feldnamen anderen Prioritätsgruppen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1028d-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="1028d-134">Auf diese Weise ist es möglich, zu entscheiden, welche Informationen auf der Hauptaufgabenseite angezeigt werden sollen, wenn Lagerarbeiter Aufgaben mithilfe der App ausführen.</span><span class="sxs-lookup"><span data-stu-id="1028d-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="1028d-135">We nn Sie auf **Standardeinstellungen erstellen** klicken, wird ein Standardsatz von Prioritätsgruppen generiert.</span><span class="sxs-lookup"><span data-stu-id="1028d-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="1028d-136">Es ist möglich, beliebig viele Prioritätsgruppen zu erstellen, aber es werden nur drei Prioritätengruppen auf der Aufgabenseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1028d-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="1028d-137">Wenn Finance and Operations Metadaten an die App sendet, weist diese jedem der Felder eine relative Priorität abhängig von seiner Prioritätsstufe zu, und die App zeigt die ersten drei Prioritätengruppen an, die in den Metadaten auf der Aufgabenseite enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1028d-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="1028d-138">Der Rest der überfließenden Metadaten wird auf einer sekundären Detailseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1028d-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="1028d-139">Die folgende Tabelle enthält ein Beispiel der fünf Prioritätengruppen.</span><span class="sxs-lookup"><span data-stu-id="1028d-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1028d-140">Prioritätsgruppe</span><span class="sxs-lookup"><span data-stu-id="1028d-140">Priority group</span></span></th>
<th><span data-ttu-id="1028d-141">Zugewiesene Felder</span><span class="sxs-lookup"><span data-stu-id="1028d-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="1028d-142">Priorität 10</span><span class="sxs-lookup"><span data-stu-id="1028d-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="1028d-143">Artikel</span><span class="sxs-lookup"><span data-stu-id="1028d-143">Item</span></span></li>
<li><span data-ttu-id="1028d-144">Leistung</span><span class="sxs-lookup"><span data-stu-id="1028d-144">Quantity</span></span></li>
<li><span data-ttu-id="1028d-145">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="1028d-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="1028d-146">Priorität 20</span><span class="sxs-lookup"><span data-stu-id="1028d-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="1028d-147">Clusterposition</span><span class="sxs-lookup"><span data-stu-id="1028d-147">Cluster position</span></span></li>
<li><span data-ttu-id="1028d-148">Cluster</span><span class="sxs-lookup"><span data-stu-id="1028d-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="1028d-149">Priorität 30</span><span class="sxs-lookup"><span data-stu-id="1028d-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="1028d-150">Artikelbeschreibung</span><span class="sxs-lookup"><span data-stu-id="1028d-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="1028d-151">Priorität 40</span><span class="sxs-lookup"><span data-stu-id="1028d-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="1028d-152">Variante</span><span class="sxs-lookup"><span data-stu-id="1028d-152">Configuration</span></span></li>
<li><span data-ttu-id="1028d-153">Farbe</span><span class="sxs-lookup"><span data-stu-id="1028d-153">Color</span></span></li>
<li><span data-ttu-id="1028d-154">Größe</span><span class="sxs-lookup"><span data-stu-id="1028d-154">Size</span></span></li>
<li><span data-ttu-id="1028d-155">Formatvorlage</span><span class="sxs-lookup"><span data-stu-id="1028d-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="1028d-156">Priorität 50</span><span class="sxs-lookup"><span data-stu-id="1028d-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="1028d-157">Ziel</span><span class="sxs-lookup"><span data-stu-id="1028d-157">Location</span></span></li>
<li><span data-ttu-id="1028d-158">Ladungsträger</span><span class="sxs-lookup"><span data-stu-id="1028d-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1028d-159">Ein Lagerarbeiter führt beispielsweise eine Aufgabe auf einem mobilen Gerät aus, wenn die Metadaten, die angezeigt werden, folgende Felder aufweisen:</span><span class="sxs-lookup"><span data-stu-id="1028d-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="1028d-160">Artikel</span><span class="sxs-lookup"><span data-stu-id="1028d-160">Item</span></span>
-   <span data-ttu-id="1028d-161">Leistung</span><span class="sxs-lookup"><span data-stu-id="1028d-161">Quantity</span></span>
-   <span data-ttu-id="1028d-162">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="1028d-162">Unit of measure</span></span>
-   <span data-ttu-id="1028d-163">Artikelbeschreibung</span><span class="sxs-lookup"><span data-stu-id="1028d-163">Item description</span></span>
-   <span data-ttu-id="1028d-164">Größe und Standort</span><span class="sxs-lookup"><span data-stu-id="1028d-164">Size and Location</span></span>

<span data-ttu-id="1028d-165">Basierend auf der Lagerort-App-Feldpriorität, die in der Tabelle oben eingerichtet wird, werden die folgenden 3 Zeilen der Informationen auf der Aufgabenseite angezeigt:</span><span class="sxs-lookup"><span data-stu-id="1028d-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="1028d-166">Zeile 1: Artikel, Menge, Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="1028d-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="1028d-167">Reihe 2: Artikelbeschreibung</span><span class="sxs-lookup"><span data-stu-id="1028d-167">Row 2: Item description</span></span>
-   <span data-ttu-id="1028d-168">Zeile 3: Größe</span><span class="sxs-lookup"><span data-stu-id="1028d-168">Row 3: Size</span></span>

<span data-ttu-id="1028d-169">Die verbleibenden Metadaten beispielsweise Lagerplatz, werden nicht auf der Aufgabenseite angezeigt, sondern werden auf einer Detailseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1028d-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="1028d-170">Weitere Informationen und Beispiele der Benutzeroberfläche finden Sie im Blogbeitrag [Ankündigung Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)</span><span class="sxs-lookup"><span data-stu-id="1028d-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="1028d-171">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1028d-171">Additional resources</span></span>
--------

[<span data-ttu-id="1028d-172">Einrichten und Konfigurieren von Microsoft Dynamics 365 for Finance and Operations – Lagerorte</span><span class="sxs-lookup"><span data-stu-id="1028d-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)



