---
title: Bankauszugsdatei-Importproblembehandlung
description: Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 Finance unterstützt wird. Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt. Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse. In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht. In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14f0e480b93e663f81db5a1edb2ae71b559bb05e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188558"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="f77d4-107">Bankauszugsdatei-Importproblembehandlung</span><span class="sxs-lookup"><span data-stu-id="f77d4-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f77d4-108">Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 Finance unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f77d4-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="f77d4-109">Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt.</span><span class="sxs-lookup"><span data-stu-id="f77d4-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="f77d4-110">Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="f77d4-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="f77d4-111">In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht.</span><span class="sxs-lookup"><span data-stu-id="f77d4-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="f77d4-112">In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.</span><span class="sxs-lookup"><span data-stu-id="f77d4-112">This article explains how to fix these differences and resolve the issues.</span></span>

## <a name="what-is-the-error"></a><span data-ttu-id="f77d4-113">Wie lautet der Fehler?</span><span class="sxs-lookup"><span data-stu-id="f77d4-113">What is the error?</span></span>

<span data-ttu-id="f77d4-114">Nachdem Sie versuchen, eine Bankauszugsdatei zu importieren, wechseln Sie zur Einzelvorgangshistorie der Datenverwaltung und den darin enthaltenen Ausführungsdetails, um den Fehler zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f77d4-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="f77d4-115">Der Fehler kann auf einen Kontoauszug, ein Saldo oder eine Auszugszeile verweisen.</span><span class="sxs-lookup"><span data-stu-id="f77d4-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="f77d4-116">Es ist allerdings unwahrscheinlich, genügend Informationen zu erhalten, um das Feld oder das Element zu identifizieren, das das Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="f77d4-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="f77d4-117">Importierte Bankauszüge können sich nur für einen bestimmten Zeitpunkt überschneiden.</span><span class="sxs-lookup"><span data-stu-id="f77d4-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="f77d4-118">Wenn ein Auszug beispielsweise am 1. Januar 2021 um 12:00 AM endet, kann das Anfangsdatum für den nächsten Auszug 12:00 AM am 1. Januar 2021 um 12:00:00 AM sein.</span><span class="sxs-lookup"><span data-stu-id="f77d4-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="f77d4-119">Wie lauten die Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="f77d4-119">What are the differences?</span></span>
<span data-ttu-id="f77d4-120">Vergleichen Sie die Bankdateilayoutdefinition mit der Finance-Importdefinition, und achten Sie auf eventuelle Unterschiede in den Feldern und den Elementen.</span><span class="sxs-lookup"><span data-stu-id="f77d4-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="f77d4-121">Vergleichen Sie die Bankauszugdatei mit der jeweiligen Finance-Datei.</span><span class="sxs-lookup"><span data-stu-id="f77d4-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="f77d4-122">In den Dateien ISO20022 sollten sämtliche Abweichungen einfach sein anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f77d4-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="f77d4-123">Zeitzonendifferenzen in importierten Bankauszügen</span><span class="sxs-lookup"><span data-stu-id="f77d4-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="f77d4-124">Die Datums- und Zeitwerte in der Importdatei können von den in Finance and Operations angezeigten Datums- und Zeitwerten abweichen.</span><span class="sxs-lookup"><span data-stu-id="f77d4-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="f77d4-125">Um diese Abweichung zu verhindern, können Sie auf der Seite **Datenquellen konfigurieren** eine Zeitzoneneinstellung einstellen.</span><span class="sxs-lookup"><span data-stu-id="f77d4-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="f77d4-126">Weitere Informationen zur Eingabe einer Zeitzoneneinstellung finden Sie unter [Einrichten des erweiterten Bankabstimmungsimportprozesses](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="f77d4-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="f77d4-127">Umwandlungen</span><span class="sxs-lookup"><span data-stu-id="f77d4-127">Transformations</span></span>
<span data-ttu-id="f77d4-128">In der Regel muss die Änderung bei einer von drei Umwandlungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f77d4-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="f77d4-129">Jede Umwandlung ist für einen bestimmten Standard geschrieben.</span><span class="sxs-lookup"><span data-stu-id="f77d4-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="f77d4-130">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="f77d4-130">Resource name</span></span>                                         | <span data-ttu-id="f77d4-131">Dateiname</span><span class="sxs-lookup"><span data-stu-id="f77d4-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="f77d4-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="f77d4-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="f77d4-133">BAI2CSV BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="f77d4-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="f77d4-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="f77d4-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="f77d4-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="f77d4-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="f77d4-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="f77d4-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="f77d4-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="f77d4-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="f77d4-138">Debuggingumwandlungen</span><span class="sxs-lookup"><span data-stu-id="f77d4-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="f77d4-139">Anpassen der Dateien BAI2 und MT940</span><span class="sxs-lookup"><span data-stu-id="f77d4-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="f77d4-140">Die Dateien BAI2 und MT940 sind text-basierte Dateien und benötigen eine Anpassung, um das Debuggen der Extensible Stylesheet Language Transformation (XSLT) zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f77d4-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="f77d4-141">Das Programm nimmt diese Anpassung vor, wenn eine Datei importiert wird.</span><span class="sxs-lookup"><span data-stu-id="f77d4-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="f77d4-142">Erstellen Sie eine XML-Datei und kopieren Sie den folgenden Text hinein.</span><span class="sxs-lookup"><span data-stu-id="f77d4-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="f77d4-143">Kopieren Sie den Inhalt der Bankauszugsdatei und fügen Sie ihn in die XML-Datei ein, sodass er **PASTESTATEMENTFILEHERE** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="f77d4-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="f77d4-144">Debuggen Sie die XSLT</span><span class="sxs-lookup"><span data-stu-id="f77d4-144">Debug the XSLT</span></span>

