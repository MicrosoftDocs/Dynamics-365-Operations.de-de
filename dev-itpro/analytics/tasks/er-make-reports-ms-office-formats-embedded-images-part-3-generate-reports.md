--- 
title: "Generieren von Berichten in Microsoft Office-Formaten mit eingebetteten Bildern für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: de2840ebc6c91e313546859f5c0d8939eb80977b
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a><span data-ttu-id="cbedd-103">Generieren von Berichten in Microsoft Office-Formaten mit eingebetteten Bildern für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="cbedd-103">Generate reports in Microsoft Office formats with embedded images for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbedd-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="cbedd-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="cbedd-105">In diesem Beispiel erstellen Sie eine ER-Konfigurationen für das Beispielunternehmen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="cbedd-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="cbedd-106">Um diese Schritte auszuführen, müssen Sie die Schritte zuerst im"ER Berichte im MS Office-Formaten mit eingebetteten Bildern (Teil 2: Konfiguration überprüfen)" Aufgabenleitfaden erstellen.</span><span class="sxs-lookup"><span data-stu-id="cbedd-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="cbedd-107">Diese Schritte können im USMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cbedd-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="cbedd-108">Führen Sie das Format mit Initialenmodellzuordnung aus</span><span class="sxs-lookup"><span data-stu-id="cbedd-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="cbedd-109">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="cbedd-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="cbedd-110">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="cbedd-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="cbedd-111">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="cbedd-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="cbedd-112">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="cbedd-112">Click Check.</span></span>
5. <span data-ttu-id="cbedd-113">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="cbedd-113">Click Print test.</span></span>
    * <span data-ttu-id="cbedd-114">Führen Sie das Format für Testzwecke aus.</span><span class="sxs-lookup"><span data-stu-id="cbedd-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="cbedd-115">Wählen Sie die Option Ja im Feld Verhandelbares Scheckformatgebiet aus.</span><span class="sxs-lookup"><span data-stu-id="cbedd-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="cbedd-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cbedd-116">Click OK.</span></span>
    * <span data-ttu-id="cbedd-117">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="cbedd-117">Review the created output.</span></span> <span data-ttu-id="cbedd-118">Beachten Sie, dass das Firmenlogo im Bericht sowie die autorisierten Unterschrift der Person angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cbedd-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="cbedd-119">Das Unterzeichnungsbild wird im Feld "Container" des Datentyps des Schecklayoutdatensatzes übernommen, der dem ausgewählten Bankkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cbedd-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="cbedd-120">Erweitern Sie den Abschnitt Kopien.</span><span class="sxs-lookup"><span data-stu-id="cbedd-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="cbedd-121">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="cbedd-121">Click Edit.</span></span>
10. <span data-ttu-id="cbedd-122">Im Wasserzeichengebiet geben Sie "Wasserzeichen als Nichtig drucken".</span><span class="sxs-lookup"><span data-stu-id="cbedd-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="cbedd-123">Ändern Sie die Wasserzeichenlayouteinstellung, um den Wasserzeichentext anzuzeigen, wenn Sie in einem Dokument Excel-Formelement generieren.</span><span class="sxs-lookup"><span data-stu-id="cbedd-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="cbedd-124">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="cbedd-124">Click Print test.</span></span>
12. <span data-ttu-id="cbedd-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cbedd-125">Click OK.</span></span>
    * <span data-ttu-id="cbedd-126">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="cbedd-126">Review the created output.</span></span> <span data-ttu-id="cbedd-127">Beachten Sie, dass das Wasserzeichen im erstellten Bericht in der Übereinstimmung der Auswahloption angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cbedd-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="cbedd-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-128">Close the page.</span></span>
