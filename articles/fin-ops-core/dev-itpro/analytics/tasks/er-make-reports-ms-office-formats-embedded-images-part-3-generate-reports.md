---
title: Berichte im Office-Format generieren, die eingebettete Bilder haben
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Rolle „Systemadministratorrolle“ oder „Entwickler für elektronische Berichterstellung“ angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 78dcdbd83dc717104d437662f7f451c9ecb714cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684378"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="4dc58-103">Berichte im Office-Format generieren, die eingebettete Bilder haben</span><span class="sxs-lookup"><span data-stu-id="4dc58-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4dc58-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Rolle „Systemadministratorrolle“ oder „Entwickler für elektronische Berichterstellung“ angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="4dc58-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="4dc58-105">In diesem Beispiel erstellen Sie eine ER-Konfigurationen für das Beispielunternehmen „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="4dc58-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="4dc58-106">Um diese Schritte auszuführen, müssen Sie die Schritte zuerst im „ER Berichte im MS Office-Formaten mit eingebetteten Bildern (Teil 2: Konfiguration überprüfen)“ Aufgabenleitfaden erstellen.</span><span class="sxs-lookup"><span data-stu-id="4dc58-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="4dc58-107">Diese Schritte können im „USMF“-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4dc58-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="4dc58-108">Führen Sie das Format mit Initialenmodellzuordnung aus</span><span class="sxs-lookup"><span data-stu-id="4dc58-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="4dc58-109">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="4dc58-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="4dc58-110">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="4dc58-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="4dc58-111">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="4dc58-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="4dc58-112">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="4dc58-112">Click Check.</span></span>
5. <span data-ttu-id="4dc58-113">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="4dc58-113">Click Print test.</span></span>
    * <span data-ttu-id="4dc58-114">Führen Sie das Format für Testzwecke aus.</span><span class="sxs-lookup"><span data-stu-id="4dc58-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="4dc58-115">Wählen Sie die Option Ja im Feld Verhandelbares Scheckformatgebiet aus.</span><span class="sxs-lookup"><span data-stu-id="4dc58-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="4dc58-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4dc58-116">Click OK.</span></span>
    * <span data-ttu-id="4dc58-117">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="4dc58-117">Review the created output.</span></span> <span data-ttu-id="4dc58-118">Das Unternehmenslogo wird ebenso im Bericht angezeigt wie die Signatur der autorisierten Person.</span><span class="sxs-lookup"><span data-stu-id="4dc58-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="4dc58-119">Das Bild der Signatur stammt aus dem Feld vom Datentyp „Container“ des Schecklayoutdatensatzes, der dem ausgewählten Bankkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4dc58-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="4dc58-120">Erweitern Sie den Abschnitt Kopien.</span><span class="sxs-lookup"><span data-stu-id="4dc58-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="4dc58-121">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="4dc58-121">Click Edit.</span></span>
10. <span data-ttu-id="4dc58-122">Im Wasserzeichengebiet geben Sie "Wasserzeichen als Nichtig drucken".</span><span class="sxs-lookup"><span data-stu-id="4dc58-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="4dc58-123">Ändern Sie die Wasserzeichenlayouteinstellung, um den Wasserzeichentext anzuzeigen, wenn Sie in einem Dokument Excel-Formelement generieren.</span><span class="sxs-lookup"><span data-stu-id="4dc58-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="4dc58-124">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="4dc58-124">Click Print test.</span></span>
12. <span data-ttu-id="4dc58-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4dc58-125">Click OK.</span></span>
    * <span data-ttu-id="4dc58-126">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="4dc58-126">Review the created output.</span></span> <span data-ttu-id="4dc58-127">Das Wasserzeichen wird im erstellten Bericht in Übereinstimmung mit der Auswahloption angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4dc58-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="4dc58-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-128">Close the page.</span></span>
