---
title: Bankauszugsdatei-Importproblembehandlung
description: Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 for Finance and Operations unterstützt wird. Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt. Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse. In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht. In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.
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
ms.openlocfilehash: 4275a4d77b03c55decbf161df8f2115183cac3d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842400"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="02090-107">Bankauszugsdatei-Importproblembehandlung</span><span class="sxs-lookup"><span data-stu-id="02090-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02090-108">Es ist wichtig, dass die Bankauszugdatei der Bank dem Layout entspricht, das von Microsoft Dynamics 365 for Finance and Operations unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="02090-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="02090-109">Aufgrund der strengen Standards für Bankauszüge, funktionieren die meisten Integrationen korrekt.</span><span class="sxs-lookup"><span data-stu-id="02090-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="02090-110">Allerdings kann manchmal die Auszugsdatei nicht importiert werden oder enthält falsche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="02090-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="02090-111">In der Regel werden diese Probleme durch geringfügige Unterschiede in der Bankauszugdatei verursacht.</span><span class="sxs-lookup"><span data-stu-id="02090-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="02090-112">In diesem Artikel wird beschrieben, wie Sie diese Unterschiede korrigieren und Probleme lösen können.</span><span class="sxs-lookup"><span data-stu-id="02090-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="02090-113">Wie lautet der Fehler?</span><span class="sxs-lookup"><span data-stu-id="02090-113">What is the error?</span></span>
------------------

<span data-ttu-id="02090-114">Nachdem Sie versuchen, eine Bankauszugsdatei zu importieren, wechseln Sie zur Einzelvorgangshistorie der Datenverwaltung und den darin enthaltenen Ausführungsdetails, um den Fehler zu suchen.</span><span class="sxs-lookup"><span data-stu-id="02090-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="02090-115">Der Fehler kann auf einen Kontoauszug, ein Saldo oder eine Auszugszeile verweisen.</span><span class="sxs-lookup"><span data-stu-id="02090-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="02090-116">Es ist allerdings unwahrscheinlich, genügend Informationen zu erhalten, um das Feld oder das Element zu identifizieren, das das Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="02090-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="02090-117">Wie lauten die Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="02090-117">What are the differences?</span></span>
<span data-ttu-id="02090-118">Vergleichen Sie die Bankdateilayoutdefinition mit der Finance and Operations-Importdefinition, und achten Sie auf eventuelle Unterschiede in den Feldern und den Elementen.</span><span class="sxs-lookup"><span data-stu-id="02090-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="02090-119">Vergleichen Sie die Bankauszugdatei mit der jeweiligen Finance and Operations-Datei.</span><span class="sxs-lookup"><span data-stu-id="02090-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="02090-120">In den Dateien ISO20022 sollten sämtliche Abweichungen einfach sein anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="02090-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="02090-121">Umwandlungen</span><span class="sxs-lookup"><span data-stu-id="02090-121">Transformations</span></span>
<span data-ttu-id="02090-122">In der Regel muss die Änderung bei einer von drei Umwandlungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="02090-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="02090-123">Jede Umwandlung ist für einen bestimmten Standard geschrieben.</span><span class="sxs-lookup"><span data-stu-id="02090-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="02090-124">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="02090-124">Resource name</span></span>                                         | <span data-ttu-id="02090-125">Dateiname</span><span class="sxs-lookup"><span data-stu-id="02090-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="02090-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="02090-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="02090-127">BAI2CSV BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="02090-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="02090-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="02090-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="02090-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="02090-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="02090-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="02090-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="02090-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="02090-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="02090-132">Debuggingumwandlungen</span><span class="sxs-lookup"><span data-stu-id="02090-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="02090-133">Anpassen der Dateien BAI2 und MT940</span><span class="sxs-lookup"><span data-stu-id="02090-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="02090-134">Die Dateien BAI2 und MT940 sind text-basierte Dateien und benötigen eine Anpassung, um das Debuggen der Extensible Stylesheet Language Transformation (XSLT) zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="02090-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="02090-135">Das Programm nimmt diese Anpassung vor, wenn eine Datei importiert wird.</span><span class="sxs-lookup"><span data-stu-id="02090-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="02090-136">Erstellen Sie eine XML-Datei und kopieren Sie den folgenden Text hinein.</span><span class="sxs-lookup"><span data-stu-id="02090-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="02090-137">Kopieren Sie den Inhalt der Bankauszugsdatei und fügen Sie ihn in die XML-Datei ein, sodass er **PASTESTATEMENTFILEHERE** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="02090-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="02090-138">Debuggen Sie die XSLT</span><span class="sxs-lookup"><span data-stu-id="02090-138">Debug the XSLT</span></span>

