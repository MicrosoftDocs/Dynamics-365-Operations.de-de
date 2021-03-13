---
title: Modelle und Zuordnungen ändern, um Dokumente zu generieren, die Anwendungsdaten haben
description: Dieses Thema zeigt, wie Sie Berichtskonfigurationen entwerfen, um ein elektronisches Dokument zu generieren und Anwendungsdaten zu aktualisieren. (Teil 2 – Dokumente generieren).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 025429c8e6775d20634703853df04d63c0651b98
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092896"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="d7878-104">Modelle und Zuordnungen ändern, um Dokumente zu generieren, die Anwendungsdaten haben</span><span class="sxs-lookup"><span data-stu-id="d7878-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7878-105">Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, „ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 2 - Dokumente erstellen)“.</span><span class="sxs-lookup"><span data-stu-id="d7878-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="d7878-106">Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d7878-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="d7878-107">In diesem Verfahren ändern Sie die ER-Konfigurationen, um sie derzeit nicht verwenden, um elektronische Dokumente zu erzeugen, wohingegen Anwendungsdaten auch zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d7878-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="d7878-108">Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="d7878-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="d7878-109">Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7878-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="d7878-110">Datenmodell ändern</span><span class="sxs-lookup"><span data-stu-id="d7878-110">Modify data model</span></span>
1. <span data-ttu-id="d7878-111">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d7878-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d7878-112">Erweitern Sie 'Intrastatmodell' in der Struktur (Modell).</span><span class="sxs-lookup"><span data-stu-id="d7878-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="d7878-113">Erweitern Sie das Datenmodell nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d7878-113">You will extend how you use the data model.</span></span> <span data-ttu-id="d7878-114">Neben der Verwendung als Datenquelle, um den Intrastat-Bericht zu generieren, wird das Datenmodell verwendet, um Details zum Intrastat-Berichts-Prozess zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="d7878-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="d7878-115">Die Details werden dann verwendet, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d7878-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="d7878-116">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="d7878-116">Click Designer.</span></span>
4. <span data-ttu-id="d7878-117">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d7878-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="d7878-118">Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="d7878-119">Geben Sie im Feld Typ Für Bewertungsdatenaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="d7878-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="d7878-120">Aktualisierung der Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="d7878-120">For application data update</span></span>  
7. <span data-ttu-id="d7878-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-121">Click Add.</span></span>
8. <span data-ttu-id="d7878-122">Wählen Sie in der Strukturdarstellung "für Bewerbungsdatenenaktualisierung " aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="d7878-123">Dieser neue Stammartikel wird hinzugefügt, um dem Datenfluss zum Bewegen von Daten vom Intrastat-Bericht (Als Datenquelle verwendet) für die Bewerbungstabellen (das Aktualisierungsziel) zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d7878-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="d7878-124">Beachten Sie, dass verschiedene Stammartikel zum Abrufen von Daten verwendet werden müssen für die ausgehenden Dokumente und zum Abrufen von Daten vom Dokuments, das verwendet wird, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d7878-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="d7878-125">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d7878-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="d7878-126">Geben Sie im Feld Typ Archivkopfzeile ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="d7878-127">Archivkopfzeile</span><span class="sxs-lookup"><span data-stu-id="d7878-127">Archive header</span></span>  
11. <span data-ttu-id="d7878-128">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="d7878-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-129">Click Add.</span></span>
    * <span data-ttu-id="d7878-130">Da ein Datensatz für jeden Intrastat-Bericht erstellt wird,, der erzeugt werden soll, müssen Sie einen neuen Artikel dafür erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7878-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="d7878-131">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d7878-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="d7878-132">Geben Sie im Feld "Name" "Dateiname" ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="d7878-133">Dateiname</span><span class="sxs-lookup"><span data-stu-id="d7878-133">File name</span></span>  
