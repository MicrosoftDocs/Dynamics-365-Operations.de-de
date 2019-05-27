---
title: Modelle und Zuordnungen ändern, um Dokumente zu generieren, die Anwendungsdaten haben
description: Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 2 - Dokumente erstellen).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 580f00faf6694dc2da476ffa75f995d9a24e0f8b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551275"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="5c435-103">Modelle und Zuordnungen ändern, um Dokumente zu generieren, die Anwendungsdaten haben</span><span class="sxs-lookup"><span data-stu-id="5c435-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c435-104">Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 2: Dokumente erstellen).</span><span class="sxs-lookup"><span data-stu-id="5c435-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="5c435-105">Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="5c435-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="5c435-106">In diesem Verfahren ändern Sie die ER-Konfigurationen, um sie derzeit nicht verwenden, um elektronische Dokumente zu erzeugen, wohingegen Anwendungsdaten auch zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5c435-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="5c435-107">Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="5c435-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="5c435-108">Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c435-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="5c435-109">Datenmodell ändern</span><span class="sxs-lookup"><span data-stu-id="5c435-109">Modify data model</span></span>
1. <span data-ttu-id="5c435-110">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5c435-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5c435-111">Erweitern Sie 'Intrastatmodell' in der Struktur (Modell).</span><span class="sxs-lookup"><span data-stu-id="5c435-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="5c435-112">Erweitern Sie das Datenmodell nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="5c435-112">You will extend how you use the data model.</span></span> <span data-ttu-id="5c435-113">Neben der Verwendung als Datenquelle, um den Intrastat-Bericht zu generieren, wird das Datenmodell verwendet, um Details zum Intrastat-Berichts-Prozess zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="5c435-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="5c435-114">Die Details werden dann verwendet, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5c435-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="5c435-115">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="5c435-115">Click Designer.</span></span>
4. <span data-ttu-id="5c435-116">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5c435-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="5c435-117">Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="5c435-118">Geben Sie im Feld Typ Für Bewertungsdatenaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="5c435-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="5c435-119">Aktualisierung der Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="5c435-119">For application data update</span></span>  
7. <span data-ttu-id="5c435-120">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-120">Click Add.</span></span>
8. <span data-ttu-id="5c435-121">Wählen Sie in der Strukturdarstellung "für Bewerbungsdatenenaktualisierung " aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="5c435-122">Dieser neue Stammartikel wird hinzugefügt, um dem Datenfluss zum Bewegen von Daten vom Intrastat-Bericht (Als Datenquelle verwendet) für die Bewerbungstabellen (das Aktualisierungsziel) zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5c435-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="5c435-123">Beachten Sie, dass verschiedene Stammartikel zum Abrufen von Daten verwendet werden müssen für die ausgehenden Dokumente und zum Abrufen von Daten vom Dokuments, das verwendet wird, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5c435-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="5c435-124">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5c435-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="5c435-125">Geben Sie im Feld Typ Archivkopfzeile ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="5c435-126">Archivkopfzeile</span><span class="sxs-lookup"><span data-stu-id="5c435-126">Archive header</span></span>  
11. <span data-ttu-id="5c435-127">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="5c435-128">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-128">Click Add.</span></span>
    * <span data-ttu-id="5c435-129">Da ein Datensatz für jeden Intrastat-Bericht erstellt wird,, der erzeugt werden soll, müssen Sie einen neuen Artikel dafür erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c435-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="5c435-130">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5c435-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="5c435-131">Geben Sie im Feld "Name" "Dateiname" ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="5c435-132">Dateiname</span><span class="sxs-lookup"><span data-stu-id="5c435-132">File name</span></span>  