<span data-ttu-id="02090-139">Weitere Informationen finden Sie unter <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="02090-139">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="02090-140">Starten Sie Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="02090-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="02090-141">Erstellen Sie eine Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="02090-141">Create a console application.</span></span>
3.  <span data-ttu-id="02090-142">Öffnen Sie die entsprechende XSLT.</span><span class="sxs-lookup"><span data-stu-id="02090-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="02090-143">Klicken Sie auf die XLST und dessen Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="02090-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="02090-144">Legen Sie die Eingabe auf den Speicherort der Bankauszugsdatei fest.</span><span class="sxs-lookup"><span data-stu-id="02090-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="02090-145">Definieren Sie einen Speicherort und Dateinamen für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="02090-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="02090-146">Legen Sie die erforderlichen Breakpoints fest.</span><span class="sxs-lookup"><span data-stu-id="02090-146">Set the required break points.</span></span>
8.  <span data-ttu-id="02090-147">Klicken Sie im Menü auf **XML** &gt; **Debuggen der XSLT starten.**</span><span class="sxs-lookup"><span data-stu-id="02090-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="02090-148">Formatieren der XSLT-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="02090-148">Format the XSLT output</span></span>

<span data-ttu-id="02090-149">Wenn die Umwandlung ausgeführt wird, erstellt sie eine Ausgabedatei, die in Visual Studio angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="02090-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="02090-150">Verwenden Sie STRG+A, STRG+K und STRG+D, um die Ausgabedatei schnell zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="02090-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="02090-151">Passen Sie die Umwandlung an</span><span class="sxs-lookup"><span data-stu-id="02090-151">Adjust the transformation</span></span>

<span data-ttu-id="02090-152">Passen Sie die Umwandlung an, um das entsprechende Feld oder Element in der Bankauszugsdatei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="02090-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="02090-153">Ordnen Sie dann diesem Feld oder Element das entsprechende Finance and Operations-Element zu.</span><span class="sxs-lookup"><span data-stu-id="02090-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="02090-154">Soll-/Habenindikator</span><span class="sxs-lookup"><span data-stu-id="02090-154">Debit/credit indicator</span></span>

<span data-ttu-id="02090-155">Manchmal können Soll- als Habenbeträge importiert werden, und Haben- als Sollbeträge.</span><span class="sxs-lookup"><span data-stu-id="02090-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="02090-156">Zur Behebung dieses Problems, müssen Sie zuerst die entsprechende XSLT ändern.</span><span class="sxs-lookup"><span data-stu-id="02090-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="02090-157">Wenn Bankauszüge von mehreren Banken stammen, müssen Sie sicherstellen, dass alle den selben Soll/Kreditansatz verwenden, oder Sie erstellen separate Umwandlungen.</span><span class="sxs-lookup"><span data-stu-id="02090-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="02090-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator Vorlage</span><span class="sxs-lookup"><span data-stu-id="02090-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="02090-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit Vorlage</span><span class="sxs-lookup"><span data-stu-id="02090-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="02090-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator Vorlage</span><span class="sxs-lookup"><span data-stu-id="02090-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="02090-161">Beispiele für Bankauszugsformate und technische Layouts</span><span class="sxs-lookup"><span data-stu-id="02090-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="02090-162">Die folgende Tabelle zeigt Beispiele der technischen Layoutdefinitionen für erweiterte Importdateien zur Bankabstimmung und drei entsprechenden Beispieldateien für Bankauszüge auf.</span><span class="sxs-lookup"><span data-stu-id="02090-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="02090-163">Sie können die Beispielsdateien und die technischen Layouts hier herunterladen: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="02090-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="02090-164">Technische Layoutdefinition</span><span class="sxs-lookup"><span data-stu-id="02090-164">Technical layout definition</span></span>                             | <span data-ttu-id="02090-165">Beispieldatei für Bankauszüge</span><span class="sxs-lookup"><span data-stu-id="02090-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="02090-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="02090-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="02090-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="02090-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="02090-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="02090-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="02090-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="02090-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="02090-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="02090-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="02090-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="02090-171">BAI2StatementExample</span></span>                 |