15. <span data-ttu-id="d7878-134">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="d7878-135">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-135">Click Add.</span></span>
17. <span data-ttu-id="d7878-136">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d7878-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="d7878-137">Geben Sie im Feld Name die Anzahl Zeilen ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="d7878-138">Anzahl Positionen</span><span class="sxs-lookup"><span data-stu-id="d7878-138">Number of lines</span></span>  
19. <span data-ttu-id="d7878-139">Wählen Sie im Artikelfeld Integer aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="d7878-140">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-140">Click Add.</span></span>
    * <span data-ttu-id="d7878-141">Fügen Sie diesen Artikel hinzu, um die Anzahl von Intrastat-Buchungen anzugeben, die während der aktuellen Generierung eines Berichts gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d7878-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="d7878-142">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d7878-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="d7878-143">Geben Sie im Feld Typ Archivzeilen ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="d7878-144">Archivieren von Positionen</span><span class="sxs-lookup"><span data-stu-id="d7878-144">Archive lines</span></span>  
23. <span data-ttu-id="d7878-145">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="d7878-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-146">Click Add.</span></span>
    * <span data-ttu-id="d7878-147">Fügen Sie diesen Artikel hinzu, um die Anzahl von Intrastat-Buchungen anzugeben, die während der aktuellen Generierung eines Berichts gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d7878-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="d7878-148">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d7878-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="d7878-149">Geben Sie im Feld Namen "Amount" ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="d7878-150">Dauer</span><span class="sxs-lookup"><span data-stu-id="d7878-150">Amount</span></span>  
27. <span data-ttu-id="d7878-151">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="d7878-152">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-152">Click Add.</span></span>
29. <span data-ttu-id="d7878-153">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d7878-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="d7878-154">Geben Sie im Feld Typ Waren Rec ID ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="d7878-155">Warendatensatz-ID</span><span class="sxs-lookup"><span data-stu-id="d7878-155">Commodity rec id</span></span>  
31. <span data-ttu-id="d7878-156">Wählen Sie im Feld "Artikeltyp" 'Int64 aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="d7878-157">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-157">Click Add.</span></span>
33. <span data-ttu-id="d7878-158">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d7878-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="d7878-159">Geben Sie im Feld Typ Artikelnummer ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="d7878-160">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="d7878-160">Item number</span></span>  
35. <span data-ttu-id="d7878-161">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="d7878-162">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-162">Click Add.</span></span>
37. <span data-ttu-id="d7878-163">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d7878-163">Click Save.</span></span>
38. <span data-ttu-id="d7878-164">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d7878-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="d7878-165">Modellzuordnung ändern</span><span class="sxs-lookup"><span data-stu-id="d7878-165">Modify model mapping</span></span>
1. <span data-ttu-id="d7878-166">Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7878-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="d7878-167">Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Zuordnung)" aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="d7878-168">Ändern Sie die bestehende Zuordnung, um die Bewerbungsdatenenaktualisierung zu starten und Intrastat-Berichts-Details zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="d7878-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="d7878-169">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="d7878-169">Click Designer.</span></span>
4. <span data-ttu-id="d7878-170">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d7878-170">Click New.</span></span>
5. <span data-ttu-id="d7878-171">Geben Sie im Feld Typ Archiv aktualisieren ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="d7878-172">Archiv aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d7878-172">Update archive</span></span>  
6. <span data-ttu-id="d7878-173">Wählen Sie im Feld Richtung Destination nach aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="d7878-174">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d7878-174">Click Save.</span></span>
    * <span data-ttu-id="d7878-175">Dieser neue Zuordung definiert den Datenfluss zum Bewegen von Daten (Intrastat-Bericht) vom Datenmodell zur Bewerbungstabelle (das Aktualisierungsziel).</span><span class="sxs-lookup"><span data-stu-id="d7878-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="d7878-176">Beachten Sie, dass Stammartikel des anderen Modells verwendet werden müssen, um Daten aus der Anwendung für den Berichterstellungsprozess und die Daten vom Datenmodell Sie anschließend die Möglichkeit für die Bewerbungsdatenenaktualisierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d7878-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="d7878-177">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="d7878-177">Click Designer.</span></span>