<span data-ttu-id="f77d4-145">Weitere Informationen finden Sie unter <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="f77d4-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="f77d4-146">Starten Sie Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f77d4-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="f77d4-147">Erstellen Sie eine Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="f77d4-147">Create a console application.</span></span>
3.  <span data-ttu-id="f77d4-148">Öffnen Sie die entsprechende XSLT.</span><span class="sxs-lookup"><span data-stu-id="f77d4-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="f77d4-149">Klicken Sie auf die XLST und dessen Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="f77d4-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="f77d4-150">Legen Sie die Eingabe auf den Speicherort der Bankauszugsdatei fest.</span><span class="sxs-lookup"><span data-stu-id="f77d4-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="f77d4-151">Definieren Sie einen Speicherort und Dateinamen für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f77d4-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="f77d4-152">Legen Sie die erforderlichen Breakpoints fest.</span><span class="sxs-lookup"><span data-stu-id="f77d4-152">Set the required break points.</span></span>
8.  <span data-ttu-id="f77d4-153">Klicken Sie im Menü auf **XML** &gt; **Debuggen der XSLT starten.**</span><span class="sxs-lookup"><span data-stu-id="f77d4-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="f77d4-154">Formatieren der XSLT-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="f77d4-154">Format the XSLT output</span></span>

<span data-ttu-id="f77d4-155">Wenn die Umwandlung ausgeführt wird, erstellt sie eine Ausgabedatei, die in Visual Studio angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f77d4-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="f77d4-156">Verwenden Sie STRG+A, STRG+K und STRG+D, um die Ausgabedatei schnell zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="f77d4-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="f77d4-157">Passen Sie die Umwandlung an</span><span class="sxs-lookup"><span data-stu-id="f77d4-157">Adjust the transformation</span></span>

<span data-ttu-id="f77d4-158">Passen Sie die Umwandlung an, um das entsprechende Feld oder Element in der Bankauszugsdatei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f77d4-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="f77d4-159">Ordnen Sie dann diesem Feld oder Element das entsprechende Finance-Element zu.</span><span class="sxs-lookup"><span data-stu-id="f77d4-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="f77d4-160">Soll-/Habenindikator</span><span class="sxs-lookup"><span data-stu-id="f77d4-160">Debit/credit indicator</span></span>

<span data-ttu-id="f77d4-161">Manchmal können Soll- als Habenbeträge importiert werden, und Haben- als Sollbeträge.</span><span class="sxs-lookup"><span data-stu-id="f77d4-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="f77d4-162">Zur Behebung dieses Problems, müssen Sie zuerst die entsprechende XSLT ändern.</span><span class="sxs-lookup"><span data-stu-id="f77d4-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="f77d4-163">Wenn Bankauszüge von mehreren Banken stammen, müssen Sie sicherstellen, dass alle den selben Soll/Kreditansatz verwenden, oder Sie erstellen separate Umwandlungen.</span><span class="sxs-lookup"><span data-stu-id="f77d4-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="f77d4-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator Vorlage</span><span class="sxs-lookup"><span data-stu-id="f77d4-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="f77d4-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit Vorlage</span><span class="sxs-lookup"><span data-stu-id="f77d4-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="f77d4-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator Vorlage</span><span class="sxs-lookup"><span data-stu-id="f77d4-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="f77d4-167">Beispiele für Bankauszugsformate und technische Layouts</span><span class="sxs-lookup"><span data-stu-id="f77d4-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="f77d4-168">Die folgende Tabelle zeigt Beispiele der technischen Layoutdefinitionen für erweiterte Importdateien zur Bankabstimmung und drei entsprechenden Beispieldateien für Bankauszüge auf.</span><span class="sxs-lookup"><span data-stu-id="f77d4-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="f77d4-169">Sie können die Beispielsdateien und die technischen Layouts hier herunterladen: [Importdateibeispiele](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="f77d4-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="f77d4-170">Technische Layoutdefinition</span><span class="sxs-lookup"><span data-stu-id="f77d4-170">Technical layout definition</span></span>                             | <span data-ttu-id="f77d4-171">Beispieldatei für Bankauszüge</span><span class="sxs-lookup"><span data-stu-id="f77d4-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="f77d4-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="f77d4-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="f77d4-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="f77d4-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="f77d4-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="f77d4-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="f77d4-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="f77d4-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="f77d4-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="f77d4-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="f77d4-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="f77d4-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
