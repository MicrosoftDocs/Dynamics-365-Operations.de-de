---
title: 'ER – Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 1: Datenmodell vorbereiten)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat (EB) für die Verwendung von Dokumentenverwaltungsdateien (Anhängen) in der EB-Ausgabe konfigurieren. (Teil 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35bffd6d3688a9887fcdaf4edbd89c344cb9b18d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559796"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="f31b4-104">ER – Verwenden von Dokumentverwaltungsdateien in Formatausgaben (Teil 1: Datenmodell vorbereiten)</span><span class="sxs-lookup"><span data-stu-id="f31b4-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f31b4-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Nutzung von Dokumentverwaltungsdateien (Anhänge) in ER-Berichten nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="f31b4-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f31b4-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f31b4-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f31b4-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="f31b4-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="f31b4-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f31b4-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="f31b4-109">Zugriff auf die Liste von Microsoft bereitgestellte von den Konfigurationen erhalten</span><span class="sxs-lookup"><span data-stu-id="f31b4-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f31b4-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="f31b4-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="f31b4-111">Überprüfen Sie, ob "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="f31b4-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="f31b4-112">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="f31b4-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="f31b4-113">Wählen Sie den "Litware, Inc."-</span><span class="sxs-lookup"><span data-stu-id="f31b4-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="f31b4-114">Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f31b4-114">provider.</span></span>
3. <span data-ttu-id="f31b4-115">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="f31b4-115">Click Repositories.</span></span>

    <span data-ttu-id="f31b4-116">Wenn ein Repository des Typs "Operations-Ressourcen" vorhanden ist, überspringen Sie die übrigen Schritte der aktuellen Unteraufgabe.</span><span class="sxs-lookup"><span data-stu-id="f31b4-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="f31b4-117">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f31b4-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="f31b4-118">Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.</span><span class="sxs-lookup"><span data-stu-id="f31b4-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="f31b4-119">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="f31b4-119">Click Create repository.</span></span>
7. <span data-ttu-id="f31b4-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f31b4-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="f31b4-121">Die Debitorenrechnungsmodell-Konfigurationen von Microsoft abrufen</span><span class="sxs-lookup"><span data-stu-id="f31b4-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f31b4-122">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="f31b4-122">Click Show filters.</span></span>
2. <span data-ttu-id="f31b4-123">Wenden Sie die nachfolgenden Filter an: Geben Sie den Filterwert "Operations-Ressourcen" im Feld " Name" ein, indem Sie den "beginnt mit"-Filteroperator verewnden; Geben Sie den Filterwert "" im Feld "Beschreibungs" ein, indem Sie den "beginnt mit"-Filteroperator verwenden.</span><span class="sxs-lookup"><span data-stu-id="f31b4-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="f31b4-124">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="f31b4-124">Click Show filters.</span></span>
4. <span data-ttu-id="f31b4-125">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="f31b4-125">Click Open.</span></span>
5. <span data-ttu-id="f31b4-126">Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell " aus.</span><span class="sxs-lookup"><span data-stu-id="f31b4-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="f31b4-127">Wählen Sie die Modellkonfiguration "Debitorenrechnungsmodell" aus, um sie zu importieren.</span><span class="sxs-lookup"><span data-stu-id="f31b4-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="f31b4-128">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="f31b4-128">Click Import.</span></span>

    <span data-ttu-id="f31b4-129">Klicken Sie auf "Importieren" für Version 1 der ausgewählten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f31b4-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="f31b4-130">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="f31b4-130">Click Yes.</span></span>
8. <span data-ttu-id="f31b4-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f31b4-131">Close the page.</span></span>
9. <span data-ttu-id="f31b4-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f31b4-132">Close the page.</span></span>
10. <span data-ttu-id="f31b4-133">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="f31b4-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="f31b4-134">Wählen Sie in der Strukturdarstellung "Debitorenrechnungsmodell " aus.</span><span class="sxs-lookup"><span data-stu-id="f31b4-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="f31b4-135">Erstellen Sie das abgeleitete Modell, um den Zugriff auf die Dokumentverwaltungsdateien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f31b4-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="f31b4-136">Sie erstellen eine eigene Konfiguration des Debitorenrechnungmodells, die von der Konfiguration von Microsoft abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="f31b4-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="f31b4-137">Sie verwenden diese Konfiguration, um den Zugriff auf die Dokumentverwaltungsdateien zu implementieren und diese für elektronische Dokumente bereitzustellen, die Sie auf Basis dieses Modell erstellen.</span><span class="sxs-lookup"><span data-stu-id="f31b4-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="f31b4-138">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f31b4-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="f31b4-139">Geben Sie im Feld "Neu" "Von Name 'Debitorenrechnungsmodell Microsoft' abgeleitet" ein.</span><span class="sxs-lookup"><span data-stu-id="f31b4-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="f31b4-140">Geben Sie im Feld "Name" "Debitorenrechnungsmodell (benutzerdefiniert)" ein.</span><span class="sxs-lookup"><span data-stu-id="f31b4-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="f31b4-141">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="f31b4-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]