14. <span data-ttu-id="cbedd-129">Klicken Sie im Aktivitätsbereich auf Zahlungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="cbedd-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="cbedd-130">Klicken Sie auf Schecks.</span><span class="sxs-lookup"><span data-stu-id="cbedd-130">Click Checks.</span></span>
16. <span data-ttu-id="cbedd-131">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="cbedd-131">Click Show filters.</span></span>
17. <span data-ttu-id="cbedd-132">Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert von 381, 385, 389 im Checkfeld mithilfe des Filterzeichens ein.</span><span class="sxs-lookup"><span data-stu-id="cbedd-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="cbedd-133">Schalten Sie in der Liste 'Alle Zeilen markieren' ein/aus.</span><span class="sxs-lookup"><span data-stu-id="cbedd-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="cbedd-134">Scheckkopie drucken anklicken.</span><span class="sxs-lookup"><span data-stu-id="cbedd-134">Click Print check copy.</span></span>
    * <span data-ttu-id="cbedd-135">Führen Sie das Format aus, um die ausgewählten Schecks erneut zu drucken.</span><span class="sxs-lookup"><span data-stu-id="cbedd-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="cbedd-136">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="cbedd-136">Review the created output.</span></span> <span data-ttu-id="cbedd-137">Beachten Sie, dass die ausgewählten Schecks erneut gedruckt wurden.</span><span class="sxs-lookup"><span data-stu-id="cbedd-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="cbedd-138">Das Firmenlogo und die Bezeichnungen werden nicht ausgedruckt, wie sie auf dem Vordruck dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cbedd-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="cbedd-139">Überprüfe Sie die Struktur des importierten Datenmodells.</span><span class="sxs-lookup"><span data-stu-id="cbedd-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="cbedd-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-140">Close the page.</span></span>
2. <span data-ttu-id="cbedd-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-141">Close the page.</span></span>
3. <span data-ttu-id="cbedd-142">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="cbedd-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="cbedd-143">Wählen Sie in der Struktur 'Modell für Cheques.</span><span class="sxs-lookup"><span data-stu-id="cbedd-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="cbedd-144">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="cbedd-144">Click Designer.</span></span>
6. <span data-ttu-id="cbedd-145">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="cbedd-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="cbedd-146">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="cbedd-146">Click Designer.</span></span>
    * <span data-ttu-id="cbedd-147">Wir ändern die Bindung des Unterzeichnungsartikels des Datenmodells, um das Unterzeichnungsbild der Datei zu erhalten, die auf den Schecklayoutdatensatz zugeordnet wurde, der dem ausgewählten Bankkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cbedd-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="cbedd-148">Anzeigedetails aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cbedd-148">Turn Show details off.</span></span>
9. <span data-ttu-id="cbedd-149">Erweitern Sie in der Struktur Layout.</span><span class="sxs-lookup"><span data-stu-id="cbedd-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="cbedd-150">Erweitern oder reduzieren Sie Layout\Unterschrift.</span><span class="sxs-lookup"><span data-stu-id="cbedd-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="cbedd-151">Wählen Sie in der Strukturdarstellung Layout\Unterschrift\Bild= chequesaccount<Beziehungen. BankChequeLayout.Signature1Bmp.</span><span class="sxs-lookup"><span data-stu-id="cbedd-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="cbedd-152">Erweitern oder reduzieren Sie chequesaccount.</span><span class="sxs-lookup"><span data-stu-id="cbedd-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="cbedd-153">In der Struktur erweitern chequesaccount\<Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="cbedd-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="cbedd-154">Erweitern Sie in der Struktur chequesaccount\<Beziehungen\BankChequeLayout.</span><span class="sxs-lookup"><span data-stu-id="cbedd-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="cbedd-155">Erweitern Sie in der Struktur chequesaccount\<BeziehungenBankChequeLayout\<Relations.</span><span class="sxs-lookup"><span data-stu-id="cbedd-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="cbedd-156">Erweitern Sie in der Struktur 'chequesaccount\<BeziehungBankChequeLayout\<Beziehung\<Dokumente'.</span><span class="sxs-lookup"><span data-stu-id="cbedd-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="cbedd-157">Wählen Sie in der Strukturdarstellung 'chequesaccount\<BeziehungBankChequeLayout\<Beziehung\<DokumentegetFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="cbedd-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="cbedd-158">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="cbedd-158">Click Bind.</span></span>
19. <span data-ttu-id="cbedd-159">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="cbedd-159">Click Save.</span></span>
20. <span data-ttu-id="cbedd-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-160">Close the page.</span></span>
21. <span data-ttu-id="cbedd-161">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-161">Close the page.</span></span>
22. <span data-ttu-id="cbedd-162">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-162">Close the page.</span></span>
23. <span data-ttu-id="cbedd-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="cbedd-164">Die Formatzuordnung zum Datenmodell ausführen</span><span class="sxs-lookup"><span data-stu-id="cbedd-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="cbedd-165">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="cbedd-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="cbedd-166">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cbedd-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cbedd-167">Filtern Sie beispielsweise im Feld "Bankkontofeld" mit dem Wert "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="cbedd-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="cbedd-168">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="cbedd-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="cbedd-169">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="cbedd-169">Click Check.</span></span>
5. <span data-ttu-id="cbedd-170">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="cbedd-170">Click Print test.</span></span>
6. <span data-ttu-id="cbedd-171">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cbedd-171">Click OK.</span></span>
    * <span data-ttu-id="cbedd-172">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="cbedd-172">Review the created output.</span></span> <span data-ttu-id="cbedd-173">Beachten Sie, ob das Bild aus dem Dokumentverwaltungsanhang als Unterschrifte eine autorisierte Person darstellt.</span><span class="sxs-lookup"><span data-stu-id="cbedd-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="cbedd-174">Verwenden Sie das MS Word-Dokument als Vorlage im importierten Format</span><span class="sxs-lookup"><span data-stu-id="cbedd-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="cbedd-175">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-175">Close the page.</span></span>
