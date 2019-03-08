---
title: ER Entwerfen einer Konfiguration für das Generieren von Berichten im OPENXML-Format (November 2016)
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "326652"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="24c99-103">ER Entwerfen einer Konfiguration für das Generieren von Berichten im OPENXML-Format (November 2016)</span><span class="sxs-lookup"><span data-stu-id="24c99-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24c99-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine neue Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die eine Vorlage zur Generierung elektronischer Dokumente im OPENXML-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="24c99-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="24c99-105">Diese Konfiguration wird zur Verarbeitung von Kreditorenzahlungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c99-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="24c99-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können im GBSI-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="24c99-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="24c99-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="24c99-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="24c99-108">Sie müssen auch über eine Excel-Datei verfügen, die importiert wird, wenn die Vorlage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="24c99-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="24c99-109">Auf diese Datei kann aus der [Vorlage des Zahlungsberichgte](https://go.microsoft.com/fwlink/?linkid=862266) zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="24c99-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="24c99-110">Laden Sie die Zahlungsdatenmodell-Konfiguration hoch</span><span class="sxs-lookup"><span data-stu-id="24c99-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="24c99-111">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="24c99-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="24c99-112">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="24c99-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="24c99-113">Wählen Sie den Konfigurationsanbieter für das Beispielunternehmen "Litware, Inc.". Wenn Sie diesen Konfigurationsanbieter nicht finden, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="24c99-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="24c99-114">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="24c99-114">Click Set active.</span></span>
4. <span data-ttu-id="24c99-115">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="24c99-115">Click Repositories.</span></span>
    * <span data-ttu-id="24c99-116">Wählen Sie ein Repository für den Typ „Betriebliche Ressource” aus, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="24c99-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="24c99-117">Wenn es verfügbar ist, überspringen Sie die folgenden Schritte zur Erstellung eines neuen Repository.</span><span class="sxs-lookup"><span data-stu-id="24c99-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="24c99-118">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="24c99-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="24c99-119">Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="24c99-120">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="24c99-120">Click Create repository.</span></span>
8. <span data-ttu-id="24c99-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24c99-121">Click OK.</span></span>
9. <span data-ttu-id="24c99-122">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="24c99-122">Click Open.</span></span>
10. <span data-ttu-id="24c99-123">Wählen Sie in der Struktur die Option "Zahlungsmodell" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="24c99-124">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="24c99-124">Click Import.</span></span>
    * <span data-ttu-id="24c99-125">Importieren Sie dieses Datenmodell.</span><span class="sxs-lookup"><span data-stu-id="24c99-125">Import this data model.</span></span> <span data-ttu-id="24c99-126">Es wird als Datenquelle in einer neuen Formatkonfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c99-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="24c99-127">Überspringen Sie diesen Schritt, wenn diese Konfiguration bereits importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="24c99-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="24c99-128">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="24c99-128">Click Yes.</span></span>
13. <span data-ttu-id="24c99-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24c99-129">Close the page.</span></span>
14. <span data-ttu-id="24c99-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24c99-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="24c99-131">Dient zum Erstellen einer neuen Format-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="24c99-131">Create a new format configuration</span></span>
1. <span data-ttu-id="24c99-132">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="24c99-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="24c99-133">Wählen Sie in der Struktur die Option "Zahlungsmodell" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="24c99-134">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="24c99-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="24c99-135">Wählen Sie im neuen Feld geben Sie "Format auf Grundlage Datenmodell PaymentModel" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="24c99-136">Erstellen Sie ein Format, das auf dem PaymentModel-Datenmodell basiert.</span><span class="sxs-lookup"><span data-stu-id="24c99-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="24c99-137">Geben Sie im Feld "Name" die Bezeichnung "Beispiel-Arbeitsblattbericht" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="24c99-138">Beispiel-Arbeitsblattbericht</span><span class="sxs-lookup"><span data-stu-id="24c99-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="24c99-139">Geben Sie im Feld "Beschreibung" die Bezeichnung "Beispiel-Arbeitsblattbericht für Kreditorenzahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="24c99-140">Beispiel-Arbeitsblattbericht für Zahlungen der Händler.</span><span class="sxs-lookup"><span data-stu-id="24c99-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="24c99-141">Geben Sie im Feld "Datenmodelldefinition" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="24c99-142">Wählen Sie die Definition "CustomerCreditTransferInitiation" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="24c99-143">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="24c99-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="24c99-144">Entwerfen Sie ein neues Dokument im OPENXML-Arbeitsblattformat</span><span class="sxs-lookup"><span data-stu-id="24c99-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="24c99-145">Wählen Sie in der Struktur die Option "Zahlungsmodell \Beispiel-Arbeitsblattbericht" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="24c99-146">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="24c99-146">Click Designer.</span></span>
3. <span data-ttu-id="24c99-147">Klicken Sie im Aktivitätsbereich auf "Importieren".</span><span class="sxs-lookup"><span data-stu-id="24c99-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="24c99-148">Klicken Sie auf "Aus Excel importieren".</span><span class="sxs-lookup"><span data-stu-id="24c99-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="24c99-149">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="24c99-149">Click Attachments.</span></span>
    * <span data-ttu-id="24c99-150">Fügen Sie das vorhandene Excel-Dokument als Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="24c99-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="24c99-151">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="24c99-151">Click New.</span></span>
