---
title: 'ER – Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 5: Format verändern und ausführen)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat (EB) für die Verwendung von Dokumentenverwaltungsdateien (Anhängen) in der EB-Ausgabe konfigurieren. (Teil 5)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092487"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="01945-104">ER – Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 5: Format verändern und ausführen)</span><span class="sxs-lookup"><span data-stu-id="01945-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01945-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="01945-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="01945-106">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="01945-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="01945-107">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Aufgabenleitfaden „ER - Verwendung der Dokumentverwaltungsdateien in Formatausgabe (Teil 4: Format ausführen)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="01945-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="01945-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="01945-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="01945-109">Bearbeiten Sie das Format, um Anlagen mit Nachrichten im Binärformat zu füllen.</span><span class="sxs-lookup"><span data-stu-id="01945-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="01945-110">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="01945-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="01945-111">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".</span><span class="sxs-lookup"><span data-stu-id="01945-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="01945-112">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.</span><span class="sxs-lookup"><span data-stu-id="01945-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="01945-113">Wählen Sie in der Strukturdarstellung 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="01945-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="01945-114">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="01945-114">Click Designer.</span></span>
    * <span data-ttu-id="01945-115">Die Rechnungsnachricht in der generierten Ausgabe wird als XML-Datei per Unicode-Codierung ausgefüllt.Rechnung</span><span class="sxs-lookup"><span data-stu-id="01945-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="01945-116">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="01945-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="01945-117">Wählen Sie in der Struktur 'Common\File' aus.</span><span class="sxs-lookup"><span data-stu-id="01945-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="01945-118">Geben Sie im Feld Name "Xml-Nachricht" ein.</span><span class="sxs-lookup"><span data-stu-id="01945-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="01945-119">Xml-Nachricht</span><span class="sxs-lookup"><span data-stu-id="01945-119">Xml message</span></span>  
9. <span data-ttu-id="01945-120">Geben Sie im Feld Kodierung "UTF-8" ein.</span><span class="sxs-lookup"><span data-stu-id="01945-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="01945-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="01945-121">UTF-8</span></span>  
10. <span data-ttu-id="01945-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="01945-122">Click OK.</span></span>
    * <span data-ttu-id="01945-123">Konfigurieren Sie das Generieren der Ausgabe als Zip-Datei.</span><span class="sxs-lookup"><span data-stu-id="01945-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="01945-124">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="01945-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="01945-125">Wählen Sie in der Struktur 'Common\Folder' aus.</span><span class="sxs-lookup"><span data-stu-id="01945-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="01945-126">Geben Sie im Feld "Name" "Zip-Ausgabe" ein.</span><span class="sxs-lookup"><span data-stu-id="01945-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="01945-127">ZIP-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="01945-127">Zip output</span></span>  
14. <span data-ttu-id="01945-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="01945-128">Click OK.</span></span>
15. <span data-ttu-id="01945-129">Wählen Sie in der Struktur 'Zip-Ausgabe' aus.</span><span class="sxs-lookup"><span data-stu-id="01945-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="01945-130">Fügen Sie Anhänge zur generierenden Zip-Datei als Dateien mit ursprünglichen Namen und Erweiterungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="01945-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="01945-131">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="01945-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="01945-132">Wählen Sie in der Struktur 'Common\File' aus.</span><span class="sxs-lookup"><span data-stu-id="01945-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="01945-133">Geben Sie im Feld "Name" "Angehängte Datei" ein.</span><span class="sxs-lookup"><span data-stu-id="01945-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="01945-134">Angehängte Datei</span><span class="sxs-lookup"><span data-stu-id="01945-134">Attached file</span></span>  
19. <span data-ttu-id="01945-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="01945-135">Click OK.</span></span>
20. <span data-ttu-id="01945-136">Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei'.</span><span class="sxs-lookup"><span data-stu-id="01945-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="01945-137">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="01945-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="01945-138">Wählen Sie in der Struktur 'Text\Base64' aus.</span><span class="sxs-lookup"><span data-stu-id="01945-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="01945-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="01945-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="01945-140">Zuweisen von neuen Formatkomponenten zum Datenmodell</span><span class="sxs-lookup"><span data-stu-id="01945-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="01945-141">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="01945-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="01945-142">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="01945-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="01945-143">Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".</span><span class="sxs-lookup"><span data-stu-id="01945-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="01945-144">Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei\Base64'.</span><span class="sxs-lookup"><span data-stu-id="01945-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="01945-145">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiinhalt" aus.</span><span class="sxs-lookup"><span data-stu-id="01945-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="01945-146">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="01945-146">Click Bind.</span></span>
7. <span data-ttu-id="01945-147">Wählen Sie in der Struktur 'Zip-Ausgabe\Angehängte Datei'.</span><span class="sxs-lookup"><span data-stu-id="01945-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="01945-148">Klicken Sie auf "Dateiname bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="01945-148">Click Edit filename.</span></span>
9. <span data-ttu-id="01945-149">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="01945-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="01945-150">Erweitern Sie in der Strukturdarstellung "Modell\Rechnungsanhänge".</span><span class="sxs-lookup"><span data-stu-id="01945-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="01945-151">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge\Dateiname" aus.</span><span class="sxs-lookup"><span data-stu-id="01945-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="01945-152">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="01945-152">Click Add data source.</span></span>
13. <span data-ttu-id="01945-153">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="01945-153">Click Save.</span></span>
14. <span data-ttu-id="01945-154">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="01945-154">Close the page.</span></span>
15. <span data-ttu-id="01945-155">Wählen Sie in der Strukturdarstellung "Modell\Rechnungsanhänge " aus.</span><span class="sxs-lookup"><span data-stu-id="01945-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="01945-156">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="01945-156">Click Bind.</span></span>
17. <span data-ttu-id="01945-157">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="01945-157">Click Save.</span></span>
18. <span data-ttu-id="01945-158">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="01945-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="01945-159">Ausführen des Berichts für die ausgewählte Rechnung</span><span class="sxs-lookup"><span data-stu-id="01945-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="01945-160">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="01945-160">Click Run.</span></span>
2. <span data-ttu-id="01945-161">Erweitern Sie den Abschnitt "Records to include ()".</span><span class="sxs-lookup"><span data-stu-id="01945-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="01945-162">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="01945-162">Click Filter.</span></span>
4. <span data-ttu-id="01945-163">Wählen Sie die Zeile des Feldes "Debitorenrechnungserfassung" und "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="01945-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="01945-164">Geben Sie im Feld „Auftrag“ die Auftragsnummer 000148 ein.</span><span class="sxs-lookup"><span data-stu-id="01945-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="01945-165">000148</span><span class="sxs-lookup"><span data-stu-id="01945-165">000148</span></span>  
6. <span data-ttu-id="01945-166">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="01945-166">Click OK.</span></span>
7. <span data-ttu-id="01945-167">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="01945-167">Click OK.</span></span>
    * <span data-ttu-id="01945-168">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="01945-168">Review the generated output.</span></span> <span data-ttu-id="01945-169">Beachten Sie, das neben der Rechnungsnachricht im XML-Format eine einzelne Datei für jede Anlage erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="01945-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="01945-170">Die Anhangdateien werden mit der gezippten Ausgabe im Binärformat ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="01945-170">The attachment files are populated with the zipped output in binary format.</span></span>  

