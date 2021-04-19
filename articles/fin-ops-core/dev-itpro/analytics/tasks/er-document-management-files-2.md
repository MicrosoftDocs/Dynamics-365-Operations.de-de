---
title: 'ER – Verwendung von Dokumentverwaltungsdateien in Formatausgaben (Teil 2: Datenmodell erweitern)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat (EB) für die Verwendung von Dokumentenverwaltungsdateien (Anhängen) in der EB-Ausgabe konfigurieren. (Teil 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754913"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="14962-104">ER – Verwendung von Dokumentverwaltungsdateien in Formatausgaben (Teil 2: Datenmodell erweitern)</span><span class="sxs-lookup"><span data-stu-id="14962-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14962-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="14962-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="14962-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="14962-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="14962-107">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden „ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 1: Vorbereiten des Datenmodells)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="14962-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="14962-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="14962-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="14962-109">Erweitern des Datenmodells zur Darstellung von Dokumentverwaltungsdateien</span><span class="sxs-lookup"><span data-stu-id="14962-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="14962-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="14962-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="14962-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="14962-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="14962-112">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".</span><span class="sxs-lookup"><span data-stu-id="14962-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="14962-113">Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.</span><span class="sxs-lookup"><span data-stu-id="14962-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="14962-114">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="14962-114">Click Designer.</span></span>
6. <span data-ttu-id="14962-115">Wählen Sie in der Strukturdarstellung "Debitorenrechnung(InvoiceCustomer)" aus.</span><span class="sxs-lookup"><span data-stu-id="14962-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="14962-116">Wir erweitern dieses Datenmodell, um es für alle Dateien zur Verfügung zu stellen, die einem Auftrag zugeordnet wurden, der einer elektronischen Rechnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="14962-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="14962-117">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="14962-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="14962-118">Geben Sie im Feld Name "Rechnungsanhänge" ein.</span><span class="sxs-lookup"><span data-stu-id="14962-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="14962-119">Anhänge fakturieren</span><span class="sxs-lookup"><span data-stu-id="14962-119">Invoice attachments</span></span>  
9. <span data-ttu-id="14962-120">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="14962-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="14962-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="14962-121">Click Add.</span></span>
11. <span data-ttu-id="14962-122">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="14962-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="14962-123">Geben Sie im Feld "Name" einen Wert "Dateiinhalt" ein.</span><span class="sxs-lookup"><span data-stu-id="14962-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="14962-124">Datei-Inhalt</span><span class="sxs-lookup"><span data-stu-id="14962-124">File content</span></span>  
13. <span data-ttu-id="14962-125">Wählen Sie im Feld "Artikeltyp" 'Container' aus.</span><span class="sxs-lookup"><span data-stu-id="14962-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="14962-126">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="14962-126">Click Add.</span></span>
15. <span data-ttu-id="14962-127">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="14962-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="14962-128">Geben Sie im Feld "Name" "Dateiname" ein.</span><span class="sxs-lookup"><span data-stu-id="14962-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="14962-129">Dateiname</span><span class="sxs-lookup"><span data-stu-id="14962-129">File name</span></span>  
17. <span data-ttu-id="14962-130">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="14962-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="14962-131">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="14962-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="14962-132">Zuordnen neue Datenmodell-Elemente zu Datenquellen</span><span class="sxs-lookup"><span data-stu-id="14962-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="14962-133">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="14962-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="14962-134">Verwenden Sie den Schnellfilter, um im Feld "Definition" nach dem Wert 'InvoiceCustomer' zu filtern.</span><span class="sxs-lookup"><span data-stu-id="14962-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="14962-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="14962-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="14962-136">Wir ordnen neue Modellelemente zu den entsprechenden Datenquellen zu.</span><span class="sxs-lookup"><span data-stu-id="14962-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="14962-137">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="14962-137">Click Designer.</span></span>
4. <span data-ttu-id="14962-138">Wählen Sie in der Strukturdarstellung "Anhänge fakturieren" aus.</span><span class="sxs-lookup"><span data-stu-id="14962-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="14962-139">Erweitern Sie in der Strukturdarstellung "Anhänge fakturieren".</span><span class="sxs-lookup"><span data-stu-id="14962-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="14962-140">Wählen Sie in der Strukturdarstellung "Anhänge fakturieren\Dateiname" aus.</span><span class="sxs-lookup"><span data-stu-id="14962-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="14962-141">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="14962-141">Click Edit.</span></span>
8. <span data-ttu-id="14962-142">Geben Sie im Feld Formel 'CustInvoiceJour.>'Relations'.SalesTable.<'Relations'.'<Documents'.'originalFileName()'' ein.</span><span class="sxs-lookup"><span data-stu-id="14962-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="14962-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="14962-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="14962-144">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="14962-144">Click Save.</span></span>
10. <span data-ttu-id="14962-145">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="14962-145">Close the page.</span></span>
11. <span data-ttu-id="14962-146">Wählen Sie in der Strukturdarstellung "Anhänge fakturieren\Dateiinhalt" aus.</span><span class="sxs-lookup"><span data-stu-id="14962-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="14962-147">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="14962-147">Click Edit.</span></span>
13. <span data-ttu-id="14962-148">Geben Sie im Feld Formel 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' ein.</span><span class="sxs-lookup"><span data-stu-id="14962-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="14962-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="14962-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="14962-150">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="14962-150">Click Save.</span></span>
15. <span data-ttu-id="14962-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="14962-151">Close the page.</span></span>
16. <span data-ttu-id="14962-152">Wählen Sie in der Strukturdarstellung "Anhänge fakturieren" aus.</span><span class="sxs-lookup"><span data-stu-id="14962-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="14962-153">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="14962-153">Click Edit.</span></span>
18. <span data-ttu-id="14962-154">Geben Sie im Feld Formel 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' ein.</span><span class="sxs-lookup"><span data-stu-id="14962-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="14962-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="14962-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="14962-156">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="14962-156">Click Save.</span></span>
20. <span data-ttu-id="14962-157">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="14962-157">Close the page.</span></span>
21. <span data-ttu-id="14962-158">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="14962-158">Click Save.</span></span>
22. <span data-ttu-id="14962-159">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="14962-159">Close the page.</span></span>
23. <span data-ttu-id="14962-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="14962-160">Close the page.</span></span>
24. <span data-ttu-id="14962-161">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="14962-161">Close the page.</span></span>
25. <span data-ttu-id="14962-162">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="14962-162">Click Change status.</span></span>
26. <span data-ttu-id="14962-163">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="14962-163">Click Complete.</span></span>
27. <span data-ttu-id="14962-164">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="14962-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]