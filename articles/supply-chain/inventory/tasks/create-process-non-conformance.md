---
title: Übereinstimmung erstellen und verarbeiten
description: Verwenden Sie dieses Verfahren, um Qualitätsmangelverwaltung, auf Basis eines vorhandenen Qualitätsprüfungsauftrag auszuführen.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "336289"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="a3af4-103">Übereinstimmung erstellen und verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a3af4-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3af4-104">Verwenden Sie dieses Verfahren, um Qualitätsmangelverwaltung, auf Basis eines vorhandenen Qualitätsprüfungsauftrag auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="a3af4-105">Sie können diese Buchung im USMF-Vorführungsunternehmen ausführen und können die vorgeschlagenen Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3af4-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="a3af4-106">Normalerweise wird diese Prozedur aus einem Qualitätssekretär ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3af4-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="a3af4-107">Als erforderliches folgenden Schaltern "überprüfen die Qualität von Waren" Aufgabenerfassen aus.</span><span class="sxs-lookup"><span data-stu-id="a3af4-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="a3af4-108">Um die Genehmigung einer Nichtübereinstimmung zu verarbeiten, muss der Benutzer der das Aufgabenerfassen ausführt einen "Name Wert besitzen, der auf der Benutzerseite zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a3af4-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="a3af4-109">Um die Hinweisdokumente verwenden zu können, muss der Benutzer Handhabung von Dokumenten verfügen aktiviert in den Benutzeroptionen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="a3af4-110">Wählen Sie einen Qualitätsprüfungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="a3af4-110">Select a quality order</span></span>
1. <span data-ttu-id="a3af4-111">Qualitätsprüfungsaufträge (Formular) anzeigen</span><span class="sxs-lookup"><span data-stu-id="a3af4-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="a3af4-112">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a3af4-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a3af4-113">Wählen Sie den Qualitätsprüfungsauftrag, der vom "überprüfen die Qualität von Waren" Aufgabenerfassen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a3af4-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="a3af4-114">Erstellen einer Nichtübereinstimmung</span><span class="sxs-lookup"><span data-stu-id="a3af4-114">Create a nonconformance</span></span>
1. <span data-ttu-id="a3af4-115">Klicken Sie auf Abfragen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-115">Click Inquiries.</span></span>
2. <span data-ttu-id="a3af4-116">Nichtübereinstimmungen klicken</span><span class="sxs-lookup"><span data-stu-id="a3af4-116">Click Non conformances.</span></span>
3. <span data-ttu-id="a3af4-117">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a3af4-117">Click New.</span></span>
4. <span data-ttu-id="a3af4-118">Klicken Sie im Feld "Problemtyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a3af4-119">Wählen Sie das Problem aus, wenn während der Inspektionsprozesses gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a3af4-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="a3af4-120">Klicken Sie im Feld "Problemtyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a3af4-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a3af4-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a3af4-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a3af4-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a3af4-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a3af4-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="a3af4-124">Qualitätsmangeldatensätze genehmigen</span><span class="sxs-lookup"><span data-stu-id="a3af4-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="a3af4-125">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-125">Click Functions.</span></span>
2. <span data-ttu-id="a3af4-126">Die Nichtübereinstimmung genehmigen</span><span class="sxs-lookup"><span data-stu-id="a3af4-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="a3af4-127">In vorliegenden Beispiel genehmigen Sie den Qualitätsmangel.</span><span class="sxs-lookup"><span data-stu-id="a3af4-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="a3af4-128">Genehmigte Qualitätsmängel können mit zugehörigen Arbeitsgängen zugeordnet werden, um Arbeit, die als Teil in der erfassenden zu erfassen Qualitätsmangelbehandlung und ausgeführt werden, wie in dieser Aufgabe, die Verarbeitung der Korrekturbehandlung.</span><span class="sxs-lookup"><span data-stu-id="a3af4-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="a3af4-129">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="a3af4-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="a3af4-130">Korrektur erstellen</span><span class="sxs-lookup"><span data-stu-id="a3af4-130">Create a correction action</span></span>
1. <span data-ttu-id="a3af4-131">Korrekturen anklicken</span><span class="sxs-lookup"><span data-stu-id="a3af4-131">Click Corrections.</span></span>
2. <span data-ttu-id="a3af4-132">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a3af4-132">Click New.</span></span>
3. <span data-ttu-id="a3af4-133">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a3af4-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a3af4-134">Klicken Sie im Feld "Personalnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a3af4-135">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a3af4-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a3af4-136">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-136">Click Select.</span></span>
7. <span data-ttu-id="a3af4-137">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="a3af4-137">Click Attach.</span></span>
    * <span data-ttu-id="a3af4-138">Erstellen Sie einen Hinweis zur Korrektur.</span><span class="sxs-lookup"><span data-stu-id="a3af4-138">Create a note about the correction.</span></span> <span data-ttu-id="a3af4-139">In vorliegenden Beispiel ist die Aktivität, mit dem Kreditor in Verbindung mit Ihnen aufzunehmen, um den Qualitätsmangelfall zu erläutern.</span><span class="sxs-lookup"><span data-stu-id="a3af4-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="a3af4-140">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a3af4-140">Click New.</span></span>
9. <span data-ttu-id="a3af4-141">Klicken Sie auf Hinweis.</span><span class="sxs-lookup"><span data-stu-id="a3af4-141">Click Note.</span></span>
    * <span data-ttu-id="a3af4-142">Beachten Sie, dass, abhängig von der Berichteinstellungen, verschiedene Dokumenttypen in den Berichten gedruckt werden können, die der Nichtübereinstimmung verwaltung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a3af4-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="a3af4-143">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a3af4-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="a3af4-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a3af4-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="a3af4-145">Korrekturen verwalten</span><span class="sxs-lookup"><span data-stu-id="a3af4-145">Maintain a correction</span></span>
1. <span data-ttu-id="a3af4-146">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="a3af4-146">Click Mark complete.</span></span>
2. <span data-ttu-id="a3af4-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a3af4-147">Click OK.</span></span>
3. <span data-ttu-id="a3af4-148">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a3af4-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="a3af4-149">Qualitätsmangel schließen</span><span class="sxs-lookup"><span data-stu-id="a3af4-149">Close a nonconformance</span></span>
1. <span data-ttu-id="a3af4-150">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a3af4-150">Click Functions.</span></span>
2. <span data-ttu-id="a3af4-151">Qualitätsmangel schließen</span><span class="sxs-lookup"><span data-stu-id="a3af4-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="a3af4-152">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="a3af4-152">Click Yes.</span></span>
4. <span data-ttu-id="a3af4-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a3af4-153">Close the page.</span></span>
5. <span data-ttu-id="a3af4-154">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a3af4-154">Close the page.</span></span>