14. <span data-ttu-id="4dc58-129">Klicken Sie im Aktivitätsbereich auf Zahlungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="4dc58-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="4dc58-130">Klicken Sie auf Schecks.</span><span class="sxs-lookup"><span data-stu-id="4dc58-130">Click Checks.</span></span>
16. <span data-ttu-id="4dc58-131">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="4dc58-131">Click Show filters.</span></span>
17. <span data-ttu-id="4dc58-132">Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert von 381, 385, 389 im Checkfeld mithilfe des Filterzeichens ein.</span><span class="sxs-lookup"><span data-stu-id="4dc58-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="4dc58-133">Schalten Sie in der Liste 'Alle Zeilen markieren' ein/aus.</span><span class="sxs-lookup"><span data-stu-id="4dc58-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="4dc58-134">Scheckkopie drucken anklicken.</span><span class="sxs-lookup"><span data-stu-id="4dc58-134">Click Print check copy.</span></span>
    * <span data-ttu-id="4dc58-135">Führen Sie das Format aus, um die ausgewählten Schecks erneut zu drucken.</span><span class="sxs-lookup"><span data-stu-id="4dc58-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="4dc58-136">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="4dc58-136">Review the created output.</span></span> <span data-ttu-id="4dc58-137">Die ausgewählten Schecks wurden erneut gedruckt.</span><span class="sxs-lookup"><span data-stu-id="4dc58-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="4dc58-138">Das Firmenlogo und die Bezeichnungen werden nicht ausgedruckt, wie sie auf dem Vordruck dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4dc58-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="4dc58-139">Überprüfe Sie die Struktur des importierten Datenmodells.</span><span class="sxs-lookup"><span data-stu-id="4dc58-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="4dc58-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-140">Close the page.</span></span>
2. <span data-ttu-id="4dc58-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-141">Close the page.</span></span>
3. <span data-ttu-id="4dc58-142">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4dc58-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="4dc58-143">Wählen Sie in der Struktur 'Modell für Cheques.</span><span class="sxs-lookup"><span data-stu-id="4dc58-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="4dc58-144">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="4dc58-144">Click Designer.</span></span>
6. <span data-ttu-id="4dc58-145">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="4dc58-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="4dc58-146">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="4dc58-146">Click Designer.</span></span>
    * <span data-ttu-id="4dc58-147">Wir ändern die Bindung des Signaturartikels des Datenmodells, um das Signaturbild aus der Datei zu erhalten, die dem Schecklayoutdatensatz zugeordnet wurde, der dem ausgewählten Bankkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4dc58-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="4dc58-148">Deaktivieren Sie „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="4dc58-148">Turn off Show details.</span></span>
9. <span data-ttu-id="4dc58-149">Erweitern Sie in der Struktur Layout.</span><span class="sxs-lookup"><span data-stu-id="4dc58-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="4dc58-150">Erweitern oder reduzieren Sie Layout\Unterschrift.</span><span class="sxs-lookup"><span data-stu-id="4dc58-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="4dc58-151">Wählen Sie in der Strukturdarstellung Layout\Unterschrift\Bild= chequesaccount<Beziehungen. BankChequeLayout.Signature1Bmp.</span><span class="sxs-lookup"><span data-stu-id="4dc58-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="4dc58-152">Erweitern oder reduzieren Sie chequesaccount.</span><span class="sxs-lookup"><span data-stu-id="4dc58-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="4dc58-153">In der Struktur erweitern chequesaccount\<Beziehungen.</span><span class="sxs-lookup"><span data-stu-id="4dc58-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="4dc58-154">Erweitern Sie in der Struktur chequesaccount\<Beziehungen\BankChequeLayout.</span><span class="sxs-lookup"><span data-stu-id="4dc58-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="4dc58-155">Erweitern Sie in der Struktur chequesaccount\<BeziehungenBankChequeLayout\<Relations.</span><span class="sxs-lookup"><span data-stu-id="4dc58-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="4dc58-156">Erweitern Sie in der Struktur 'chequesaccount\<BeziehungBankChequeLayout\<Beziehung\<Dokumente'.</span><span class="sxs-lookup"><span data-stu-id="4dc58-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="4dc58-157">Wählen Sie in der Strukturdarstellung 'chequesaccount\<BeziehungBankChequeLayout\<Beziehung\<DokumentegetFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="4dc58-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="4dc58-158">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="4dc58-158">Click Bind.</span></span>
19. <span data-ttu-id="4dc58-159">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4dc58-159">Click Save.</span></span>
20. <span data-ttu-id="4dc58-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-160">Close the page.</span></span>
21. <span data-ttu-id="4dc58-161">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-161">Close the page.</span></span>
22. <span data-ttu-id="4dc58-162">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-162">Close the page.</span></span>
23. <span data-ttu-id="4dc58-163">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="4dc58-164">Die Formatzuordnung zum Datenmodell ausführen</span><span class="sxs-lookup"><span data-stu-id="4dc58-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="4dc58-165">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="4dc58-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="4dc58-166">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4dc58-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4dc58-167">Filtern Sie beispielsweise im Feld "Bankkontofeld" mit dem Wert "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="4dc58-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="4dc58-168">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="4dc58-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="4dc58-169">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="4dc58-169">Click Check.</span></span>
5. <span data-ttu-id="4dc58-170">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="4dc58-170">Click Print test.</span></span>
6. <span data-ttu-id="4dc58-171">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4dc58-171">Click OK.</span></span>
    * <span data-ttu-id="4dc58-172">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="4dc58-172">Review the created output.</span></span> <span data-ttu-id="4dc58-173">Das Bild aus dem Dokumentverwaltungsanhang stellt die Signatur einer autorisierten Person dar.</span><span class="sxs-lookup"><span data-stu-id="4dc58-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="4dc58-174">Verwenden Sie das MS Word-Dokument als Vorlage im importierten Format</span><span class="sxs-lookup"><span data-stu-id="4dc58-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="4dc58-175">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-175">Close the page.</span></span>
