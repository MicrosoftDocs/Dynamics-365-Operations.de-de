---
title: 'ER Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 4: Format ausführen)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat für die Verwendung von Dokumentenverwaltungsdateien in der EB-Ausgabe konfigurieren. (Teil 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ede71118f64eec27b150a4c575aead97d3174509
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559724"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="e804d-104">ER Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 4: Format ausführen)</span><span class="sxs-lookup"><span data-stu-id="e804d-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e804d-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="e804d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="e804d-106">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e804d-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="e804d-107">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Aufgabenleitfaden „ER Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 3: Format erstellen)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="e804d-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="e804d-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e804d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="e804d-109">Erforderliche Anhänge für den Auftrag einer einzelnen Rechnung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e804d-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="e804d-110">Wechseln Sie zu "Debitoren" > "Rechnungen" > "Offene Debitorenrechnungen".</span><span class="sxs-lookup"><span data-stu-id="e804d-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="e804d-111">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e804d-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e804d-112">Filtern Sie beispielsweise im Feld "Rechnung" mit dem Wert "CIV-000148".</span><span class="sxs-lookup"><span data-stu-id="e804d-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="e804d-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="e804d-113">CIV-000148</span></span>  
3. <span data-ttu-id="e804d-114">Klicken Sie darauf, um dem ausgewählten Link von der Rechnung zu folgen.</span><span class="sxs-lookup"><span data-stu-id="e804d-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="e804d-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="e804d-115">CIV-000148</span></span>  
4. <span data-ttu-id="e804d-116">Klicken Sie, um dem Link im Feld "Auftrag" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="e804d-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="e804d-117">000148</span><span class="sxs-lookup"><span data-stu-id="e804d-117">000148</span></span>  
5. <span data-ttu-id="e804d-118">Wählen Sie im Feld "Positionen oder Kopfzeile" "Kopfzeile" aus.</span><span class="sxs-lookup"><span data-stu-id="e804d-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="e804d-119">Wählen Sie den Kopf aus, um anzugeben, dass dies das Ziel für das Hinzufügen von Anlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e804d-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="e804d-120">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="e804d-120">Click Attach.</span></span>
    * <span data-ttu-id="e804d-121">Fügen Sie einige Dateien als Anhänge für diesen Auftrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="e804d-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="e804d-122">Verwenden Sie die Dateien der Dokumenttypen, die von der Dokumentverwaltung unterstützt werden (mit DOCX-, DPF- XML-, JPG-Dateierweiterungen, usw.).</span><span class="sxs-lookup"><span data-stu-id="e804d-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="e804d-123">Wählen Sie Dateien aus, die angehängt und mit der entsprechenden Rechnung in der elektronischen ER-Nachricht weiterverarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e804d-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="e804d-124">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e804d-124">Click New.</span></span>
8. <span data-ttu-id="e804d-125">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="e804d-125">Click File.</span></span>
9. <span data-ttu-id="e804d-126">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e804d-126">Click New.</span></span>
10. <span data-ttu-id="e804d-127">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="e804d-127">Click File.</span></span>
11. <span data-ttu-id="e804d-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e804d-128">Close the page.</span></span>
12. <span data-ttu-id="e804d-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e804d-129">Close the page.</span></span>
13. <span data-ttu-id="e804d-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e804d-130">Close the page.</span></span>
14. <span data-ttu-id="e804d-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e804d-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="e804d-132">Ausführen des Berichts für die ausgewählte Rechnung</span><span class="sxs-lookup"><span data-stu-id="e804d-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="e804d-133">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e804d-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e804d-134">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".</span><span class="sxs-lookup"><span data-stu-id="e804d-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="e804d-135">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.</span><span class="sxs-lookup"><span data-stu-id="e804d-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="e804d-136">Wählen Sie in der Strukturdarstellung 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="e804d-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="e804d-137">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="e804d-137">Click Run.</span></span>
6. <span data-ttu-id="e804d-138">Erweitern Sie den Abschnitt "Records to include ()".</span><span class="sxs-lookup"><span data-stu-id="e804d-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="e804d-139">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="e804d-139">Click Filter.</span></span>
8. <span data-ttu-id="e804d-140">Wählen Sie die Zeile des Feldes "Debitorenrechnungserfassung" und "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="e804d-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="e804d-141">Geben Sie im Feld "Kriterien" den Wert "000148" ein.</span><span class="sxs-lookup"><span data-stu-id="e804d-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="e804d-142">Geben Sie im Feld Auftrag die Auftragsnummer 000148 ein.</span><span class="sxs-lookup"><span data-stu-id="e804d-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="e804d-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e804d-143">Click OK.</span></span>
11. <span data-ttu-id="e804d-144">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e804d-144">Click OK.</span></span>
    * <span data-ttu-id="e804d-145">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="e804d-145">Review the generated output.</span></span> <span data-ttu-id="e804d-146">Beachten Sie, das für jede Anlage ein einzelner XML-Knoten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e804d-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="e804d-147">Der Inhalt des Anhangs wird dann mit der XML-Ausgabe im MIME-Textformat (Base64) ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="e804d-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]