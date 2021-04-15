---
title: Felder für die mobile Warehouse Management Mobile App konfigurieren
description: In diesem Thema wird beschrieben, wie Feldnamen und -prioritäten in der Warehouse Management Mobile App definiert und konfiguriert werden.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808821"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="7322e-103">Felder für die mobile Warehouse Management Mobile App konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7322e-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7322e-104">In diesem Thema wird beschrieben, wie Feldnamen und -prioritäten in der Warehouse Management Mobile App definiert und konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="7322e-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="7322e-105">Dieser Artikel gilt für Funktionen im Modul „Lagerortverwaltung“.</span><span class="sxs-lookup"><span data-stu-id="7322e-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="7322e-106">Er gilt nicht für Funktionen im Modul "Bestandverwaltung".</span><span class="sxs-lookup"><span data-stu-id="7322e-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="7322e-107">Die Warehouse Management Mobile App ist eine Anwendung, die Sie verwenden können, um Lagerortaufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7322e-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="7322e-108">Sie können die Feldnamen definieren und konfigurieren, die in der App verwendet werden und die Priorität konfigurieren, der die Feldnamen zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7322e-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="7322e-109">In diesem Thema wird beschrieben, wie die Feldnamen und -prioritäten in der Warehouse Management Mobile App definiert, konfiguriert und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7322e-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="7322e-110">Konfigurieren von Lagerort-Feldnamen in der App</span><span class="sxs-lookup"><span data-stu-id="7322e-110">Configure warehouse app field names</span></span>