15. <span data-ttu-id="5c435-133">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="5c435-134">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-134">Click Add.</span></span>
17. <span data-ttu-id="5c435-135">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5c435-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="5c435-136">Geben Sie im Feld Name die Anzahl Zeilen ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="5c435-137">Anzahl Positionen</span><span class="sxs-lookup"><span data-stu-id="5c435-137">Number of lines</span></span>  
19. <span data-ttu-id="5c435-138">Wählen Sie im Artikelfeld Integer aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="5c435-139">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-139">Click Add.</span></span>
    * <span data-ttu-id="5c435-140">Fügen Sie diesen Artikel hinzu, um die Anzahl von Intrastat-Buchungen anzugeben, die während der aktuellen Generierung eines Berichts gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="5c435-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="5c435-141">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5c435-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="5c435-142">Geben Sie im Feld Typ Archivzeilen ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="5c435-143">Archivieren von Positionen</span><span class="sxs-lookup"><span data-stu-id="5c435-143">Archive lines</span></span>  
23. <span data-ttu-id="5c435-144">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="5c435-145">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-145">Click Add.</span></span>
    * <span data-ttu-id="5c435-146">Fügen Sie diesen Artikel hinzu, um die Anzahl von Intrastat-Buchungen anzugeben, die während der aktuellen Generierung eines Berichts gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="5c435-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="5c435-147">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5c435-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="5c435-148">Geben Sie im Feld Namen "Amount" ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="5c435-149">Dauer</span><span class="sxs-lookup"><span data-stu-id="5c435-149">Amount</span></span>  
27. <span data-ttu-id="5c435-150">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="5c435-151">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-151">Click Add.</span></span>
29. <span data-ttu-id="5c435-152">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5c435-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="5c435-153">Geben Sie im Feld Typ Waren Rec ID ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="5c435-154">Warendatensatz-ID</span><span class="sxs-lookup"><span data-stu-id="5c435-154">Commodity rec id</span></span>  
31. <span data-ttu-id="5c435-155">Wählen Sie im Feld "Artikeltyp" 'Int64 aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="5c435-156">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-156">Click Add.</span></span>
33. <span data-ttu-id="5c435-157">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="5c435-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="5c435-158">Geben Sie im Feld Typ Artikelnummer ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="5c435-159">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="5c435-159">Item number</span></span>  
35. <span data-ttu-id="5c435-160">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="5c435-161">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-161">Click Add.</span></span>
37. <span data-ttu-id="5c435-162">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5c435-162">Click Save.</span></span>
38. <span data-ttu-id="5c435-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5c435-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="5c435-164">Modellzuordnung ändern</span><span class="sxs-lookup"><span data-stu-id="5c435-164">Modify model mapping</span></span>
1. <span data-ttu-id="5c435-165">Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="5c435-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="5c435-166">Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Zuordnung)" aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="5c435-167">Ändern Sie die bestehende Zuordnung, um die Bewerbungsdatenenaktualisierung zu starten und Intrastat-Berichts-Details zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="5c435-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="5c435-168">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="5c435-168">Click Designer.</span></span>
4. <span data-ttu-id="5c435-169">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="5c435-169">Click New.</span></span>
5. <span data-ttu-id="5c435-170">Geben Sie im Feld Typ Archiv aktualisieren ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="5c435-171">Archiv aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5c435-171">Update archive</span></span>  
6. <span data-ttu-id="5c435-172">Wählen Sie im Feld Richtung Destination nach aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="5c435-173">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5c435-173">Click Save.</span></span>
    * <span data-ttu-id="5c435-174">Dieser neue Zuordung definiert den Datenfluss zum Bewegen von Daten (Intrastat-Bericht) vom Datenmodell zur Bewerbungstabelle (das Aktualisierungsziel).</span><span class="sxs-lookup"><span data-stu-id="5c435-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="5c435-175">Beachten Sie, dass Stammartikel des anderen Modells verwendet werden müssen, um Daten aus der Anwendung für den Berichterstellungsprozess und die Daten vom Datenmodell Sie anschließend die Möglichkeit für die Bewerbungsdatenenaktualisierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5c435-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="5c435-176">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="5c435-176">Click Designer.</span></span>
