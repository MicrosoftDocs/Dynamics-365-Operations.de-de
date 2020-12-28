---
title: Übereinstimmung erstellen und verarbeiten
description: Dieses Thema erklärt, wie Sie die Qualitätsmangelverwaltung auf Basis eines vorhandenen Qualitätsprüfungsauftrags ausführen.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428967"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="71974-103">Übereinstimmung erstellen und verarbeiten</span><span class="sxs-lookup"><span data-stu-id="71974-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71974-104">Dieses Thema erklärt, wie Sie die Qualitätsmangelverwaltung auf Basis eines vorhandenen Qualitätsprüfungsauftrags ausführen.</span><span class="sxs-lookup"><span data-stu-id="71974-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="71974-105">Sie können diese Buchung im USMF-Vorführungsunternehmen ausführen und können die vorgeschlagenen Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="71974-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="71974-106">Normalerweise wird diese Prozedur aus einem Qualitätssekretär ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71974-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="71974-107">Als Voraussetzung müssen Sie die Anweisungen in [Qualität der Waren inspizieren](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="71974-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="71974-108">Um die Genehmigung einer Nichtübereinstimmung zu verarbeiten, muss der Benutzer der das Aufgabenerfassen ausführt einen Wert Name besitzen, der auf der Benutzerseite zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="71974-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="71974-109">Um die Hinweisdokumente verwenden zu können, muss der Benutzer Handhabung von Dokumenten verfügen aktiviert in den Benutzeroptionen.</span><span class="sxs-lookup"><span data-stu-id="71974-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="71974-110">Wählen Sie einen Qualitätsprüfungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="71974-110">Select a quality order</span></span>
1. <span data-ttu-id="71974-111">Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Periodische Aufgaben > Qualitätsmanagement > Qualitätsprüfungsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="71974-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="71974-112">Wählen Sie in der Liste den Qualitätsprüfungsauftrag aus, der in [Qualität der Waren inspizieren](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="71974-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="71974-113">Erstellen einer Nichtübereinstimmung</span><span class="sxs-lookup"><span data-stu-id="71974-113">Create a nonconformance</span></span>
1. <span data-ttu-id="71974-114">Wählen Sie im Aktivitätsbereich **Abfragen** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="71974-115">Wählen Sie **Nichtübereinstimmungen** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="71974-116">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-116">Select **New**.</span></span>
4. <span data-ttu-id="71974-117">Wählen Sie im Dropdownmenü des Feldes **Problemtyp**, das Problem aus, das während des Prüfprozesses gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="71974-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="71974-118">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71974-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="71974-119">Qualitätsmangeldatensätze genehmigen</span><span class="sxs-lookup"><span data-stu-id="71974-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="71974-120">Wählen Sie **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-120">Select **Functions**.</span></span>
2. <span data-ttu-id="71974-121">Wählen Sie **Nichtübereinstimmung genehmigen** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="71974-122">In vorliegenden Beispiel genehmigen Sie den Qualitätsmangel.</span><span class="sxs-lookup"><span data-stu-id="71974-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="71974-123">Genehmigte Qualitätsmängel können zugehörigen Arbeitsgängen zugeordnet werden, um Arbeit, die als Teil der Qualitätsmangelbehandlung ausgeführt wird, und, wie in diesem Thema, der Verarbeitung der Korrekturbehandlung, erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="71974-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="71974-124">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="71974-125">Korrektur erstellen</span><span class="sxs-lookup"><span data-stu-id="71974-125">Create a correction action</span></span>
1. <span data-ttu-id="71974-126">Wählen Sie **Veränderungen** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="71974-127">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-127">Select **New**.</span></span>
3. <span data-ttu-id="71974-128">Wählen Sie im Feld **Personalnummer** der neuen Zeile den gewünschten Datensatz aus dem Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="71974-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="71974-129">Klicken Sie auf **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="71974-129">Click **Select**.</span></span>
5. <span data-ttu-id="71974-130">Wählen Sie **Zuordnen** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-130">Select **Attach**.</span></span> <span data-ttu-id="71974-131">Erstellen Sie einen Hinweis zur Korrektur.</span><span class="sxs-lookup"><span data-stu-id="71974-131">Create a note about the correction.</span></span> <span data-ttu-id="71974-132">In vorliegenden Beispiel ist die Aktivität, mit dem Kreditor in Verbindung mit Ihnen aufzunehmen, um den Qualitätsmangelfall zu erläutern.</span><span class="sxs-lookup"><span data-stu-id="71974-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="71974-133">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-133">Select **New**.</span></span>
7. <span data-ttu-id="71974-134">Wählen Sie **Hinweis** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-134">Select **Note**.</span></span> <span data-ttu-id="71974-135">Abhängig von den Berichteinstellungen können verschiedene Dokumenttypen in den Berichten gedruckt werden, die der Qualitätsmangelverwaltung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="71974-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="71974-136">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="71974-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="71974-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="71974-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="71974-138">Korrekturen verwalten</span><span class="sxs-lookup"><span data-stu-id="71974-138">Maintain a correction</span></span>
1. <span data-ttu-id="71974-139">Wählen Sie **Als abgeschlossen markieren** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="71974-140">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="71974-140">Select **OK**.</span></span>
3. <span data-ttu-id="71974-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="71974-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="71974-142">Qualitätsmangel schließen</span><span class="sxs-lookup"><span data-stu-id="71974-142">Close a nonconformance</span></span>
1. <span data-ttu-id="71974-143">Wählen Sie **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-143">Select **Functions**.</span></span>
2. <span data-ttu-id="71974-144">Wählen Sie **Qualitätsmangel schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="71974-145">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="71974-145">Select **Yes**.</span></span>
4. <span data-ttu-id="71974-146">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="71974-146">Close the pages.</span></span>