7. <span data-ttu-id="24c99-152">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="24c99-152">Click File.</span></span>
    * <span data-ttu-id="24c99-153">Zeigen Sie auf die vorhandene Excel-Datei.</span><span class="sxs-lookup"><span data-stu-id="24c99-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="24c99-154">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24c99-154">Close the page.</span></span>
9. <span data-ttu-id="24c99-155">Geben Sie im Feld "Vorlage" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="24c99-156">Wählen Sie die angefügte Excel-Datei aus, um als Vorlage verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="24c99-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="24c99-157">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24c99-157">Click OK.</span></span>
    * <span data-ttu-id="24c99-158">Beachten Sie, dass ER-Formatkomponenten im Entwurfsformat auf Grundlage der Struktur des verweisenden MS Excel-Dokuments (genannte Bereiche) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="24c99-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="24c99-159">Erstellen Sie eine neue Datenquelle, um Summen nach Währungscodes zu berechnen</span><span class="sxs-lookup"><span data-stu-id="24c99-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="24c99-160">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="24c99-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="24c99-161">Klicken Sie auf "Stamm hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="24c99-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="24c99-162">Wählen Sie in der Struktur "Funktionen\Gruppieren nach" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="24c99-163">Geben Sie im Feld "Name" die Zeichenfolge "PaymentByCurrency" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="24c99-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="24c99-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="24c99-165">Klicken Sie auf "Gruppe bearbeiten von".</span><span class="sxs-lookup"><span data-stu-id="24c99-165">Click Edit group by.</span></span>