2. <span data-ttu-id="cbedd-176">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-176">Close the page.</span></span>
3. <span data-ttu-id="cbedd-177">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="cbedd-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="cbedd-178">Wählen Sie in der Struktur erweitern 'Modell für Cheques.</span><span class="sxs-lookup"><span data-stu-id="cbedd-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="cbedd-179">Wählen Sie in der Strukturdarstellung "Modell für Cheques\Cheques-Druckformat.</span><span class="sxs-lookup"><span data-stu-id="cbedd-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="cbedd-180">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="cbedd-180">Click Designer.</span></span>
7. <span data-ttu-id="cbedd-181">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="cbedd-181">Click Attachments.</span></span>
8. <span data-ttu-id="cbedd-182">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="cbedd-182">Click Delete.</span></span>
9. <span data-ttu-id="cbedd-183">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="cbedd-183">Click Yes.</span></span>
10. <span data-ttu-id="cbedd-184">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="cbedd-184">Click New.</span></span>
11. <span data-ttu-id="cbedd-185">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="cbedd-185">Click File.</span></span>
    * <span data-ttu-id="cbedd-186">Navigieren und wählen Sie die heruntergeladene Datei "Scheck-Vorlage Word.docx" aus.</span><span class="sxs-lookup"><span data-stu-id="cbedd-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="cbedd-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-187">Close the page.</span></span>
13. <span data-ttu-id="cbedd-188">Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="cbedd-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="cbedd-189">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="cbedd-189">Click Save.</span></span>
15. <span data-ttu-id="cbedd-190">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-190">Close the page.</span></span>
16. <span data-ttu-id="cbedd-191">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="cbedd-191">Click Edit.</span></span>
17. <span data-ttu-id="cbedd-192">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="cbedd-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="cbedd-193">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cbedd-193">Close the page.</span></span>
19. <span data-ttu-id="cbedd-194">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="cbedd-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="cbedd-195">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="cbedd-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="cbedd-196">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="cbedd-196">Click Check.</span></span>
22. <span data-ttu-id="cbedd-197">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="cbedd-197">Click Print test.</span></span>
23. <span data-ttu-id="cbedd-198">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cbedd-198">Click OK.</span></span>
    * <span data-ttu-id="cbedd-199">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="cbedd-199">Review the created output.</span></span> <span data-ttu-id="cbedd-200">Beachten Sie, dass die MS Word-Dokument Ausgabe mit den eingebetteten Zeichen generiert wurde, die das Firmenlogo, die Unterschrift einer autorisierten Person und den markierten Text des Wasserzeichens darstellt.</span><span class="sxs-lookup"><span data-stu-id="cbedd-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


