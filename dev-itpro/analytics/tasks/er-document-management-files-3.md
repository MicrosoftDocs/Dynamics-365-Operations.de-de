--- 
title: "Erstellen von Format zur Verwendung von Dokumentverwaltungsdateien in Formatausgaben für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5548839c4d394d45cfb39da50ca78dab4b4e08e4
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="b109c-103">Erstellen von Format zur Verwendung von Dokumentverwaltungsdateien in Formatausgaben für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="b109c-103">Create format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b109c-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="b109c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b109c-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b109c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b109c-106">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 2: Erweitern des Datenmodells)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="b109c-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="b109c-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b109c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="b109c-108">Erstellen eines Formats zur Rechnungsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="b109c-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="b109c-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="b109c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b109c-110">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="b109c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b109c-111">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".</span><span class="sxs-lookup"><span data-stu-id="b109c-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="b109c-112">Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="b109c-113">Sie erstellen ein Format, um elektronische Nachrichten mit Informationen zu allen Dateien zu generieren, die einem Auftrag zugeordnet wurden, der einer elektronischen Rechnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b109c-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="b109c-114">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b109c-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="b109c-115">Geben Sie im Feld "Neu" "Format basierend auf Debitorenrechnungsmodell (benutzerdefiniert)" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="b109c-116">Geben Sie im Feld Name "Beispielnachricht für elektronische Rechnung" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="b109c-117">Beispielnachricht für elektronische Rechnung</span><span class="sxs-lookup"><span data-stu-id="b109c-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="b109c-118">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="b109c-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="b109c-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="b109c-120">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="b109c-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="b109c-121">Entwerfen Sie ein Format, um Anlagen in einem MIME-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b109c-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="b109c-122">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="b109c-122">Click Designer.</span></span>
2. <span data-ttu-id="b109c-123">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b109c-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="b109c-124">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="b109c-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="b109c-125">Geben Sie im Feld "Name" "Rechnung" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="b109c-126">Rechnung</span><span class="sxs-lookup"><span data-stu-id="b109c-126">Invoice</span></span>  
5. <span data-ttu-id="b109c-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-127">Click OK.</span></span>
6. <span data-ttu-id="b109c-128">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b109c-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="b109c-129">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="b109c-130">Geben Sie im Feld "Name" "SalesOrder" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="b109c-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="b109c-131">SalesOrder</span></span>  
9. <span data-ttu-id="b109c-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-132">Click OK.</span></span>
10. <span data-ttu-id="b109c-133">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b109c-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="b109c-134">Geben Sie im Feld "Name" "InvoiceNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="b109c-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="b109c-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="b109c-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-136">Click OK.</span></span>
13. <span data-ttu-id="b109c-137">Klicken Sie auf "Attribut hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b109c-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="b109c-138">Geben Sie im Feld "Name" "InvoiceAmount" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="b109c-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="b109c-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="b109c-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-140">Click OK.</span></span>
16. <span data-ttu-id="b109c-141">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b109c-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="b109c-142">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="b109c-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="b109c-143">Geben Sie im Feld "Name" "EnclosedDocs" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="b109c-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="b109c-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="b109c-145">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-145">Click OK.</span></span>
20. <span data-ttu-id="b109c-146">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="b109c-147">Klicken Sie auf "Element hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b109c-147">Click Add Element.</span></span>
22. <span data-ttu-id="b109c-148">Geben Sie im Feld "Name" 'Dokument' ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="b109c-149">Dokument</span><span class="sxs-lookup"><span data-stu-id="b109c-149">Document</span></span>  
23. <span data-ttu-id="b109c-150">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-150">Click OK.</span></span>
24. <span data-ttu-id="b109c-151">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="b109c-152">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b109c-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="b109c-153">Wählen Sie in der Struktur 'XML\Attribute' aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="b109c-154">Geben Sie im Feld "Name" "FileName" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="b109c-155">Dateiname</span><span class="sxs-lookup"><span data-stu-id="b109c-155">FileName</span></span>  
28. <span data-ttu-id="b109c-156">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-156">Click OK.</span></span>
29. <span data-ttu-id="b109c-157">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b109c-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="b109c-158">Wählen Sie in der Struktur den Knoten 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="b109c-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="b109c-159">Geben Sie im Feld "Name" den Wert "FileContent" ein.</span><span class="sxs-lookup"><span data-stu-id="b109c-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="b109c-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="b109c-160">FileContent</span></span>  
32. <span data-ttu-id="b109c-161">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-161">Click OK.</span></span>
33. <span data-ttu-id="b109c-162">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileContent" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="b109c-163">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b109c-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="b109c-164">Wählen Sie in der Struktur 'Text\Base64' aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="b109c-165">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b109c-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="b109c-166">Zuordnen von Formatelementen zum Datenmodell als Datenquelle</span><span class="sxs-lookup"><span data-stu-id="b109c-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="b109c-167">Wählen Sie in der Strukturdarstellung "Rechnung\SalesOrder" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="b109c-168">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="b109c-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="b109c-169">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="b109c-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="b109c-170">Wählen Sie in der Strukturdarstellung "Modell\Auftragsnummer(SalesId)") aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="b109c-171">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b109c-171">Click Bind.</span></span>
6. <span data-ttu-id="b109c-172">Wählen Sie in der Strukturdarstellung "Rechnung\InvoiceNumber" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="b109c-173">Erweitern Sie in der Strukturdarstellung "Modell\Basisrechnung(InvoiceBase)".</span><span class="sxs-lookup"><span data-stu-id="b109c-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="b109c-174">Wählen Sie in der Struktur 'Modell\Basisrechnung(InvoiceBase)\Rechnungsnummer(Id)' aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="b109c-175">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b109c-175">Click Bind.</span></span>
10. <span data-ttu-id="b109c-176">Wählen Sie in der Strukturdarstellung "Rechnung\InvoiceAmount" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="b109c-177">Wählen Sie in der Struktur 'Modell\Basisrechnung(InvoiceBase)\Rechnungsbetrag(Amount)' aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="b109c-178">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b109c-178">Click Bind.</span></span>
13. <span data-ttu-id="b109c-179">Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".</span><span class="sxs-lookup"><span data-stu-id="b109c-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="b109c-180">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiinhalt" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="b109c-181">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileContent\Base64" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="b109c-182">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b109c-182">Click Bind.</span></span>
17. <span data-ttu-id="b109c-183">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiname" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="b109c-184">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument\FileName" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="b109c-185">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b109c-185">Click Bind.</span></span>
20. <span data-ttu-id="b109c-186">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge " aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="b109c-187">Wählen Sie in der Strukturdarstellung "Rechnung\EnclosedDocs\Dokument" aus.</span><span class="sxs-lookup"><span data-stu-id="b109c-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="b109c-188">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="b109c-188">Click Bind.</span></span>
23. <span data-ttu-id="b109c-189">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b109c-189">Click Save.</span></span>
24. <span data-ttu-id="b109c-190">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b109c-190">Close the page.</span></span>


