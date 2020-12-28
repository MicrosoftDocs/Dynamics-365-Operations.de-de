---
title: Wellenetikettendruck einrichten und verwenden
description: In diesem Thema wird das Drucken von Wellenetiketten beschrieben und die Einrichtung erläutert.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6314fd25d8d8a0013984d484f57a832c26f82b5a
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "4429144"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="e4cf9-103">Wellenetikettendruck einrichten und verwenden</span><span class="sxs-lookup"><span data-stu-id="e4cf9-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4cf9-104">Das Drucken von Wellenetiketten bietet einen alternativen Ansatz zum Drucken von Etiketten, indem eine neue Wellenschrittmethode eingeführt wird, mit der Sie während der Wellenausführung Etikette direkt aus der Wellenvorlage erstellen und drucken können.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="e4cf9-105">Daher sind die Etikette bereits verfügbar, bevor Mitarbeiter den Arbeitsauftrag auf einem mobilen Gerät ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="e4cf9-106">Die Arbeiter können dann die erforderlichen Etikette während der Kommissionierung anstatt nach der Kommissionierung anbringen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="e4cf9-107">Beim Drucken von Wellenetiketten wird die Zebra-Programmiersprache (ZPL) zum Erstellen von Etikettenlayouts verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="e4cf9-108">Ein Etikettenlayout ist in drei Abschnitte (Kopfzeile, Text und Fußzeile) unterteilt, um Etikette mit sich wiederholender Struktur zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="e4cf9-109">Wellenetikettenvorlagen teilen dem System mit, welches Etikettenlayout verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="e4cf9-110">Benutzer können angeben, welcher Drucker verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-110">Users can specify which printer is used.</span></span> <span data-ttu-id="e4cf9-111">Sie können bei Bedarf auch Etikette auf mehreren Druckern gleichzeitig drucken.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="e4cf9-112">Die Seite **Wellenetikettverlauf** zeigt die Erfassung aller Etikette an, die mit diesem Setup erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="e4cf9-113">Sie können Etikette basierend auf Arbeitsüberschriften drucken und sortieren, Sie können Unterbrechungsetikette pro Arbeitsüberschrift drucken und Sie können Etikette für Containerinhalte, Falletikette und andere ähnliche Etikette drucken.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="e4cf9-114">Diese Funktion ersetzt nicht die vorhandene Etikettendruckfunktion, die auf dem Routing von Dokumenten basiert.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="e4cf9-115">Der Wellenetikettendruck bietet die folgenden Verbesserungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="e4cf9-116">Drucken Sie Etikette entsprechend der Anzahl der Kartons in einer einzelnen Arbeitsposition, ohne Containerisierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="e4cf9-117">(Ein „Karton“ ist eine Einheit, die in Einheitennummernkreis-Positionen angegeben ist.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="e4cf9-118">Drucken Sie verschiedene Etikettsequenzen (z. B. Karton- und Palettenetikette).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="e4cf9-119">Schließen Sie die Etikettaufzählung ein (z. B. 1/124, 2/124, ... 124/124) und definieren Sie den Enumerationsbereich (z. B. Arbeitspostion, Ladungsposition oder Lieferung).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="e4cf9-120">Erstellen und drucken Sie eine Frachtbrief-ID auf Etiketten, bevor der Frachtbrief generiert wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="e4cf9-121">Erstellen Sie für jeden Karton eine eindeutige Nummer der Versandeinheit (SSCC) und fügen Sie diese auf jedem Etikett ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="e4cf9-122">Erstellen Sie GS1-konforme Nummernkreise für Frachtbrief-IDs und SSCCs.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="e4cf9-123">Drucken Sie erneut Etikette sowohl von Mobilgeräten als auch vom Rich-Client.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="e4cf9-124">Stornieren Sie Etikette (z. B. in Szenarien von Entnahme mit unzureichender Menge) und drucken Sie sie erneut.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="e4cf9-125">Serienetikettenverlauf löschen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="e4cf9-126">Verbesserungen an Dokumentrouting-Layouts werden zwischen Dokumentrouting-Layouts und Wellenetikettenlayouts geteilt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="e4cf9-127">(Weitere Informationen finden Sie unter [Dokumentrouting-Layout für Kennzeichen](../warehousing/document-routing-layout-for-license-plates.md) .)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="e4cf9-128">Diese Verbesserungen machen es effizienter, Kartons zu etikettieren, bevor sie auf Paletten geladen werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="e4cf9-129">Sie kommen insbesondere Unternehmen zugute, die an große Einzelhändler liefern, die automatisch Auftragseingänge bestätigen, indem sie jeden Karton separat scannen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="e4cf9-130">Sie können die in diesem Thema beschriebenen Konfigurationsszenarien je nach Ihren Geschäftsanforderungen entweder separat oder in Kombination implementieren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="e4cf9-131">Sie können mehrere Wellenetikettenvorlagen entwerfen, die nacheinander arbeiten (wie in Szenario 3 dargestellt).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="e4cf9-132">Sie können beispielsweise Szenario 1 zum Drucken von Kartonetiketten und Szenario 2 zum Drucken von Palettenetiketten verwenden (wenn die vorrätigen Paletten in Größe und Anordnung variieren).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="e4cf9-133">Funktion für Wellenetikettendruck aktivieren</span><span class="sxs-lookup"><span data-stu-id="e4cf9-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="e4cf9-134">Bevor Sie die Funktion *Wellenetikettendruck* verwenden können, muss sie in Ihrem System aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="e4cf9-135">Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e4cf9-136">Dort wird die Funktion folgendermaßen aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e4cf9-137">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e4cf9-138">**Funktionsname:** *Wellenetikettendruck*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="e4cf9-139">Szenario 1: Drucken von Wellenetiketten, bei dem ein einzelnes Wellenetikett generiert wird</span><span class="sxs-lookup"><span data-stu-id="e4cf9-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="e4cf9-140">Dieses Szenario zeigt, wie ein Unternehmen Adressetikett für einen großen Einzelhändler drucken kann, der Auftragseingänge automatisch bestätigt, indem jeder Karton separat gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="e4cf9-141">Dieses Szenario zeigt den End-to-End-Flow.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e4cf9-142">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-142">Make demo data available</span></span>

<span data-ttu-id="e4cf9-143">Um diesem Szenario zu folgen, müssen Demodaten installiert sein, und Sie müssen die juristische Person **USMF** auswählen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="e4cf9-144">Stellen Sie sicher, dass die Wellenetikettmethode verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="e4cf9-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="e4cf9-145">Möglicherweise müssen Sie die Wellenprozessmethoden erneut generieren, um die Wellenetiketdruck-Methode verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="e4cf9-146">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="e4cf9-147">Bestätigen Sie, dass **waveLabelPrinting** in der Liste ist.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="e4cf9-148">Wenn nicht, wählen Sie im Aktionsbereich **Methoden erneut generieren** aus, um es hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="e4cf9-149">Eine Wellenvorlage konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e4cf9-149">Configure a wave template</span></span>

