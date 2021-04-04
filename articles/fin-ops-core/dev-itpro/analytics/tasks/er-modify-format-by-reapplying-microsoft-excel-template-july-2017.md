---
title: Formate durch erneute Anwendung von Excel-Vorlagen ändern
description: Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden „Eine ER-Konfiguration zum Generieren von Berichten im OPENXML-Format erstellen” abschließen.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ca6707095765c25851ee864a99844a82844fae1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564313"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="f3850-103">Formate durch erneute Anwendung von Excel-Vorlagen ändern</span><span class="sxs-lookup"><span data-stu-id="f3850-103">Modify formats by reapplying Excel templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3850-104">Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden „Eine ER-Konfiguration zum Generieren von Berichten im OPENXML-Format erstellen” abschließen.</span><span class="sxs-lookup"><span data-stu-id="f3850-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="f3850-105">Dieses Verfahren zeigt, wie eine Konfiguration für das Format der elektronischen Berichterstellung (EB) geändert wird, indem eine Microsoft Excel-Vorlage erneut angewendet wird, die geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f3850-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="f3850-106">In diesem Verfahren importieren Sie eine geänderte Excel-Vorlage in eine ER-Formatkonfigurationen, die für das Beispielunternehmen, Litware, Inc. erstellt wurde, und erstellen dann die elektronischen Dokumente.</span><span class="sxs-lookup"><span data-stu-id="f3850-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="f3850-107">Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="f3850-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="f3850-108">Die Schritte können abgeschlossen werden, indem Sie den GBSI-Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3850-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="f3850-109">Bevor Sie beginnen, laden und speichern Sie die Datei, SampleVendPaymWsReport2.xlsx, die im Hilfethema aufgeführt ist, ändern elektronisches Berichterstellungsformat, indem Sie eine Tabelle erneut öffnen (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="f3850-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="f3850-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="f3850-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f3850-111">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist.</span><span class="sxs-lookup"><span data-stu-id="f3850-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="f3850-112">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zuerst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="f3850-112">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="f3850-113">Wählen Sie ER-Format aus.</span><span class="sxs-lookup"><span data-stu-id="f3850-113">Select the ER format</span></span>
1. <span data-ttu-id="f3850-114">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="f3850-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="f3850-115">Erweitern oder reduzieren Sie 'Zahlungsmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f3850-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="f3850-116">Wählen Sie in der Struktur die Option "Zahlungsmodell \Beispiel-Arbeitsblattbericht" aus.</span><span class="sxs-lookup"><span data-stu-id="f3850-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="f3850-117">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="f3850-117">Click Attachments.</span></span>
    * <span data-ttu-id="f3850-118">Beachten Sie, dass die SampleVendPaymWsReport.xlsx-Excel-Datei derzeit als Vorlage für die Zahlungserfassungsverarbeitung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3850-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="f3850-119">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="f3850-119">Click Open.</span></span>
    * <span data-ttu-id="f3850-120">Klicken Sie auf Öffnen, um das Layout der Tabelle zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="f3850-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="f3850-121">Überprüfen der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="f3850-121">Review the template.</span></span> <span data-ttu-id="f3850-122">Beachten Sie, dass derzeit die folgenden Details für jede Zahlungsposition eingeschlossen sind: Kreditorenkontonummer, Kreditor, Bank, Bankleitzahl, Kontonummer, Soll, Haben und Währung.</span><span class="sxs-lookup"><span data-stu-id="f3850-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="f3850-123">In vorliegenden Beispiel möchten wir dieser Liste erweitern, indem wir Details zum Zahlungsdatum hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f3850-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="f3850-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f3850-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="f3850-125">Wenden Sie eine neue Excelvorlage im ER-Format erneut an</span><span class="sxs-lookup"><span data-stu-id="f3850-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="f3850-126">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="f3850-126">Click Designer.</span></span>
    * <span data-ttu-id="f3850-127">Öffnet die Entwurfsversion des ausgewählten ER-Formats zur Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="f3850-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="f3850-128">Klicken Sie im Aktivitätsbereich auf "Importieren".</span><span class="sxs-lookup"><span data-stu-id="f3850-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="f3850-129">Auf "Aus Excel aktualisieren" klicken.</span><span class="sxs-lookup"><span data-stu-id="f3850-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="f3850-130">Klicken Sie auf „Vorlage aktualisieren“ und wählen Sie die Datei, SampleVendPaymWsReport2.xlsx aus.</span><span class="sxs-lookup"><span data-stu-id="f3850-130">Click 'Update template', and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="f3850-131">Klicken Sie auf Vorlage aktualisieren und suchen Sie die zuvor heruntergeladene Datei SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="f3850-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="f3850-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f3850-132">Click OK.</span></span>
    * <span data-ttu-id="f3850-133">Die SampleVendPaymWsReport2.xlsx-Vorlage wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="f3850-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="f3850-134">Die Struktur des ER-Formats wird mit dem Inhalt der Vorlage synchronisiert, deren Elemente in ER-Format hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f3850-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="f3850-135">Alle vorhandenen Elemente im ER-Format, die nicht in der Vorlage enthalten sind, werden von der Formatdefinition entfernt.</span><span class="sxs-lookup"><span data-stu-id="f3850-135">Any existing elements in the ER format that aren't included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="f3850-136">Wählen Sie in der Struktur "Excel" aus.</span><span class="sxs-lookup"><span data-stu-id="f3850-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="f3850-137">Beachten Sie, dass das Vorlagenfeld nun eine Referenz in der neuen Vorlage beinhaltet.</span><span class="sxs-lookup"><span data-stu-id="f3850-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="f3850-138">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="f3850-138">Click Attachments.</span></span>
