---
title: Berichte im Office-Format generieren, die eingebettete Bilder haben
description: In diesem Thema wird beschrieben, wie die Konfigurationen für die elektronische Berichterstellung (EB) entworfen werden, um elektronische Dokumente in Excel und Word zu generieren, die eingebettete Bilder enthalten.
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b93c14fc4819fffd322a1b364feac3d25a0d24
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751557"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="517ec-103">Berichte im Office-Format generieren, die eingebettete Bilder haben</span><span class="sxs-lookup"><span data-stu-id="517ec-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="517ec-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Rolle „Systemadministratorrolle“ oder „Entwickler für elektronische Berichterstellung“ angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="517ec-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="517ec-105">In diesem Beispiel erstellen Sie eine ER-Konfigurationen für das Beispielunternehmen „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="517ec-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="517ec-106">Um diese Schritte auszuführen, müssen Sie die Schritte zuerst im „ER Berichte im MS Office-Formaten mit eingebetteten Bildern (Teil 2: Konfiguration überprüfen)“ Aufgabenleitfaden erstellen.</span><span class="sxs-lookup"><span data-stu-id="517ec-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="517ec-107">Diese Schritte können im „USMF“-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="517ec-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="517ec-108">Führen Sie das Format mit Initialenmodellzuordnung aus</span><span class="sxs-lookup"><span data-stu-id="517ec-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="517ec-109">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="517ec-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="517ec-110">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="517ec-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="517ec-111">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="517ec-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="517ec-112">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="517ec-112">Click Check.</span></span>
5. <span data-ttu-id="517ec-113">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="517ec-113">Click Print test.</span></span>
    * <span data-ttu-id="517ec-114">Führen Sie das Format für Testzwecke aus.</span><span class="sxs-lookup"><span data-stu-id="517ec-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="517ec-115">Wählen Sie die Option Ja im Feld Verhandelbares Scheckformatgebiet aus.</span><span class="sxs-lookup"><span data-stu-id="517ec-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="517ec-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="517ec-116">Click OK.</span></span>
    * <span data-ttu-id="517ec-117">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="517ec-117">Review the created output.</span></span> <span data-ttu-id="517ec-118">Das Unternehmenslogo wird ebenso im Bericht angezeigt wie die Signatur der autorisierten Person.</span><span class="sxs-lookup"><span data-stu-id="517ec-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="517ec-119">Das Bild der Signatur stammt aus dem Feld vom Datentyp „Container“ des Schecklayoutdatensatzes, der dem ausgewählten Bankkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="517ec-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="517ec-120">Erweitern Sie den Abschnitt Kopien.</span><span class="sxs-lookup"><span data-stu-id="517ec-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="517ec-121">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="517ec-121">Click Edit.</span></span>
10. <span data-ttu-id="517ec-122">Im Wasserzeichengebiet geben Sie "Wasserzeichen als Nichtig drucken".</span><span class="sxs-lookup"><span data-stu-id="517ec-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="517ec-123">Ändern Sie die Wasserzeichenlayouteinstellung, um den Wasserzeichentext anzuzeigen, wenn Sie in einem Dokument Excel-Formelement generieren.</span><span class="sxs-lookup"><span data-stu-id="517ec-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="517ec-124">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="517ec-124">Click Print test.</span></span>
12. <span data-ttu-id="517ec-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="517ec-125">Click OK.</span></span>
    * <span data-ttu-id="517ec-126">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="517ec-126">Review the created output.</span></span> <span data-ttu-id="517ec-127">Das Wasserzeichen wird im erstellten Bericht in Übereinstimmung mit der Auswahloption angezeigt.</span><span class="sxs-lookup"><span data-stu-id="517ec-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="517ec-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-128">Close the page.</span></span>
