--- 
title: "Ändern von Modell und Zuordnung zum Generieren von Dokumenten mit Anwendungsdatenupdate für elektronische Berichterstellung"
description: "Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, \"ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 2 -  Dokumente erstellen)."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a29e273e5ef377826c0002a9a0a956defef6aa77
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="modify-model-and-mapping-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="40d81-103">Ändern von Modell und Zuordnung zum Generieren von Dokumenten mit Anwendungsdatenupdate für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="40d81-103">Modify model and mapping to generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40d81-104">Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 2: Dokumente erstellen).</span><span class="sxs-lookup"><span data-stu-id="40d81-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="40d81-105">Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="40d81-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="40d81-106">In diesem Verfahren ändern Sie die ER-Konfigurationen, um sie derzeit nicht verwenden, um elektronische Dokumente zu erzeugen, wohingegen Anwendungsdaten auch zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="40d81-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="40d81-107">Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="40d81-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="40d81-108">Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="40d81-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="40d81-109">Datenmodell ändern</span><span class="sxs-lookup"><span data-stu-id="40d81-109">Modify data model</span></span>
1. <span data-ttu-id="40d81-110">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="40d81-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="40d81-111">Erweitern Sie 'Intrastatmodell' in der Struktur (Modell).</span><span class="sxs-lookup"><span data-stu-id="40d81-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="40d81-112">Erweitern Sie das Datenmodell nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="40d81-112">You will extend how you use the data model.</span></span> <span data-ttu-id="40d81-113">Neben der Verwendung als Datenquelle, um den Intrastat-Bericht zu generieren, wird das Datenmodell verwendet, um Details zum Intrastat-Berichts-Prozess zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="40d81-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="40d81-114">Die Details werden dann verwendet, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="40d81-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="40d81-115">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="40d81-115">Click Designer.</span></span>
4. <span data-ttu-id="40d81-116">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="40d81-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="40d81-117">Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="40d81-118">Geben Sie im Feld Typ Für Bewertungsdatenaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="40d81-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="40d81-119">Aktualisierung der Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="40d81-119">For application data update</span></span>  
7. <span data-ttu-id="40d81-120">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-120">Click Add.</span></span>
8. <span data-ttu-id="40d81-121">Wählen Sie in der Strukturdarstellung "für Bewerbungsdatenenaktualisierung " aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="40d81-122">Dieser neue Stammartikel wird hinzugefügt, um dem Datenfluss zum Bewegen von Daten vom Intrastat-Bericht (Als Datenquelle verwendet) für die Bewerbungstabellen (das Aktualisierungsziel) zu definieren.</span><span class="sxs-lookup"><span data-stu-id="40d81-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="40d81-123">Beachten Sie, dass verschiedene Stammartikel zum Abrufen von Daten verwendet werden müssen für die ausgehenden Dokumente und zum Abrufen von Daten vom Dokuments, das verwendet wird, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="40d81-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="40d81-124">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="40d81-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="40d81-125">Geben Sie im Feld Typ Archivkopfzeile ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="40d81-126">Archivkopfzeile</span><span class="sxs-lookup"><span data-stu-id="40d81-126">Archive header</span></span>  
11. <span data-ttu-id="40d81-127">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="40d81-128">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-128">Click Add.</span></span>
    * <span data-ttu-id="40d81-129">Da ein Datensatz für jeden Intrastat-Bericht erstellt wird,, der erzeugt werden soll, müssen Sie einen neuen Artikel dafür erstellen.</span><span class="sxs-lookup"><span data-stu-id="40d81-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="40d81-130">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="40d81-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="40d81-131">Geben Sie im Feld "Name" "Dateiname" ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="40d81-132">Dateiname</span><span class="sxs-lookup"><span data-stu-id="40d81-132">File name</span></span>  
