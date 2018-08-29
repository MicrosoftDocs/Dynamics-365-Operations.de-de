--- 
title: "Ändern und Ausführen von Formaten zur Verwendung von Dokumentverwaltungsdateien in EB-Ausgabe"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5effbecf98e633d07f9e5eb22d3df1a12967c1e4
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="modify-and-run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="95b3d-103">Ändern und Ausführen von Formaten zur Verwendung von Dokumentverwaltungsdateien in EB-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="95b3d-103">Modify and run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95b3d-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="95b3d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="95b3d-105">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95b3d-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="95b3d-106">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 4: Format ausführen)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="95b3d-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="95b3d-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="95b3d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="95b3d-108">Bearbeiten Sie das Format, um Anlagen mit Nachrichten im Binärformat zu füllen.</span><span class="sxs-lookup"><span data-stu-id="95b3d-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="95b3d-109">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="95b3d-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="95b3d-110">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".</span><span class="sxs-lookup"><span data-stu-id="95b3d-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="95b3d-111">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="95b3d-112">Wählen Sie in der Strukturdarstellung 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="95b3d-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="95b3d-113">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="95b3d-113">Click Designer.</span></span>
    * <span data-ttu-id="95b3d-114">Die Rechnungsnachricht in der generierten Ausgabe wird als XML-Datei per Unicode-Codierung ausgefüllt.Rechnung</span><span class="sxs-lookup"><span data-stu-id="95b3d-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="95b3d-115">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="95b3d-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="95b3d-116">Wählen Sie in der Struktur 'Common\File' aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="95b3d-117">Geben Sie im Feld Name "Xml-Nachricht" ein.</span><span class="sxs-lookup"><span data-stu-id="95b3d-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="95b3d-118">Xml-Nachricht</span><span class="sxs-lookup"><span data-stu-id="95b3d-118">Xml message</span></span>  
9. <span data-ttu-id="95b3d-119">Geben Sie im Feld Kodierung "UTF-8" ein.</span><span class="sxs-lookup"><span data-stu-id="95b3d-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="95b3d-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="95b3d-120">UTF-8</span></span>  
10. <span data-ttu-id="95b3d-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="95b3d-121">Click OK.</span></span>
    * <span data-ttu-id="95b3d-122">Konfigurieren Sie das Generieren der Ausgabe als Zip-Datei.</span><span class="sxs-lookup"><span data-stu-id="95b3d-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="95b3d-123">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="95b3d-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="95b3d-124">Wählen Sie in der Struktur 'Common\Folder' aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="95b3d-125">Geben Sie im Feld "Name" "Zip-Ausgabe" ein.</span><span class="sxs-lookup"><span data-stu-id="95b3d-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="95b3d-126">ZIP-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="95b3d-126">Zip output</span></span>  
14. <span data-ttu-id="95b3d-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="95b3d-127">Click OK.</span></span>
15. <span data-ttu-id="95b3d-128">Wählen Sie in der Struktur 'Zip-Ausgabe' aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="95b3d-129">Fügen Sie Anhänge zur generierenden Zip-Datei als Dateien mit ursprünglichen Namen und Erweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="95b3d-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="95b3d-130">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="95b3d-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="95b3d-131">Wählen Sie in der Struktur 'Common\File' aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="95b3d-132">Geben Sie im Feld "Name" "Angehängte Datei" ein.</span><span class="sxs-lookup"><span data-stu-id="95b3d-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="95b3d-133">Angehängte Datei</span><span class="sxs-lookup"><span data-stu-id="95b3d-133">Attached file</span></span>  
19. <span data-ttu-id="95b3d-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="95b3d-134">Click OK.</span></span>
20. <span data-ttu-id="95b3d-135">Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei'.</span><span class="sxs-lookup"><span data-stu-id="95b3d-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="95b3d-136">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="95b3d-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="95b3d-137">Wählen Sie in der Struktur 'Text\Base64' aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="95b3d-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="95b3d-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="95b3d-139">Zuweisen von neuen Formatkomponenten zum Datenmodell</span><span class="sxs-lookup"><span data-stu-id="95b3d-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="95b3d-140">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="95b3d-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="95b3d-141">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="95b3d-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="95b3d-142">Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".</span><span class="sxs-lookup"><span data-stu-id="95b3d-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="95b3d-143">Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei\Base64'.</span><span class="sxs-lookup"><span data-stu-id="95b3d-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="95b3d-144">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiinhalt" aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="95b3d-145">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="95b3d-145">Click Bind.</span></span>
7. <span data-ttu-id="95b3d-146">Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei'.</span><span class="sxs-lookup"><span data-stu-id="95b3d-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="95b3d-147">Klicken Sie auf "Dateiname bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="95b3d-147">Click Edit filename.</span></span>
9. <span data-ttu-id="95b3d-148">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="95b3d-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="95b3d-149">Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".</span><span class="sxs-lookup"><span data-stu-id="95b3d-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="95b3d-150">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiname" aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="95b3d-151">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="95b3d-151">Click Add data source.</span></span>
13. <span data-ttu-id="95b3d-152">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="95b3d-152">Click Save.</span></span>
14. <span data-ttu-id="95b3d-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="95b3d-153">Close the page.</span></span>
15. <span data-ttu-id="95b3d-154">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge " aus.</span><span class="sxs-lookup"><span data-stu-id="95b3d-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="95b3d-155">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="95b3d-155">Click Bind.</span></span>
17. <span data-ttu-id="95b3d-156">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="95b3d-156">Click Save.</span></span>
18. <span data-ttu-id="95b3d-157">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="95b3d-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="95b3d-158">Ausführen des Berichts für die ausgewählte Rechnung</span><span class="sxs-lookup"><span data-stu-id="95b3d-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="95b3d-159">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="95b3d-159">Click Run.</span></span>
2. <span data-ttu-id="95b3d-160">Erweitern Sie den Abschnitt "Records to include ()".</span><span class="sxs-lookup"><span data-stu-id="95b3d-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="95b3d-161">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="95b3d-161">Click Filter.</span></span>
4. <span data-ttu-id="95b3d-162">Wählen Sie die Zeile des Feldes "Debitorenrechnungserfassung" und "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="95b3d-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="95b3d-163">Geben Sie im Feld "Auftrag" die Auftragsnummer 000148 ein.</span><span class="sxs-lookup"><span data-stu-id="95b3d-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="95b3d-164">000148</span><span class="sxs-lookup"><span data-stu-id="95b3d-164">000148</span></span>  
6. <span data-ttu-id="95b3d-165">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="95b3d-165">Click OK.</span></span>
7. <span data-ttu-id="95b3d-166">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="95b3d-166">Click OK.</span></span>
    * <span data-ttu-id="95b3d-167">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="95b3d-167">Review the generated output.</span></span> <span data-ttu-id="95b3d-168">Beachten Sie, das neben der Rechnungsnachricht im XML-Format eine einzelne Datei für jede Anlage erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="95b3d-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="95b3d-169">Die Anhangdateien werden mit der gezippten Ausgabe im Binärformat ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="95b3d-169">The attachment files are populated with the zipped output in binary format.</span></span>  