<span data-ttu-id="e4cf9-150">Mit Wellenvorlagen können Sie bestimmte Instanzen von Wellenmethoden mit einer entsprechenden Wellenetikettenvorlage verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="e4cf9-151">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="e4cf9-152">Wählen Sie eine Vorlage aus, wie beispielsweise **62 Lieferungsstandard**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="e4cf9-153">Im Inforegister **Methoden** verschieben Sie die Methode **Wellenetikettendruck** zur Spalte **Ausgewählte Methoden**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="e4cf9-154">Wählen Sie in der Spalte **Ausgewählte Methoden** die Methode **Wellenetikettendruck** aus, und legen Sie deren Feld **Wellenschrittcode** auf *PrintLabel* fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="e4cf9-155">Weitere Informationen über Wellenschrittcodes finden Sie unter [Wellenschrittcodes](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="e4cf9-156">Ein Wellenetikettenlayout erstellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-156">Create a wave label layout</span></span>

<span data-ttu-id="e4cf9-157">Das Etikettenlayout steuert, welche Informationen auf dem Etikett gedruckt werden und wie sie angeordnet sind. Hier geben Sie den ZPL-Code ein, der an den Drucker gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="e4cf9-158">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenlayouts**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="e4cf9-159">Erstellen Sie einen Datensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-160">**Etikettenlayout-ID:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4cf9-161">**Beschreibung:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="e4cf9-162">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-163">Wählen Sie im Aktionsbereich **Einstellungen für Wellenetikettzeile** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="e4cf9-164">Die Seite **Einstellungen für Wellenetikettzeile** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="e4cf9-165">Hier können Sie den dynamischen Teil des Etiketts konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="e4cf9-166">Fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-167">**Zeilen-ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="e4cf9-168">**Zeilentabellenname:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="e4cf9-169">**Zeilenstartposition:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="e4cf9-170">Dieses Feld definiert die vertikale Position, an der die Zeile im Etikett beginnt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="e4cf9-171">**Zeilenhöhe:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-171">**Row height:** *0*</span></span>

        <span data-ttu-id="e4cf9-172">Dieses Feld definiert die Höhe jeder Zeile (in Punkten) gemäß dem ZPL-Standard.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="e4cf9-173">Die Zeilenhöhe ist positiv für horizontale Etikette und negativ für vertikale Etikette.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="e4cf9-174">Da es in diesem Beispiel nur eine Zeile gibt, können Sie den Wert auf *0* (Null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="e4cf9-175">**Zeilen pro Seite:** *1*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="e4cf9-176">Dieses Feld definiert die Anzahl der Zeilen, die auf jedes Etikett gedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4cf9-177">Durch dieses Setup wird für jeden Datensatz in der Wellenetikettentabelle ein separates ZPL-Etikett gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="e4cf9-178">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-178">Close the page.</span></span>
1. <span data-ttu-id="e4cf9-179">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e4cf9-180">Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-181">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-182">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-183">**Feld:** *Arbeitstyp*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e4cf9-184">**Kriterien:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="e4cf9-185">Diese Abfrage stellt sicher, dass nur Arbeitspositionen vom Entnahmetyp auf dem Etikett gedruckt werden und nicht Arbeitspositionen vom Einlagerungstyp.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="e4cf9-186">Wenn Sie die Frachtbrief-ID ausdrucken möchten, wählen Sie auf der Registerkarte **Verknüpfungen** die Tabelle **Arbeitspositionen** aus, und verknüpften Sie die Tabelle **Lieferungen** damit.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="e4cf9-187">Schließen Sie das Abfrage-Editor-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4cf9-188">Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4cf9-189">Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie Code für die erforderliche Kopfzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="e4cf9-190">Wenn Sie beispielsweise Zebra-Drucker verwenden, können Sie den folgenden Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="e4cf9-191">Im Abschnitt **Textabschnitt** im Feld **Etikettentext** geben Sie ZPL-Code für den erforderlichen Text ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="e4cf9-192">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="e4cf9-193">Im Abschnitt **Textabschnitt** im Feld **Etikettenfußzeile** geben Sie ZPL-Code für die erforderlichen Fußzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="e4cf9-194">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="e4cf9-195">Durch dieses Setup wird eine Kopie jedes Etiketts gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="e4cf9-196">Wenn Sie mehr Kopien benötigen (z. B. eine Kopie für jede Seite der Palette), legen Sie den **n**-Wert für den Abschnitt **\^PQn** in der Fußzeile auf die erforderliche Anzahl von Kopien fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="e4cf9-197">Um vier Kopien jedes Etiketts zu drucken, geben Sie beispielsweise **\^PQ4** an.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="e4cf9-198">Ihr Etikett kann jetzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="e4cf9-199">Einen Wellenetikettentyp erstellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-199">Create a wave label type</span></span>

<span data-ttu-id="e4cf9-200">Wellenetikettentypen werden verwendet, um Wellenetikettenvorlagen mit einer Einheit in Einheitsnummernkreisgruppen-Positionen zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="e4cf9-201">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettentypen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="e4cf9-202">Fügen Sie ein Wellenetikettentyp mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-203">**Etikettentyp:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="e4cf9-204">**Beschreibung:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="e4cf9-205">Einheitensequenzgruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="e4cf9-205">Set up unit sequence groups</span></span>

<span data-ttu-id="e4cf9-206">Richten Sie als Nächstes die Einheitsnummernkreisgruppe für den Wellenetikettentyp ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="e4cf9-207">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Lagerort \> Einheitsnummernkreisgruppe**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="e4cf9-208">Wählen Sie die Gruppe **Ea Box PL** (Einzelstücke Kiste/Palette) aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="e4cf9-209">Für die Position **Kiste** legen Sie das Feld **Wellenetikettentyp** auf *Karton* fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="e4cf9-210">Eine Wellenetikettenvorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-210">Create a wave label template</span></span>

<span data-ttu-id="e4cf9-211">Erstellen Sie als Nächstes die Wellenetikettenvorlage für den Wellenetikettentyp.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="e4cf9-212">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="e4cf9-213">Fügen Sie eine Wellenetikettenvorlage hinzu und legen Sie die folgenden Werte in der Kopfzeile fest:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="e4cf9-214">**Etikettenvorlagenname:** *Kartonetikette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="e4cf9-215">**Beschreibung:** *Kartonetikette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="e4cf9-216">**Wellenschrittcode:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="e4cf9-217">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4cf9-218">Im Inforegister **Allgemein** legen Sie das Feld **Wellenetikettentyp** auf *Karton* fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="e4cf9-219">Im Inforegister **Details zur Wellenetikettenvorlage** fügen Sie eine neue Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-220">**Etikettenlayout-ID:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4cf9-221">**Druckername:** Wählen Sie einen geeigneten ZPL-Drucker aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="e4cf9-222">**Abfrage ausführen:** *Ja* (Diese Einstellung ist optional, wird jedoch für eine optimale Leistung empfohlen.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="e4cf9-223">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-224">Optional: Wenn Sie ein kundenspezifisches Etikettendesign einrichten, müssen Sie eine Abfrage erstellen, um das Kundenkonto zu finden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="e4cf9-225">Im Inforegister **Details zur Wellenetikettenvorlage** wählen Sie **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="e4cf9-226">Fügen Sie dann im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-227">**Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e4cf9-228">**Abgeleitete Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e4cf9-229">**Feld:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="e4cf9-230">**Kriterien:** Geben Sie die relevante Kundenkontonummer ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="e4cf9-231">Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="e4cf9-232">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus, um das Dialogfeld des Abfrage-Editors für die gesamte Etikettenvorlage zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="e4cf9-233">Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Sortieren** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-234">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-235">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-236">**Feld:** *Referenzladungspositions-ID (Datensatz-ID)*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="e4cf9-237">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4cf9-238">Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4cf9-239">In einem Meldungsfeld werden Sie aufgefordert, den Vorgang zum Zurücksetzen der Gruppierung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="e4cf9-240">Wählen Sie **Ja** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e4cf9-241">Wählen Sie im Aktionsbereich **Wellenetikettenvorlagen-Gruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="e4cf9-242">Im Dialogfeld **Wellenetikettenvorlagen-Gruppe** wählen Sie die Zeile aus, in der das Feld **Referenzfeldname** auf *Referenzladungspositions-ID* festgelegt ist und aktivieren Sie dann das Kontrollkästchen **Etiketten-Build-ID** für diese Zeile.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4cf9-243">Dieses Setup erstellt eine Etikettensequenz („Karton 1 von X“) pro Ladeposition während der gesamten Welle, unabhängig vom Setup der Arbeitsgruppierung.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="e4cf9-244">Diese Etikettensequenz kann auf das Etikettenlayout gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="e4cf9-245">Nummernkreiserweiterungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e4cf9-245">Configure number sequence extensions</span></span>

<span data-ttu-id="e4cf9-246">Nummernkreiserweiterungen steuern die GS1-Konformität bestimmter Nummernkreise.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="e4cf9-247">Diese Konfiguration ist für das aktuelle Szenario optional.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="e4cf9-248">Weitere Informationen und Konfigurationsanweisungen finden Sie unter [Nummernkreiserweiterungen konfigurieren](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="e4cf9-249">Einen Auftrag erstellen und ihn für den Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="e4cf9-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="e4cf9-250">Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="e4cf9-251">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-252">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e4cf9-253">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4cf9-254">Fügen Sie zwei Auftragspositionen mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="e4cf9-255">Auftragsposition 1:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-255">Sales order line 1:</span></span>

        - <span data-ttu-id="e4cf9-256">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e4cf9-257">**Menge** *9024*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="e4cf9-258">**Einheit:** *ea* (9024 Einzelstücke = 376 Kisten = 47 Paletten)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="e4cf9-259">Auftragsposition 2:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-259">Sales order line 2:</span></span>

        - <span data-ttu-id="e4cf9-260">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e4cf9-261">**Menge** *9016*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="e4cf9-262">**Einheit:** *ea* (9016 Einzelstücke = 322 Kisten = 46 Paletten)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4cf9-263">Die hier angegebenen Artikel und Mengen sind nur Beispiele.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="e4cf9-264">Sie müssen die zuvor definierte Einheitsnummernkreisgruppe verwenden, für sie müssen entsprechende Einheitsumrechnungen von *ea* (Einzelstück) zu *Box* (Kiste) zu *PL* (Palette) definiert sein, und sie müssen Bestand im Lager haben *62*.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="e4cf9-265">Weitere Informationen finden Sie unter [Maßeinheit und Lagerhaltungsrichtlinien](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="e4cf9-266">Wählen Sie Auftragsposition 1 aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-266">Select sales order line 1.</span></span> <span data-ttu-id="e4cf9-267">Wählen Sie dann im Abschnitt **Auftragsposition** im Menü **Bestand** die Option **Reservierungen** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="e4cf9-268">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, und schließen Sie dann die Seite.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="e4cf9-269">Wiederholen Sie die Schritte 4 und 5 für Auftragsposition 2.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="e4cf9-270">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e4cf9-271">Folgende Ereignisse treten auf:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-271">The following events occur:</span></span>

    - <span data-ttu-id="e4cf9-272">Das System verarbeitet die erstellte Lieferung mithilfe der Vorlage, die den Etikettendruckschritt enthält.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="e4cf9-273">Das Etikettenlayout wird verwendet, um das Format des Etiketts zu definieren. Das Ergebnis ist ein Etikett, das auf dem in der Etikettenvorlage ausgewählten Drucker gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="e4cf9-274">Wellenetiketten werden generiert und gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="e4cf9-275">Die Anzahl der Etikette entspricht der Anzahl der Kartons (in diesem Beispiel 376 Kartonetikette für Position 1 und 322 Kartonetikette für Position 2).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="e4cf9-276">Für die Lieferung wird eine neue Frachtbrief-ID generiert.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="e4cf9-277">Wenn Sie die Nummernkreiserweiterungen konfiguriert haben, folgen die Wellenetikett-IDs dem Zahlenformat **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="e4cf9-278">Sie können Serienetiketten von den folgenden Seiten anzeigen und erneut drucken.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="e4cf9-279">Wählen Sie im Aktivitätsbereich jeder Seite, auf der Registerkarte **Lieferungen** in der Gruppe **Zugehörige Informationen** die Option **Serienetiketten**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="e4cf9-280">Alle Lieferungen \> Lieferdetails</span><span class="sxs-lookup"><span data-stu-id="e4cf9-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="e4cf9-281">Alle Ladungen \> Ladungsdetails</span><span class="sxs-lookup"><span data-stu-id="e4cf9-281">All loads \> Load details</span></span>
- <span data-ttu-id="e4cf9-282">Alle Wellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-282">All waves</span></span>
- <span data-ttu-id="e4cf9-283">Serienetiketten</span><span class="sxs-lookup"><span data-stu-id="e4cf9-283">Wave labels</span></span>
- <span data-ttu-id="e4cf9-284">Wellenbeschriftungsverlauf</span><span class="sxs-lookup"><span data-stu-id="e4cf9-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="e4cf9-285">Szenario 2: Wellenetikettendruck zur Containerisierung (ohne Wellenetikettendatensätze)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="e4cf9-286">In diesem Szenario können Sie Wellenetiketten drucken, wenn Sie die Containerisierung verwenden, um Artikel automatisch in Kartons aufzuteilen, und daher keinen Wellenetikettendatensatz benötigen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="e4cf9-287">In diesem Fall fungiert die Container-ID als Platzhalter für den SSCC.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="e4cf9-288">Hier sind die Hauptunterschiede zwischen diesem Szenario und Szenario 1:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="e4cf9-289">**Wellenetikettenvorlagen:** Sie wählen keinen Wellenetikettentyp in der Wellenetikettenvorlage aus und benötigen keine Etiketten-Build-Gruppierung.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="e4cf9-290">Andernfalls konfigurieren Sie die Wellenetikettenvorlage und verknüpfen sie mit der Wellenvorlage auf dieselbe Weise wie in Szenario 1 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="e4cf9-291">Sie müssen den Wellenetikettentyp leer lassen, um zu verhindern, dass Wellenetiketten generiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="e4cf9-292">**Wellenetikettenlayouts:** Sie konfigurieren die Zeileneinstellungen für das Wellenetikettenlayout für Arbeitspositionen anstelle von Wellenetikettendatensätzen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="e4cf9-293">Sie müssen die Zeileneinstellung für das Etikettenlayout mithilfe der Tabelle **WHSWorkLine** anstelle der Tabelle **WHSWaveLabel** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="e4cf9-294">Die Einstellung **Zeilen pro Seite** steuert die Anzahl der Zeilen, die der Textabschnitt haben wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="e4cf9-295">Diese Konfiguration eignet sich auch für Geschäftsszenarien, in denen mehrere verschiedene Artikel in eine etikettierte Schachtel oder auf einer Palette gepackt werden. Dieser Verpackungsprozess kann durch die Arbeitserstellung definiert werden (z. B. Arbeit, die nach Lieferung gruppiert wird).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="e4cf9-296">Dieses Szenario zeigt den End-to-End-Flow.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e4cf9-297">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-297">Make demo data available</span></span>

<span data-ttu-id="e4cf9-298">Um diesem Szenario zu folgen, müssen Demodaten installiert sein, und Sie müssen die juristische Person **USMF** auswählen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="e4cf9-299">Stellen Sie sicher, dass die Wellenetikettmethode verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="e4cf9-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="e4cf9-300">Möglicherweise müssen Sie die Wellenprozessmethoden erneut generieren, um die Wellenetiketdruck-Methode verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="e4cf9-301">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="e4cf9-302">Bestätigen Sie, dass **waveLabelPrinting** in der Liste ist.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="e4cf9-303">Wenn nicht, wählen Sie im Aktionsbereich **Methoden erneut generieren** aus, um es hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="e4cf9-304">Richten Sie eine Wellenvorlage ein</span><span class="sxs-lookup"><span data-stu-id="e4cf9-304">Set up a wave template</span></span>

<span data-ttu-id="e4cf9-305">Mit Wellenvorlagen können Sie bestimmte Instanzen von Wellenmethoden mit einer entsprechenden Wellenetikettenvorlage verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="e4cf9-306">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="e4cf9-307">Wählen Sie eine Vorlage aus, wie beispielsweise **63 Containerisierung**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="e4cf9-308">Im Inforegister **Methoden** verschieben Sie die Methode **Wellenetikettendruck** zur Spalte **Ausgewählte Methoden**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="e4cf9-309">Wählen Sie in der Spalte **Ausgewählte Methoden** die Methode **Wellenetikettendruck** aus, und legen Sie deren Feld **Wellenschrittcode** auf *PrintLabel* fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="e4cf9-310">Weitere Informationen über Wellenschrittcodes finden Sie unter [Wellenschrittcodes](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="e4cf9-311">Ein Wellenetikettenlayout erstellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-311">Create a wave label layout</span></span>

1. <span data-ttu-id="e4cf9-312">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenlayouts**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="e4cf9-313">Erstellen Sie einen Datensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-314">**Etikettenlayout-ID:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4cf9-315">**Beschreibung:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="e4cf9-316">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-317">Wählen Sie im Aktionsbereich **Einstellungen für Wellenetikettzeile** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="e4cf9-318">Die Seite **Einstellungen für Wellenetikettzeile** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="e4cf9-319">Hier können Sie den dynamischen Teil des Etiketts konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="e4cf9-320">Fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-321">**Zeilen-ID:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="e4cf9-322">**Zeilentabellenname:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="e4cf9-323">**Zeilenstartposition:** *500*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="e4cf9-324">Dieses Feld definiert die vertikale Position, an der die Zeile im Etikett beginnt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="e4cf9-325">**Zeilenhöhe:** *-50*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="e4cf9-326">Dieses Feld definiert die Höhe jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-326">This field defines the height of each row.</span></span> <span data-ttu-id="e4cf9-327">Die Zeilenhöhe ist positiv für horizontale Etikette und negativ für vertikale Etikette.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="e4cf9-328">**Zeilen pro Seite:** *5*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="e4cf9-329">Dieses Feld definiert die Anzahl der Zeilen, die auf jedes Etikett gedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4cf9-330">Dieses Setup druckt mehrere ZPL-Etiketten pro Arbeit, wobei jede Seite bis zu fünf Arbeitspositionen enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="e4cf9-331">Wenn beispielsweise ein Etikett für einen Container mit 12 Positionen gedruckt wird, werden drei Etiketten gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="e4cf9-332">Wenn Sie für jede Entnahmeposition ein separates Etikett drucken möchten, legen Sie diesen Wert auf *1* fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="e4cf9-333">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-333">Close the page.</span></span>
1. <span data-ttu-id="e4cf9-334">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e4cf9-335">Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-336">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-337">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-338">**Feld:** *Arbeitstyp*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e4cf9-339">**Kriterien:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="e4cf9-340">Wenn Sie die Frachtbrief-ID ausdrucken möchten, wählen Sie auf der Registerkarte **Verknüpfungen** die Tabelle **Arbeitspositionen** aus, und verknüpften Sie die Tabelle **Lieferungen** damit.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="e4cf9-341">Schließen Sie das Abfrage-Editor-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4cf9-342">Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4cf9-343">Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie Code für die erforderliche Kopfzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="e4cf9-344">Wenn Sie beispielsweise Zebra-Drucker verwenden, können Sie den folgenden Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="e4cf9-345">Im Abschnitt **Textabschnitt** im Feld **Etikettentext** geben Sie ZPL-Code für den erforderlichen Text ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="e4cf9-346">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="e4cf9-347">Im Abschnitt **Textabschnitt** im Feld **Etikettenfußzeile** geben Sie ZPL-Code für die erforderlichen Fußzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="e4cf9-348">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="e4cf9-349">Durch dieses Setup wird eine Kopie jedes Etiketts gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="e4cf9-350">Wenn Sie mehr Kopien benötigen (z. B. eine Kopie für jede Seite der Palette), legen Sie den **n**-Wert für den Abschnitt **\^PQn** in der Fußzeile auf die erforderliche Anzahl von Kopien fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="e4cf9-351">Um vier Kopien jedes Etiketts zu drucken, geben Sie beispielsweise **\^PQ4** an.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="e4cf9-352">Ihr Etikett kann jetzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="e4cf9-353">Eine Wellenetikettenvorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-353">Create a wave label template</span></span>

1. <span data-ttu-id="e4cf9-354">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="e4cf9-355">Fügen Sie eine Wellenetikettenvorlage hinzu und legen Sie die folgenden Werte in der Kopfzeile fest:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="e4cf9-356">**Etikettenvorlagenname:** *Containeretikette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="e4cf9-357">**Beschreibung:** *Containeretikette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="e4cf9-358">**Wellenschrittcode:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="e4cf9-359">**Lagerort:** *63*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="e4cf9-360">Im Inforegister **Details zur Wellenetikettenvorlage** fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-361">**Etikettenlayout-ID:** *Container*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="e4cf9-362">**Druckername:** Wählen Sie einen geeigneten ZPL-Drucker aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="e4cf9-363">**Abfrage ausführen:** *Ja* (Diese Einstellung ist optional, wird jedoch für eine optimale Leistung empfohlen.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="e4cf9-364">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-365">Optional: Wenn Sie ein kundenspezifisches Etikettendesign einrichten, müssen Sie eine Abfrage erstellen, um das Kundenkonto zu finden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="e4cf9-366">Im Inforegister **Details zur Wellenetikettenvorlage** wählen Sie **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="e4cf9-367">Fügen Sie dann im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-368">**Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e4cf9-369">**Abgeleitete Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e4cf9-370">**Feld:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="e4cf9-371">**Kriterien:** Geben Sie die relevante Kundenkontonummer ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="e4cf9-372">Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="e4cf9-373">Nummernkreiserweiterungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e4cf9-373">Configure number sequence extensions</span></span>

<span data-ttu-id="e4cf9-374">Nummernkreiserweiterungen steuern die GS1-Konformität bestimmter Nummernkreise.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="e4cf9-375">Diese Konfiguration ist für das aktuelle Szenario optional.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="e4cf9-376">Weitere Informationen und Konfigurationsanweisungen finden Sie unter [Nummernkreiserweiterungen konfigurieren](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="e4cf9-377">Einen Auftrag erstellen und ihn für den Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="e4cf9-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="e4cf9-378">Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="e4cf9-379">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-380">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e4cf9-381">**Lagerort:** *63*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="e4cf9-382">Fünf Auftragspositionen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="e4cf9-383">Auftragsposition 1:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-383">Sales order line 1:</span></span>

        - <span data-ttu-id="e4cf9-384">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e4cf9-385">**Menge** *10*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="e4cf9-386">Auftragsposition 2:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-386">Sales order line 2:</span></span>

        - <span data-ttu-id="e4cf9-387">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e4cf9-388">**Menge** *20*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="e4cf9-389">Auftragsposition 3:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-389">Sales order line 3:</span></span>

        - <span data-ttu-id="e4cf9-390">**Artikelnummer:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="e4cf9-391">**Menge** *20*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="e4cf9-392">Auftragsposition 4:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-392">Sales order line 4:</span></span>

        - <span data-ttu-id="e4cf9-393">**Artikelnummer:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="e4cf9-394">**Menge** *40*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="e4cf9-395">Auftragsposition 5:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-395">Sales order line 5:</span></span>

        - <span data-ttu-id="e4cf9-396">**Artikelnummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="e4cf9-397">**Menge** *50*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4cf9-398">Die hier angegebenen Artikel und Mengen sind nur Beispiele.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="e4cf9-399">Sie müssen Lagerbestand im angegebenen Lager haben.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="e4cf9-400">Wählen Sie Auftragsposition 1 aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-400">Select sales order line 1.</span></span> <span data-ttu-id="e4cf9-401">Wählen Sie dann im Abschnitt **Auftragsposition** im Menü **Bestand** die Option **Reservierungen** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="e4cf9-402">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, und schließen Sie dann die Seite.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="e4cf9-403">Wiederholen Sie die Schritte 4 und 5 für jede zusätzliche Auftragsposition.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="e4cf9-404">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e4cf9-405">Folgende Ereignisse treten auf:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-405">The following events occur:</span></span>

    - <span data-ttu-id="e4cf9-406">Das System verarbeitet die erstellte Lieferung mithilfe der Vorlage, die den Etikettendruckschritt enthält.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="e4cf9-407">Das Etikettenlayout wird verwendet, um das Format des Etiketts zu definieren. Das Endergebnis ist ein Etikett, das fünf Positionen hat und das auf dem in der Etikettenvorlage ausgewählten Drucker gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="e4cf9-408">Für die Lieferung wird eine neue Frachtbrief-ID generiert.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="e4cf9-409">Wenn Sie die Nummernkreiserweiterungen konfiguriert haben, folgen die Wellenetikett-IDs dem Zahlenformat **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="e4cf9-410">Sie können diese Wellenetiketten erneut drucken, indem Sie zu **Lagerortverwaltung \> Anfragen und Berichte \> Wellenetikettenverlauf** gehen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="e4cf9-411">Szenario 3: Wellenetikettendruck für mehrstufige Etiketten</span><span class="sxs-lookup"><span data-stu-id="e4cf9-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="e4cf9-412">Dieses Szenario zeigt, wie die Funktion zum Drucken von Wellenetiketten verwendet wird, wenn für die Lagerhaltungsprozesse mehrere Ebenen von Adressetiketten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="e4cf9-413">Beispielsweise müssen möglicherweise separate Etiketten für Kartons und Paletten gedruckt werden, und ein Unterbrechungsetikett muss möglicherweise für eine gesamte Lieferung gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="e4cf9-414">Unterbrechungsetiketten sind separate Typen von Etiketten, die als Trennmarke zwischen Rollen und Containern verwendet werden können, z. B. Etiketten für die Lieferungs-ID und einen Strichcode, damit die Etiketten nach dem Drucken leicht sortiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="e4cf9-415">Der Hauptunterschied zwischen der Konfiguration dieses Szenarios und der Konfiguration von Szenario 1 besteht neben der Tatsache, dass Unterbrechungsetiketten aktiviert sind, darin, dass mehrere Wellenetikettentypen den Wellenetikettenvorlagen und Einheitsnummernkreisgruppen-Positionen zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="e4cf9-416">Um diese Konfiguration durchzuführen, richten Sie die folgenden Elemente für dieses Szenario ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="e4cf9-417">**Wellenverarbeitungsmethoden:** Sie markieren die Wellenetikettenmethode als „wiederholbar“, fügen sie zwei (oder mehrere) Male zur Wellenvorlage hinzu und legen verschiedene Wellenschrittcodes fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="e4cf9-418">**Wellenetikettenvorlagen:** Sie konfigurieren die Wellenetikettenvorlagen und verknüpfen sie mit der Wellenvorlage.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="e4cf9-419">Jede Wellenetikettenvorlage hat ihren eigenen Wellenetikettentyp.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="e4cf9-420">**Wellenetikettenlayouts:** Sie erstellen mehrere Wellenetikettenlayouts.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="e4cf9-421">Es wird ein separates Etikettenlayout für jede „Ebene“ von Etiketten geben, und es wird auch ein Unterbrechungsetikettenlayout geben.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="e4cf9-422">Dieses Szenario zeigt den End-to-End-Flow.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e4cf9-423">Demodaten zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-423">Make demo data available</span></span>

<span data-ttu-id="e4cf9-424">Um diesem Szenario zu folgen, müssen Demodaten installiert sein, und Sie müssen die juristische Person **USMF** auswählen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="e4cf9-425">Eine Wellenverarbeitungsmethode einrichten</span><span class="sxs-lookup"><span data-stu-id="e4cf9-425">Set up a wave process method</span></span>

1. <span data-ttu-id="e4cf9-426">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="e4cf9-427">Bestätigen Sie, dass **waveLabelPrinting** in der Liste ist.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="e4cf9-428">Wenn nicht, wählen Sie im Aktionsbereich **Methoden erneut generieren** aus, um es hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="e4cf9-429">Für die Methode **waveLabelPrinting** aktivieren Sie das Kontrollkästchen **Methode wiederholbar machen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="e4cf9-430">Richten Sie eine Wellenvorlage ein</span><span class="sxs-lookup"><span data-stu-id="e4cf9-430">Set up a wave template</span></span>

1. <span data-ttu-id="e4cf9-431">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="e4cf9-432">Wählen Sie eine Vorlage aus, wie beispielsweise **62 Lieferungsstandard**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="e4cf9-433">Im Inforegister **Methoden** verschieben Sie die Methode **Wellenetikettendruck** zur Spalte **Ausgewählte Methoden**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="e4cf9-434">In der Spalte **Ausgewählte Methoden** weisen Sie einen Wert **Wellenschrittcode**, wie z. B. *Karton*, der Methode **Wellenetikettendruck** zu.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="e4cf9-435">Weitere Informationen über Wellenschrittcodes finden Sie unter [Wellenschrittcodes](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="e4cf9-436">Verschieben Sie die Methode **Wellenetikettendruck** ein zweites Mal zur Spalte **Ausgewählte Methoden**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="e4cf9-437">In der Spalte **Ausgewählte Methoden** weisen Sie einen anderen **Wellenschrittcode**-Wert, wie z. B. *Palette*, der zweiten **Wellenetikettendruck**-Methode zu.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="e4cf9-438">Weitere Informationen über Wellenschrittcodes finden Sie unter [Wellenschrittcodes](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="e4cf9-439">Drei Wellenetikettenlayouts erstellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="e4cf9-440">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenlayouts**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="e4cf9-441">Erstellen Sie einen Datensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-442">**Etikettenlayout-ID:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4cf9-443">**Beschreibung:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="e4cf9-444">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-445">Wählen Sie im Aktionsbereich **Einstellungen für Wellenetikettzeile** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="e4cf9-446">Die Seite **Einstellungen für Wellenetikettzeile** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="e4cf9-447">Hier können Sie den dynamischen Teil des Etiketts konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="e4cf9-448">Fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-449">**Zeilen-ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="e4cf9-450">**Zeilentabellenname:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="e4cf9-451">**Zeilenstartposition:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="e4cf9-452">Dieses Feld definiert die vertikale Position, an der die Zeile im Etikett beginnt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="e4cf9-453">**Zeilenhöhe:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-453">**Row height:** *0*</span></span>

        <span data-ttu-id="e4cf9-454">Dieses Feld definiert die Höhe jeder Zeile (in Punkten) gemäß dem ZPL-Standard.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="e4cf9-455">Die Zeilenhöhe ist positiv für horizontale Etikette und negativ für vertikale Etikette.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="e4cf9-456">Da es in diesem Beispiel nur eine Zeile gibt, können Sie den Wert auf *0* (Null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="e4cf9-457">**Zeilen pro Seite:** *1*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="e4cf9-458">Dieses Feld definiert die Anzahl der Zeilen, die auf jedes Etikett gedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4cf9-459">Durch dieses Setup wird für jeden Datensatz in der Wellenetikettentabelle ein separates ZPL-Etikett gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="e4cf9-460">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-460">Close the page.</span></span>
1. <span data-ttu-id="e4cf9-461">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e4cf9-462">Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-463">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-464">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-465">**Feld:** *Arbeitstyp*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e4cf9-466">**Kriterien:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="e4cf9-467">Diese Abfrage stellt sicher, dass nur Arbeitspositionen vom Entnahmetyp auf dem Etikett gedruckt werden und nicht Arbeitspositionen vom Einlagerungstyp.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="e4cf9-468">Wenn Sie die Frachtbrief-ID ausdrucken möchten, wählen Sie auf der Registerkarte **Verknüpfungen** die Tabelle **Arbeitspositionen** aus, und verknüpften Sie die Tabelle **Lieferungen** damit.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="e4cf9-469">Schließen Sie das Abfrage-Editor-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4cf9-470">Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4cf9-471">Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie Code für die erforderliche Kopfzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="e4cf9-472">Wenn Sie beispielsweise Zebra-Drucker verwenden, können Sie den folgenden Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="e4cf9-473">Im Abschnitt **Textabschnitt** im Feld **Etikettentext** geben Sie ZPL-Code für den erforderlichen Text ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="e4cf9-474">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="e4cf9-475">Im Abschnitt **Textabschnitt** im Feld **Etikettenfußzeile** geben Sie ZPL-Code für die erforderlichen Fußzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="e4cf9-476">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="e4cf9-477">Durch dieses Setup wird eine Kopie jedes Etiketts gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="e4cf9-478">Wenn Sie mehr Kopien benötigen (z. B. eine Kopie für jede Seite der Palette), legen Sie den **n**-Wert für den Abschnitt **\^PQn** in der Fußzeile auf die erforderliche Anzahl von Kopien fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="e4cf9-479">Um vier Kopien jedes Etiketts zu drucken, geben Sie beispielsweise **\^PQ4** an.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="e4cf9-480">Das erste Etikett kann jetzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="e4cf9-481">Erstellen Sie einen zweiten Layoutdatensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-482">**Etikettenlayout-ID:** *Palette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="e4cf9-483">**Beschreibung:** *Palette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="e4cf9-484">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-485">Wählen Sie im Aktionsbereich **Einstellungen für Wellenetikettzeile** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="e4cf9-486">Die Seite **Einstellungen für Wellenetikettzeile** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="e4cf9-487">Hier können Sie den dynamischen Teil des Etiketts konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="e4cf9-488">Fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-489">**Zeilen-ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="e4cf9-490">**Zeilentabellenname:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="e4cf9-491">**Zeilenstartposition:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="e4cf9-492">Dieses Feld definiert die vertikale Position, an der die Zeile im Etikett beginnt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="e4cf9-493">**Zeilenhöhe:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-493">**Row height:** *0*</span></span>

        <span data-ttu-id="e4cf9-494">Dieses Feld definiert die Höhe jeder Zeile (in Punkten) gemäß dem ZPL-Standard.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="e4cf9-495">Die Zeilenhöhe ist positiv für horizontale Etikette und negativ für vertikale Etikette.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="e4cf9-496">Da es in diesem Beispiel nur eine Zeile gibt, können Sie den Wert auf *0* (Null) festlegen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="e4cf9-497">**Zeilen pro Seite:** *1*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="e4cf9-498">Dieses Feld definiert die Anzahl der Zeilen, die auf jedes Etikett gedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4cf9-499">Durch dieses Setup wird für jeden Datensatz in der Wellenetikettentabelle ein separates ZPL-Etikett gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="e4cf9-500">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-500">Close the page.</span></span>
1. <span data-ttu-id="e4cf9-501">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e4cf9-502">Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-503">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-504">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-505">**Feld:** *Arbeitstyp*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e4cf9-506">**Kriterien:** *Entnahme*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="e4cf9-507">Diese Abfrage stellt sicher, dass nur Arbeitspositionen vom Entnahmetyp auf dem Etikett gedruckt werden und nicht Arbeitspositionen vom Einlagerungstyp.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="e4cf9-508">Wenn Sie die Frachtbrief-ID ausdrucken möchten, wählen Sie auf der Registerkarte **Verknüpfungen** die Tabelle **Arbeitspositionen** aus, und verknüpften Sie die Tabelle **Lieferungen** damit.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="e4cf9-509">Schließen Sie das Abfrage-Editor-Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4cf9-510">Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4cf9-511">Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie Code für die erforderliche Kopfzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="e4cf9-512">Wenn Sie beispielsweise Zebra-Drucker verwenden, können Sie den folgenden Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="e4cf9-513">Im Abschnitt **Textabschnitt** im Feld **Etikettentext** geben Sie ZPL-Code für den erforderlichen Text ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="e4cf9-514">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="e4cf9-515">Im Abschnitt **Textabschnitt** im Feld **Etikettenfußzeile** geben Sie ZPL-Code für die erforderlichen Fußzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="e4cf9-516">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="e4cf9-517">Durch dieses Setup wird eine Kopie jedes Etiketts gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="e4cf9-518">Wenn Sie mehr Kopien benötigen (z. B. eine Kopie für jede Seite der Palette), legen Sie den **n**-Wert für den Abschnitt **\^PQn** in der Fußzeile auf die erforderliche Anzahl von Kopien fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="e4cf9-519">Um vier Kopien jedes Etiketts zu drucken, geben Sie beispielsweise **\^PQ4** an.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="e4cf9-520">Das zweite Etikett kann jetzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="e4cf9-521">Erstellen Sie einen dritten Layoutdatensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-522">**Etikettenlayout-ID:** *Unterbrechung*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="e4cf9-523">**Beschreibung:** *Unterbrechungsetikett*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="e4cf9-524">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-525">Das Inforegister **Druckertextlayout** besteht aus drei Abschnitten, in denen Sie Druckercode schreiben können: **Kopfzeilenabschnitt**, **Textabschnitt** und **Fußzeilenabschnitt**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4cf9-526">Im Abschnitt **Kopfzeilenabschnitt** im Feld **Etikettenkopfzeile** geben Sie den ZPL-Code für die erforderliche Kopfzeile ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="e4cf9-527">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="e4cf9-528">Diesmal ist kein Textabschnitt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-528">This time, no body is required.</span></span> <span data-ttu-id="e4cf9-529">Geben Sie daher einfach den gewünschten Text in den Abschnitt **Fußzeilenabschnitt** ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="e4cf9-530">Hier ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="e4cf9-531">Das dritte Etikett kann jetzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4cf9-532">Dieses dritte Etikett ist ein Unterbrechungsetikett, das als Teiler zwischen Etikettenrollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="e4cf9-533">Zwei Wellenetikettentypen erstellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-533">Create two wave label types</span></span>

1. <span data-ttu-id="e4cf9-534">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettentypen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="e4cf9-535">Erstellen Sie einen Datensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-536">**Etikettentyp:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="e4cf9-537">**Beschreibung:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="e4cf9-538">Erstellen Sie einen zweiten Datensatz mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-539">**Etikettentyp:** *Palette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="e4cf9-540">**Beschreibung:** *Palette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="e4cf9-541">Einheitensequenzgruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="e4cf9-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="e4cf9-542">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Lagerort \> Einheitsnummernkreisgruppe**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="e4cf9-543">Wählen oder erstellen Sie eine Gruppe **Ea Box PL** (Einzelstücke Kiste/Palette).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="e4cf9-544">Für die Position **Kiste** legen Sie das Feld **Wellenetikettentyp** auf *Karton* fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="e4cf9-545">Für die Position **PL** (Palette) legen Sie das Feld **Wellenetikettentyp** auf *Palette* fest.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="e4cf9-546">Wellenetikettenvorlagen erstellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-546">Create wave label templates</span></span>

1. <span data-ttu-id="e4cf9-547">Wechseln Sie zu **Lagerortverwaltung \> Setup \> Dokumentrouting \> Wellenetikettenvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="e4cf9-548">Erstellen Sie eine Etikettenvorlage mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-549">**Etikettenvorlagenname:** *Kartonetikette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="e4cf9-550">**Beschreibung:** *Kartonetikette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="e4cf9-551">**Wellenschrittcode:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="e4cf9-552">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4cf9-553">Wählen Sie im Inforegister **Allgemein** im Feld **Wellenetikettentyp** einen Wert aus, wie z. B. *Karton*.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="e4cf9-554">Im Inforegister **Details zur Wellenetikettenvorlage** fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-555">**Etikettenlayout-ID:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4cf9-556">**Druckername:** Wählen Sie einen geeigneten ZPL-Drucker aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="e4cf9-557">**Abfrage ausführen:** *Ja* (Diese Einstellung ist optional, wird jedoch für eine optimale Leistung empfohlen.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="e4cf9-558">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-559">Optional: Wenn Sie ein kundenspezifisches Etikettendesign einrichten, müssen Sie eine Abfrage erstellen, um das Kundenkonto zu finden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="e4cf9-560">Im Inforegister **Details zur Wellenetikettenvorlage** wählen Sie **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="e4cf9-561">Fügen Sie dann im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-562">**Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e4cf9-563">**Abgeleitete Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e4cf9-564">**Feld:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="e4cf9-565">**Kriterien:** Geben Sie die relevante Kundenkontonummer ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="e4cf9-566">Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="e4cf9-567">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus, um das Dialogfeld des Abfrage-Editors für die gesamte Etikettenvorlage zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="e4cf9-568">Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Sortieren** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-569">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-570">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-571">**Feld:** *Referenzladungspositions-ID (Datensatz-ID)*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="e4cf9-572">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4cf9-573">Fügen Sie eine zweite Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-574">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-575">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-576">**Feld:** *Lieferungs-ID*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="e4cf9-577">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4cf9-578">Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4cf9-579">In einem Meldungsfeld werden Sie aufgefordert, den Vorgang zum Zurücksetzen der Gruppierung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="e4cf9-580">Wählen Sie **Ja** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e4cf9-581">Wählen Sie im Aktionsbereich **Wellenetikettenvorlagen-Gruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="e4cf9-582">Legen Sie im Dialogfeld **Wellenetiketten-Vorlagengruppe** für die Zeile, in der das Feld **Referenzfeldname** auf *Lieferungs-ID* festgelegt ist, die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="e4cf9-583">**Unterbrechungsetikett drucken:** Aktivieren Sie dieses Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="e4cf9-584">**Etikettenlayout-ID:** Wählen Sie ein Unterbrechungsetikett aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="e4cf9-585">(Wählen Sie zum Beispiel das Etikettenlayout *Unterbrechung* aus, dass Sie zuvor in diesem Szenario erstellt haben.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="e4cf9-586">**Druckername:** Wählen Sie den Drucker für das Unterbrechungsetikett aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="e4cf9-587">(Normalerweise sollten Sie zum Teilen von Etikettenrollen denselben Drucker auswählen, der im Inforegister **Details zur Wellenetikettenvorlage** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="e4cf9-588">Es sind jedoch andere Szenarien möglich.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="e4cf9-589">Für die Zeile, in der das Feld **Referenzfeldname** auf *Referenzladungspositions-ID* festgelegt ist, aktivieren Sie das Kontrollkästchen **Etiketten-Build-ID**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4cf9-590">Dieses Setup erstellt eine Etikettensequenz („Karton 1 von X“) pro Ladeposition während der gesamten Welle, unabhängig vom Setup der Arbeitsgruppierung.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="e4cf9-591">Diese Etikettensequenz kann auf ein Etikettenlayout gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="e4cf9-592">Außerdem werden Etiketten für verschiedene Lieferungen durch das ausgewählte Unterbrechungsetikett getrennt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="e4cf9-593">Wählen Sie **OK** aus, um das Dialogfeld **Wellenetiketten-Vorlagengruppe** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="e4cf9-594">Erstellen Sie eine zweite Etikettenvorlage mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-595">**Etikettenvorlagenname:** *Palettenetikette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="e4cf9-596">**Beschreibung:** *Palettenetikette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="e4cf9-597">**Wellenschrittcode:** *Palette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="e4cf9-598">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4cf9-599">Wählen Sie im Inforegister **Allgemein** im Feld **Wellenetikettentyp** einen Wert aus, wie z. B. *Palette*.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="e4cf9-600">Im Inforegister **Details zur Wellenetikettenvorlage** fügen Sie eine Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-601">**Etikettenlayout-ID:** *Palette*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="e4cf9-602">**Druckername:** Wählen Sie einen geeigneten ZPL-Drucker aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="e4cf9-603">**Abfrage ausführen:** *Ja* (Diese Einstellung ist optional, wird jedoch für eine optimale Leistung empfohlen.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="e4cf9-604">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4cf9-605">Optional: Wenn Sie ein kundenspezifisches Etikettendesign einrichten, müssen Sie eine Abfrage erstellen, um das Kundenkonto zu finden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="e4cf9-606">Im Inforegister **Details zur Wellenetikettenvorlage** wählen Sie **Abfrage bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="e4cf9-607">Fügen Sie dann im Abfrage-Editor-Dialogfeld auf der Registerkarte **Bereich** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-608">**Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e4cf9-609">**Abgeleitete Tabelle:** *Lieferungen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e4cf9-610">**Feld:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="e4cf9-611">**Kriterien:** Geben Sie die relevante Kundenkontonummer ein.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="e4cf9-612">Wenn Sie fertig sind, wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="e4cf9-613">Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus, um das Dialogfeld des Abfrage-Editors für die gesamte Etikettenvorlage zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="e4cf9-614">Fügen Sie im Abfrage-Editor-Dialogfeld auf der Registerkarte **Sortieren** eine Zeile mit den folgenden Einstellungen ein:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-615">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-616">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-617">**Feld:** *Referenzladungspositions-ID (Datensatz-ID)*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="e4cf9-618">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4cf9-619">Fügen Sie eine zweite Zeile mit den folgenden Einstellungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-620">**Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-621">**Abgeleitete Tabelle:** *Arbeitspositionen*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4cf9-622">**Feld:** *Lieferungs-ID*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="e4cf9-623">**Suchrichtigung:** *Aufsteigend*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4cf9-624">Wählen Sie **OK** aus, um das Dialogfeld des Abfrage-Editors zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4cf9-625">In einem Meldungsfeld werden Sie aufgefordert, den Vorgang zum Zurücksetzen der Gruppierung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="e4cf9-626">Wählen Sie **Ja** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e4cf9-627">Wählen Sie im Aktionsbereich **Wellenetikettenvorlagen-Gruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="e4cf9-628">Legen Sie im Dialogfeld **Wellenetiketten-Vorlagengruppe** für die Zeile, in der das Feld **Referenzfeldname** auf *Lieferungs-ID* festgelegt ist, die folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="e4cf9-629">**Unterbrechungsetikett drucken:** Aktivieren Sie dieses Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="e4cf9-630">**Etikettenlayout-ID:** Wählen Sie ein Unterbrechungsetikett aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="e4cf9-631">(Wählen Sie zum Beispiel das Etikettenlayout *Unterbrechung* aus, dass Sie zuvor in diesem Szenario erstellt haben.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="e4cf9-632">**Druckername:** Wählen Sie den Drucker für das Unterbrechungsetikett aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="e4cf9-633">(Normalerweise sollten Sie zum Teilen von Etikettenrollen denselben Drucker auswählen, der im Inforegister **Details zur Wellenetikettenvorlage** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="e4cf9-634">Es sind jedoch andere Szenarien möglich.)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="e4cf9-635">Für die Zeile, in der das Feld **Referenzfeldname** auf *Referenzladungspositions-ID* festgelegt ist, aktivieren Sie das Kontrollkästchen **Etiketten-Build-ID**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4cf9-636">Dieses Setup erstellt eine Etikettensequenz („Karton 1 von X“) pro Ladeposition während der gesamten Welle, unabhängig vom Setup der Arbeitsgruppierung.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="e4cf9-637">Diese Etikettensequenz kann auf ein Etikettenlayout gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="e4cf9-638">Außerdem werden Etiketten für verschiedene Lieferungen durch das ausgewählte Unterbrechungsetikett getrennt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="e4cf9-639">Nummernkreiserweiterungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e4cf9-639">Configure number sequence extensions</span></span>

<span data-ttu-id="e4cf9-640">Nummernkreiserweiterungen steuern die GS1-Konformität bestimmter Nummernkreise.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="e4cf9-641">Diese Konfiguration ist für das aktuelle Szenario optional.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="e4cf9-642">Weitere Informationen und Konfigurationsanweisungen finden Sie unter [Nummernkreiserweiterungen konfigurieren](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="e4cf9-643">Einen Auftrag erstellen und ihn für den Lagerort freigeben</span><span class="sxs-lookup"><span data-stu-id="e4cf9-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="e4cf9-644">Gehen Sie zu **Vertrieb und Marketing \> Auftrag \> Alle Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="e4cf9-645">Erstellen Sie einen Auftrag mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e4cf9-646">**Debitorenkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e4cf9-647">**Lagerort:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4cf9-648">Zwei Auftragspositionen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="e4cf9-649">Auftragsposition 1:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-649">Sales order line 1:</span></span>

        - <span data-ttu-id="e4cf9-650">**Artikelnummer** *A001*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e4cf9-651">**Menge** *9024*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="e4cf9-652">**Einheit:** *ea* (9024 Einzelstücke = 376 Kisten = 47 Paletten)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="e4cf9-653">Auftragsposition 2:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-653">Sales order line 2:</span></span>

        - <span data-ttu-id="e4cf9-654">**Artikelnummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e4cf9-655">**Menge** *9016*</span><span class="sxs-lookup"><span data-stu-id="e4cf9-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="e4cf9-656">**Einheit:** *ea* (9016 Einzelstücke = 322 Kisten = 46 Paletten)</span><span class="sxs-lookup"><span data-stu-id="e4cf9-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4cf9-657">Die hier angegebenen Artikel und Mengen sind nur Beispiele.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="e4cf9-658">Sie müssen die zuvor definierte Einheitsnummernkreisgruppe verwenden, für sie müssen entsprechende Einheitsumrechnungen von *ea* (Einzelstück) zu *Box* (Kiste) zu *PL* (Palette) definiert sein, und sie müssen Bestand im Lager haben *62*.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="e4cf9-659">Weitere Informationen finden Sie unter [Maßeinheit und Lagerhaltungsrichtlinien](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="e4cf9-660">Wählen Sie Auftragsposition 1 aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-660">Select sales order line 1.</span></span> <span data-ttu-id="e4cf9-661">Wählen Sie dann im Abschnitt **Auftragsposition** im Menü **Bestand** die Option **Reservierungen** aus.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="e4cf9-662">Wählen Sie auf der Seite **Reservierung** im Aktionsbereich die Option **Los reservieren** aus, und schließen Sie dann die Seite.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="e4cf9-663">Wiederholen Sie die Schritte 4 und 5 für Auftragsposition 2.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="e4cf9-664">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** auf **Lagerortfreigabe**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e4cf9-665">Folgende Ereignisse treten auf:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-665">The following events occur:</span></span> 

    - <span data-ttu-id="e4cf9-666">Das System verarbeitet die erstellte Lieferung mithilfe der Vorlage, die den Etikettendruckschritt enthält.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="e4cf9-667">Das Etikettenlayout wird verwendet, um das Format des Etiketts zu definieren. Das Ergebnis ist ein Etikett, das auf dem in der Etikettenvorlage ausgewählten Drucker gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="e4cf9-668">Wellenetiketten werden generiert und gedruckt.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="e4cf9-669">Die Anzahl der Etiketten entspricht der Anzahl der Kartons (in diesem Beispiel 376 Kistenetiketten für Position 1, 322 Kistenetiketten für Position 2, 47 PL-Etiketten für Position 1, 47 PL-Etiketten für Position 2 und zwei Unterbrechungsetiketten mit der Lieferungs-ID).</span><span class="sxs-lookup"><span data-stu-id="e4cf9-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="e4cf9-670">Für die Lieferung wird eine neue Frachtbrief-ID generiert.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="e4cf9-671">Wenn Sie die Nummernkreiserweiterungen konfiguriert haben, folgen die Wellenetikett-IDs dem Zahlenformat **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="e4cf9-672">Sie können Wellenetiketten von den folgenden Seiten anzeigen und erneut drucken:</span><span class="sxs-lookup"><span data-stu-id="e4cf9-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="e4cf9-673">Alle Lieferungen \> Lieferdetails</span><span class="sxs-lookup"><span data-stu-id="e4cf9-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="e4cf9-674">Alle Ladungen \> Ladungsdetails</span><span class="sxs-lookup"><span data-stu-id="e4cf9-674">All loads \> Load details</span></span>
- <span data-ttu-id="e4cf9-675">Alle Wellen</span><span class="sxs-lookup"><span data-stu-id="e4cf9-675">All waves</span></span>
- <span data-ttu-id="e4cf9-676">Serienetiketten</span><span class="sxs-lookup"><span data-stu-id="e4cf9-676">Wave labels</span></span>
- <span data-ttu-id="e4cf9-677">Wellenbeschriftungsverlauf</span><span class="sxs-lookup"><span data-stu-id="e4cf9-677">Wave label history</span></span>

<span data-ttu-id="e4cf9-678">Für die meisten dieser Seiten finden Sie die relevante Funktion durch Auswahl der **Wellenetiketten** in der Gruppe **Zugehörige Informationen** auf der Registerkarte **Lieferungen** des Aktionsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e4cf9-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
