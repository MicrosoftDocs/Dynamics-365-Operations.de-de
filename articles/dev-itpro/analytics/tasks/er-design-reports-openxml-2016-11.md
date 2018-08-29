--- 
title: EB-Konfigurationen entwerfen, um Berichte im OpenXML-Format zu generieren
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="2d12f-103">EB-Konfigurationen entwerfen, um Berichte im OpenXML-Format zu generieren</span><span class="sxs-lookup"><span data-stu-id="2d12f-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d12f-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="2d12f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="2d12f-105">Diese Konfiguration wird zur Verarbeitung von Kreditorenzahlungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d12f-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="2d12f-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können im GBSI-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="2d12f-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="2d12f-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="2d12f-108">Sie müssen auch die Microsoft Excel-Datei herunterladen und speichern [Vorlage des Zahlungsberichts](https://go.microsoft.com/fwlink/?linkid=862266) und speichern.</span><span class="sxs-lookup"><span data-stu-id="2d12f-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="2d12f-109">Laden Sie die Zahlungsdatenmodell-Konfiguration hoch</span><span class="sxs-lookup"><span data-stu-id="2d12f-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="2d12f-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="2d12f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2d12f-111">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="2d12f-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2d12f-112">Wählen Sie den Konfigurationsanbieter für das Beispielunternehmen "Litware, Inc.". Wenn Sie diesen Konfigurationsanbieter nicht finden, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="2d12f-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="2d12f-113">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="2d12f-113">Click Set active.</span></span>
4. <span data-ttu-id="2d12f-114">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="2d12f-114">Click Repositories.</span></span>
    * <span data-ttu-id="2d12f-115">Wählen Sie ein Repository für den Typ „Betriebliche Ressource” aus, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2d12f-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="2d12f-116">Wenn es verfügbar ist, überspringen Sie die folgenden Schritte zur Erstellung eines neuen Repository.</span><span class="sxs-lookup"><span data-stu-id="2d12f-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="2d12f-117">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="2d12f-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="2d12f-118">Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="2d12f-119">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="2d12f-119">Click Create repository.</span></span>
8. <span data-ttu-id="2d12f-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2d12f-120">Click OK.</span></span>
9. <span data-ttu-id="2d12f-121">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="2d12f-121">Click Open.</span></span>
10. <span data-ttu-id="2d12f-122">Wählen Sie in der Struktur die Option "Zahlungsmodell" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="2d12f-123">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="2d12f-123">Click Import.</span></span>
    * <span data-ttu-id="2d12f-124">Importieren Sie dieses Datenmodell.</span><span class="sxs-lookup"><span data-stu-id="2d12f-124">Import this data model.</span></span> <span data-ttu-id="2d12f-125">Es wird als Datenquelle in einer neuen Formatkonfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d12f-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="2d12f-126">Überspringen Sie diesen Schritt, wenn diese Konfiguration bereits importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2d12f-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="2d12f-127">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="2d12f-127">Click Yes.</span></span>