15. <span data-ttu-id="40d81-133">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="40d81-134">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-134">Click Add.</span></span>
17. <span data-ttu-id="40d81-135">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="40d81-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="40d81-136">Geben Sie im Feld Name die Anzahl Zeilen ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="40d81-137">Anzahl Positionen</span><span class="sxs-lookup"><span data-stu-id="40d81-137">Number of lines</span></span>  
19. <span data-ttu-id="40d81-138">Wählen Sie im Artikelfeld Integer aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="40d81-139">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-139">Click Add.</span></span>
    * <span data-ttu-id="40d81-140">Fügen Sie diesen Artikel hinzu, um die Anzahl von Intrastat-Buchungen anzugeben, die während der aktuellen Generierung eines Berichts gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="40d81-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="40d81-141">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="40d81-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="40d81-142">Geben Sie im Feld Typ Archivzeilen ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="40d81-143">Archivieren von Positionen</span><span class="sxs-lookup"><span data-stu-id="40d81-143">Archive lines</span></span>  
23. <span data-ttu-id="40d81-144">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="40d81-145">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-145">Click Add.</span></span>
    * <span data-ttu-id="40d81-146">Fügen Sie diesen Artikel hinzu, um die Anzahl von Intrastat-Buchungen anzugeben, die während der aktuellen Generierung eines Berichts gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="40d81-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="40d81-147">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="40d81-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="40d81-148">Geben Sie im Feld Namen "Amount" ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="40d81-149">Dauer</span><span class="sxs-lookup"><span data-stu-id="40d81-149">Amount</span></span>  
27. <span data-ttu-id="40d81-150">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="40d81-151">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-151">Click Add.</span></span>
29. <span data-ttu-id="40d81-152">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="40d81-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="40d81-153">Geben Sie im Feld Typ Waren Rec ID ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="40d81-154">Warendatensatz-ID</span><span class="sxs-lookup"><span data-stu-id="40d81-154">Commodity rec id</span></span>  
31. <span data-ttu-id="40d81-155">Wählen Sie im Feld "Artikeltyp" 'Int64 aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="40d81-156">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-156">Click Add.</span></span>
33. <span data-ttu-id="40d81-157">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="40d81-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="40d81-158">Geben Sie im Feld Typ Artikelnummer ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="40d81-159">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="40d81-159">Item number</span></span>  
35. <span data-ttu-id="40d81-160">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="40d81-161">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-161">Click Add.</span></span>
37. <span data-ttu-id="40d81-162">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="40d81-162">Click Save.</span></span>
38. <span data-ttu-id="40d81-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="40d81-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="40d81-164">Modellzuordnung ändern</span><span class="sxs-lookup"><span data-stu-id="40d81-164">Modify model mapping</span></span>
1. <span data-ttu-id="40d81-165">Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="40d81-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="40d81-166">Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Zuordnung)" aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="40d81-167">Ändern Sie die bestehende Zuordnung, um die Bewerbungsdatenenaktualisierung zu starten und Intrastat-Berichts-Details zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="40d81-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="40d81-168">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="40d81-168">Click Designer.</span></span>
4. <span data-ttu-id="40d81-169">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="40d81-169">Click New.</span></span>
5. <span data-ttu-id="40d81-170">Geben Sie im Feld Typ Archiv aktualisieren ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="40d81-171">Archiv aktualisieren</span><span class="sxs-lookup"><span data-stu-id="40d81-171">Update archive</span></span>  
6. <span data-ttu-id="40d81-172">Wählen Sie im Feld Richtung Destination nach aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="40d81-173">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="40d81-173">Click Save.</span></span>
    * <span data-ttu-id="40d81-174">Dieser neue Zuordung definiert den Datenfluss zum Bewegen von Daten (Intrastat-Bericht) vom Datenmodell zur Bewerbungstabelle (das Aktualisierungsziel).</span><span class="sxs-lookup"><span data-stu-id="40d81-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="40d81-175">Beachten Sie, dass Stammartikel des anderen Modells verwendet werden müssen, um Daten aus der Anwendung für den Berichterstellungsprozess und die Daten vom Datenmodell Sie anschließend die Möglichkeit für die Bewerbungsdatenenaktualisierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="40d81-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="40d81-176">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="40d81-176">Click Designer.</span></span>