9. <span data-ttu-id="5c435-177">Wählen Sie in der Strukturdarstellung Datenmodell\Datenmodell aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="5c435-178">Die erforderliche Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-178">Add the required data source.</span></span> <span data-ttu-id="5c435-179">Dies ist das Datenmodell, das Details der gemeldeten Intrastat-Buchungen enthält, die archiviert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5c435-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="5c435-180">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="5c435-180">Click Add root.</span></span>
11. <span data-ttu-id="5c435-181">Geben Sie im Feld Namen die Modelart ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="5c435-182">Modell</span><span class="sxs-lookup"><span data-stu-id="5c435-182">model</span></span>  
12. <span data-ttu-id="5c435-183">Wählen Sie im Definitionsfeld den Wert Für Anwendungsdatenaktualisierung aus oder geben Sie diesen ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="5c435-184">Aktualisierung der Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="5c435-184">For application data update</span></span>  
13. <span data-ttu-id="5c435-185">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5c435-185">Click OK.</span></span>
14. <span data-ttu-id="5c435-186">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="5c435-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="5c435-187">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="5c435-188">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="5c435-189">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-189">Click Add.</span></span>
    * <span data-ttu-id="5c435-190">Da Sie Intrastat-Buchungen für das gemeldete Chargenattribut archivieren möchten, muss die entsprechende Datenquelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5c435-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="5c435-191">Geben Sie im Feld Name den Typ Auzählungszeile ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="5c435-192">Aufgezählte Positionen</span><span class="sxs-lookup"><span data-stu-id="5c435-192">Enumerated lines</span></span>  
19. <span data-ttu-id="5c435-193">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c435-193">Click Edit formula.</span></span>
20. <span data-ttu-id="5c435-194">Wählen Sie in der Struktur Liste\AUFZÄHLUNG aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="5c435-195">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-195">Click Add function.</span></span>
22. <span data-ttu-id="5c435-196">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="5c435-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="5c435-197">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="5c435-198">Wählen Sie in der Struktur Modell\ArchivkopfzeileArchivzeilen aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="5c435-199">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5c435-199">Click Add data source.</span></span>
26. <span data-ttu-id="5c435-200">Im Formelfeld bestimmt geben Sie "AUFZÄHLUNG (Modell Archivkopfzeile, Archivzeilen) ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="5c435-201">AUFZÄHLEN (Modell. Archivpositionen, Archivzeilen)</span><span class="sxs-lookup"><span data-stu-id="5c435-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="5c435-202">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5c435-202">Click Save.</span></span>
28. <span data-ttu-id="5c435-203">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5c435-203">Close the page.</span></span>
29. <span data-ttu-id="5c435-204">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5c435-204">Click OK.</span></span>
30. <span data-ttu-id="5c435-205">Klicken Sie Destination hinzfügen aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-205">Click Add destination.</span></span>
    * <span data-ttu-id="5c435-206">Fügen Sie der Bewerbungstabellen nach Bedarf hinzu, die Aktualisierungen benötigen, u, Details der gemeldeten Intrastat-Buchungen zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="5c435-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="5c435-207">Geben Sie im Feld den Archivtyp ein..</span><span class="sxs-lookup"><span data-stu-id="5c435-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="5c435-208">Archiv</span><span class="sxs-lookup"><span data-stu-id="5c435-208">Archive</span></span>  
