--- 
title: "Format zum Verwenden von Dokumentverwaltungsdateien in Formatausgaben ausführen"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 554de60fb8d2b6cb03cac5dc8d01df98390ad844
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="run-format-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="6bd3e-103">Format zum Verwenden von Dokumentverwaltungsdateien in Formatausgaben ausführen</span><span class="sxs-lookup"><span data-stu-id="6bd3e-103">Run format to use Document Management files in format outputs</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6bd3e-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="6bd3e-105">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="6bd3e-106">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 3: Format erstellen)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="6bd3e-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="6bd3e-108">Erforderliche Anhänge für den Auftrag einer einzelnen Rechnung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="6bd3e-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="6bd3e-109">Wechseln Sie zu "Debitoren" > "Rechnungen" > "Offene Debitorenrechnungen".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="6bd3e-110">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6bd3e-111">Filtern Sie beispielsweise im Feld "Rechnung" mit dem Wert "CIV-000148".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="6bd3e-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="6bd3e-112">CIV-000148</span></span>  
3. <span data-ttu-id="6bd3e-113">Klicken Sie darauf, um dem ausgewählten Link der Rechnung zu folgen.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="6bd3e-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="6bd3e-114">CIV-000148</span></span>  
4. <span data-ttu-id="6bd3e-115">Klicken Sie, um dem Link im Feld "Auftrag" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="6bd3e-116">000148</span><span class="sxs-lookup"><span data-stu-id="6bd3e-116">000148</span></span>  
5. <span data-ttu-id="6bd3e-117">Wählen Sie im Feld "Positionen oder Kopfzeile" "Kopfzeile" aus.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="6bd3e-118">Wählen Sie den Kopf aus, um anzugeben, dass dies das Ziel für das Hinzufügen von Anlagen ist.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="6bd3e-119">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-119">Click Attach.</span></span>
    * <span data-ttu-id="6bd3e-120">Fügen Sie einige Dateien als Anhänge für diesen Auftrag hinzu.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="6bd3e-121">Verwenden Sie die Dateien der Dokumenttypen, die von der Dokumentverwaltung unterstützt werden (mit DOCX-, DPF- XML-, JPG-Dateierweiterungen, usw.).</span><span class="sxs-lookup"><span data-stu-id="6bd3e-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="6bd3e-122">Wählen Sie Dateien aus, die angehängt und mit der entsprechenden Rechnung in der elektronischen ER-Nachricht weiterverarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="6bd3e-123">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-123">Click New.</span></span>
8. <span data-ttu-id="6bd3e-124">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-124">Click File.</span></span>
9. <span data-ttu-id="6bd3e-125">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-125">Click New.</span></span>
10. <span data-ttu-id="6bd3e-126">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-126">Click File.</span></span>
11. <span data-ttu-id="6bd3e-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-127">Close the page.</span></span>
12. <span data-ttu-id="6bd3e-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-128">Close the page.</span></span>
13. <span data-ttu-id="6bd3e-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-129">Close the page.</span></span>
14. <span data-ttu-id="6bd3e-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="6bd3e-131">Ausführen des Berichts für die ausgewählte Rechnung</span><span class="sxs-lookup"><span data-stu-id="6bd3e-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="6bd3e-132">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6bd3e-133">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="6bd3e-134">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="6bd3e-135">Wählen Sie in der Strukturdarstellung 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="6bd3e-136">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-136">Click Run.</span></span>
6. <span data-ttu-id="6bd3e-137">Erweitern Sie den Abschnitt "Records to include ()".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="6bd3e-138">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-138">Click Filter.</span></span>
8. <span data-ttu-id="6bd3e-139">Wählen Sie die Zeile des Feldes "Debitorenrechnungserfassung" und "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="6bd3e-140">Geben Sie im Feld "Kriterien" den Wert "000148" ein.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="6bd3e-141">Geben Sie im Feld "Auftrag" die Auftragsnummer 000148 ein.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="6bd3e-142">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-142">Click OK.</span></span>
11. <span data-ttu-id="6bd3e-143">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6bd3e-143">Click OK.</span></span>
    * <span data-ttu-id="6bd3e-144">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-144">Review the generated output.</span></span> <span data-ttu-id="6bd3e-145">Beachten Sie, das für jede Anlage ein einzelner XML-Knoten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="6bd3e-146">Der Inhalt des Anhangs wird mit der XML-Ausgabe im MIME-Textformat (Base64) ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6bd3e-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  