6. <span data-ttu-id="24c99-166">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="24c99-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="24c99-167">Wählen Sie 'Modell\Zahlungen' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="24c99-168">Klicken Sie auf "Feld hinzufügen zu".</span><span class="sxs-lookup"><span data-stu-id="24c99-168">Click Add field to.</span></span>
9. <span data-ttu-id="24c99-169">Klicken Sie auf "Was gruppieren".</span><span class="sxs-lookup"><span data-stu-id="24c99-169">Click What to group.</span></span>
10. <span data-ttu-id="24c99-170">Erweitern Sie 'Modell\Zahlungen' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="24c99-171">Wählen Sie in der Struktur "Modell\Zahlungen\Währung" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="24c99-172">Klicken Sie auf "Feld hinzufügen zu".</span><span class="sxs-lookup"><span data-stu-id="24c99-172">Click Add field to.</span></span>
13. <span data-ttu-id="24c99-173">Klicken Sie auf "Gruppierte Felder".</span><span class="sxs-lookup"><span data-stu-id="24c99-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="24c99-174">In der Struktur wählen Sie "Modell\Zahlungen\Angewiesener Betrag (InstructedAmount)" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="24c99-175">Klicken Sie auf "Feld hinzufügen zu".</span><span class="sxs-lookup"><span data-stu-id="24c99-175">Click Add field to.</span></span>
16. <span data-ttu-id="24c99-176">Klicken Sie auf "Aggregationsfelder".</span><span class="sxs-lookup"><span data-stu-id="24c99-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="24c99-177">Wählen Sie im Feld "Methode" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="24c99-178">Wählen Sie die SUMMEN_Aggregationsfunktion aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="24c99-179">Geben Sie im Feld "Name" die Zeichenfolge "TotalInstructuredAmount" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="24c99-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="24c99-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="24c99-181">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="24c99-181">Click Save.</span></span>
20. <span data-ttu-id="24c99-182">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24c99-182">Close the page.</span></span>
21. <span data-ttu-id="24c99-183">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24c99-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="24c99-184">Weisen Sie Datenquellen Formatkomponenten zu</span><span class="sxs-lookup"><span data-stu-id="24c99-184">Map format components to data sources</span></span>
1. <span data-ttu-id="24c99-185">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="24c99-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="24c99-186">Erweitern Sie 'Modell\Zahlungen' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="24c99-187">Erweitern Sie in der Struktur "Modell\Zahlungen\Einleitende Partei(InitiatingParty)".</span><span class="sxs-lookup"><span data-stu-id="24c99-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="24c99-188">Wählen Sie in der Struktur "'Modell\Zahlungen\Einleitende Partei(InitiatingParty)\Name" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="24c99-189">Erweitern oder reduzieren Sie „Excel\ReportHeader” in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="24c99-190">Wählen Sie „Excel\ReportHeader\CompanyName” in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="24c99-191">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-191">Click Bind.</span></span>
8. <span data-ttu-id="24c99-192">Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="24c99-193">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Kennung".</span><span class="sxs-lookup"><span data-stu-id="24c99-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="24c99-194">In der Struktur wählen Sie "Modell\Zahlungen\Kreditor\Kennung\Quell-ID(SourceID)" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="24c99-195">Erweitern Sie „Excel\PaymLines” in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="24c99-196">Wählen Sie in der Struktur „Excel\PaymLines\VendAccountName” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="24c99-197">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-197">Click Bind.</span></span>
14. <span data-ttu-id="24c99-198">Wählen Sie 'Modell\Payments\Creditor\Account\Name' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="24c99-199">Wählen Sie in der Struktur „Excel\PaymLines\VendName” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="24c99-200">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-200">Click Bind.</span></span>
17. <span data-ttu-id="24c99-201">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)".</span><span class="sxs-lookup"><span data-stu-id="24c99-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="24c99-202">In der Struktur wählen Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)\Name" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="24c99-203">Wählen Sie in der Struktur „Excel\PaymLines\Bank” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="24c99-204">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-204">Click Bind.</span></span>
21. <span data-ttu-id="24c99-205">Wählen Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)\Bankleitzahl(RoutingNumber)" in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="24c99-206">Wählen Sie in der Struktur „Excel\PaymLines\RoutingNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="24c99-207">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-207">Click Bind.</span></span>
24. <span data-ttu-id="24c99-208">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="24c99-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="24c99-209">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)\Identification".</span><span class="sxs-lookup"><span data-stu-id="24c99-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="24c99-210">In der Struktur wählen Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)\Kennung\Nummer".</span><span class="sxs-lookup"><span data-stu-id="24c99-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="24c99-211">Wählen Sie in der Struktur „Excel\PaymLines\AccountNumber” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="24c99-212">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-212">Click Bind.</span></span>
29. <span data-ttu-id="24c99-213">In der Struktur wählen Sie "Modell\Zahlungen\Angewiesener Betrag (InstructedAmount)" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="24c99-214">Wählen Sie in der Struktur „Excel\PaymLines\Soll” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="24c99-215">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-215">Click Bind.</span></span>
32. <span data-ttu-id="24c99-216">Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="24c99-217">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditorenkonto(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="24c99-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="24c99-218">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditoragent(CreditorAgent)".</span><span class="sxs-lookup"><span data-stu-id="24c99-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="24c99-219">Wählen Sie in der Struktur "Modell\Zahlungen\Währung" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="24c99-220">Wählen Sie in der Struktur „Excel\PaymLines\Währung” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="24c99-221">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-221">Click Bind.</span></span>
38. <span data-ttu-id="24c99-222">Erweitern Sie "PaymentByCurrency" in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="24c99-223">Erweitern Sie "PaymentByCurrency\grouped" in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="24c99-224">Wählen Sie in der Struktur "PaymentByCurrency\grouped\Currency" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="24c99-225">Erweitern Sie „Excel\SummaryLines” in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="24c99-226">Wählen Sie in der Struktur „Excel\SummaryLines\SummaryCurrency” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="24c99-227">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-227">Click Bind.</span></span>
44. <span data-ttu-id="24c99-228">Erweitern Sie "PaymentByCurrency\aggregated" in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="24c99-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="24c99-229">Wählen Sie in der Struktur "PaymentByCurrency\aggregated\TotalInstructuredAmount" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="24c99-230">Wählen Sie in der Struktur „Excel\SummaryLines\SummaryAmount” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="24c99-231">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-231">Click Bind.</span></span>
48. <span data-ttu-id="24c99-232">Wählen Sie in der Struktur "PaymentByCurrency" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="24c99-233">Wählen Sie in der Struktur „Excel\SummaryLines” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="24c99-234">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-234">Click Bind.</span></span>
51. <span data-ttu-id="24c99-235">Wählen Sie 'Modell\Zahlungen' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="24c99-236">Wählen Sie in der Struktur „Excel\PaymLines” aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="24c99-237">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="24c99-237">Click Bind.</span></span>
54. <span data-ttu-id="24c99-238">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="24c99-238">Click Save.</span></span>
55. <span data-ttu-id="24c99-239">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24c99-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="24c99-240">Nutzen Sie die erstellte Konfiguration für die Zahlungsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="24c99-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="24c99-241">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="24c99-241">Click Change status.</span></span>
2. <span data-ttu-id="24c99-242">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="24c99-242">Click Complete.</span></span>
3. <span data-ttu-id="24c99-243">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24c99-243">Click OK.</span></span>
4. <span data-ttu-id="24c99-244">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24c99-244">Close the page.</span></span>
5. <span data-ttu-id="24c99-245">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24c99-245">Close the page.</span></span>
6. <span data-ttu-id="24c99-246">Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="24c99-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="24c99-247">Verwenden Sie den Schnellfilter, um im Feld „Zahlungsmethode” nach dem Wert „Elektronisch” zu filtern.</span><span class="sxs-lookup"><span data-stu-id="24c99-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="24c99-248">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="24c99-248">Electronic</span></span>  
8. <span data-ttu-id="24c99-249">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="24c99-249">Click Edit.</span></span>
9. <span data-ttu-id="24c99-250">Erweitern Sie den Abschnitt 'Dateiformate'.</span><span class="sxs-lookup"><span data-stu-id="24c99-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="24c99-251">Wählen Sie "Ja" im Feld "Generische elektronische Berichterstellung" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="24c99-252">Wählen Sie im Feld "Formatkonfiguration exportieren" einen Wert aus oder geben Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="24c99-253">Wählen Sie die Variante "Beispiel-Arbeitsblattbericht" aus.</span><span class="sxs-lookup"><span data-stu-id="24c99-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="24c99-254">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="24c99-254">Click Save.</span></span>
13. <span data-ttu-id="24c99-255">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24c99-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="24c99-256">Verwenden Sie die erstellte Konfiguration für das Testen der Zahlungserfassungsverarbeitung</span><span class="sxs-lookup"><span data-stu-id="24c99-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="24c99-257">Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="24c99-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="24c99-258">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="24c99-258">Click New.</span></span>
    * <span data-ttu-id="24c99-259">Erstellen Sie eine Zahlungserfassung.</span><span class="sxs-lookup"><span data-stu-id="24c99-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="24c99-260">Geben Sie im Namensfeld "VendPay" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="24c99-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="24c99-261">VendPay</span></span>  
4. <span data-ttu-id="24c99-262">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="24c99-262">Click Lines.</span></span>
5. <span data-ttu-id="24c99-263">Geben Sie im Feld "Konto" die Werte "GB_SI_000001" an.</span><span class="sxs-lookup"><span data-stu-id="24c99-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="24c99-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="24c99-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="24c99-265">Legen Sie "Soll" auf "1000" fest.</span><span class="sxs-lookup"><span data-stu-id="24c99-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="24c99-266">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="24c99-266">Click New.</span></span>
8. <span data-ttu-id="24c99-267">Geben Sie im Feld "Konto" die Werte "GB_SI_000005" an.</span><span class="sxs-lookup"><span data-stu-id="24c99-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="24c99-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="24c99-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="24c99-269">Legen Sie "Soll" auf "2000" fest.</span><span class="sxs-lookup"><span data-stu-id="24c99-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="24c99-270">Geben Sie im Feld "Währung" die Zeichenfolge "EUR" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="24c99-271">EUR</span><span class="sxs-lookup"><span data-stu-id="24c99-271">EUR</span></span>  
11. <span data-ttu-id="24c99-272">Geben Sie im Feld "Gegenkonto" die Werte "GBSI OPER" an.</span><span class="sxs-lookup"><span data-stu-id="24c99-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="24c99-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="24c99-273">GBSI OPER</span></span>  
12. <span data-ttu-id="24c99-274">Geben Sie im Feld "Zahlungsmethode" die Option "Elektronisch" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="24c99-275">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="24c99-275">Electronic</span></span>  
13. <span data-ttu-id="24c99-276">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="24c99-276">Click Save.</span></span>
14. <span data-ttu-id="24c99-277">Klicken Sie auf Zahlungen generieren.</span><span class="sxs-lookup"><span data-stu-id="24c99-277">Click Generate payments.</span></span>
15. <span data-ttu-id="24c99-278">Geben Sie im Feld "Zahlungsmethode" die Option "Elektronisch" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="24c99-279">Elektronisch</span><span class="sxs-lookup"><span data-stu-id="24c99-279">Electronic</span></span>  
16. <span data-ttu-id="24c99-280">Geben Sie im Feld „Dateiname” die Bezeichnung „Zahlungen” ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="24c99-281">Geben Sie beispielsweise "Zahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="24c99-282">Geben Sie im Feld "Bankkonto" die Zeichenfolge "GBSI OPER" ein.</span><span class="sxs-lookup"><span data-stu-id="24c99-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="24c99-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="24c99-283">GBSI OPER</span></span>  
18. <span data-ttu-id="24c99-284">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24c99-284">Click OK.</span></span>
19. <span data-ttu-id="24c99-285">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24c99-285">Click OK.</span></span>
    * <span data-ttu-id="24c99-286">Überprüfen Sie das erstellte Arbeitsblatt, einschließlich Details von Zahlungspositionen sowie der Summen für jeden Währungscode, der in dieser Zahlungsnachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="24c99-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

