--- 
title: Datenmodelle zum Verwenden von Dokumentverwaltungsdateien in EB-Ausgabe vorbereiten
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fcafaf17315f54594116a143f36e924bc705d839
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="prepare-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="a64f2-103">Datenmodelle zum Verwenden von Dokumentverwaltungsdateien in EB-Ausgabe vorbereiten</span><span class="sxs-lookup"><span data-stu-id="a64f2-103">Prepare data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a64f2-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="a64f2-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="a64f2-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a64f2-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a64f2-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="a64f2-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="a64f2-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a64f2-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="a64f2-108">Zugriff auf die Liste von Microsoft bereitgestellte von den Konfigurationen erhalten</span><span class="sxs-lookup"><span data-stu-id="a64f2-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="a64f2-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="a64f2-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="a64f2-110">Überprüfen Sie, ob "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="a64f2-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="a64f2-111">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="a64f2-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="a64f2-112">Wählen Sie den "Litware, Inc."-</span><span class="sxs-lookup"><span data-stu-id="a64f2-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="a64f2-113">Anbieter.</span><span class="sxs-lookup"><span data-stu-id="a64f2-113">provider.</span></span>
3. <span data-ttu-id="a64f2-114">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="a64f2-114">Click Repositories.</span></span>
    * <span data-ttu-id="a64f2-115">Wenn ein Repository des Typs "Operations-Ressourcen" vorhanden ist, überspringen Sie die übrigen Schritte der aktuellen Unteraufgabe.</span><span class="sxs-lookup"><span data-stu-id="a64f2-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="a64f2-116">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="a64f2-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="a64f2-117">Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.</span><span class="sxs-lookup"><span data-stu-id="a64f2-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="a64f2-118">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="a64f2-118">Click Create repository.</span></span>
7. <span data-ttu-id="a64f2-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a64f2-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="a64f2-120">Die Debitorenrechnungsmodell-Konfigurationen von Microsoft abrufen</span><span class="sxs-lookup"><span data-stu-id="a64f2-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="a64f2-121">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="a64f2-121">Click Show filters.</span></span>
2. <span data-ttu-id="a64f2-122">Wenden Sie die nachfolgenden Filter an: Geben Sie den Filterwert "Operations-Ressourcen" im Feld " Name" ein, indem Sie den "beginnt mit"-Filteroperator verewnden; Geben Sie den Filterwert "" im Feld "Beschreibungs" ein, indem Sie den "beginnt mit"-Filteroperator verwenden.</span><span class="sxs-lookup"><span data-stu-id="a64f2-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="a64f2-123">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="a64f2-123">Click Show filters.</span></span>
4. <span data-ttu-id="a64f2-124">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="a64f2-124">Click Open.</span></span>
5. <span data-ttu-id="a64f2-125">Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell " aus.</span><span class="sxs-lookup"><span data-stu-id="a64f2-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="a64f2-126">Wählen Sie die Modellkonfiguration "Debitorenrechnungsmodell" aus, um sie zu importieren.</span><span class="sxs-lookup"><span data-stu-id="a64f2-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="a64f2-127">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="a64f2-127">Click Import.</span></span>
    * <span data-ttu-id="a64f2-128">Klicken Sie auf "Importieren" für Version 1 der ausgewählten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a64f2-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="a64f2-129">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="a64f2-129">Click Yes.</span></span>
8. <span data-ttu-id="a64f2-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a64f2-130">Close the page.</span></span>
9. <span data-ttu-id="a64f2-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a64f2-131">Close the page.</span></span>
10. <span data-ttu-id="a64f2-132">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="a64f2-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="a64f2-133">Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell " aus.</span><span class="sxs-lookup"><span data-stu-id="a64f2-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="a64f2-134">Erstellen Sie das abgeleitete Modell, um den Zugriff auf die Dokumentverwaltungsdateien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a64f2-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="a64f2-135">Sie erstellen eine eigene Konfiguration des Debitorenrechnungmodells, die von der Konfiguration von Microsoft abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="a64f2-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="a64f2-136">Sie verwenden diese Konfiguration, um den Zugriff auf die Dokumentverwaltungsdateien zu implementieren und diese für elektronische Dokumente bereitzustellen, die Sie auf Basis dieses Modell erstellen.</span><span class="sxs-lookup"><span data-stu-id="a64f2-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="a64f2-137">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a64f2-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="a64f2-138">Geben Sie im Feld "Neu" "Von Name 'Debitorenrechnungsmodell Microsoft' abgeleitet" ein.</span><span class="sxs-lookup"><span data-stu-id="a64f2-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="a64f2-139">Geben Sie im Feld "Name" "Debitorenrechnungsmodell (benutzerdefiniert)" ein.</span><span class="sxs-lookup"><span data-stu-id="a64f2-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="a64f2-140">Debitorenrechnungsmodell (benutzerdefiniert)</span><span class="sxs-lookup"><span data-stu-id="a64f2-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="a64f2-141">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="a64f2-141">Click Create configuration.</span></span>


