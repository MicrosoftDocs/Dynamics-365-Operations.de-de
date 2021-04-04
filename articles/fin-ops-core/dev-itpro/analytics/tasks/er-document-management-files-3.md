---
title: 'ER Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 3: Format erstellen)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat für die Verwendung von Dokumentenverwaltungsdateien in der EB-Ausgabe konfigurieren. (Teil 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec1ebc15cd980734aebec63d6758404868c1e36
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559748"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="0e8f6-104">ER Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 3: Format erstellen)</span><span class="sxs-lookup"><span data-stu-id="0e8f6-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e8f6-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0e8f6-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="0e8f6-107">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden „.ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 2: Erweitern des Datenmodells)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="0e8f6-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="0e8f6-109">Erstellen eines Formats zur Rechnungsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="0e8f6-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="0e8f6-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0e8f6-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0e8f6-112">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="0e8f6-113">Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="0e8f6-114">Sie erstellen ein Format, um elektronische Nachrichten mit Informationen zu allen Dateien zu generieren, die einem Auftrag zugeordnet wurden, der einer elektronischen Rechnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="0e8f6-115">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="0e8f6-116">Geben Sie im Feld "Neu" "Format basierend auf Debitorenrechnungsmodell (benutzerdefiniert)" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="0e8f6-117">Geben Sie im Feld Name "Beispielnachricht für elektronische Rechnung" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="0e8f6-118">Beispielnachricht für elektronische Rechnung</span><span class="sxs-lookup"><span data-stu-id="0e8f6-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="0e8f6-119">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="0e8f6-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="0e8f6-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="0e8f6-121">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="0e8f6-122">Entwerfen Sie ein Format, um Anlagen in einem MIME-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="0e8f6-123">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-123">Click Designer.</span></span>
2. <span data-ttu-id="0e8f6-124">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="0e8f6-125">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="0e8f6-126">Geben Sie im Feld "Name" "Rechnung" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="0e8f6-127">Rechnung</span><span class="sxs-lookup"><span data-stu-id="0e8f6-127">Invoice</span></span>  
5. <span data-ttu-id="0e8f6-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-128">Click OK.</span></span>
6. <span data-ttu-id="0e8f6-129">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="0e8f6-130">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="0e8f6-131">Geben Sie im Feld "Name" "SalesOrder" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="0e8f6-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="0e8f6-132">SalesOrder</span></span>  
9. <span data-ttu-id="0e8f6-133">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-133">Click OK.</span></span>
10. <span data-ttu-id="0e8f6-134">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="0e8f6-135">Geben Sie im Feld "Name" "InvoiceNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="0e8f6-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="0e8f6-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="0e8f6-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-137">Click OK.</span></span>
13. <span data-ttu-id="0e8f6-138">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="0e8f6-139">Geben Sie im Feld "Name" "InvoiceAmount" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="0e8f6-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="0e8f6-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="0e8f6-141">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-141">Click OK.</span></span>
16. <span data-ttu-id="0e8f6-142">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="0e8f6-143">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="0e8f6-144">Geben Sie im Feld "Name" "EnclosedDocs" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="0e8f6-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="0e8f6-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="0e8f6-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-146">Click OK.</span></span>
20. <span data-ttu-id="0e8f6-147">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="0e8f6-148">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-148">Click Add Element.</span></span>
22. <span data-ttu-id="0e8f6-149">Geben Sie im Feld "Name" 'Dokument' ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="0e8f6-150">Dokument</span><span class="sxs-lookup"><span data-stu-id="0e8f6-150">Document</span></span>  
23. <span data-ttu-id="0e8f6-151">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-151">Click OK.</span></span>
24. <span data-ttu-id="0e8f6-152">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="0e8f6-153">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="0e8f6-154">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="0e8f6-155">Geben Sie im Feld "Name" "FileName" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="0e8f6-156">Dateiname</span><span class="sxs-lookup"><span data-stu-id="0e8f6-156">FileName</span></span>  
28. <span data-ttu-id="0e8f6-157">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-157">Click OK.</span></span>
29. <span data-ttu-id="0e8f6-158">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="0e8f6-159">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="0e8f6-160">Geben Sie im Feld "Name" den Wert "FileContent" ein.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="0e8f6-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="0e8f6-161">FileContent</span></span>  
32. <span data-ttu-id="0e8f6-162">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-162">Click OK.</span></span>
33. <span data-ttu-id="0e8f6-163">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileContent" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="0e8f6-164">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="0e8f6-165">Wählen Sie in der Struktur 'Text\Base64' aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="0e8f6-166">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="0e8f6-167">Zuordnen von Formatelementen zum Datenmodell als Datenquelle</span><span class="sxs-lookup"><span data-stu-id="0e8f6-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="0e8f6-168">Wählen Sie in der Strukturdarstellung "Rechnung\SalesOrder" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="0e8f6-169">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="0e8f6-170">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="0e8f6-171">Wählen Sie in der Strukturdarstellung "Modell\Auftragsnummer(SalesId)" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="0e8f6-172">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-172">Click Bind.</span></span>
6. <span data-ttu-id="0e8f6-173">Wählen Sie in der Strukturdarstellung "Rechnung\InvoiceNumber" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="0e8f6-174">Erweitern Sie in der Strukturdarstellung "Modell\Basisrechnung(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="0e8f6-175">Wählen Sie in der Struktur 'Modell\Basisrechnung(InvoiceBase)\Rechnungsnummer(Id)' aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="0e8f6-176">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-176">Click Bind.</span></span>
10. <span data-ttu-id="0e8f6-177">Wählen Sie in der Strukturdarstellung "Rechnung\InvoiceAmount" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="0e8f6-178">Wählen Sie in der Struktur 'Modell\Basisrechnung(InvoiceBase)\Rechnungsbetrag(Amount)' aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="0e8f6-179">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-179">Click Bind.</span></span>
13. <span data-ttu-id="0e8f6-180">Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="0e8f6-181">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiinhalt" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="0e8f6-182">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileContent\Base64" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="0e8f6-183">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-183">Click Bind.</span></span>
17. <span data-ttu-id="0e8f6-184">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiname" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="0e8f6-185">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileName" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="0e8f6-186">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-186">Click Bind.</span></span>
20. <span data-ttu-id="0e8f6-187">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge " aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="0e8f6-188">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument" aus.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="0e8f6-189">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-189">Click Bind.</span></span>
23. <span data-ttu-id="0e8f6-190">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0e8f6-190">Click Save.</span></span>
24. <span data-ttu-id="0e8f6-191">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]