9. <span data-ttu-id="d7878-178">Wählen Sie in der Strukturdarstellung Datenmodell\Datenmodell aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="d7878-179">Die erforderliche Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-179">Add the required data source.</span></span> <span data-ttu-id="d7878-180">Dies ist das Datenmodell, das Details der gemeldeten Intrastat-Buchungen enthält, die archiviert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d7878-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="d7878-181">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="d7878-181">Click Add root.</span></span>
11. <span data-ttu-id="d7878-182">Geben Sie im Feld Namen die Modelart ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="d7878-183">Modell</span><span class="sxs-lookup"><span data-stu-id="d7878-183">model</span></span>  
12. <span data-ttu-id="d7878-184">Wählen Sie im Definitionsfeld den Wert Für Anwendungsdatenaktualisierung aus oder geben Sie diesen ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="d7878-185">Aktualisierung der Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="d7878-185">For application data update</span></span>  
13. <span data-ttu-id="d7878-186">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d7878-186">Click OK.</span></span>
14. <span data-ttu-id="d7878-187">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="d7878-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="d7878-188">Wählen Sie in der Strukturdarstellung "Funktionen\berechnetes Feld" aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="d7878-189">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="d7878-190">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-190">Click Add.</span></span>
    * <span data-ttu-id="d7878-191">Da Sie Intrastat-Buchungen für das gemeldete Chargenattribut archivieren möchten, muss die entsprechende Datenquelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d7878-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="d7878-192">Geben Sie im Feld Name den Typ Auzählungszeile ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="d7878-193">Aufgezählte Positionen</span><span class="sxs-lookup"><span data-stu-id="d7878-193">Enumerated lines</span></span>  
19. <span data-ttu-id="d7878-194">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d7878-194">Click Edit formula.</span></span>
20. <span data-ttu-id="d7878-195">Wählen Sie in der Struktur Liste\AUFZÄHLUNG aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="d7878-196">Klicken Sie auf Funktion hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-196">Click Add function.</span></span>
22. <span data-ttu-id="d7878-197">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="d7878-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="d7878-198">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="d7878-199">Wählen Sie in der Struktur Modell\ArchivkopfzeileArchivzeilen aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="d7878-200">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7878-200">Click Add data source.</span></span>
26. <span data-ttu-id="d7878-201">Im Formelfeld bestimmt geben Sie "AUFZÄHLUNG (Modell Archivkopfzeile, Archivzeilen) ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="d7878-202">AUFZÄHLEN (Modell. Archivpositionen, Archivzeilen)</span><span class="sxs-lookup"><span data-stu-id="d7878-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="d7878-203">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d7878-203">Click Save.</span></span>
28. <span data-ttu-id="d7878-204">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d7878-204">Close the page.</span></span>
29. <span data-ttu-id="d7878-205">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d7878-205">Click OK.</span></span>
30. <span data-ttu-id="d7878-206">Klicken Sie Destination hinzfügen aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-206">Click Add destination.</span></span>
    * <span data-ttu-id="d7878-207">Fügen Sie der Bewerbungstabellen nach Bedarf hinzu, die Aktualisierungen benötigen, u, Details der gemeldeten Intrastat-Buchungen zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="d7878-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="d7878-208">Geben Sie im Feld den Archivtyp ein..</span><span class="sxs-lookup"><span data-stu-id="d7878-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="d7878-209">Archiv</span><span class="sxs-lookup"><span data-stu-id="d7878-209">Archive</span></span>  