9. <span data-ttu-id="40d81-177">Wählen Sie in der Strukturdarstellung Datenmodell\Datenmodell aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="40d81-178">Die erforderliche Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-178">Add the required data source.</span></span> <span data-ttu-id="40d81-179">Dies ist das Datenmodell, das Details der gemeldeten Intrastat-Buchungen enthält, die archiviert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="40d81-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="40d81-180">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="40d81-180">Click Add root.</span></span>
11. <span data-ttu-id="40d81-181">Geben Sie im Feld Namen die Modelart ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="40d81-182">Modell</span><span class="sxs-lookup"><span data-stu-id="40d81-182">model</span></span>  
12. <span data-ttu-id="40d81-183">Wählen Sie im Definitionsfeld den Wert Für Anwendungsdatenaktualisierung aus oder geben Sie diesen ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="40d81-184">Aktualisierung der Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="40d81-184">For application data update</span></span>  
13. <span data-ttu-id="40d81-185">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="40d81-185">Click OK.</span></span>
14. <span data-ttu-id="40d81-186">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="40d81-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="40d81-187">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="40d81-188">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="40d81-189">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-189">Click Add.</span></span>
    * <span data-ttu-id="40d81-190">Da Sie Intrastat-Buchungen für das gemeldete Chargenattribut archivieren möchten, muss die entsprechende Datenquelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="40d81-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="40d81-191">Geben Sie im Feld Name den Typ Auzählungszeile ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="40d81-192">Aufgezählte Positionen</span><span class="sxs-lookup"><span data-stu-id="40d81-192">Enumerated lines</span></span>  
19. <span data-ttu-id="40d81-193">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="40d81-193">Click Edit formula.</span></span>
20. <span data-ttu-id="40d81-194">Wählen Sie in der Struktur Liste\AUFZÄHLUNG aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="40d81-195">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-195">Click Add function.</span></span>
22. <span data-ttu-id="40d81-196">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="40d81-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="40d81-197">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="40d81-198">Wählen Sie in der Struktur Modell\ArchivkopfzeileArchivzeilen aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="40d81-199">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="40d81-199">Click Add data source.</span></span>
26. <span data-ttu-id="40d81-200">Im Formelfeld bestimmt geben Sie "AUFZÄHLUNG (Modell Archivkopfzeile, Archivzeilen) ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="40d81-201">AUFZÄHLEN (Modell. Archivpositionen, Archivzeilen)</span><span class="sxs-lookup"><span data-stu-id="40d81-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="40d81-202">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="40d81-202">Click Save.</span></span>
28. <span data-ttu-id="40d81-203">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="40d81-203">Close the page.</span></span>
29. <span data-ttu-id="40d81-204">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="40d81-204">Click OK.</span></span>
30. <span data-ttu-id="40d81-205">Klicken Sie Destination hinzfügen aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-205">Click Add destination.</span></span>
    * <span data-ttu-id="40d81-206">Fügen Sie der Bewerbungstabellen nach Bedarf hinzu, die Aktualisierungen benötigen, u, Details der gemeldeten Intrastat-Buchungen zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="40d81-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="40d81-207">Geben Sie im Feld den Archivtyp ein..</span><span class="sxs-lookup"><span data-stu-id="40d81-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="40d81-208">Archiv</span><span class="sxs-lookup"><span data-stu-id="40d81-208">Archive</span></span>  
