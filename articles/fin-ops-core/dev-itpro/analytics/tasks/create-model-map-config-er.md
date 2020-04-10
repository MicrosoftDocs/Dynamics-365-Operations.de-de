---
title: Modellzuordnungskonfigurationen der elektronischen Berichterstellung (EB) erstellen
description: Verwenden Sie diese Prozedur, um eine neue Modellzuordnungskonfiguration für elektronische Berichterstellung (EB) zu entwerfen und integrierte EB-Funktionen für effiziente Aggregationsberechnungen zu verwenden.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6ba23af5f7eb517cc58994e54e918b2a305da17
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142162"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="c88a3-103">Modellzuordnungskonfigurationen der elektronischen Berichterstellung (EB) erstellen</span><span class="sxs-lookup"><span data-stu-id="c88a3-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c88a3-104">Verwenden Sie diese Prozedur, um eine neue Modellzuordnungskonfiguration für elektronische Berichterstellung (EB) zu entwerfen und integrierte EB-Funktionen für effiziente Aggregationsberechnungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c88a3-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="c88a3-105">In dieser Prozedur erstellen Sie eine Konfiguration für das Beispielunternehmen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c88a3-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="c88a3-106">Diese Prozedur wird für Verwendungszwecke erstellt, die die Rolle des Systemadministrators oder des Entwicklers für elektronische Berichterstellung haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="c88a3-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="c88a3-107">Diese Schritte können mithilfe eines beliebigen Dataset abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c88a3-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="c88a3-108">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="c88a3-108">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="c88a3-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="c88a3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c88a3-110">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c88a3-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c88a3-111">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zuerst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="c88a3-111">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>  
2. <span data-ttu-id="c88a3-112">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="c88a3-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c88a3-113">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="c88a3-113">Click Show filters.</span></span>
4. <span data-ttu-id="c88a3-114">Geben Sie im Feld „Name” den Filterwert „Intrastat” ein, und verwenden Sie den Filteroperator „beginnt mit”.</span><span class="sxs-lookup"><span data-stu-id="c88a3-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="c88a3-115">Nehmen Sie diesen Filter um die Datenmodellkonfiguration „Intrastat“ zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c88a3-115">Apply this filter to find the 'Intrastat' data model configuration.</span></span> <span data-ttu-id="c88a3-116">Dieses Modell besteht möglicherweise bereits in der Konfigurationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="c88a3-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="c88a3-117">Wenn es der Fall, überspringen Sie nächste Unteraufgabe.</span><span class="sxs-lookup"><span data-stu-id="c88a3-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="c88a3-118">Intrastat-Modellkonfiguration von Microsoft erhalten</span><span class="sxs-lookup"><span data-stu-id="c88a3-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="c88a3-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c88a3-119">Close the page.</span></span>
2. <span data-ttu-id="c88a3-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c88a3-120">Close the page.</span></span>
3. <span data-ttu-id="c88a3-121">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="c88a3-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="c88a3-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c88a3-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c88a3-123">Wählen Sie die Microsoft-Anbieterkachel aus.</span><span class="sxs-lookup"><span data-stu-id="c88a3-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="c88a3-124">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="c88a3-124">Click Repositories.</span></span>
    * <span data-ttu-id="c88a3-125">Klicken Sie auf „Repositorys” in der Kachel „Microsoft-Anbieter”.</span><span class="sxs-lookup"><span data-stu-id="c88a3-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="c88a3-126">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="c88a3-126">Click Show filters.</span></span>
7. <span data-ttu-id="c88a3-127">Geben Sie im Feld „Name eingeben“ den Filterwert „Ressourcen“ ein, und verwenden Sie dann den Filteroperator „enthält“.</span><span class="sxs-lookup"><span data-stu-id="c88a3-127">In the "Type name" field, enter the filter value, "resources" and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="c88a3-128">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="c88a3-128">Click Open.</span></span>
9. <span data-ttu-id="c88a3-129">In der Struktur wählen Sie „Intrastatmodell” aus.</span><span class="sxs-lookup"><span data-stu-id="c88a3-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="c88a3-130">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="c88a3-130">Click Import.</span></span>
11. <span data-ttu-id="c88a3-131">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="c88a3-131">Click Yes.</span></span>
    * <span data-ttu-id="c88a3-132">Sie haben die EB-Modellkonfiguration importiert, die das Datenmodell enthält, das Sie verwenden werden, um zu erkunden, wie die neuen EB-Funktionen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c88a3-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="c88a3-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c88a3-133">Close the page.</span></span>
13. <span data-ttu-id="c88a3-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c88a3-134">Close the page.</span></span>
14. <span data-ttu-id="c88a3-135">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="c88a3-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="c88a3-136">Neue Modellzuordnungskonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c88a3-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="c88a3-137">In der Struktur wählen Sie „Intrastatmodell” aus.</span><span class="sxs-lookup"><span data-stu-id="c88a3-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="c88a3-138">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c88a3-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="c88a3-139">Geben Sie im Feld „Neu” folgende Bezeichnung ein: „Modellzuordnung auf Grunlage des Datenmodells Intrastat”.</span><span class="sxs-lookup"><span data-stu-id="c88a3-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="c88a3-140">Geben Sie im Feld „Name” die Bezeichnung „Intrastat-Beispielzuordnung” ein.</span><span class="sxs-lookup"><span data-stu-id="c88a3-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="c88a3-141">Intrastat-Beispielzuordnung</span><span class="sxs-lookup"><span data-stu-id="c88a3-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="c88a3-142">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="c88a3-142">Click Create configuration.</span></span>