14. <span data-ttu-id="517ec-129">Klicken Sie im Aktivitätsbereich auf Zahlungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="517ec-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="517ec-130">Klicken Sie auf Schecks.</span><span class="sxs-lookup"><span data-stu-id="517ec-130">Click Checks.</span></span>
16. <span data-ttu-id="517ec-131">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="517ec-131">Click Show filters.</span></span>
17. <span data-ttu-id="517ec-132">Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert von 381, 385, 389 im Checkfeld mithilfe des Filterzeichens ein.</span><span class="sxs-lookup"><span data-stu-id="517ec-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="517ec-133">Schalten Sie in der Liste 'Alle Zeilen markieren' ein/aus.</span><span class="sxs-lookup"><span data-stu-id="517ec-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="517ec-134">Scheckkopie drucken anklicken.</span><span class="sxs-lookup"><span data-stu-id="517ec-134">Click Print check copy.</span></span>
    * <span data-ttu-id="517ec-135">Führen Sie das Format aus, um die ausgewählten Schecks erneut zu drucken.</span><span class="sxs-lookup"><span data-stu-id="517ec-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="517ec-136">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="517ec-136">Review the created output.</span></span> <span data-ttu-id="517ec-137">Die ausgewählten Schecks wurden erneut gedruckt.</span><span class="sxs-lookup"><span data-stu-id="517ec-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="517ec-138">Das Firmenlogo und die Bezeichnungen werden nicht ausgedruckt, wie sie auf dem Vordruck dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="517ec-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="517ec-139">Überprüfe Sie die Struktur des importierten Datenmodells.</span><span class="sxs-lookup"><span data-stu-id="517ec-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="517ec-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-140">Close the page.</span></span>
2. <span data-ttu-id="517ec-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-141">Close the page.</span></span>
3. <span data-ttu-id="517ec-142">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="517ec-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="517ec-143">Wählen Sie in der Struktur 'Modell für Cheques.</span><span class="sxs-lookup"><span data-stu-id="517ec-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="517ec-144">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="517ec-144">Click Designer.</span></span>
6. <span data-ttu-id="517ec-145">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="517ec-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="517ec-146">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="517ec-146">Click Designer.</span></span>
    * <span data-ttu-id="517ec-147">Wir ändern die Bindung des Signaturartikels des Datenmodells, um das Signaturbild aus der Datei zu erhalten, die dem Schecklayoutdatensatz zugeordnet wurde, der dem ausgewählten Bankkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="517ec-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="517ec-148">Deaktivieren Sie „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="517ec-148">Turn off Show details.</span></span>
9. <span data-ttu-id="517ec-149">Erweitern Sie in der Struktur Layout.</span><span class="sxs-lookup"><span data-stu-id="517ec-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="517ec-150">Erweitern oder reduzieren Sie Layout\Unterschrift.</span><span class="sxs-lookup"><span data-stu-id="517ec-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="517ec-151">Wählen Sie in der Strukturdarstellung Layout\Unterschrift\Bild= chequesaccount<Beziehungen. BankChequeLayout.Signature1Bmp.</span><span class="sxs-lookup"><span data-stu-id="517ec-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="517ec-152">Erweitern oder reduzieren Sie chequesaccount.</span><span class="sxs-lookup"><span data-stu-id="517ec-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="517ec-153">In der Struktur erweitern chequesaccount\<Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="517ec-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="517ec-154">Erweitern Sie in der Struktur chequesaccount\<Beziehungen\BankChequeLayout.</span><span class="sxs-lookup"><span data-stu-id="517ec-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="517ec-155">Erweitern Sie in der Struktur chequesaccount\<BeziehungenBankChequeLayout\<Relations.</span><span class="sxs-lookup"><span data-stu-id="517ec-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="517ec-156">Erweitern Sie in der Struktur 'chequesaccount\<BeziehungBankChequeLayout\<Beziehung\<Dokumente'.</span><span class="sxs-lookup"><span data-stu-id="517ec-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="517ec-157">Wählen Sie in der Strukturdarstellung 'chequesaccount\<BeziehungBankChequeLayout\<Beziehung\<DokumentegetFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="517ec-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="517ec-158">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="517ec-158">Click Bind.</span></span>
19. <span data-ttu-id="517ec-159">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="517ec-159">Click Save.</span></span>
20. <span data-ttu-id="517ec-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-160">Close the page.</span></span>
21. <span data-ttu-id="517ec-161">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-161">Close the page.</span></span>
22. <span data-ttu-id="517ec-162">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-162">Close the page.</span></span>
23. <span data-ttu-id="517ec-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="517ec-164">Die Formatzuordnung zum Datenmodell ausführen</span><span class="sxs-lookup"><span data-stu-id="517ec-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="517ec-165">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="517ec-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="517ec-166">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="517ec-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="517ec-167">Filtern Sie beispielsweise im Feld "Bankkontofeld" mit dem Wert "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="517ec-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="517ec-168">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="517ec-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="517ec-169">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="517ec-169">Click Check.</span></span>
5. <span data-ttu-id="517ec-170">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="517ec-170">Click Print test.</span></span>
6. <span data-ttu-id="517ec-171">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="517ec-171">Click OK.</span></span>
    * <span data-ttu-id="517ec-172">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="517ec-172">Review the created output.</span></span> <span data-ttu-id="517ec-173">Das Bild aus dem Dokumentverwaltungsanhang stellt die Signatur einer autorisierten Person dar.</span><span class="sxs-lookup"><span data-stu-id="517ec-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="517ec-174">Verwenden Sie das MS Word-Dokument als Vorlage im importierten Format</span><span class="sxs-lookup"><span data-stu-id="517ec-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="517ec-175">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-175">Close the page.</span></span>