13. <span data-ttu-id="2d12f-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2d12f-128">Close the page.</span></span>
14. <span data-ttu-id="2d12f-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2d12f-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="2d12f-130">Dient zum Erstellen einer neuen Format-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d12f-130">Create a new format configuration</span></span>
1. <span data-ttu-id="2d12f-131">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="2d12f-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="2d12f-132">Wählen Sie in der Struktur die Option "Zahlungsmodell" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="2d12f-133">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2d12f-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="2d12f-134">Wählen Sie im neuen Feld geben Sie "Format auf Grundlage Datenmodell PaymentModel" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="2d12f-135">Erstellen Sie ein Format, das auf dem PaymentModel-Datenmodell basiert.</span><span class="sxs-lookup"><span data-stu-id="2d12f-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="2d12f-136">Geben Sie im Feld "Name" die Bezeichnung "Beispiel-Arbeitsblattbericht" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="2d12f-137">Beispiel-Arbeitsblattbericht</span><span class="sxs-lookup"><span data-stu-id="2d12f-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="2d12f-138">Geben Sie im Feld "Beschreibung" die Bezeichnung "Beispiel-Arbeitsblattbericht für Kreditorenzahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="2d12f-139">Beispiel-Arbeitsblattbericht für Zahlungen der Händler.</span><span class="sxs-lookup"><span data-stu-id="2d12f-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="2d12f-140">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2d12f-141">Wählen Sie die Definition "CustomerCreditTransferInitiation" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="2d12f-142">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="2d12f-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="2d12f-143">Entwerfen Sie ein neues Dokument im OPENXML-Arbeitsblattformat</span><span class="sxs-lookup"><span data-stu-id="2d12f-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="2d12f-144">Wählen Sie in der Struktur die Option "Zahlungsmodell \Beispiel-Arbeitsblattbericht" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="2d12f-145">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="2d12f-145">Click Designer.</span></span>
3. <span data-ttu-id="2d12f-146">Klicken Sie im Aktivitätsbereich auf "Importieren".</span><span class="sxs-lookup"><span data-stu-id="2d12f-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="2d12f-147">Klicken Sie auf "Aus Excel importieren".</span><span class="sxs-lookup"><span data-stu-id="2d12f-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="2d12f-148">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="2d12f-148">Click Attachments.</span></span>
    * <span data-ttu-id="2d12f-149">Fügen Sie das vorhandene Excel-Dokument als Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="2d12f-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="2d12f-150">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2d12f-150">Click New.</span></span>
7. <span data-ttu-id="2d12f-151">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="2d12f-151">Click File.</span></span>
    * <span data-ttu-id="2d12f-152">Zeigen Sie auf die vorhandene Excel-Datei.</span><span class="sxs-lookup"><span data-stu-id="2d12f-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="2d12f-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2d12f-153">Close the page.</span></span>
9. <span data-ttu-id="2d12f-154">Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="2d12f-155">Wählen Sie die angefügte Excel-Datei aus, um als Vorlage verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="2d12f-156">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2d12f-156">Click OK.</span></span>
    * <span data-ttu-id="2d12f-157">Beachten Sie, dass ER-Formatkomponenten im Entwurfsformat auf Grundlage der Struktur des verweisenden MS Excel-Dokuments (genannte Bereiche) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="2d12f-158">Erstellen Sie eine neue Datenquelle, um Summen nach Währungscodes zu berechnen</span><span class="sxs-lookup"><span data-stu-id="2d12f-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="2d12f-159">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="2d12f-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="2d12f-160">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2d12f-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="2d12f-161">Wählen Sie in der Struktur "Funktionen\Gruppieren nach" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="2d12f-162">Geben Sie im Feld "Name" die Zeichenfolge "PaymentByCurrency" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="2d12f-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="2d12f-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="2d12f-164">Klicken Sie auf "Gruppe bearbeiten von".</span><span class="sxs-lookup"><span data-stu-id="2d12f-164">Click Edit group by.</span></span>