32. <span data-ttu-id="40d81-209">Geben Sie im Feld Tabelle den Typ IntrastatArchiveGeneral ein.</span><span class="sxs-lookup"><span data-stu-id="40d81-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="40d81-210">Formular "IntrastatArchiveGeneral"</span><span class="sxs-lookup"><span data-stu-id="40d81-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="40d81-211">Behalten Sie die Belegaktion "Einfügen", sodass Sie Datensätze für das Detailarchivierens jedes Intrastat-Berichts-Prozesses hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="40d81-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="40d81-212">Wählen Sie "Ja" im Feld Beleg-Infoprotokoll.</span><span class="sxs-lookup"><span data-stu-id="40d81-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="40d81-213">Wählen Sie die Option Ja aus, um Informationen zu Problemen mit der Bewerbungsdatenenaktualisierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="40d81-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="40d81-214">Wählen Sie Ja im Feld Belegaktionsüberprüfungsfeld aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="40d81-215">Wählen Sie die Option Ja aus, um leere Prüfungsfehler zum Feld "Intrastat-Archiv ID-" zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="40d81-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="40d81-216">Dieses erfolgt, nachdem Datensätze hinzugefügt wurden, basierend auf den Einstellungen der Nummernkreise, die für diese Tabelle in der Außenhandelparameterform konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="40d81-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="40d81-217">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="40d81-217">Click OK.</span></span>
    * <span data-ttu-id="40d81-218">Binden Sie Elemente der hinzugefügten Datenquelle (das gefilterte Modell auf Basis des ausgewählten Stammartikel) mit Elementen des hinzugefügten Ziels.</span><span class="sxs-lookup"><span data-stu-id="40d81-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="40d81-219">In der Struktur erweitern Sie Archiv.</span><span class="sxs-lookup"><span data-stu-id="40d81-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="40d81-220">In der Struktur erweitern Sie Archiv\<Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="40d81-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="40d81-221">In der Struktur erweitern Sie Archiv\<BeziehungenIntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="40d81-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="40d81-222">Wählen Sie in der Struktur Archiv\<BeziehungenIntrastat\\ArchiveDetail\Betrag (AmountMST).</span><span class="sxs-lookup"><span data-stu-id="40d81-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="40d81-223">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen.</span><span class="sxs-lookup"><span data-stu-id="40d81-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="40d81-224">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert.</span><span class="sxs-lookup"><span data-stu-id="40d81-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="40d81-225">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Betrag.</span><span class="sxs-lookup"><span data-stu-id="40d81-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="40d81-226">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="40d81-226">Click Bind.</span></span>
44. <span data-ttu-id="40d81-227">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetail\Waren(IntrastatCommodity).</span><span class="sxs-lookup"><span data-stu-id="40d81-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="40d81-228">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Waren Rec.-ID.</span><span class="sxs-lookup"><span data-stu-id="40d81-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="40d81-229">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="40d81-229">Click Bind.</span></span>
47. <span data-ttu-id="40d81-230">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetai\lArtikelzahl (ItemId).</span><span class="sxs-lookup"><span data-stu-id="40d81-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="40d81-231">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="40d81-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="40d81-232">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="40d81-232">Click Bind.</span></span>
50. <span data-ttu-id="40d81-233">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetail\Artikelzahl (LineNumber) aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="40d81-234">Wählen Sie in der Struktur Modell\Archivkopfzeile\Zeilen\Anzahl aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="40d81-235">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="40d81-235">Click Bind.</span></span>
53. <span data-ttu-id="40d81-236">In der Struktur wählen Sie Archiv\<Beziehungen\Intrastat\ArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="40d81-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="40d81-237">Wählen Sie in der Struktur Modell\Archivkopfzeile\Anzahl Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="40d81-238">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="40d81-238">Click Bind.</span></span>
56. <span data-ttu-id="40d81-239">Wählen Sie in der Struktur Archive\Dateinamen (FileName) aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="40d81-240">Wählen Sie in der Struktur Modell\Archivkopfzeile\Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="40d81-241">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="40d81-241">Click Bind.</span></span>
59. <span data-ttu-id="40d81-242">Wählen Sie in der Strukturdarstellung Archiv\Anzahl Zeilen(NumberOfLines) aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="40d81-243">Wählen Sie in der Struktur Modell\Archivkopfzeile\Anzahl Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="40d81-244">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="40d81-244">Click Bind.</span></span>
62. <span data-ttu-id="40d81-245">Wählen Sie in der Struktur Archiv aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="40d81-246">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="40d81-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="40d81-247">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="40d81-247">Click Bind.</span></span>
65. <span data-ttu-id="40d81-248">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="40d81-248">Click Save.</span></span>
66. <span data-ttu-id="40d81-249">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="40d81-249">Close the page.</span></span>
67. <span data-ttu-id="40d81-250">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="40d81-250">Close the page.</span></span>