2. <span data-ttu-id="517ec-176">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-176">Close the page.</span></span>
3. <span data-ttu-id="517ec-177">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="517ec-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="517ec-178">Wählen Sie in der Struktur erweitern 'Modell für Cheques.</span><span class="sxs-lookup"><span data-stu-id="517ec-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="517ec-179">Wählen Sie in der Strukturdarstellung "Modell für Cheques\Cheques-Druckformat.</span><span class="sxs-lookup"><span data-stu-id="517ec-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="517ec-180">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="517ec-180">Click Designer.</span></span>
7. <span data-ttu-id="517ec-181">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="517ec-181">Click Attachments.</span></span>
8. <span data-ttu-id="517ec-182">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="517ec-182">Click Delete.</span></span>
9. <span data-ttu-id="517ec-183">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="517ec-183">Click Yes.</span></span>
10. <span data-ttu-id="517ec-184">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="517ec-184">Click New.</span></span>
11. <span data-ttu-id="517ec-185">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="517ec-185">Click File.</span></span>
    * <span data-ttu-id="517ec-186">Navigieren und wählen Sie die heruntergeladene Datei „Scheck-Vorlage Word.docx“ aus.</span><span class="sxs-lookup"><span data-stu-id="517ec-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="517ec-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-187">Close the page.</span></span>
13. <span data-ttu-id="517ec-188">Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="517ec-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="517ec-189">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="517ec-189">Click Save.</span></span>
15. <span data-ttu-id="517ec-190">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-190">Close the page.</span></span>
16. <span data-ttu-id="517ec-191">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="517ec-191">Click Edit.</span></span>
17. <span data-ttu-id="517ec-192">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="517ec-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="517ec-193">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="517ec-193">Close the page.</span></span>
19. <span data-ttu-id="517ec-194">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="517ec-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="517ec-195">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="517ec-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="517ec-196">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="517ec-196">Click Check.</span></span>
22. <span data-ttu-id="517ec-197">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="517ec-197">Click Print test.</span></span>
23. <span data-ttu-id="517ec-198">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="517ec-198">Click OK.</span></span>
    * <span data-ttu-id="517ec-199">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="517ec-199">Review the created output.</span></span> <span data-ttu-id="517ec-200">Die Ausgabe wurde als ein Word-Dokument mit eingebetteten Bildern generiert, die das Unternehmenslogo, die Signatur einer autorisierten Person und den markierten Text des Wasserzeichens darstellen.</span><span class="sxs-lookup"><span data-stu-id="517ec-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]