2. <span data-ttu-id="4dc58-176">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-176">Close the page.</span></span>
3. <span data-ttu-id="4dc58-177">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4dc58-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="4dc58-178">Wählen Sie in der Struktur erweitern 'Modell für Cheques.</span><span class="sxs-lookup"><span data-stu-id="4dc58-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="4dc58-179">Wählen Sie in der Strukturdarstellung "Modell für Cheques\Cheques-Druckformat.</span><span class="sxs-lookup"><span data-stu-id="4dc58-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="4dc58-180">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="4dc58-180">Click Designer.</span></span>
7. <span data-ttu-id="4dc58-181">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="4dc58-181">Click Attachments.</span></span>
8. <span data-ttu-id="4dc58-182">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="4dc58-182">Click Delete.</span></span>
9. <span data-ttu-id="4dc58-183">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="4dc58-183">Click Yes.</span></span>
10. <span data-ttu-id="4dc58-184">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4dc58-184">Click New.</span></span>
11. <span data-ttu-id="4dc58-185">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="4dc58-185">Click File.</span></span>
    * <span data-ttu-id="4dc58-186">Navigieren und wählen Sie die heruntergeladene Datei „Scheck-Vorlage Word.docx“ aus.</span><span class="sxs-lookup"><span data-stu-id="4dc58-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="4dc58-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-187">Close the page.</span></span>
13. <span data-ttu-id="4dc58-188">Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4dc58-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="4dc58-189">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4dc58-189">Click Save.</span></span>
15. <span data-ttu-id="4dc58-190">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-190">Close the page.</span></span>
16. <span data-ttu-id="4dc58-191">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="4dc58-191">Click Edit.</span></span>
17. <span data-ttu-id="4dc58-192">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="4dc58-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="4dc58-193">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4dc58-193">Close the page.</span></span>
19. <span data-ttu-id="4dc58-194">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="4dc58-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="4dc58-195">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="4dc58-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="4dc58-196">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="4dc58-196">Click Check.</span></span>
22. <span data-ttu-id="4dc58-197">Drucktest anklicken.</span><span class="sxs-lookup"><span data-stu-id="4dc58-197">Click Print test.</span></span>
23. <span data-ttu-id="4dc58-198">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4dc58-198">Click OK.</span></span>
    * <span data-ttu-id="4dc58-199">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="4dc58-199">Review the created output.</span></span> <span data-ttu-id="4dc58-200">Die Ausgabe wurde als ein Word-Dokument mit eingebetteten Bildern generiert, die das Unternehmenslogo, die Signatur einer autorisierten Person und den markierten Text des Wasserzeichens darstellen.</span><span class="sxs-lookup"><span data-stu-id="4dc58-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  