7. <span data-ttu-id="f3850-139">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="f3850-139">Click Open.</span></span>
    * <span data-ttu-id="f3850-140">Klicken Sie auf Öffnen, um das Layout der Excel-Vorlage zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f3850-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="f3850-141">Überprüfen der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="f3850-141">Review the template.</span></span> <span data-ttu-id="f3850-142">Beachten Sie, dass es jetzt eine Position für das Zahlungsdatum enthält.</span><span class="sxs-lookup"><span data-stu-id="f3850-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="f3850-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f3850-143">Close the page.</span></span>
9. <span data-ttu-id="f3850-144">In der Struktur erweitern Sie "Excel".</span><span class="sxs-lookup"><span data-stu-id="f3850-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="f3850-145">Erweitern Sie „Excel\PaymLines” in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f3850-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="f3850-146">Wählen Sie in der Struktur Excel\Zahlungszeilen\Zahlungsdatum</span><span class="sxs-lookup"><span data-stu-id="f3850-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="f3850-147">Beachten Sie, dass das ER-Format nun einen anderen Artikel enthält.</span><span class="sxs-lookup"><span data-stu-id="f3850-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="f3850-148">Eine Zelle, PaymDate, wurde der Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f3850-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="f3850-149">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="f3850-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="f3850-150">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="f3850-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="f3850-151">Erweitern Sie 'Modell\Zahlungen' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="f3850-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="f3850-152">Wählen Sie in der Strukturdarstellung "Modell\Payments\Transaction date(TransactionDate)" aus.</span><span class="sxs-lookup"><span data-stu-id="f3850-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="f3850-153">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="f3850-153">Click Bind.</span></span>
    * <span data-ttu-id="f3850-154">Geben Sie an, welche Daten zur neuen Zelle zur Laufzeit hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f3850-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="f3850-155">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f3850-155">Click Save.</span></span>
18. <span data-ttu-id="f3850-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f3850-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="f3850-157">Aktivieren Sie die geänderte Entwurfsversion des ER-Formats für die Verwendung bei Zahlungserfassungsverarbeitunge</span><span class="sxs-lookup"><span data-stu-id="f3850-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="f3850-158">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f3850-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="f3850-159">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="f3850-159">Click User parameters.</span></span>
3. <span data-ttu-id="f3850-160">Wählen Sie "Ja" im Feld "Testlaufeinstellungen".</span><span class="sxs-lookup"><span data-stu-id="f3850-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="f3850-161">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f3850-161">Click OK.</span></span>
5. <span data-ttu-id="f3850-162">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="f3850-162">Click Edit.</span></span>
6. <span data-ttu-id="f3850-163">Wählen Sie "Ja" im Feld "Testentwurf".</span><span class="sxs-lookup"><span data-stu-id="f3850-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="f3850-164">Nutzen Sie die geänderte Entwurfsversion des ER-Formats für die Verwendung bei Zahlungserfassungsverarbeitungen</span><span class="sxs-lookup"><span data-stu-id="f3850-164">Use the modified draft version of the ER format for payment journal processing</span></span>

<span data-ttu-id="f3850-165">Wiederholen Sie das erstellte Arbeitsblatt, einschließlich neue Details der Zahlungszeilen - Zahlungsdatum.</span><span class="sxs-lookup"><span data-stu-id="f3850-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]