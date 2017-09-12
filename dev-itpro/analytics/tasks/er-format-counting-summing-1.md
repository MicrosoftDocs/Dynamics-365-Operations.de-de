--- 
title: "Erstellen von Format zur Zählung und Summierung für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: cac3748182ba27735264acc947403d7b857f1b6e
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="fec32-103">Erstellen von Format zur Zählung und Summierung für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="fec32-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fec32-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="fec32-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="fec32-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fec32-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="fec32-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="fec32-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="fec32-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="fec32-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="fec32-108">Zugriff auf die Liste von Microsoft bereitgestellte von den Konfigurationen erhalten</span><span class="sxs-lookup"><span data-stu-id="fec32-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="fec32-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="fec32-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fec32-110">Überprüfen Sie, ob "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="fec32-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="fec32-111">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="fec32-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="fec32-112">Wählen Sie den "Litware, Inc."-</span><span class="sxs-lookup"><span data-stu-id="fec32-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="fec32-113">Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fec32-113">provider.</span></span>
3. <span data-ttu-id="fec32-114">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="fec32-114">Click Repositories.</span></span>
    * <span data-ttu-id="fec32-115">Wenn ein Repository des Typs "Operations-Ressourcen" vorhanden ist, überspringen Sie die übrigen Schritte der aktuellen Unteraufgabe.</span><span class="sxs-lookup"><span data-stu-id="fec32-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="fec32-116">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="fec32-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="fec32-117">Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.</span><span class="sxs-lookup"><span data-stu-id="fec32-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="fec32-118">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="fec32-118">Click Create repository.</span></span>
7. <span data-ttu-id="fec32-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="fec32-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="fec32-120">Intrastat-Konfigurationen von Microsoft erhalten</span><span class="sxs-lookup"><span data-stu-id="fec32-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="fec32-121">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="fec32-121">Click Open.</span></span>
2. <span data-ttu-id="fec32-122">Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.</span><span class="sxs-lookup"><span data-stu-id="fec32-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="fec32-123">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="fec32-123">Click Import.</span></span>
    * <span data-ttu-id="fec32-124">Klicken Sie auf "Importieren" für Version 1.1 der ausgewählten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fec32-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="fec32-125">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="fec32-125">Click Yes.</span></span>
5. <span data-ttu-id="fec32-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fec32-126">Close the page.</span></span>
6. <span data-ttu-id="fec32-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fec32-127">Close the page.</span></span>
7. <span data-ttu-id="fec32-128">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="fec32-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="fec32-129">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="fec32-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="fec32-130">Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.</span><span class="sxs-lookup"><span data-stu-id="fec32-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


