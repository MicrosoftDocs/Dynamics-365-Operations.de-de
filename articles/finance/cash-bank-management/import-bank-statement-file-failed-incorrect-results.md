---
title: Bankauszugsdatei-Importproblembehandlung
description: Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 Finance unterstützt wird. Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt. Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse. In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht. In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5e7e6897f19dc0303ffbd3111f93669a91daa1b
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059375"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="76a3f-107">Bankauszugsdatei-Importproblembehandlung</span><span class="sxs-lookup"><span data-stu-id="76a3f-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76a3f-108">Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 Finance unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="76a3f-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="76a3f-109">Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt.</span><span class="sxs-lookup"><span data-stu-id="76a3f-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="76a3f-110">Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="76a3f-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="76a3f-111">In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht.</span><span class="sxs-lookup"><span data-stu-id="76a3f-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="76a3f-112">In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.</span><span class="sxs-lookup"><span data-stu-id="76a3f-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="76a3f-113">Wie lautet der Fehler?</span><span class="sxs-lookup"><span data-stu-id="76a3f-113">What is the error?</span></span>
------------------

<span data-ttu-id="76a3f-114">Nachdem Sie versuchen, eine Bankauszugsdatei zu importieren, wechseln Sie zur Einzelvorgangshistorie der Datenverwaltung und den darin enthaltenen Ausführungsdetails, um den Fehler zu suchen.</span><span class="sxs-lookup"><span data-stu-id="76a3f-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="76a3f-115">Der Fehler kann auf einen Kontoauszug, ein Saldo oder eine Auszugszeile verweisen.</span><span class="sxs-lookup"><span data-stu-id="76a3f-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="76a3f-116">Es ist allerdings unwahrscheinlich, genügend Informationen zu erhalten, um das Feld oder das Element zu identifizieren, das das Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="76a3f-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="76a3f-117">Wie lauten die Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="76a3f-117">What are the differences?</span></span>
<span data-ttu-id="76a3f-118">Vergleichen Sie die Bankdateilayoutdefinition mit der Finance-Importdefinition, und achten Sie auf eventuelle Unterschiede in den Feldern und den Elementen.</span><span class="sxs-lookup"><span data-stu-id="76a3f-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="76a3f-119">Vergleichen Sie die Bankauszugdatei mit der jeweiligen Finance-Datei.</span><span class="sxs-lookup"><span data-stu-id="76a3f-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="76a3f-120">In den Dateien ISO20022 sollten sämtliche Abweichungen einfach sein anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="76a3f-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="76a3f-121">Zeitzonendifferenzen in importierten Bankauszügen</span><span class="sxs-lookup"><span data-stu-id="76a3f-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="76a3f-122">Die Datums- und Zeitwerte in der Importdatei können von den in Finance and Operations angezeigten Datums- und Zeitwerten abweichen.</span><span class="sxs-lookup"><span data-stu-id="76a3f-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="76a3f-123">Um diese Abweichung zu verhindern, können Sie auf der Seite **Datenquellen konfigurieren** eine Zeitzoneneinstellung einstellen.</span><span class="sxs-lookup"><span data-stu-id="76a3f-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="76a3f-124">Weitere Informationen zur Eingabe einer Zeitzoneneinstellung finden Sie unter [Einrichten des erweiterten Bankabstimmungsimportprozesses](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="76a3f-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="76a3f-125">Umwandlungen</span><span class="sxs-lookup"><span data-stu-id="76a3f-125">Transformations</span></span>
<span data-ttu-id="76a3f-126">In der Regel muss die Änderung bei einer von drei Umwandlungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="76a3f-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="76a3f-127">Jede Umwandlung ist für einen bestimmten Standard geschrieben.</span><span class="sxs-lookup"><span data-stu-id="76a3f-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="76a3f-128">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="76a3f-128">Resource name</span></span>                                         | <span data-ttu-id="76a3f-129">Dateiname</span><span class="sxs-lookup"><span data-stu-id="76a3f-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="76a3f-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="76a3f-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="76a3f-131">BAI2CSV BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="76a3f-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="76a3f-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="76a3f-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="76a3f-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="76a3f-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="76a3f-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="76a3f-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="76a3f-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="76a3f-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="76a3f-136">Debuggingumwandlungen</span><span class="sxs-lookup"><span data-stu-id="76a3f-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="76a3f-137">Anpassen der Dateien BAI2 und MT940</span><span class="sxs-lookup"><span data-stu-id="76a3f-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="76a3f-138">Die Dateien BAI2 und MT940 sind text-basierte Dateien und benötigen eine Anpassung, um das Debuggen der Extensible Stylesheet Language Transformation (XSLT) zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="76a3f-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="76a3f-139">Das Programm nimmt diese Anpassung vor, wenn eine Datei importiert wird.</span><span class="sxs-lookup"><span data-stu-id="76a3f-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="76a3f-140">Erstellen Sie eine XML-Datei und kopieren Sie den folgenden Text hinein.</span><span class="sxs-lookup"><span data-stu-id="76a3f-140">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="76a3f-141">Kopieren Sie den Inhalt der Bankauszugsdatei und fügen Sie ihn in die XML-Datei ein, sodass er **PASTESTATEMENTFILEHERE** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="76a3f-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="76a3f-142">Debuggen Sie die XSLT</span><span class="sxs-lookup"><span data-stu-id="76a3f-142">Debug the XSLT</span></span>

<span data-ttu-id="76a3f-143">Weitere Informationen finden Sie unter <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="76a3f-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="76a3f-144">Starten Sie Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="76a3f-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="76a3f-145">Erstellen Sie eine Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="76a3f-145">Create a console application.</span></span>
3.  <span data-ttu-id="76a3f-146">Öffnen Sie die entsprechende XSLT.</span><span class="sxs-lookup"><span data-stu-id="76a3f-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="76a3f-147">Klicken Sie auf die XLST und dessen Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="76a3f-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="76a3f-148">Legen Sie die Eingabe auf den Speicherort der Bankauszugsdatei fest.</span><span class="sxs-lookup"><span data-stu-id="76a3f-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="76a3f-149">Definieren Sie einen Speicherort und Dateinamen für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="76a3f-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="76a3f-150">Legen Sie die erforderlichen Breakpoints fest.</span><span class="sxs-lookup"><span data-stu-id="76a3f-150">Set the required break points.</span></span>
8.  <span data-ttu-id="76a3f-151">Klicken Sie im Menü auf **XML** &gt; **Debuggen der XSLT starten.**</span><span class="sxs-lookup"><span data-stu-id="76a3f-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="76a3f-152">Formatieren der XSLT-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="76a3f-152">Format the XSLT output</span></span>

<span data-ttu-id="76a3f-153">Wenn die Umwandlung ausgeführt wird, erstellt sie eine Ausgabedatei, die in Visual Studio angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="76a3f-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="76a3f-154">Verwenden Sie STRG+A, STRG+K und STRG+D, um die Ausgabedatei schnell zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="76a3f-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="76a3f-155">Passen Sie die Umwandlung an</span><span class="sxs-lookup"><span data-stu-id="76a3f-155">Adjust the transformation</span></span>

<span data-ttu-id="76a3f-156">Passen Sie die Umwandlung an, um das entsprechende Feld oder Element in der Bankauszugsdatei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="76a3f-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="76a3f-157">Ordnen Sie dann diesem Feld oder Element das entsprechende Finance-Element zu.</span><span class="sxs-lookup"><span data-stu-id="76a3f-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="76a3f-158">Soll-/Habenindikator</span><span class="sxs-lookup"><span data-stu-id="76a3f-158">Debit/credit indicator</span></span>

<span data-ttu-id="76a3f-159">Manchmal können Soll- als Habenbeträge importiert werden, und Haben- als Sollbeträge.</span><span class="sxs-lookup"><span data-stu-id="76a3f-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="76a3f-160">Zur Behebung dieses Problems, müssen Sie zuerst die entsprechende XSLT ändern.</span><span class="sxs-lookup"><span data-stu-id="76a3f-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="76a3f-161">Wenn Bankauszüge von mehreren Banken stammen, müssen Sie sicherstellen, dass alle den selben Soll/Kreditansatz verwenden, oder Sie erstellen separate Umwandlungen.</span><span class="sxs-lookup"><span data-stu-id="76a3f-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="76a3f-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator Vorlage</span><span class="sxs-lookup"><span data-stu-id="76a3f-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="76a3f-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit Vorlage</span><span class="sxs-lookup"><span data-stu-id="76a3f-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="76a3f-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator Vorlage</span><span class="sxs-lookup"><span data-stu-id="76a3f-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="76a3f-165">Beispiele für Bankauszugsformate und technische Layouts</span><span class="sxs-lookup"><span data-stu-id="76a3f-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="76a3f-166">Die folgende Tabelle zeigt Beispiele der technischen Layoutdefinitionen für erweiterte Importdateien zur Bankabstimmung und drei entsprechenden Beispieldateien für Bankauszüge auf.</span><span class="sxs-lookup"><span data-stu-id="76a3f-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="76a3f-167">Sie können die Beispielsdateien und die technischen Layouts hier herunterladen: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="76a3f-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="76a3f-168">Technische Layoutdefinition</span><span class="sxs-lookup"><span data-stu-id="76a3f-168">Technical layout definition</span></span>                             | <span data-ttu-id="76a3f-169">Beispieldatei für Bankauszüge</span><span class="sxs-lookup"><span data-stu-id="76a3f-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="76a3f-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="76a3f-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="76a3f-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="76a3f-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="76a3f-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="76a3f-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="76a3f-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="76a3f-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="76a3f-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="76a3f-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="76a3f-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="76a3f-175">BAI2StatementExample</span></span>                 |