32. <span data-ttu-id="d7878-210">Geben Sie im Feld Tabelle den Typ IntrastatArchiveGeneral ein.</span><span class="sxs-lookup"><span data-stu-id="d7878-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="d7878-211">Formular "IntrastatArchiveGeneral"</span><span class="sxs-lookup"><span data-stu-id="d7878-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="d7878-212">Behalten Sie die Belegaktion „Einfügen“, sodass Sie Datensätze für das Detailarchivierens jedes Intrastat-Berichts-Prozesses hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="d7878-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="d7878-213">Wählen Sie "Ja" im Feld Beleg-Infoprotokoll.</span><span class="sxs-lookup"><span data-stu-id="d7878-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="d7878-214">Wählen Sie die Option Ja aus, um Informationen zu Problemen mit der Bewerbungsdatenenaktualisierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d7878-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="d7878-215">Wählen Sie Ja im Feld Belegaktionsüberprüfungsfeld aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="d7878-216">Wählen Sie die Option „Ja“ aus, um leere Prüfungsfehler zum Feld „Intrastat-Archiv ID“ zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="d7878-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="d7878-217">Dieses erfolgt, nachdem Datensätze hinzugefügt wurden, basierend auf den Einstellungen der Nummernkreise, die für diese Tabelle in der Außenhandelparameterform konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d7878-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="d7878-218">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d7878-218">Click OK.</span></span>
    * <span data-ttu-id="d7878-219">Binden Sie Elemente der hinzugefügten Datenquelle (das gefilterte Modell auf Basis des ausgewählten Stammartikel) mit Elementen des hinzugefügten Ziels.</span><span class="sxs-lookup"><span data-stu-id="d7878-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="d7878-220">In der Struktur erweitern Sie Archiv.</span><span class="sxs-lookup"><span data-stu-id="d7878-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="d7878-221">In der Struktur erweitern Sie Archiv\<Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="d7878-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="d7878-222">In der Struktur erweitern Sie Archiv\<BeziehungenIntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="d7878-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="d7878-223">Wählen Sie in der Struktur Archiv\<BeziehungenIntrastat\ArchiveDetail\Betrag (AmountMST).</span><span class="sxs-lookup"><span data-stu-id="d7878-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="d7878-224">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen.</span><span class="sxs-lookup"><span data-stu-id="d7878-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="d7878-225">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert.</span><span class="sxs-lookup"><span data-stu-id="d7878-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="d7878-226">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Betrag.</span><span class="sxs-lookup"><span data-stu-id="d7878-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="d7878-227">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="d7878-227">Click Bind.</span></span>
44. <span data-ttu-id="d7878-228">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetail\Waren(IntrastatCommodity).</span><span class="sxs-lookup"><span data-stu-id="d7878-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="d7878-229">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Waren Rec.-ID.</span><span class="sxs-lookup"><span data-stu-id="d7878-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="d7878-230">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="d7878-230">Click Bind.</span></span>
47. <span data-ttu-id="d7878-231">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetai\lArtikelzahl (ItemId).</span><span class="sxs-lookup"><span data-stu-id="d7878-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="d7878-232">Wählen Sie in der Struktur Modell\Archivkopfzeile\Auswahl Zeilen\Wert\Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="d7878-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="d7878-233">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="d7878-233">Click Bind.</span></span>
50. <span data-ttu-id="d7878-234">Wählen Sie in der Struktur Archiv\<Beziehungen\Intrastat\ArchiveDetail\Artikelzahl (LineNumber) aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="d7878-235">Wählen Sie in der Struktur Modell\Archivkopfzeile\Zeilen\Anzahl aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="d7878-236">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="d7878-236">Click Bind.</span></span>
53. <span data-ttu-id="d7878-237">In der Struktur wählen Sie Archiv\<Beziehungen\Intrastat\ArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="d7878-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="d7878-238">Wählen Sie in der Struktur Modell\Archivkopfzeile\Anzahl Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="d7878-239">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="d7878-239">Click Bind.</span></span>
56. <span data-ttu-id="d7878-240">Wählen Sie in der Struktur Archive\Dateinamen (FileName) aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="d7878-241">Wählen Sie in der Struktur Modell\Archivkopfzeile\Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="d7878-242">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="d7878-242">Click Bind.</span></span>
59. <span data-ttu-id="d7878-243">Wählen Sie in der Strukturdarstellung Archiv\Anzahl Zeilen(NumberOfLines) aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="d7878-244">Wählen Sie in der Struktur Modell\Archivkopfzeile\Anzahl Zeilen aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="d7878-245">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="d7878-245">Click Bind.</span></span>
62. <span data-ttu-id="d7878-246">Wählen Sie in der Struktur Archiv aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="d7878-247">Wählen Sie in der Struktur Modell\Archivkopfzeile aus.</span><span class="sxs-lookup"><span data-stu-id="d7878-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="d7878-248">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="d7878-248">Click Bind.</span></span>
65. <span data-ttu-id="d7878-249">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d7878-249">Click Save.</span></span>
66. <span data-ttu-id="d7878-250">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d7878-250">Close the page.</span></span>
67. <span data-ttu-id="d7878-251">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d7878-251">Close the page.</span></span>