6. <span data-ttu-id="2d12f-165">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="2d12f-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="2d12f-166">Wählen Sie 'Modell\Zahlungen' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="2d12f-167">Klicken Sie auf "Feld hinzufügen zu".</span><span class="sxs-lookup"><span data-stu-id="2d12f-167">Click Add field to.</span></span>
9. <span data-ttu-id="2d12f-168">Klicken Sie auf "Was gruppieren".</span><span class="sxs-lookup"><span data-stu-id="2d12f-168">Click What to group.</span></span>
10. <span data-ttu-id="2d12f-169">Erweitern Sie 'Modell\Zahlungen' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="2d12f-170">Wählen Sie in der Struktur "Modell\Zahlungen\Währung" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="2d12f-171">Klicken Sie auf "Feld hinzufügen zu".</span><span class="sxs-lookup"><span data-stu-id="2d12f-171">Click Add field to.</span></span>
13. <span data-ttu-id="2d12f-172">Klicken Sie auf "Gruppierte Felder".</span><span class="sxs-lookup"><span data-stu-id="2d12f-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="2d12f-173">In der Struktur wählen Sie "Modell\Zahlungen\Angewiesener Betrag (InstructedAmount)" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="2d12f-174">Klicken Sie auf "Feld hinzufügen zu".</span><span class="sxs-lookup"><span data-stu-id="2d12f-174">Click Add field to.</span></span>
16. <span data-ttu-id="2d12f-175">Klicken Sie auf "Aggregationsfelder".</span><span class="sxs-lookup"><span data-stu-id="2d12f-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="2d12f-176">Wählen Sie im Feld "Methode" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="2d12f-177">Wählen Sie die SUMMEN_Aggregationsfunktion aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="2d12f-178">Geben Sie im Feld "Name" die Zeichenfolge "TotalInstructuredAmount" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="2d12f-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="2d12f-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="2d12f-180">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2d12f-180">Click Save.</span></span>
20. <span data-ttu-id="2d12f-181">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2d12f-181">Close the page.</span></span>
21. <span data-ttu-id="2d12f-182">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2d12f-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="2d12f-183">Weisen Sie Datenquellen Formatkomponenten zu</span><span class="sxs-lookup"><span data-stu-id="2d12f-183">Map format components to data sources</span></span>
1. <span data-ttu-id="2d12f-184">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="2d12f-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="2d12f-185">Erweitern Sie 'Modell\Zahlungen' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="2d12f-186">Erweitern Sie in der Struktur "Modell\Zahlungen\Einleitende Partei(InitiatingParty)".</span><span class="sxs-lookup"><span data-stu-id="2d12f-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="2d12f-187">Wählen Sie in der Struktur "'Modell\Zahlungen\Einleitende Partei(InitiatingParty)\Name" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="2d12f-188">Erweitern oder reduzieren Sie „Excel\ReportHeader” in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="2d12f-189">Wählen Sie „Excel\ReportHeader\CompanyName” in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="2d12f-190">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-190">Click Bind.</span></span>
8. <span data-ttu-id="2d12f-191">Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="2d12f-192">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Kennung".</span><span class="sxs-lookup"><span data-stu-id="2d12f-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="2d12f-193">In der Struktur wählen Sie "Modell\Zahlungen\Kreditor\Kennung\Quell-ID(SourceID)" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="2d12f-194">Erweitern Sie „Excel\PaymLines” in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="2d12f-195">Wählen Sie in der Struktur „Excel\PaymLines\VendAccountName” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="2d12f-196">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-196">Click Bind.</span></span>
14. <span data-ttu-id="2d12f-197">Wählen Sie 'Modell\Payments\Creditor\Account\Name' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="2d12f-198">Wählen Sie in der Struktur „Excel\PaymLines\VendName” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="2d12f-199">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-199">Click Bind.</span></span>
17. <span data-ttu-id="2d12f-200">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)".</span><span class="sxs-lookup"><span data-stu-id="2d12f-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="2d12f-201">In der Struktur wählen Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)\Name" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="2d12f-202">Wählen Sie in der Struktur „Excel\PaymLines\Bank” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="2d12f-203">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-203">Click Bind.</span></span>
21. <span data-ttu-id="2d12f-204">Wählen Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)\Bankleitzahl(RoutingNumber)" in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="2d12f-205">Wählen Sie in der Struktur „Excel\PaymLines\RoutingNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="2d12f-206">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-206">Click Bind.</span></span>
24. <span data-ttu-id="2d12f-207">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="2d12f-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="2d12f-208">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)\Identification".</span><span class="sxs-lookup"><span data-stu-id="2d12f-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="2d12f-209">In der Struktur wählen Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)\Kennung\Nummer".</span><span class="sxs-lookup"><span data-stu-id="2d12f-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="2d12f-210">Wählen Sie in der Struktur „Excel\PaymLines\AccountNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="2d12f-211">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-211">Click Bind.</span></span>
29. <span data-ttu-id="2d12f-212">In der Struktur wählen Sie "Modell\Zahlungen\Angewiesener Betrag (InstructedAmount)" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="2d12f-213">Wählen Sie in der Struktur „Excel\PaymLines\Soll” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="2d12f-214">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-214">Click Bind.</span></span>
32. <span data-ttu-id="2d12f-215">Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="2d12f-216">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="2d12f-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="2d12f-217">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)".</span><span class="sxs-lookup"><span data-stu-id="2d12f-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="2d12f-218">Wählen Sie in der Struktur "Modell\Zahlungen\Währung" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="2d12f-219">Wählen Sie in der Struktur „Excel\PaymLines\Währung” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="2d12f-220">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-220">Click Bind.</span></span>
38. <span data-ttu-id="2d12f-221">Erweitern Sie "PaymentByCurrency" in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="2d12f-222">Erweitern Sie "PaymentByCurrency\grouped" in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="2d12f-223">Wählen Sie in der Struktur "PaymentByCurrency\grouped\Currency" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="2d12f-224">Erweitern Sie „Excel\SummaryLines” in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="2d12f-225">Wählen Sie in der Struktur „Excel\SummaryLines\SummaryCurrency” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="2d12f-226">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-226">Click Bind.</span></span>
44. <span data-ttu-id="2d12f-227">Erweitern Sie "PaymentByCurrency\aggregated" in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="2d12f-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="2d12f-228">Wählen Sie in der Struktur "PaymentByCurrency\aggregated\TotalInstructuredAmount" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="2d12f-229">Wählen Sie in der Struktur „Excel\SummaryLines\SummaryAmount” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="2d12f-230">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-230">Click Bind.</span></span>
48. <span data-ttu-id="2d12f-231">Wählen Sie in der Struktur "PaymentByCurrency" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="2d12f-232">Wählen Sie in der Struktur „Excel\SummaryLines” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="2d12f-233">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-233">Click Bind.</span></span>
51. <span data-ttu-id="2d12f-234">Wählen Sie 'Modell\Zahlungen' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="2d12f-235">Wählen Sie in der Struktur „Excel\PaymLines” aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="2d12f-236">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="2d12f-236">Click Bind.</span></span>
54. <span data-ttu-id="2d12f-237">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2d12f-237">Click Save.</span></span>
55. <span data-ttu-id="2d12f-238">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2d12f-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="2d12f-239">Nutzen Sie die erstellte Konfiguration für die Zahlungsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="2d12f-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="2d12f-240">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="2d12f-240">Click Change status.</span></span>
2. <span data-ttu-id="2d12f-241">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="2d12f-241">Click Complete.</span></span>
3. <span data-ttu-id="2d12f-242">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2d12f-242">Click OK.</span></span>
4. <span data-ttu-id="2d12f-243">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2d12f-243">Close the page.</span></span>
5. <span data-ttu-id="2d12f-244">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2d12f-244">Close the page.</span></span>
6. <span data-ttu-id="2d12f-245">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="2d12f-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="2d12f-246">Verwenden Sie den Schnellfilter, um im Feld „Zahlungsmethode” nach dem Wert „Elektronisch” zu filtern.</span><span class="sxs-lookup"><span data-stu-id="2d12f-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="2d12f-247">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="2d12f-247">Electronic</span></span>  
8. <span data-ttu-id="2d12f-248">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="2d12f-248">Click Edit.</span></span>
9. <span data-ttu-id="2d12f-249">Erweitern Sie den Abschnitt 'Dateiformate'.</span><span class="sxs-lookup"><span data-stu-id="2d12f-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="2d12f-250">Wählen Sie "Ja" im Feld "Generische elektronische Berichterstellung" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="2d12f-251">Wählen Sie im Feld "Formatkonfiguration exportieren" einen Wert aus oder geben Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="2d12f-252">Wählen Sie die Variante "Beispiel-Arbeitsblattbericht" aus.</span><span class="sxs-lookup"><span data-stu-id="2d12f-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="2d12f-253">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2d12f-253">Click Save.</span></span>
13. <span data-ttu-id="2d12f-254">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2d12f-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="2d12f-255">Verwenden Sie die erstellte Konfiguration für das Testen der Zahlungserfassungsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="2d12f-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="2d12f-256">Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="2d12f-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2d12f-257">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2d12f-257">Click New.</span></span>
    * <span data-ttu-id="2d12f-258">Erstellen Sie eine Zahlungserfassung.</span><span class="sxs-lookup"><span data-stu-id="2d12f-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="2d12f-259">Geben Sie im Namensfeld "VendPay" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="2d12f-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="2d12f-260">VendPay</span></span>  
