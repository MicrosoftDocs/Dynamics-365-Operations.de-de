--- 
title: "Erweitern des Datenmodells zur Verwendung von Dokumentverwaltungsdateien in Formatausgaben für elektronische Berichterstellung (ER)"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="8c05b-103">Erweitern des Datenmodells zur Verwendung von Dokumentverwaltungsdateien in Formatausgaben für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="8c05b-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c05b-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="8c05b-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="8c05b-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c05b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="8c05b-106">Um diese Schritte ausgeführt, müssen Sie erst die Schritte im Aufgabenleitfaden "ER - Verwendung der Dokumentverwaltungsdateien in Formatausgaben (Teil 1: Vorbereiten des Datenmodells)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c05b-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="8c05b-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c05b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="8c05b-108">Erweitern des Datenmodells zur Darstellung von Dokumentverwaltungsdateien</span><span class="sxs-lookup"><span data-stu-id="8c05b-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="8c05b-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="8c05b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8c05b-110">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="8c05b-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8c05b-111">Erweitern Sie in der Strukturdarstellung "Debitorenrechnungsmodell ".</span><span class="sxs-lookup"><span data-stu-id="8c05b-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="8c05b-112">Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell\Debitorenrechnungsmodell (Benutzerdefiniert)" aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="8c05b-113">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8c05b-113">Click Designer.</span></span>
6. <span data-ttu-id="8c05b-114">Wählen Sie in der Strukturdarstellung "Debitorenrechnung(InvoiceCustomer)" aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="8c05b-115">Wir erweitern dieses Datenmodell, um es für alle Dateien zur Verfügung zu stellen, die einem Auftrag zugeordnet wurden, der einer elektronischen Rechnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8c05b-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="8c05b-116">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8c05b-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="8c05b-117">Geben Sie im Feld Name "Rechnungsanhänge" ein.</span><span class="sxs-lookup"><span data-stu-id="8c05b-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="8c05b-118">Anhänge fakturieren</span><span class="sxs-lookup"><span data-stu-id="8c05b-118">Invoice attachments</span></span>  
9. <span data-ttu-id="8c05b-119">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="8c05b-120">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c05b-120">Click Add.</span></span>
11. <span data-ttu-id="8c05b-121">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8c05b-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="8c05b-122">Geben Sie im Feld "Name" einen Wert "Dateiinhalt" ein.</span><span class="sxs-lookup"><span data-stu-id="8c05b-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="8c05b-123">Datei-Inhalt</span><span class="sxs-lookup"><span data-stu-id="8c05b-123">File content</span></span>  
13. <span data-ttu-id="8c05b-124">Wählen Sie im Feld "Artikeltyp" 'Container' aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="8c05b-125">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c05b-125">Click Add.</span></span>
15. <span data-ttu-id="8c05b-126">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8c05b-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="8c05b-127">Geben Sie im Feld "Name" "Dateiname" ein.</span><span class="sxs-lookup"><span data-stu-id="8c05b-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="8c05b-128">Dateiname</span><span class="sxs-lookup"><span data-stu-id="8c05b-128">File name</span></span>  
17. <span data-ttu-id="8c05b-129">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="8c05b-130">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c05b-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="8c05b-131">Ordnet Modellelementen die neuen Daten in Dynamics 365 for Finance and Operations zu</span><span class="sxs-lookup"><span data-stu-id="8c05b-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="8c05b-132">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="8c05b-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="8c05b-133">Verwenden Sie den Schnellfilter, um im Feld "Definition" nach dem Wert 'InvoiceCustomer' zu filtern.</span><span class="sxs-lookup"><span data-stu-id="8c05b-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="8c05b-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="8c05b-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="8c05b-135">Wir ordnen neue Modellelemente zu den entsprechenden Datenquellen zu.</span><span class="sxs-lookup"><span data-stu-id="8c05b-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="8c05b-136">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="8c05b-136">Click Designer.</span></span>
4. <span data-ttu-id="8c05b-137">Wählen Sie in der Strukturdarstellung "Anhänge fakturieren" aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="8c05b-138">Erweitern Sie in der Strukturdarstellung "Anhänge fakturieren".</span><span class="sxs-lookup"><span data-stu-id="8c05b-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="8c05b-139">Wählen Sie in der Strukturdarstellung "Anhänge fakturieren\Dateiname" aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="8c05b-140">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8c05b-140">Click Edit.</span></span>
8. <span data-ttu-id="8c05b-141">Geben Sie im Feld Formel 'CustInvoiceJour.>'Relations'.SalesTable.<'Relations'.'<Documents'.'originalFileName()'' ein.</span><span class="sxs-lookup"><span data-stu-id="8c05b-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="8c05b-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="8c05b-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="8c05b-143">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8c05b-143">Click Save.</span></span>
10. <span data-ttu-id="8c05b-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c05b-144">Close the page.</span></span>
11. <span data-ttu-id="8c05b-145">Wählen Sie in der Strukturdarstellung "Anhänge fakturieren\Dateiinhalt" aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="8c05b-146">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8c05b-146">Click Edit.</span></span>
13. <span data-ttu-id="8c05b-147">Geben Sie im Feld Formel 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' ein.</span><span class="sxs-lookup"><span data-stu-id="8c05b-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="8c05b-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="8c05b-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="8c05b-149">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8c05b-149">Click Save.</span></span>
15. <span data-ttu-id="8c05b-150">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c05b-150">Close the page.</span></span>
16. <span data-ttu-id="8c05b-151">Wählen Sie in der Strukturdarstellung "Anhänge fakturieren" aus.</span><span class="sxs-lookup"><span data-stu-id="8c05b-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="8c05b-152">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8c05b-152">Click Edit.</span></span>
18. <span data-ttu-id="8c05b-153">Geben Sie im Feld Formel 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' ein.</span><span class="sxs-lookup"><span data-stu-id="8c05b-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="8c05b-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="8c05b-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="8c05b-155">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8c05b-155">Click Save.</span></span>
20. <span data-ttu-id="8c05b-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c05b-156">Close the page.</span></span>
21. <span data-ttu-id="8c05b-157">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8c05b-157">Click Save.</span></span>
22. <span data-ttu-id="8c05b-158">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c05b-158">Close the page.</span></span>
23. <span data-ttu-id="8c05b-159">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c05b-159">Close the page.</span></span>
24. <span data-ttu-id="8c05b-160">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8c05b-160">Close the page.</span></span>
25. <span data-ttu-id="8c05b-161">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="8c05b-161">Click Change status.</span></span>
26. <span data-ttu-id="8c05b-162">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="8c05b-162">Click Complete.</span></span>
27. <span data-ttu-id="8c05b-163">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8c05b-163">Click OK.</span></span>