<span data-ttu-id="7322e-111">Wenn Sie Arbeitsgänge für Warehousing auf Ihrem mobilen Gerät nutzen, können Sie auf der Seite **Lagerort-App-Feldnamen** konfigurieren, wie Metadaten für das Gerät angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7322e-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="7322e-112">In einem neuen Unternehmen wählen Sie **Standardeinstellungen erstellen** aus, um alle Feldnamen zu generieren, die im Workflow des mobilen Geräts für Lagerort verwendet werden, und weisen Sie diesen dann einen bevorzugten Eingabemodus zu, und geben Sie einen Typ ein.</span><span class="sxs-lookup"><span data-stu-id="7322e-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="7322e-113">Nachdem Sie alle Feldnamen generiert haben, können folgende Eingabeoptionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="7322e-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7322e-114">Mit der folgenden Option...</span><span class="sxs-lookup"><span data-stu-id="7322e-114">Option</span></span></th>
<th><span data-ttu-id="7322e-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7322e-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7322e-116">Bevorzugter Eingabemodus</span><span class="sxs-lookup"><span data-stu-id="7322e-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="7322e-117">Mit dieser Option wird definiert, ob eine Bildfläche oder ein Eingabefeld oder eine manuelle Eingabe für den Feldnamen ausgewählt und angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7322e-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="7322e-118">Dies ist nützlich, um Felder entsprechend den Strichcodes zu unterscheiden, wenn solche für das Feld verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7322e-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="7322e-119"><strong>Hinweis:</strong> Für Feldnamen mit bevorzugtem Eingabemodus wählen Sie <strong>Durchsuchen</strong>. Sie können Informationen manuell eingeben, wenn der Strichcode nicht lesbar oder beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="7322e-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7322e-120">Eingabetyp</span><span class="sxs-lookup"><span data-stu-id="7322e-120">Input type</span></span></td>
<td><span data-ttu-id="7322e-121">Diese Option definiert, welcher eingegebene Typ des ausgewählten Feldnamen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7322e-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="7322e-122">Es sind vier Optionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7322e-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="7322e-123"><strong>Auswahl</strong> - Enthält eine Liste der Optionen zum Auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7322e-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="7322e-124">Feldnamen mit dieser Option können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7322e-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="7322e-125"><strong>Datum</strong> - Feldnamen, definiert als Datum zeigen das Datumsformat der Beschriftung an.</span><span class="sxs-lookup"><span data-stu-id="7322e-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="7322e-126">Damit können Lagerarbeiter sehen, welches Datumsformat sie eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="7322e-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="7322e-127">Feldnamen mit dieser Option können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7322e-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="7322e-128"><strong>Alphanumerisch</strong> - Wenn ausgewähltes, wird die Gerätentastatur verwendet, um die Informationen manuell in de App einzugeben.</span><span class="sxs-lookup"><span data-stu-id="7322e-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="7322e-129">Die Tastaturerfahrung kann geändert werden, je nach Gerät, das verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7322e-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="7322e-130"><strong>Numerisch</strong> - Für Feldnamen, die nur numerische Eingaben verwenden; Sie könne diese Option auswählen, um eine benutzerdefinierte Zehnertastatur dem Eingabefeld anstelle der Gerätentastatur anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7322e-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="7322e-131">Feldpriorität in Lagerortanwendung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7322e-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="7322e-132">Auf der Seite L **agerort-App-Feldpriorität** können Sie Feldnamen anderen Prioritätsgruppen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7322e-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="7322e-133">Auf diese Weise ist es möglich, zu entscheiden, welche Informationen auf der Hauptaufgabenseite angezeigt werden sollen, wenn Lagerarbeiter Aufgaben mithilfe der App ausführen.</span><span class="sxs-lookup"><span data-stu-id="7322e-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="7322e-134">We nn Sie auf **Standardeinstellungen erstellen** klicken, wird ein Standardsatz von Prioritätsgruppen generiert.</span><span class="sxs-lookup"><span data-stu-id="7322e-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="7322e-135">Es ist möglich, beliebig viele Prioritätsgruppen zu erstellen, aber es werden nur drei Prioritätengruppen auf der Aufgabenseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7322e-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="7322e-136">Wenn das System Metadaten an die App sendet, weist diese jedem der Felder eine relative Priorität abhängig von seiner Prioritätsstufe zu, und die App zeigt die ersten drei Prioritätengruppen an, die in den Metadaten auf der Aufgabenseite enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7322e-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="7322e-137">Der Rest der überfließenden Metadaten wird auf einer sekundären Detailseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7322e-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="7322e-138">Die folgende Tabelle enthält ein Beispiel der fünf Prioritätengruppen.</span><span class="sxs-lookup"><span data-stu-id="7322e-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7322e-139">Prioritätsgruppe</span><span class="sxs-lookup"><span data-stu-id="7322e-139">Priority group</span></span></th>
<th><span data-ttu-id="7322e-140">Zugewiesene Felder</span><span class="sxs-lookup"><span data-stu-id="7322e-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="7322e-141">Priorität 10</span><span class="sxs-lookup"><span data-stu-id="7322e-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="7322e-142">Artikel</span><span class="sxs-lookup"><span data-stu-id="7322e-142">Item</span></span></li>
<li><span data-ttu-id="7322e-143">Leistung</span><span class="sxs-lookup"><span data-stu-id="7322e-143">Quantity</span></span></li>
<li><span data-ttu-id="7322e-144">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="7322e-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="7322e-145">Priorität 20</span><span class="sxs-lookup"><span data-stu-id="7322e-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="7322e-146">Clusterposition</span><span class="sxs-lookup"><span data-stu-id="7322e-146">Cluster position</span></span></li>
<li><span data-ttu-id="7322e-147">Cluster</span><span class="sxs-lookup"><span data-stu-id="7322e-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="7322e-148">Priorität 30</span><span class="sxs-lookup"><span data-stu-id="7322e-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="7322e-149">Artikelbeschreibung</span><span class="sxs-lookup"><span data-stu-id="7322e-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="7322e-150">Priorität 40</span><span class="sxs-lookup"><span data-stu-id="7322e-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="7322e-151">Variante</span><span class="sxs-lookup"><span data-stu-id="7322e-151">Configuration</span></span></li>
<li><span data-ttu-id="7322e-152">Farbe</span><span class="sxs-lookup"><span data-stu-id="7322e-152">Color</span></span></li>
<li><span data-ttu-id="7322e-153">Größe</span><span class="sxs-lookup"><span data-stu-id="7322e-153">Size</span></span></li>
<li><span data-ttu-id="7322e-154">Formatvorlage</span><span class="sxs-lookup"><span data-stu-id="7322e-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="7322e-155">Priorität 50</span><span class="sxs-lookup"><span data-stu-id="7322e-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="7322e-156">Ziel</span><span class="sxs-lookup"><span data-stu-id="7322e-156">Location</span></span></li>
<li><span data-ttu-id="7322e-157">Ladungsträger</span><span class="sxs-lookup"><span data-stu-id="7322e-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7322e-158">Ein Lagerarbeiter führt beispielsweise eine Aufgabe auf einem mobilen Gerät aus, wenn die Metadaten, die angezeigt werden, folgende Felder aufweisen:</span><span class="sxs-lookup"><span data-stu-id="7322e-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="7322e-159">Artikel</span><span class="sxs-lookup"><span data-stu-id="7322e-159">Item</span></span>
-   <span data-ttu-id="7322e-160">Leistung</span><span class="sxs-lookup"><span data-stu-id="7322e-160">Quantity</span></span>
-   <span data-ttu-id="7322e-161">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="7322e-161">Unit of measure</span></span>
-   <span data-ttu-id="7322e-162">Artikelbeschreibung</span><span class="sxs-lookup"><span data-stu-id="7322e-162">Item description</span></span>
-   <span data-ttu-id="7322e-163">Größe und Standort</span><span class="sxs-lookup"><span data-stu-id="7322e-163">Size and Location</span></span>

<span data-ttu-id="7322e-164">Basierend auf der Lagerort-App-Feldpriorität, die in der Tabelle oben eingerichtet wird, werden die folgenden 3 Zeilen der Informationen auf der Aufgabenseite angezeigt:</span><span class="sxs-lookup"><span data-stu-id="7322e-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="7322e-165">Zeile 1: Artikel, Menge, Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="7322e-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="7322e-166">Reihe 2: Artikelbeschreibung</span><span class="sxs-lookup"><span data-stu-id="7322e-166">Row 2: Item description</span></span>
-   <span data-ttu-id="7322e-167">Zeile 3: Größe</span><span class="sxs-lookup"><span data-stu-id="7322e-167">Row 3: Size</span></span>

<span data-ttu-id="7322e-168">Die verbleibenden Metadaten beispielsweise Lagerplatz, werden nicht auf der Aufgabenseite angezeigt, sondern werden auf einer Detailseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7322e-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="7322e-169">Weitere Informationen und Beispiele der Benutzeroberfläche finden Sie im Blogbeitrag [Ankündigung Finance and Operations - Lagerverwaltung](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="7322e-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="7322e-170">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7322e-170">Additional resources</span></span>
--------

[<span data-ttu-id="7322e-171">Mobile Lagerortsverwaltungs-App installieren und verbinden</span><span class="sxs-lookup"><span data-stu-id="7322e-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]