4. <span data-ttu-id="2d12f-261">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="2d12f-261">Click Lines.</span></span>
5. <span data-ttu-id="2d12f-262">Geben Sie im Feld "Konto" die Werte "GB_SI_000001" an.</span><span class="sxs-lookup"><span data-stu-id="2d12f-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="2d12f-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="2d12f-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="2d12f-264">Legen Sie "Soll" auf "1000" fest.</span><span class="sxs-lookup"><span data-stu-id="2d12f-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="2d12f-265">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2d12f-265">Click New.</span></span>
8. <span data-ttu-id="2d12f-266">Geben Sie im Feld "Konto" die Werte "GB_SI_000005" an.</span><span class="sxs-lookup"><span data-stu-id="2d12f-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="2d12f-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="2d12f-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="2d12f-268">Legen Sie "Soll" auf "2000" fest.</span><span class="sxs-lookup"><span data-stu-id="2d12f-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="2d12f-269">Geben Sie im Feld "Währung" die Zeichenfolge "EUR" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="2d12f-270">EUR</span><span class="sxs-lookup"><span data-stu-id="2d12f-270">EUR</span></span>  
11. <span data-ttu-id="2d12f-271">Geben Sie im Feld "Gegenkonto" die Werte "GBSI OPER" an.</span><span class="sxs-lookup"><span data-stu-id="2d12f-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="2d12f-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="2d12f-272">GBSI OPER</span></span>  
12. <span data-ttu-id="2d12f-273">Geben Sie im Feld "Zahlungsmethode" die Option "Elektronisch" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="2d12f-274">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="2d12f-274">Electronic</span></span>  
13. <span data-ttu-id="2d12f-275">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2d12f-275">Click Save.</span></span>
14. <span data-ttu-id="2d12f-276">Klicken Sie auf Zahlungen generieren.</span><span class="sxs-lookup"><span data-stu-id="2d12f-276">Click Generate payments.</span></span>
15. <span data-ttu-id="2d12f-277">Geben Sie im Feld "Zahlungsmethode" die Option "Elektronisch" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="2d12f-278">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="2d12f-278">Electronic</span></span>  
16. <span data-ttu-id="2d12f-279">Geben Sie im Feld „Dateiname” die Bezeichnung „Zahlungen” ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="2d12f-280">Geben Sie beispielsweise "Zahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="2d12f-281">Geben Sie im Feld "Bankkonto" die Zeichenfolge "GBSI OPER" ein.</span><span class="sxs-lookup"><span data-stu-id="2d12f-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="2d12f-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="2d12f-282">GBSI OPER</span></span>  
18. <span data-ttu-id="2d12f-283">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2d12f-283">Click OK.</span></span>
19. <span data-ttu-id="2d12f-284">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2d12f-284">Click OK.</span></span>
    * <span data-ttu-id="2d12f-285">Überprüfen Sie das erstellte Arbeitsblatt, einschließlich Details von Zahlungspositionen sowie der Summen für jeden Währungscode, der in dieser Zahlungsnachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d12f-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