32. <span data-ttu-id="5c435-209">Geben Sie im Feld Tabelle den Typ IntrastatArchiveGeneral ein.</span><span class="sxs-lookup"><span data-stu-id="5c435-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="5c435-210">Formular "IntrastatArchiveGeneral"</span><span class="sxs-lookup"><span data-stu-id="5c435-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="5c435-211">Behalten Sie die Belegaktion "Einfügen", sodass Sie Datensätze für das Detailarchivierens jedes Intrastat-Berichts-Prozesses hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="5c435-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="5c435-212">Wählen Sie "Ja" im Feld Beleg-Infoprotokoll.</span><span class="sxs-lookup"><span data-stu-id="5c435-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="5c435-213">Wählen Sie die Option Ja aus, um Informationen zu Problemen mit der Bewerbungsdatenenaktualisierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5c435-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="5c435-214">Wählen Sie Ja im Feld Belegaktionsüberprüfungsfeld aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="5c435-215">Wählen Sie die Option Ja aus, um leere Prüfungsfehler zum Feld "Intrastat-Archiv ID-" zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="5c435-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="5c435-216">Dieses erfolgt, nachdem Datensätze hinzugefügt wurden, basierend auf den Einstellungen der Nummernkreise, die für diese Tabelle in der Außenhandelparameterform konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5c435-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="5c435-217">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5c435-217">Click OK.</span></span>
    * <span data-ttu-id="5c435-218">Binden Sie Elemente der hinzugefügten Datenquelle (das gefilterte Modell auf Basis des ausgewählten Stammartikel) mit Elementen des hinzugefügten Ziels.</span><span class="sxs-lookup"><span data-stu-id="5c435-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="5c435-219">In der Struktur erweitern Sie Archiv.</span><span class="sxs-lookup"><span data-stu-id="5c435-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="5c435-220">In der Struktur erweitern Sie Archiv\<Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="5c435-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="5c435-221">In der Struktur erweitern Sie Archiv\<BeziehungenIntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="5c435-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="5c435-222">Wählen Sie in der Struktur Archiv\<BeziehungenIntrastat\ArchiveDetail\Betrag (AmountMST).</span><span class="sxs-lookup"><span data-stu-id="5c435-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="5c435-223">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen.</span><span class="sxs-lookup"><span data-stu-id="5c435-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="5c435-224">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert.</span><span class="sxs-lookup"><span data-stu-id="5c435-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="5c435-225">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Betrag.</span><span class="sxs-lookup"><span data-stu-id="5c435-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="5c435-226">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="5c435-226">Click Bind.</span></span>
44. <span data-ttu-id="5c435-227">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetail\Waren(IntrastatCommodity).</span><span class="sxs-lookup"><span data-stu-id="5c435-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="5c435-228">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Waren Rec.-ID.</span><span class="sxs-lookup"><span data-stu-id="5c435-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="5c435-229">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="5c435-229">Click Bind.</span></span>
47. <span data-ttu-id="5c435-230">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetai\lArtikelzahl (ItemId).</span><span class="sxs-lookup"><span data-stu-id="5c435-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="5c435-231">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="5c435-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="5c435-232">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="5c435-232">Click Bind.</span></span>
50. <span data-ttu-id="5c435-233">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetail\Artikelzahl (LineNumber) aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="5c435-234">Wählen Sie in der Struktur Modell\Archivkopfzeile\Zeilen\Anzahl aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="5c435-235">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="5c435-235">Click Bind.</span></span>
53. <span data-ttu-id="5c435-236">In der Struktur wählen Sie Archiv\<Beziehungen\Intrastat\ArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="5c435-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="5c435-237">Wählen Sie in der Struktur Modell\Archivkopfzeile\Anzahl Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="5c435-238">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="5c435-238">Click Bind.</span></span>
56. <span data-ttu-id="5c435-239">Wählen Sie in der Struktur Archive\Dateinamen (FileName) aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="5c435-240">Wählen Sie in der Struktur Modell\Archivkopfzeile\Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="5c435-241">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="5c435-241">Click Bind.</span></span>
59. <span data-ttu-id="5c435-242">Wählen Sie in der Strukturdarstellung Archiv\Anzahl Zeilen(NumberOfLines) aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="5c435-243">Wählen Sie in der Struktur Modell\Archivkopfzeile\Anzahl Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="5c435-244">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="5c435-244">Click Bind.</span></span>
62. <span data-ttu-id="5c435-245">Wählen Sie in der Struktur Archiv aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="5c435-246">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="5c435-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="5c435-247">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="5c435-247">Click Bind.</span></span>
65. <span data-ttu-id="5c435-248">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5c435-248">Click Save.</span></span>
66. <span data-ttu-id="5c435-249">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5c435-249">Close the page.</span></span>
67. <span data-ttu-id="5c435-250">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5c435-250">Close the page.</span></span>

